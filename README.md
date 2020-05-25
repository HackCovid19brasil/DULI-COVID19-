# [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr): Detector Universal de Lesões por Imagem [COVID-19]


<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/100/426/datas/original.png" /><br /><br />
</div>


## Sobre
O Modelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) foi treinado usando a biblioteca [TensorFlow.js](https://js.tensorflow.org/).

### Desenvolva seus projetos, customize e treine seus modelos usando [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr).

### Para o desafio [#hackcovid19]( https://devpost.com/software/covid-19-detect-ii), treinamos o modelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) usando os datasets:

[`CanalSandeco`](https://github.com/scoobiii/CanalSandeco/tree/master/Deep%20Learning%20s%C3%A9rie/%2315%20-%20Detectando%20Covid-19%20em%20imagens%20m%C3%A9dicas/dataset), [`ieee8023/covid-chestxray-dataset`](https://github.com/scoobiii/covid-chestxray-dataset/tree/master/images),  [`COVID-Net Open Source Initiative`](https://github.com/lindawangg/COVID-Net),  [`COVID-CT-Dataset: A CT Scan Dataset about COVID-19`](https://github.com/UCSD-AI4H/COVID-CT),  [`National Institutes of Health`](https://www.nih.gov/news-events/news-releases/nih-clinical-center-releases-dataset-32000-ct-images) e [`JHU CSSE COVID-19 Dataset`](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data).

### Diversidade de datasets? 
Treinar o modelo Deep Learning [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) com duas classes, embora com elevada `acurácia`, (96%) possui baixa assertividade:
- `"NORMAL"`
- `"COVID-19"`. 
- Isso signfica zero assertividade em detectar outras patologias normalmente associadas ao COVID-19, resultando em `subnotificação`, ou seja, um exorbitante e assustador número de pacientes que morrem em casa ou nos hospitais `Aguardando Resultado`.

<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/095/316/datas/original.jpg" /><br /><br />
</div> 

### Para mudar este cenário, incluimos as classes CPGC no modelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) - São elas: 
- `"CPGC: Classes Patológicas Genéricas Conhecidas"`. Resultando em `assertividade` do modelo  [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) .
- As classes `CPGC`:

`{"tfjsVersion":"1.3.1","tmVersion":"2.1.2","packageVersion":"0.8.4","packageName":"@teachablemachine/image","timeStamp":"2020-05-20T11:28:36.478Z","userMetadata":{},"modelName":"mellieri human covid detecta 1",`

``` "labels":["saars","Pneumocistose","pneumonia aspiração","pneumonia cavitante","pneumonia-clamídia-L","pneumonia por Klebsiella","pneumonia legionella","pneumonia pneumococcal","pneumonia pneumocystis carinii","pneumonia pneumocystis jirovecii","pneumonia pneumocystis-","Pneumonia Streptococcus ","NORMAL","Pneumonia","Covid-19 ARDS","Covid-19 & Pneumonia","Covid-19 Tomografia Coputadorizada ","Não Covid-19 Tomografia Computadorizada ","Covid-19","NIMG"]}```

### Nota:
Adicionamos a classe "NIMG" para quando for usado webcam para leitura de raio x ou tomografia não gerando falsos (positivos e negativos) quando fora da área de leitura da imagem. Essa clase signfica "NÃO IMAGEM"

### Resultados:
- Identificamos subnotificão em bases oficiais.
- Sabendo-se o correto diagnóstico/classificação orientamos os profissionais de saúde em ações assertivas/efetivas.
- Reverter o quadro: "Em pandemias morrem mais pessoas lambanças médicas, políticas e da população ontem, hoje e menos amanhã.

<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/100/457/datas/original.png" /><br /><br />
</div>

### Você tem uma imagem para testar? Click agora em [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr).

### Próximo passos.

1 - Detector de patologias por voz/assistentes uma treinado o modelo por voz, convertendo as analises clinicas em voz 
2 - Detector Universal de Patologias (cancer, insuficência cardíaca) uma vez que temos e aumentaremos o acesso a diversidade de datasetes não disponiveis até pouco tempo o que demanda parceria com o [NLCC](htt ps://www.lncc.br/). Modelado e treinado, distribuimos carga aos AWS privados para tornar escalável a solução.
NOTA: 80% dos óbitos intalianos estavam associados a cardiopatia, mas não ficou claro se eram grupos de riscos ou resultante de lesões provovocadas pelo COVID-19. Agora podemos descobrir, pela correlação e análise de diversas patologias, traçando a correlação COVID-19.

### Desenvolvimento
### Instale dependências executando (semelhante a npm install)
```
yarn
```
### Projeto de construção
```
yarn build
```
### Inicie o servidor local executando
``` 
yarn run watch
```
### Estilos de código
- Existe um gancho de pré-confirmação configurado que evitará confirmações quando houver erros
- Executar `yarn eslint` para es6 de erros e avisos
- Executar `yarn stylint` para stylus de erros e avisos

### Para executar https localmente:
https é necessário para que as permissões da câmera do pc ou celular funcionem quando não estiver trabalhando com `localhost`

1 - Gerar chaves
``` openssl genrsa -out server.key 2048
openssl req -new -x509 -sha256 -key server.key -out server.cer -days 365 -subj /CN=YOUR_IP
````
2 - Use `yarn run watch-https`
3 - Acesse `https://SEUIP:3000`, aceite o aviso de privacidade e continue.
### Crédito
Este não é um produto oficial do Google, mas um experimento que foi um esforço colaborativo de amigos das equipes [Støj](http://stoj.io/), [Use All Five](https://useallfive.com/) and Creative Lab and [PAIR](https://ai.google/pair/) do Google.
