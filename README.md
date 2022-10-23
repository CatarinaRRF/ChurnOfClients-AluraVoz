> <B>⚠️ Esse README ainda esta sob construção</B>

> <B>⚠️ Don't speak Portuguese? access the <a href=''>EN version</a></B>

<h1 align="center">
<h1 align="center">
  <br>
  <img src="https://github.com/CatarinaRRF/Challenge-Alura-Cash-19-08-22/blob/main/media/logo_alura_cash.png" alt="logo">
</h1>

<h3 align="center">Challenge Dados 1° Edição - Alura Voz</h3>

<p align="center">
    <a href="">
    <img src="https://img.shields.io/github/last-commit/CatarinaRRF/Challenge-Alura-Cash-19-08-22?color=informational&style=flat-square"
         alt="GitHub last commit">
    <a href="https://github.com/CatarinaRRF/Challenge-Alura-Cash-19-08-22">
    <img src= http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=green&style=flat-square >

</p>

<p align="center">
  <a href="#sobre">Sobre</a> •
  <a href="#metodologia">Metodologia</a> •
  <a href="#resultados">Resultados</a> •
  <a href="#conclusão">Conclusão</a> •
  <a href="#arquivos">Arquivos</a> •
  <a href="#creditos">Creditos</a>
  
</p>

# Sobre 
<p align="justify"> A <b>Alura Voz</b>, atua na área de telecomunicações através de serviços de telefônia e como Internet Service Provider (ISP), com diversas tecnologias de internet (DNS e Fibra Otica). No mercado desde 1999, a empresa atraiu diversos clientes e parceiros na área corporativa e de telefonia celular, e se firmou como forte nome nacional em soluções que integravam internet e internet móvel, apostando em sua capacidade de entrega de soluções altamente inovadora. Porém, recentemente vem apresentando <i><b>uma alta taxa de churn</b></i> entre seus clientes, que tem prejudicado seu crescimento. * <br>
A <b>taxa de churn</b>, também conhecida como churn de clientes ou taxa de churn, é a taxa na qual os clientes param de fazer negócios com uma entidade. É mais frequentemente expresso como a porcentagem de assinantes do serviço que pararam de assinar durante um período de tempo específico. Para uma empresa expandir sua base de clientes, <b>sua taxa de crescimento</b> (medida pelo número de novos clientes) deve exceder <b>sua taxa de churn</b>. Desse modo, cabe ao cientista de dados responsavel, analizar as informações coletadas no banco de dados da empresa e destacar as informações necessarias, de modo, a auxiliar a tomada de deciçoes da empresa.

<sup>* <b>Disclamer:</b> esta empresa é ficticia e essas informações não correspondem a realidade</sup>

## Metodologia
<p align="justify"> Os dados foram obtidos através da API da empresa e foi solicitado sua analise para definir os motivos do alto churn de clientes. Assim, o projeto será dividido entre 4 partes, que contemplaram as fases da pipeline de dados sendo elas limpeza, Análise Exploratória, Modelagem e Visualização dos dados. <br>
Na fase de <b>limpeza os dados</b> será certificado se os atributos e entidades são válidos, completos e limpos para permitir o inicio de qualquer análise. Uma boa adequação significa que os dados são relevantes e que vão ajudar a resolver o problema de negócios apresentado ou determinar um curso de ação para atingir o objetivo da alura voz.<br>
Na fase de <b>análise exploratória</b> será usada de estatísticas para coletar, revisar, analisar e tirar conclusões de dados, bem como aplicar modelos matemáticos quantificados a variáveis. Além disso, na fase de <b>modelagem</b>, usando a biblioteca python Sklearn, as estatísticas também estaram no centro dos algoritmos de machine learning produzidos, capturando e traduzindo padrões de dados em evidências acionáveis.<br>
Por fim, será realizado um <b>dashboard</b>, por meio do programa Power BI, que contém indicadores e métricas referentes as descobertas durante o processo de análise dos dados. A fim de demonstrar para os stakehoadas uma noção global do perfil dos clientes e seus padrões de consumo, visualizando também, de forma dinâmica e objetiva, dados referentes a ao churn dos clientes em relação aos produtos.</p>

### Metodos usados
* Estatística inferencial
* Visualização de dados
* Machine Learning

### Tecnologias 
* Python
* Google Colab
* Python libraries: Pandas, Nunphy, Matplot.lib, Seaborn, Pandas profiling, SKLearn
* Power BI

## Resultados
Aqui se encontra resumido o que foi feito durante cada etapa

