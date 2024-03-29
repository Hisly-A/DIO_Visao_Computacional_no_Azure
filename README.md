# DIO - Visão Computacional no Azure
Reconhecimento Facial e transformação de imagens em Dados no Azure ML

## 🔎 O que é o Azure Vision Studio?	

>O Vision Studio é um conjunto de ferramentas baseadas em interface do usuário que permitem explorar, compilar e integrar recursos do Azure AI Vision. O serviço do Azure AI Vision lhe dá acesso a algoritmos avançados que processam imagens e retornam informações com base nos recursos visuais do seu interesse. Os serviços oferecidos são: OCR (reconhecimento óptico de caracteres), Análise de imagens, Detecção Facial e Análise de Vídeo.

<sub>Fonte: <https://learn.microsoft.com/pt-br/azure/ai-services/computer-vision/overview></sub>


## Criação do recurso de serviços de IA do Azure

Abra o portal do Azure em https://portal.azure.com, entrando com a conta da Microsoft associada à sua assinatura do Azure.

Clique em ```＋Create a resource``` e pesquise por **Azure AI services**.

<div align="center">
    <img width="700" title="VC01" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC01.PNG"/>
</div>

Clique em ```create``` para criar um plano do **Azure AI services** e configure-o da seguinte forma:
- *Subscription*: Sua assinatura do Azure.
- *Resource group*: Selecione ou crie um grupo de recursos com um nome exclusivo.
- *Region*: Leste dos EUA.
- *Name*: Insira um nome exclusivo.
- *Pricing tier*: Padrão S0.
- *Marque o campo*: By checking this box I acknowledge that I have read and understood all the terms below.

<div align="center">
    <img width="700" title="VC02" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC02.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC03" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC03.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC04" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC04.PNG"/>
</div>

Clique em ```Review + create``` e depois ```Create``` e aguarde a conclusão da implantação.

<div align="center">
    <img width="700" title="VC05" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC05.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC06" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC06.PNG"/>
</div>

## Conecte seu recurso de serviço de IA do Azure ao Vision Studio

Acesse Vision Studio em https://portal.vision.cognitive.azure.com.

Entre com sua conta e certifique-se de usar o mesmo diretório onde você criou seu recurso de serviços de IA do Azure.

Na página inicial do Vision Studio, clique em ```View all resources``` no título **Get started with Vision**.

<div align="center">
    <img width="700" title="VC07" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC07.PNG"/>
</div>

Na página **Select a resource to work with**, marque o recurso criado e clique em ```Select as default resource```.

<div align="center">
    <img width="700" title="VC08" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC08.PNG"/>
</div>

Feche a página de configurações.

## Detecte rostos no Vision Studio
Num navegador web, acesse o Vision Studio em https://portal.vision.cognitive.azure.com.

Na página inicial **Get started with Vision**, clique na guia **Face** e, em seguida, clique no bloco **Detect Faces in an image**.

<div align="center">
    <img width="700" title="VC09" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC09.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC10" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC10.PNG"/>
</div>

No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa.

<div align="center">
    <img width="700" title="VC11" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC11.PNG"/>
</div>

Com uma das imagens de amostra selecionada observe os dados de detecção facial retornados.

<div align="center">
    <img width="700" title="VC12" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC12.PNG"/>
</div>

Agora observe que para a [imagem01](https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/inputs/imagem01.jpg) não foi possível reconhecer uma face:

<div align="center">
    <img width="700" title="VC13" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC13.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC14" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC14.PNG"/>
</div>

Já na imagem abaixo foi possível reconhecer a face do cachorro:

<br>
<div align="center">
    <img width="700" title="VC15" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC15.PNG"/>
</div>

Faça upload de store-camera-3.jpg e revise os detalhes de detecção de rosto retornados. Observe como o Azure AI Face não detectou o rosto que está obscurecido.


## Extraia texto de imagens no Vision Studio
Acesse o Vision Studio em https://portal.vision.cognitive.azure.com.

Na página inicial **Get started with Vision**, clique em **Optical character recognition** e, em seguida, no bloco **Extract text from images**.

No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa.

Selecione https://aka.ms/mslearn-ocr-images para baixar ocr-images.zip . Em seguida, abra a pasta.

No portal, clique em ```Browse for a file``` e navegue até a pasta do computador onde a imagem foi salva, selecione-a e clique em ```Open```.

