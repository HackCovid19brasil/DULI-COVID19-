# [DULI] Detector Universal de Lesões por Imagem [COVID-19]

## Versão APP e fontes acima: 
## DULI_APP_Android.apk	
## DULI_Android_Fontes.tar.gz



## Sobre
O Modelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) foi treinado usando a biblioteca [TensorFlow.js](https://js.tensorflow.org/).

### Desenvolva seus projetos, customize e treine seus modelos usando [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr).

#### Para o desafio [#hackcovid19]( https://devpost.com/software/covid-19-detect-ii), treinamos o modelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) usando os datasets:

[`CanalSandeco`](https://github.com/scoobiii/CanalSandeco/tree/master/Deep%20Learning%20s%C3%A9rie/%2315%20-%20Detectando%20Covid-19%20em%20imagens%20m%C3%A9dicas/dataset), [`ieee8023/covid-chestxray-dataset`](https://github.com/scoobiii/covid-chestxray-dataset/tree/master/images),  [`COVID-Net Open Source Initiative`](https://github.com/lindawangg/COVID-Net),  [`COVID-CT-Dataset: A CT Scan Dataset about COVID-19`](https://github.com/UCSD-AI4H/COVID-CT),  [`National Institutes of Health`](https://www.nih.gov/news-events/news-releases/nih-clinical-center-releases-dataset-32000-ct-images) e [`JHU CSSE COVID-19 Dataset`](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data).

### Diversidade de datasets? 
Geralmente os modelos DeepLearning para detecção de patologias são treinados com duas classes, e, embora possuam elevada `acurácia`, (96%) possuem zero assertividade a saber:
- `"NORMAL"`
- `"COVID-19"`. 
- Incapacidade de detectar outras patologias normalmente associadas ao COVID-19, resultando em zero assertividade, ou seja, `subnotificação`, que significam elevado número de óbitos de pacientes em casa ou nos hospitais `Aguardando Resultado`.

<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/095/316/datas/original.jpg" /><br /><br />
</div> 

### Subnotificação ZERO: Incluimos no modelo  [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) as classes CPGC  - São elas: 
- `"CPGC: Classes Patológicas Genéricas Conhecidas"`.

`{"tfjsVersion":"1.3.1","tmVersion":"2.1.2","packageVersion":"0.8.4","packageName":"@teachablemachine/image","timeStamp":"2020-05-20T11:28:36.478Z","userMetadata":{},"modelName":"mellieri human covid detecta 1",`

``` "labels":["saars","Pneumocistose","pneumonia aspiração","pneumonia cavitante","pneumonia-clamídia-L","pneumonia por Klebsiella","pneumonia legionella","pneumonia pneumococcal","pneumonia pneumocystis carinii","pneumonia pneumocystis jirovecii","pneumonia pneumocystis-","Pneumonia Streptococcus ","NORMAL","Pneumonia","Covid-19 ARDS","Covid-19 & Pneumonia","Covid-19 Tomografia Coputadorizada ","Não Covid-19 Tomografia Computadorizada ","Covid-19","NIMG"]}```

### Nota:
Adicionamos a classe `"NIMG" (NÃO IMAGEM)` útil no modo webcam, impedindo falsos positivos/negativos quando fora da área de leitura das imagens fisicas de raio x ou tomografica.

### Resultados:
- Identificamos subnotificação em bases oficiais.
- Sabendo-se o correto diagnóstico/classificação orientamos os profissionais de saúde em ações assertivas/efetivas.
- Reverter o quadro: "Em pandemias morrem mais pessoas lambanças médicas, políticas e da população ontem, hoje e menos amanhã.

<div align="center">
  <img src="https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/100/457/datas/original.png" /><br /><br />
</div>

### Você tem uma imagem para testar? Click agora em [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr).

### Próximo passos.
- Detector de patologias por voz/assistentes.
- Detector Universal de Patologias (cancer, insuficência cardíaca, .., outros)
- Parceria Estratégica [NLCC](htt ps://www.lncc.br/) em virtude da quantidade e diversidade de datasets processados pelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr).


##NOTA:
80% dos óbitos Italianos provocados pela pandemia de COVID-19 estavam associados a insuficiência cardiovascular, mas não ficou claro se eram grupos de risco ou resultante de lesões provocadas pelo COVID-19. Agora podemos descobrir, pela correlação e análise de diversas patologias que o modelo [DULI](https://teachablemachine.withgoogle.com/models/1f9ATyXbr) pode processar e entregar.

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
