# Detector Universal de Lesões Covid-19 por imagens##

<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/100/426/datas/original.png" /><br /><br />
</div>


## Sobre
O Modelo foi treinado usando a biblioteca [TensorFlow.js](https://js.tensorflow.org/).

Voce pode customizar seus próprios projetos e treinar seus modelo apartir deste GitHub.
Para o desafio hackcovid19, treinamos o Modelo Mellieri MCD19 usando datasets [Sandeco - Normal e Covid-19](https://github.com/scoobiii/CanalSandeco/tree/master/Deep%20Learning%20s%C3%A9rie/%2315%20-%20Detectando%20Covid-19%20em%20imagens%20m%C3%A9dicas/dataset), [ieee8023/covid-chestxray-dataset](https://github.com/scoobiii/covid-chestxray-dataset/tree/master/images)

### Porque usar dois data-sets? 

Usamos o dataset especialiazado Sandeco (Noramal e Covid-19 o que gera elevada acurácia, e o data set ieee8023/covid-chestxray-dataset com diversar classes patológicas, unindo o melhor dos dois mundos: especialidade e generalidade:

{"tfjsVersion":"1.3.1","tmVersion":"2.1.2","packageVersion":"0.8.4","packageName":"@teachablemachine/image","timeStamp":"2020-05-20T11:28:36.478Z","userMetadata":{},"modelName":"mellieri human covid detecta 1","labels":["saars","Pneumocistose","pneumonia aspiração","pneumonia cavitante","pneumonia-clamídia-L","pneumonia por Klebsiella","pneumonia legionella","pneumonia pneumococcal","pneumonia pneumocystis carinii","pneumonia pneumocystis jirovecii","pneumonia pneumocystis-","Pneumonia Streptococcus ","NORMAL","Pneumonia","Covid-19 ARDS","Covid-19 & Pneumonia","Covid-19 Tomografia Coputadorizada ","Não Covid-19 Tomografia Computadorizada ","Covid-19","NIMG"]}

Nota: Quando acionado a WebCam, e esta não estar apontada para uma imagem de raio x ou tomografia, criamos uma classe genérica "NIMG", "NÃO IMAGEM"

### Resultados:
Identificamos subnotificão em bases oficiais.
### O que signfica + ou menos subnotificação? 
mais ou menos óbitos.
mais ou menos tempo para vc iar a praia, passear com seu cachorro, amar, pular carnaval, ir a igreja, ...,...

<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/100/426/datas/original.png" /><br /><br />
</div>

### Você tem uma imagem ai testar agora !! [CLICK AAQUI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr).


### Desenvolvimento
## Instale dependências executando (semelhante a npm install)
```
yarn
```
### Projeto de construção
```
yarn build
```
### Inicie o servidor local executando
``` yarn run watch
````
### Estilos de código
- Existe um gancho de pré-confirmação configurado que evitará confirmações quando houver erros
- Executar `yarn eslint` para es6 de erros e avisos
- Executar `yarn stylint` para stylus de erros e avisos

#### Para executar https localmente:
https é necessário para que as permissões da câmera do pc ou celular funcionem quando não estiver trabalhando com `localhost`

1 - Gerar chaves
``` openssl genrsa -out server.key 2048
openssl req -new -x509 -sha256 -key server.key -out server.cer -days 365 -subj /CN=YOUR_IP
````
2 - Use `yarn run watch-https`
3 - Acesse https://SEUIP:3000, aceite o aviso de privacidade e continue.
## Crédito
Este não é um produto oficial do Google, mas um experimento que foi um esforço colaborativo de amigos das equipes [Støj](http://stoj.io/), [Use All Five](https://useallfive.com/) and Creative Lab and [PAIR](https://ai.google/pair/) do Google.
