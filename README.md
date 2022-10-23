> <B>⚠️ Don't speak Portuguese? access the <a href=''>EN version</a></B>

<h1 align="center">
<h1 align="center">
  <br>
  <img src="https://camo.githubusercontent.com/aa692eada954179409fa3b8ab82fcac93f680effe075a086b1c523966e044f9e/68747470733a2f2f692e696d6775722e636f6d2f6a6e376b6d386f2e706e67" alt="logo">
</h1>

<h3 align="center">Challenge Dados 1° Edição - Alura Voz</h3>

<p align="center">
    <a href="">
    <img src="https://img.shields.io/github/last-commit/CatarinaRRF/Churn_Alura_Voz?color=informational&style=flat-square"
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
<p align="justify"> A <b>Alura Voz</b>, atua na área de telecomunicações através de serviços de telefonia e como Internet Service Provider (ISP), com diversas tecnologias de internet (DNS e Fibra Ótica). No mercado desde 1999, a empresa atraiu diversos clientes e parceiros na área corporativa e de telefonia celular, e se firmou como forte nome nacional em soluções que integravam internet e internet móvel, apostando em sua capacidade de entrega de soluções altamente inovadoras. Porém, recentemente vem apresentando <i><b>uma alta taxa de churn</b></i> entre seus clientes, que tem prejudicado seu crescimento. * <br>
A <b>taxa de churn</b>, também conhecida como churn de clientes ou taxa de churn, é a taxa na qual os clientes param de fazer negócios com uma entidade. É mais frequentemente expresso como a porcentagem de assinantes do serviço que pararam de assinar durante um período de tempo específico. Para uma empresa expandir sua base de clientes, <b>sua taxa de crescimento</b> (medida pelo número de novos clientes) deve exceder <b>sua taxa de churn</b>. Desse modo, cabe ao cientista de dados responsável, analisar as informações coletadas no banco de dados da empresa e destacar as informações necessárias, de modo, a auxiliar na tomada de decisões da empresa.

<sup>* <b>Disclaimer:</b> esta empresa é fictícia e essas informações não correspondem à realidade</sup>

## Metodologia
<p align="justify"> Os dados foram obtidos através da API da empresa e foi solicitado sua análise para definir os motivos do alto churn de clientes. Assim, o projeto será dividido entre 4 partes, que contemplaram as fases da pipeline de dados sendo elas limpeza, análise exploratória, modelagem e visualização dos dados. <br>
Na fase de <b>limpeza os dados</b> será certificado se os atributos e entidades são válidos, completos e limpos para permitir o início de qualquer análise. Uma boa adequação significa que os dados são relevantes e que vão ajudar a resolver o problema de negócios apresentado ou determinar um curso de ação para atingir o objetivo da alura voz.<br>
Na fase de <b>análise exploratória</b> será usada de estatísticas para coletar, revisar, analisar e tirar conclusões de dados, bem como aplicar modelos matemáticos quantificados a variáveis. Além disso, na fase de <b>modelagem</b>, usando a biblioteca python Sklearn, as estatísticas também estarão no centro dos algoritmos de machine learning produzidos, capturando e traduzindo padrões de dados em evidências acionáveis.<br>
Por fim, será realizado um <b>dashboard</b>, por meio do programa Power BI, que contém indicadores e métricas referentes às descobertas durante o processo de análise dos dados. A fim de demonstrar para os stakeholders uma noção global do perfil dos clientes e seus padrões de consumo, visualizando também, de forma dinâmica e objetiva, dados referentes ao churn dos clientes em relação aos produtos.</p>

### Métodos usados
* Estatística inferencial
* Visualização de dados
* Machine Learning

### Tecnologias 
* Python
* Google Colab
* Python libraries: Pandas, Numpy, Matplotlib, Seaborn, Pandas profiling, SKLearn
* Power BI

## Resultados
Aqui se encontra resumido o que foi feito durante cada etapa

### <i>📡 Limpeza de Dados</i>
<p align="justify">A limpeza de dados é o processo de corrigir ou remover dados incorretos, corrompidos, formatados incorretamente, duplicados ou incompletos em um conjunto de dados. Desse modo, foi identificado e corrigido os problemas encontrados no dataset da Alura Voz com a intenção de estruturar esses dados, de modo que, sejam consistentes e permitam uma análise autêntica ao requisitado pelas partes interessadas. Abaixo um resumo de quais foram essas mudanças e a justificativa para tais:</p>