### <i>📡 Limpeza de Dados</i>
<p align="justify">A limpeza de dados é o processo de corrigir ou remover dados incorretos, corrompidos, formatados incorretamente, duplicados ou incompletos em um conjunto de dados. Desse modo, foi identificado e corrigido os problemas encontrados no dataset da Alura Voz com a intenção de estruturar esses dados, de modo que, sejam consistentes e permitam uma análise autêntica ao requisitado pelas partes interessadas. Abaixo um resumo de quais foram essas mudanças e a justificativa para tais:</p>

* <b>Normalizar dos dados</b>: As colunas do dataframe possuem dicionários como valores, logo, para extrair informações do mesmo é necessário normaliza-los
* <b>Traduzir</b> as colunas para português facilitando a compreensão das informações que contém.
* Algumas colunas possuem dados binarios que <b>não estão no formato de 0 e 1</b>, o que leva a problemas futuros. As colunas então devem ser modificados para se encaixarem nesse formato. Foram alteradas: "Telefonia", "Multiplas_Linhas", "Segurança_On-line",	"Backup_On-line",	"Proteção_Dispositivos",	"Suporte_Técnico",	"TV_Streaming",	"Streaming_Filmes", "Pagamento_Eletrônico", "Churn"
* Algumas colunas possuem <b>mais de duas variáveis</b>, também podem gerar problemas em futuras análises, mas, não podem ser trasformadas em 0 e 1 . Desse modo, será usado o metodo de One-Hot-Enconding, que fará cada variável uma nova coluna do tipo booleano(0 ou 1).
* Existem inconsistencias em Churn com números vazios, esses dados foram removidos pois, como variavel target, precisa ser o mais representativo da população possivel.
* Existem inconsistencias em Cobrança total é do tipo object e deveria ser int. 

Em clonclusão, será necessário fazer uma análise gráfica para entender quais as variáveis que são relacionadas com o churn para que a equipe de vendas tenha uma noção do cenário atual, e também para que seja possivél entender de uma forma mais clara os dados e facilite a formação de possíveis hipóteses do que está acontecendo com os clientes. Planeja-se então, fazer uma análise estatística dos dados, verificar os tipos de dados que temos, gerar gráficos de distribuição de dados binários ou categóricos, plot de Boxplots para detecção de outliers e matriz de correlação. Ou seja, uma Visualização dos dados.

### <i>📡 Análise Exploratória de Dados</i>
<p align="justify">A <b>análise exploratória de dados (EDA)</b> tem como intenção a analise e investigação dos conjuntos de dados e resumir suas principais características, geralmente usando métodos de visualização de dados. Deste modo, este relatório abordará o EDA a partir de <b>3 hipótesis principais</b>, formadas a partir de uma matrx de correlação, e a visualização de dados como direcionadores para a análise. As Hipoteses criadas são:<br>

* <b>A Primeira hipótese</b> é há da possibilidade de clientes que pagaram um valor acima da media geral na Cobrança Mensal, possuem maior taxa de evasão que os outros, e caso a hipotese seja confirmada, analizar a razão deste valor elevado.<br>
* <b>A Segunda Hipótese</b> tem como foco os produtos. A empresa oferta três tipos de serviços, sendo elas, linhas telefônicas, serviços de Internet e Serviço de Streaming, será analisado para cada serviço (e os produtos que englobam) a quantidade de churn e verificar se, existe alguma relação entre o tipo de serviço e as características dos clientes.<br>
* <b>A Terceira Hipótese</b> buscar identificar se existe alto churn entre os clientes que possuem tempo de contrato (tenure) maior em relação aos que possuem menor tenure.<br>

Alem disso, foi analisado as informações referentes ao perfil dos clientes. Isso porque, pode auxiliar o relatório futuramente na formação de novas hipótesis e na retirada de algumas conclusões. O seguinte grafíco foi produzido e o perfil dos clientes observado foi:

![image](https://user-images.githubusercontent.com/105402331/197404085-3bb064e1-7f3b-4bae-ad56-94baf22762ee.png)

<p>A partir do gráfico pode-se traçar as seguintes caracteristicas dos clientes:</p>

<b>1.</b> Maior parte dos clientes não possuem <b><em>dependentes</em></b>. <br>
<b>2.</b> Maior parte dos clientes não são <b><em>Idosos</em></b> (idade < 65 anos). <br>
<b>3.</b> Quanto ao <b><em>Sexo</em></b> e <b><em>estado civil</em></b> a proporção está bem equlibrida (quase 50%) entre <em>solteiros</em> e <em>com parceiros</em>, assim como o <em>mulheres</em> e <em>homens</em>.<br>

<p align="justify">Após a utilização de estatisticas e visualização de dados, juntamente com as informações retiradas do perfil dos clientes foi tirado as seguintes conclusões das hipoteses:

### <b>1. Conclusões da Primeira hipótese</b> 

<p align="justify">Foi observado o padrão de gastos dos clientes de forma geral e a partir disso definido a media global de gastos dos clientes (70.4) para auxiliar a criação de uma grafico que relaciona churn e o gasto mensal abaixo e acima da media, observe:</p>

![image](https://user-images.githubusercontent.com/105402331/197404900-15a944e1-d638-41bd-a18f-f1c6f6344280.png)

![image](https://user-images.githubusercontent.com/105402331/197404338-70720957-5c57-4db8-8b04-17532b53fbf6.png)

<p align="justify">No histograma de gastos é possivel perceber que maioria dos clientes pagam entre R$ 0,00 - R$ 20,00 na cobrança mensal e que pagaram entre R$ 0,00 - R$ 50,00 na cobrança anual, o que para um modelo baseado em pagamentos recorrentes essa cobrança anual esta muito baixa e já indica um problema no tenure (tempo de contrato). Além disso, no segundo gráfico podemos inferir que a hipótese 1 é verdadeira, os dados apresentam que, no caso do clientes que pagam abaixo da mediana de gastos apresentam um churn bem menor quanto aos de alto gasto. Logo, duas existe uma probalilidade de que os valores de mensalidade e/ou qualidade dos produtos não estão conseguindo competir com a concorrencia.</p>

### <b>2. Conclusões da Segunda hipótese</b>
<p align="justify">NA Segunda Hipótese tem como foco os produtos. A empresa oferta dois três de serviços, sendo elas, linhas telefônicas, serviços de Internet DSL e Internet Fibra Otica. Será analisado para cada serviço (e os produtos que englobam) a quantidade de churn e verificar se, existe alguma relação entre o tipo de serviço e as características dos clientes, com um foco, em especial, a idade (Cidadão Senior).

Primeiramente foi verificado se há relação de churn entre os serviços ofertados, e ficou claro que a quantidade de clientes esta muito concentrada no serviço de tecnologia e menos na internet DSL, observe:</p>

<p align="center"><b>Telefonia (90.3%) > Internet Fibra Optica (44%) > Internet DSL (34.4%)</b></p>

Em seguida foi verificado se há relação entre os produtos e o churn, nesse caso quantidade de churn se concentra mais na internet de fibra optica e há pouca quantidade no serviço de internet DSL. Os dados seguem a ordem de:

<p align="center"><b>Internet Fibra Optica (41.9%) > Telefonia (27.1%) > Internet DSL(19%) < </b></p>

Por fim, foi verificado se há relação entre os sub-produtos e o churn, e foi criado o seguinte grafico sunburt, para relacionar o churn desses produtos e a porcentagem que os subprodutos representam desse churn. O comportamento observado foi:

![newplot](https://user-images.githubusercontent.com/105402331/197405717-5f19a677-e62a-47a6-beea-29a14ddb2d74.png)

<p align="justify"> Quanto aos sub-produtos da Telefônia, o serviço de telefônia possui apenas o sub-produto Multiplas Linhas que apresenta menos da metade do churn deste produto. Já em relação aos sub-produtos da Internet, os serviços relacionados ao StremingTV (tv a cabo) e Streming Filmes possuem grande taxa de churn. Proteção de Dispositivos e Backup online também apresentam uma quantidade consideravel de churn Suporte Técnico e Segurança Online possuem a menor quantidade de churn.</p>

### <b>3. Conclusões da Terceira hipótese</b>
Foi analisado principalmente a coluna de ternure, e foi idenficado, primeramente, que no histograma o ternure não há normalidade, ou seja, a distribuição do tempo de contratação esta concentrada nos extremos, nesse caso, há uma grande quantidade de clientes com tempo de contratação 0 e acima de 65, observe: 

![image](https://user-images.githubusercontent.com/105402331/197406316-d8d4a539-0480-4108-a3a4-f8a829b17d24.png)

Logo, faz sentido identificar se esse comportamento vem da evasão, relacionado as duas variaveis, para isso foi criado um violinplot que representa isso:

![image](https://user-images.githubusercontent.com/105402331/197406499-f604ed7f-571f-4424-b6cf-640e5931f9e6.png)

A partir desse dados, se infere que o churn está muito concentrado em quem possui 10 ou menos tempo de contrato, o que explica o comportamento identificado pelo histograma. Uma razão para esta questão é a de que pode ter a ver com a qualidade dos produtos ou a expectativa que os clientes tinham do produto. Alguns dados que poderiam ser relacionados seria a de relação do perfil dos clientes com esse fator, por exemplo, foi identificado que há uma quantidade de Idosos maior e que, em geral, possuem necessidades mais basicas quanto a intenet e uso de telefone. Deste modo, será analisar os dados já considerando esses perfils e traçar algumas razões para esse quadro.

![image](https://user-images.githubusercontent.com/105402331/197406569-971aff8e-9310-4e5b-bdf5-26748184d959.png)

A partir do grafico pode-se dizer que pessoas que não possuem dependentes e estão solteiras, tendem a ser mais jovens, este fato somado com o fato do churn desta faixa etária ser elevado (assim como a quantidade abaixo de 10 de ternure) indicam que os serviços ofertados podem não serem capazes de suprirem está faixa étaria.
Também se pode fazer um argumento de que há uma quantidade, pequena, mas relevante de novos clientes idosos que estão evadindo. O que pode nos informar que não há uma evasão forte de clientes idosos com ternure alto por acomodação dessa população ao seriço contratato.

### <b>4. Conclusões da análise exploratória de dados (EDA)</b>
Em suma, a evasão parece estar concetrada entre os primeiros meses de contrato dos clientes, e que em geral, apresentam um perfil predominantente jovens e solteiros, sem dependetentes, indicando que os produtos ofertados não estão sendo suficientes para suprir a necessidade dessa parcela da população.
Entre os produtos ofertados a fibra optica é a que mais possui churn relativo (quantidade de clientes/churn), visto que no mercado a procura desse tipo de produto esta em alta pode indicar um sério problema de qualidade nesse produto e na sua competitividade com os concorrentes. Nessa linha, os sub-produtos de internet, apresentaram uma quantidade grande de churn relevantes, em especial os relacionados ao serviço de streming, que também são serviços de alta procura, levando a conclusão de que a competitivdade destes também está baixa.
Conclui-se que a melhor forma para minimizar a evasão de clientes na Alura Voz é ter um modelo treinado que vai classificar clientes como potenciais pessoas a deixar a empresa de modo, a auxiliar a equipe de vendas. Dessa forma, o proximo relatório tera como foco a contrução desses modelos.

### <i>📡 Modelagem de Dados</i>
Os seguintes passos realizados para a criação do modelo
* <b>Balanceando os Dados:</b> Ao se analizar a variavel target (churn) é possivel notar que nos dados existe uma quantidade desbalanceada de clientes que não evadiram para os que evadiram
* <b>Criando Dummy Classifier:</b> Para poder realmente entender e melhorar o desempenho do nosso modelo, primeiro precisamos estabelecer uma linha de base para os dados que temos.
* Foram treinados três modelos com diferentes algoritomos para identificar o que melhor se enquadra para os dados usados, foram eles: <b>SVC</b>, <b>Arvore de decisão</b> e <b>Random Forest</b>.
* Apos a comparação foi definido que o modelo de Random Forest teve melhor desempenho.
* <b>Otimizando o modelo Random Forest</b> utilizando o método RandomizedSearchCV, e apos encontrar os melhores paramêtros utilizando atributo .best_params_ criar um novo modelo melhorado.
* As sehuintes hipoteses foram determinadas a partir do modelo: 

### <i>📡 Dashboard</i>

*
*

## Conclusão
<p align="justify">Em linhas gerais, constatou-se que <b>Lorem ipsum dolor sit amet</b>. Verifica-se, portanto, <b>consectetur adipiscing elit</b>. Ademais, verifica-se <b>sed do eiusmod tempor incididunt ut labore et dolore magna aliqua</b>.

Cabe destacar ainda que Lorem ipsum dolor sit amet.
</p>

## Arquivos
<img align="right" height="150" src="https://img.freepik.com/vetores-gratis/caixa-de-armazenamento-de-arquivamento-de-arquivos-de-gabinete-de-documentos_33099-829.jpg?w=740&t=st=1662167069~exp=1662167669~hmac=fb6f9c20366de7cfa78155d9e4e0219a230a9affa0fccec9c10875147c2d2c85">

* Dados <i>"Crus"</i> <a href=''>Link</a>
* Dados processados pós limpeza de dados <a href=''>Link</a>
* Notebooks da Análise Exploratória de Dados <a href=''>Link</a>
* Notebooks da Modelagem de Dados <a href=''>Link</a>
* Dashboard <a href=''>Link</a>

## Creditos
* Challenge desenvolvido pelo Scuba Team da escola de tecnologia <a href='https://www.alura.com.br/'>Alura</a> <sup><img src='https://user-images.githubusercontent.com/105402331/187300705-229c3543-398f-41b5-9e23-44bbf5796f21.png' height=10px></sup>

<img src="https://github.com/CatarinaRRF/Challenge-Alura-Cash-19-08-22/blob/974dd832c3980dd107a36a4b6906b616bb7b71f2/media/hr_line_redme.png" alt="logo">

<p align="center">
 <a href='https://www.linkedin.com/public-profile'><img src='https://cdn-icons-png.flaticon.com/512/174/174857.png' height=20px></a> <a href='https://www.kaggle.com/ccfreitas'><img src='https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/189_Kaggle_logo_logos-512.png' height=20px></a>
</p>