Agora revise o que é retornado:
Em **Detected attributes**, qualquer texto encontrado na imagem é organizado em uma estrutura hierárquica de regiões, linhas e palavras.
Na imagem, a localização do texto é indicada por uma caixa delimitadora, conforme mostrado aqui:

Agora você pode tentar outra imagem. Selecione Procurar um arquivo e navegue até a pasta onde você salvou os arquivos do GitHub. Selecione carta.jpg .



Revise os resultados da segunda imagem. Deve retornar o texto e as caixas delimitadoras do texto. Se você tiver tempo, tente note.jpg e recibo.jpg .



## Gerar legendas para uma imagem

Em um navegador da web, navegue até Vision Studio.

Na página **Get started with Vision**, clique em **Image analysis** e, em seguida, no bloco **Add captions to images**.

Em **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa.

Abra a pasta do computador e localize uma imagem, para este exercício foi utilizada a seguinte imagem:

Carregue a imagem arrastando-a para a caixa **Drag and drop files here** ou navegando até ela em seu sistema de arquivos.

Observe o texto da legenda gerado, visível no painel **Detected attributes** à direita da imagem.

A funcionalidade Caption fornece uma única frase em inglês legível que descreve o conteúdo da imagem.

Em seguida, use a mesma imagem para realizar legendas densas. Retorne à página inicial do Vision Studio e, como fez antes, clique em **Image analysis** e, em seguida, no bloco **Dense captioning**.

O recurso Dense Captions difere do recurso Caption porque fornece diversas legendas legíveis para uma imagem, uma descrevendo o conteúdo da imagem e outras, cada uma cobrindo os objetos essenciais detectados na imagem. Cada objeto detectado inclui uma caixa delimitadora, que define as coordenadas dos pixels na imagem associada ao objeto.

Passe o mouse sobre uma das legendas na lista de atributos detectados e observe o que acontece na imagem.



Mova o cursor do mouse sobre as outras legendas da lista e observe como a caixa delimitadora muda na imagem para destacar a parte da imagem usada para gerar a legenda.




## Marcando imagens
Retorne à página inicial do Vision Studio e clique no bloco **Extract common tags from images** na guia **Image analysis**.

Em **Choose the model you want to try out**, deixe selecionado **Prebuilt product vs. gap model**. Em **Choose your language**, selecione Inglês ou um idioma de sua preferência.

Abra a pasta que contém as imagens que você baixou e localize o arquivo chamado store-image-2.jpg , que se parece com isto:


Carregue o arquivo store-camera-2.jpg .

Revise a lista de tags extraídas da imagem e a pontuação de confiança de cada uma no painel de atributos detectados. Aqui, a pontuação de confiança é a probabilidade de o texto do atributo detectado descrever o que realmente está na imagem. Observe na lista de tags que ela inclui não apenas objetos, mas ações, como compras, vendas e permanência.


## Detecção de objetos

Retorne à página inicial do Vision Studio e clique no bloco **Detect common objects in images** na guia **Image analysis**.

Em **Choose the model you want to try out**, deixe selecionado **Prebuilt product vs. gap model**.

Abra a pasta que contém as imagens que você baixou e localize o arquivo chamado store-camera-3.jpg , que se parece com isto:


Carregue o arquivo store-camera-3.jpg .

Na caixa **Detected attributes**, observe a lista de objetos detectados e suas pontuações de confiança.

Passe o cursor do mouse sobre os objetos na lista **Detected attributes** para destacar a caixa delimitadora do objeto na imagem.

Mova o controle deslizante **Threshold value** até que um valor de 70 seja exibido à direita do controle deslizante. Observe o que acontece com os objetos da lista. O controle deslizante de limite especifica que somente objetos identificados com uma pontuação de confiança ou probabilidade maior que o limite devem ser exibidos.



## Excluir os recursos utilizados nos testes

Abra o portal do Azure em https://portal.azure.com e selecione o grupo de recursos que contém o recurso que você criou.
Selecione o recurso e clique em ```Delete``` e depois ```Yes``` para confirmar. O recurso é então excluído.





## Links utilizados

- https://learn.microsoft.com/pt-br/azure/ai-services/computer-vision/overview

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/03-image-analysis.html

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/04-face.html

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/05-ocr.html