* <b>Normalização dos dados</b>: As colunas do dataframe possuem dicionários como valores, logo, para extrair informações do mesmo é necessário normalizá-los
* <b>Traduzir</b> as colunas para português facilitando a compreensão das informações que contém.
* Algumas colunas possuem dados binários que <b>não estão no formato de 0 e 1</b>, o que leva a problemas futuros. As colunas então devem ser modificadas para se encaixarem nesse formato. Foram alteradas: "Telefonia", "Múltiplas Linhas", "Segurança On-line",	"Backup On-line",	"Proteção Dispositivos",	"Suporte Técnico",	"TV Streaming",	"Streaming Filmes", "Pagamento Eletrônico", "Churn"
* Algumas colunas possuem <b>mais de duas variáveis</b>, também podem gerar problemas em futuras análises, mas, não podem ser transformadas em 0 e 1 . Desse modo, será usado o método de One-Hot-Encoding, que fará cada variável uma nova coluna do tipo booleano(0 ou 1).
* Existem inconsistências em Churn com números vazios, esses dados foram removidos pois, como variável target, precisa ser o mais representativo da população possível.
* Existem inconsistências em Cobrança total é do tipo object e deveria ser int. 

Em conclusão, será necessário fazer uma análise gráfica para entender quais as variáveis que são relacionadas com o churn para que a equipe de vendas tenha uma noção do cenário atual, e também para que seja possível entender de uma forma mais clara os dados e facilite a formação de possíveis hipóteses do que está acontecendo com os clientes. Planeja-se então, fazer uma análise estatística dos dados, verificar os tipos de dados que temos, gerar gráficos de distribuição de dados binários ou categóricos, plot de Boxplots para detecção de outliers e matriz de correlação. Ou seja, uma visualização dos dados.

### <i>📡 Análise Exploratória de Dados</i>
<p align="justify">A <b>análise exploratória de dados (EDA)</b> tem como intenção a análise e investigação dos conjuntos de dados e resumir suas principais características, geralmente usando métodos de visualização de dados. Deste modo, este relatório abordará o EDA a partir de <b>3 hipóteses principais</b>, formadas a partir de uma matriz de correlação, e a visualização de dados como direcionadores para a análise. As Hipóteses criadas são:<br>

* <b>A Primeira hipótese</b> é há da possibilidade de clientes que pagaram um valor acima da média geral na Cobrança Mensal, possuem maior taxa de evasão que os outros, e caso a hipótese seja confirmada, analisar a razão deste valor elevado.<br>
* <b>A Segunda Hipótese</b> tem como foco os produtos. A empresa oferta três tipos de serviços, sendo elas, linhas telefônicas, serviços de Internet e Serviço de Streaming, será analisado para cada serviço (e os produtos que englobam) a quantidade de churn e verificar se, existe alguma relação entre o tipo de serviço e as características dos clientes.<br>
* <b>A Terceira Hipótese</b> buscar identificar se existe alto churn entre os clientes que possuem tempo de contrato (tenure) maior em relação aos que possuem menor tenure.<br>

Além disso, foram analisadas as informações referentes ao perfil dos clientes. Isso porque, pode auxiliar o relatório futuramente na formação de novas hipóteses e na retirada de algumas conclusões. O seguinte gráfico foi produzido e o perfil dos clientes observado foi:

<img align="right" src="https://user-images.githubusercontent.com/105402331/197404085-3bb064e1-7f3b-4bae-ad56-94baf22762ee.png">

<p>A partir do gráfico pode-se traçar as seguintes características dos clientes:</p>


<ol>
<li> Maior parte dos clientes não possuem <b><em>dependentes</em></b>.</li>
<li> Maior parte dos clientes não são <b><em>Idosos</em></b> (idade < 65 anos).</li>
<li><p align="justify">Quanto ao <b><em>Sexo</em></b> e <b><em>estado civil</em></b> a proporção está bem equlibrida (≅ 50%) entre <em>solteiros</em> e <em>com parceiros</em>, assim como o <em>mulheres</em> e <em>homens</em>.</p></li>
</ol>
 
<p align="justify">Após a utilização de estatísticas e visualização de dados, juntamente com as informações retiradas do perfil dos clientes foi tirado as seguintes conclusões das hipóteses:

### <b>1. Conclusões da Primeira hipótese</b> 

