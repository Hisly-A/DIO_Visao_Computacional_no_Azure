# DIO - Visão Computacional no Azure
Reconhecimento Facial e transformação de imagens em Dados no Azure ML


## 🔎 O que é o Azure Vision Studio?	

>O Vision Studio é um conjunto de ferramentas baseadas em interface do usuário que permitem explorar, compilar e integrar recursos do Azure AI Vision. O serviço do Azure AI Vision lhe dá acesso a algoritmos avançados que processam imagens e retornam informações com base nos recursos visuais do seu interesse. Os serviços oferecidos são: OCR (reconhecimento óptico de caracteres), Análise de imagens, Detecção Facial e Análise de Vídeo.

<sub>Fonte: <https://learn.microsoft.com/pt-br/azure/ai-services/computer-vision/overview></sub>


## Criação do recurso de serviços de IA do Azure

Abra o portal do [`Azure`](https://portal.azure.com), entrando com a conta da Microsoft associada à sua assinatura do Azure.

Clique em `＋Create a resource` e pesquise por **Azure AI services**.

<div align="center">
    <img width="700" title="VC01" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC01.PNG"/>
</div>
<br>

Clique em ```Create``` para criar um plano do **Azure AI services** e configure-o da seguinte forma:
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
<br>

Clique em `Review + create` e depois `Create` e aguarde a conclusão da implantação.

<div align="center">
    <img width="700" title="VC05" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC05.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC06" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC06.PNG"/>
</div>
<br>


## Conecte seu recurso de serviço de IA do Azure ao Vision Studio

Acesse [`Vision Studio`](https://portal.vision.cognitive.azure.com), entre com sua conta e certifique-se de usar o mesmo diretório onde foi criado o recurso de serviços de IA do Azure.

Na página inicial do Vision Studio, clique em `View all resources` no título **Get started with Vision**.

<div align="center">
    <img width="700" title="VC07" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC07.PNG"/>
</div>
<br>

Na página **Select a resource to work with**, marque o recurso criado e clique em `Select as default resource`.

<div align="center">
    <img width="700" title="VC08" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC08.PNG"/>
</div>
<br>

## Detecte rostos no Vision Studio
Num navegador web, acesse o [`Vision Studio`](https://portal.vision.cognitive.azure.com).

Na página inicial **Get started with Vision**, clique na guia **Face** e, em seguida, clique no bloco **Detect Faces in an image**.

<div align="center">
    <img width="700" title="VC09" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC09.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC10" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC10.PNG"/>
</div>
<br>

No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa.

<div align="center">
    <img width="700" title="VC11" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC11.PNG"/>
</div>
<br>

Com uma das imagens de amostra selecionada observe os dados de detecção facial retornados.

<div align="center">
    <img width="700" title="VC12" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC12.PNG"/>
</div>
<br>

Agora observe que para a [`imagem01`](https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/inputs/imagem01.jpg) não foi possível reconhecer uma face:

<div align="center">
    <img width="700" title="VC13" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC13.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC14" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC14.PNG"/>
</div>
<br>

Já na imagem abaixo foi possível reconhecer a face do cachorro:

<div align="center">
    <img width="700" title="VC15" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC15.PNG"/>
</div>
<br>

Na [`imagem03`](https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/inputs/imagem03.jpg) foi possível reconhecer o rosto das pessoas, mas não dos cães.

<div align="center">
    <img width="700" title="VC16" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC16.PNG"/>
</div>
<br>

## Extraia texto de imagens no Vision Studio
Acesse o [`Vision Studio`](https://portal.vision.cognitive.azure.com).

Na página inicial **Get started with Vision**, clique em **Optical character recognition** e, em seguida, no bloco **Extract text from images**.

<div align="center">
    <img width="700" title="VC17" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC17.PNG"/>
</div>
<br>

No subtítulo **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa e em seguida clique em `Browse for a file` e navegue até a pasta do computador onde a imagem foi salva, selecione-a e clique em `Open`.

<div align="center">
    <img width="700" title="VC18" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC18.PNG"/>
</div>
<br>

Em **Detected attributes**, qualquer texto encontrado na imagem é organizado em uma estrutura hierárquica de regiões, linhas e palavras.

<div align="center">
    <img width="700" title="VC20" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC20.PNG"/>
</div>
<br>

A localização do texto é indicada por uma caixa delimitadora, conforme a imagem abaixo:

<div align="center">
    <img width="700" title="VC21" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC21.PNG"/>
</div>
<br>

Observe alguns detalhes do JSON gerado para uma das imagens:

<div align="center">
    <img width="700" title="VC19" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC19.PNG"/>
</div>
<br>


## Gerar legendas para uma imagem

Na página **Get started with Vision**, clique em **Image analysis** e, em seguida, no bloco **Add captions to images**.

<div align="center">
    <img width="700" title="VC22" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC22.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC23" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC23.PNG"/>
</div>
<br>

Em **Try it out**, reconheça a política de uso de recursos lendo e marcando a caixa.

<div align="center">
    <img width="700" title="VC24" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC24.PNG"/>
</div>
<br>

Abra a pasta do computador, localize e carregue a imagem arrastando-a para a caixa **Drag and drop files here** ou navegando até ela em seu sistema de arquivos.

Observe o texto da legenda gerado, visível no painel **Detected attributes** à direita da imagem:

<div align="center">
    <img width="700" title="VC25" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC25.PNG"/>
</div>
<br>

Observe o detalhe do JSON gerado para a imagem:

<div align="center">
    <img width="700" title="VC26" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC26.PNG"/>
</div>
<br>

A funcionalidade Caption fornece uma única frase em inglês legível que descreve o conteúdo da imagem.

Em seguida, use a mesma imagem para realizar legendas densas. Retorne à página inicial do Vision Studio e, como fez antes, clique em **Image analysis** e, em seguida, no bloco **Dense captioning**.

<div align="center">
    <img width="700" title="VC27" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC27.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC28" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC28.PNG"/>
</div>
<br>

O recurso Dense Captions difere do recurso Caption porque fornece diversas legendas legíveis para uma imagem, uma descrevendo o conteúdo da imagem e outras, cada uma cobrindo os objetos essenciais detectados na imagem. Cada objeto detectado inclui uma caixa delimitadora, que define as coordenadas dos pixels na imagem associada ao objeto.

<div align="center">
    <img width="700" title="VC29" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC29.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC30" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC30.PNG"/>
</div>
<br>

Mova o cursor do mouse sobre as legendas da lista e observe como a caixa delimitadora muda na imagem para destacar a parte da imagem usada para gerar a legenda:

<div align="center">
    <img width="700" title="VC31" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC31.PNG"/>
</div>
<br>

## Marcando imagens

Retorne à página inicial do [`Vision Studio`](https://portal.vision.cognitive.azure.com) e clique no bloco **Extract common tags from images** na guia **Image analysis**.

<div align="center">
    <img width="700" title="VC32" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC32.PNG"/>
</div>
<br>

Em **Choose the model you want to try out**, deixe selecionado **Prebuilt product vs. gap model**. Em **Choose your language**, selecione Inglês ou um idioma de sua preferência.

<div align="center">
    <img width="700" title="VC33" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC33.PNG"/>
</div>
<br>

Carregue uma imagem e revise a lista de tags extraídas da imagem e a pontuação de confiança de cada uma no painel de atributos detectados. Aqui, a pontuação de confiança é a probabilidade de o texto do atributo detectado descrever o que realmente está na imagem.

<div align="center">
    <img width="700" title="VC34" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC34.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC35" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC35.PNG"/>
</div>
<br>

## Detecção de objetos

Retorne à página inicial do [`Vision Studio`](https://portal.vision.cognitive.azure.com) e clique no bloco **Detect common objects in images** na guia **Image analysis**.

<div align="center">
    <img width="700" title="VC36" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC36.PNG"/>
</div>
<br>

Em **Choose the model you want to try out**, deixe selecionado **Prebuilt product vs. gap model**.

<div align="center">
    <img width="700" title="VC37" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC37.PNG"/>
</div>
<br>

Carregue uma imagem e na caixa **Detected attributes**, observe a lista de objetos detectados e suas pontuações de confiança.

Passe o cursor do mouse sobre os objetos na lista **Detected attributes** para destacar a caixa delimitadora do objeto na imagem.

<div align="center">
    <img width="700" title="VC38" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC38.PNG"/>
</div>
<br>

Mova o controle deslizante **Threshold value** até que um valor de 70 seja exibido à direita do controle deslizante. Observe o que acontece com os objetos da lista. O controle deslizante de limite especifica que somente objetos identificados com uma pontuação de confiança ou probabilidade maior que o limite devem ser exibidos.

<div align="center">
    <img width="700" title="VC39" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC39.PNG"/>
</div>
<br>

## Excluir os recursos utilizados nos testes

Abra o portal do [`Azure`](https://portal.azure.com) e selecione o grupo de recursos que contém o recurso criado.

<div align="center">
    <img width="700" title="VC40" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC40.PNG"/>
</div>
<br>

Selecione o recurso e clique em `Delete resource group` e depois `Delete` novamente para confirmar.

<div align="center">
    <img width="700" title="VC41" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC41.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC42" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC42.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC43" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC43.PNG"/>
</div>
<br>

O recurso é então excluído:

<div align="center">
    <img width="700" title="VC44" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC44.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC45" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC45.PNG"/>
</div>
<br>
<div align="center">
    <img width="700" title="VC46" src="https://github.com/Hisly-A/DIO_Visao_Computacional_no_Azure/blob/main/output/VC46.PNG"/>
</div>
<br>

## Links utilizados

- https://learn.microsoft.com/pt-br/azure/ai-services/computer-vision/overview

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/03-image-analysis.html

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/04-face.html

- https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/05-ocr.html