<p align="justify">Foi observado o padrão de gastos dos clientes de forma geral e a partir disso definido a média global de gastos dos clientes (70.4) para auxiliar a criação de uma gráfico que relaciona churn e o gasto mensal abaixo e acima da média, observe:</p>

<img src="https://user-images.githubusercontent.com/105402331/197404900-15a944e1-d638-41bd-a18f-f1c6f6344280.png"> <img src="https://user-images.githubusercontent.com/105402331/197404338-70720957-5c57-4db8-8b04-17532b53fbf6.png">

<p align="justify">No histograma de gastos é possível perceber que maioria dos clientes pagam entre R$ 0,00 - R$ 20,00 na cobrança mensal e que pagaram entre R$ 0,00 - R$ 50,00 na cobrança anual, o que para um modelo baseado em pagamentos recorrentes essa cobrança anual está muito baixa e já indica um problema no tenure (tempo de contrato). Além disso, no segundo gráfico podemos inferir que a hipótese 1 é verdadeira, os dados apresentam que, no caso dos clientes que pagam abaixo da mediana de gastos, apresentam um churn bem menor quanto aos de alto gasto. Logo, duas existe uma probabilidade de que os valores de mensalidade e/ou qualidade dos produtos não estão conseguindo competir com a concorrência.</p>

### <b>2. Conclusões da Segunda hipótese</b>
<p align="justify">Na Segunda Hipótese tem como foco os produtos. A empresa oferta dois três de serviços, sendo elas, linhas telefônicas, serviços de Internet DSL e Internet Fibra Ótica. Será analisado para cada serviço (e os produtos que englobam) a quantidade de churn e verificar se existe alguma relação entre o tipo de serviço e as características dos clientes, com um foco, em especial, a idade (Cidadão Sénior).<br>
Primeiramente foi verificado se há relação de churn entre os serviços ofertados, e ficou claro que a quantidade de clientes está muito concentrada no serviço de tecnologia e menos na internet DSL, observe:</p>

<p align="center"><b>Telefonia (90.3%) > Internet Fibra Óptica (44%) > Internet DSL (34.4%)</b></p>

<p align="justify">Em seguida foi verificado se há relação entre os produtos e o churn, nesse caso quantidade de churn se concentra mais na internet de fibra óptica e há pouca quantidade no serviço de internet DSL. Os dados seguem a ordem de:</p>

<p align="center"><b>Internet Fibra Optica (41.9%) > Telefonia (27.1%) > Internet DSL(19%) < </b></p>

<p align="justify">Por fim, foi verificado se há relação entre os subprodutos e o churn, e foi criado o seguinte gráfico sunburst, para relacionar o churn desses produtos e a porcentagem que os subprodutos representam desse churn. O comportamento observado foi:</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/105402331/197405717-5f19a677-e62a-47a6-beea-29a14ddb2d74.png">  
</p>
  
<p align="justify"> Quanto aos subprodutos da Telefonia, o serviço de telefonia possui apenas o subproduto Múltiplas Linhas que apresenta menos da metade do churn deste produto. Já em relação aos subprodutos da Internet, os serviços relacionados ao Streaming TV (tv a cabo) e Streaming Filmes possuem grande taxa de churn. Proteção de Dispositivos e Backup online também apresentam uma quantidade considerável de churn Suporte Técnico e Segurança Online possuem a menor quantidade de churn.</p>

### <b>3. Conclusões da Terceira hipótese</b>
<p align="justify">Foi analisado principalmente a coluna de tenure, e foi identificado, primeiramente, que no histograma o tenure não há normalidade, ou seja, a distribuição do tempo de contratação está concentrada nos extremos, nesse caso, há uma grande quantidade de clientes com tempo de contratação 0 e acima de 65, observe:</p> 

<p align="center">
<img src="https://user-images.githubusercontent.com/105402331/197406316-d8d4a539-0480-4108-a3a4-f8a829b17d24.png">  
</p>

Logo, faz sentido identificar se esse comportamento vem da evasão, relacionado as duas variáveis, para isso foi criado um violin plot que representa isso:

<p align="center">
<img src="https://user-images.githubusercontent.com/105402331/197406499-f604ed7f-571f-4424-b6cf-640e5931f9e6.png">  
</p>

<p align="justify">A partir desses dados, se infere que o churn está muito concentrado em quem possui 10 ou menos tempo de contrato, o que explica o comportamento identificado pelo histograma. Uma razão para esta questão é a de que pode ter a ver com a qualidade dos produtos ou a expectativa que os clientes tinham do produto. Alguns dados que poderiam ser relacionados seria a relação do perfil dos clientes com esse fator, por exemplo, foi identificado que há uma quantidade de Idosos maior e que, em geral, possuem necessidades mais básicas quanto a internet e uso de telefone. Deste modo, será possível analisar os dados já considerando esses perfis e traçar algumas razões para esse quadro.</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/105402331/197406569-971aff8e-9310-4e5b-bdf5-26748184d959.png">  
</p>

<p align="justify">A partir do gráfico pode-se dizer que pessoas que não possuem dependentes e estão solteiras, tendem a ser mais jovens, este fato somado com o fato do churn desta faixa etária ser elevado (assim como a quantidade abaixo de 10 de tenure) indicam que os serviços ofertados podem não serem capazes de suprirem esta faixa etária. Também se pode fazer um argumento de que há uma quantidade pequena, mas relevante de novos clientes idosos que estão evadindo. O que pode nos informar que não há uma evasão forte de clientes idosos com tenure alta por acomodação dessa população ao serviço contratado.</p>

### <b>4. Conclusões da análise exploratória de dados (EDA)</b>
<p align="justify">Em suma, a evasão parece estar concentrada entre os primeiros meses de contrato dos clientes, e que em geral, apresentam um perfil predominantemente jovens e solteiros, sem dependentes, indicando que os produtos ofertados não estão sendo suficientes para suprir a necessidade dessa parcela da população.
Entre os produtos ofertados a fibra óptica é a que mais possui churn relativo (quantidade de clientes/churn), visto que no mercado a procura desse tipo de produto está em alta pode indicar um sério problema de qualidade nesse produto e na sua competitividade com os concorrentes. Nessa linha, os subprodutos de internet, apresentaram uma quantidade grande de churn relevantes, em especial os relacionados ao serviço de streaming, que também são serviços de alta procura, levando a conclusão de que a competitividade destes também está baixa.<br>
Conclui-se que a melhor forma para minimizar a evasão de clientes na Alura Voz é ter um modelo treinado que vai classificar clientes como potenciais pessoas a deixar a empresa de modo a auxiliar a equipe de vendas. Dessa forma, o próximo relatório terá como foco a construção desses modelos.</p>

### <i>📡 Modelagem de Dados</i>
Os seguintes passos realizados para a criação do modelo:

* <b>Balanceando os Dados:</b> Ao se analisar a variável target (churn) é possível notar que nos dados existe uma quantidade desbalanceada de clientes que não evadiram para os que evadiram
* <b>Criando Dummy Classifier:</b> Para poder realmente entender e melhorar o desempenho do nosso modelo, primeiro precisamos estabelecer uma linha de base para os dados que temos.
* Foram treinados três modelos com diferentes algoritmos para identificar o que melhor se enquadra para os dados usados, foram eles: <b>SVC</b>, <b>Árvore de decisão</b> e <b>Random Forest</b>.
* Após a comparação foi definido que o modelo de Random Forest teve melhor desempenho.
* <b>Otimizando o modelo Random Forest</b> utilizando o método RandomizedSearchCV, e após encontrar os melhores parâmetros utilizando atributo .best_params_ criar um novo modelo melhorado. 

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
* Dados processados após limpeza de dados <a href=''>Link</a>
* Notebooks da Análise Exploratória de Dados <a href=''>Link</a>
* Notebooks da Modelagem de Dados <a href=''>Link</a>
* Dashboard <a href=''>Link</a>

## Créditos
* Challenge desenvolvido pelo Scuba Team da escola de tecnologia <a href='https://www.alura.com.br/'>Alura</a> <sup><img src='https://user-images.githubusercontent.com/105402331/187300705-229c3543-398f-41b5-9e23-44bbf5796f21.png' height=10px></sup>

<img src="https://github.com/CatarinaRRF/Challenge-Alura-Cash-19-08-22/blob/974dd832c3980dd107a36a4b6906b616bb7b71f2/media/hr_line_redme.png" alt="logo">

<p align="center">
 <a href='https://www.linkedin.com/public-profile'><img src='https://cdn-icons-png.flaticon.com/512/174/174857.png' height=20px></a> <a href='https://www.kaggle.com/ccfreitas'><img src='https://cdn4.iconfinder.com/data/icons/logos-and-brands/512/189_Kaggle_logo_logos-512.png' height=20px></a>
</p>


