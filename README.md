<h1><strong>Rossmann Stores Sales Forecast</strong></h1>
<h1><strong>Previs&atilde;o de Vendas das Lojas Rossmann</strong></h1>
<p>(INSERIR TITULO EM IMAGEM)</p>
<h2><strong>Problema de Neg&oacute;cio</strong></h2>
<p>O CFO (Chief Financial Officer) da Rossmann precisa determinar qual parcela do faturamento de cada unidade sera destinado a sua reforma. Desta forma, durante uma reuni&atilde;o mensal de resultados, solicitou a cada gerente de loja, que fosse realizada uma previs&atilde;o di&aacute;ria do faturamento de vendas das pr&oacute;ximas 6 semanas.</p>
<p>O objetivo &eacute; fornecer uma ferramenta que realize previs&otilde;es pr&oacute;ximas do real para auxiliar na decis&atilde;o de qual ser&aacute; o tamanho da parcela que o CFO determinar&aacute; para reforma de cada loja.</p>
<h2><strong>Estrutura da Solu&ccedil;&atilde;o</strong></h2>
<p>A metodologia empregada para a cria&ccedil;&atilde;o do projeto ser&aacute; a CRISP-DS (Cross Industry Standard Process for Data Science) ilustrada abaixo. Consiste em um processo c&iacute;clico de desenvolvimento, cujo foco &eacute; ser constru&iacute;do em fases que permitem a entrega r&aacute;pida de uma solu&ccedil;&atilde;o, al&eacute;m da possibilidade de melhorias e atualiza&ccedil;&otilde;es em seus processos a cada nova itera&ccedil;&atilde;o.</p>
<p>(INSERIR IMAGEM DA METODOLOGIA)</p>
<h2><strong>Quest&atilde;o de Neg&oacute;cio&nbsp;</strong></h2>
<p>A empresa atualmente n&atilde;o possui uma ferramenta de previs&atilde;o de vendas para cada loja, conforme citado anteriormente. O projeto consiste em fornecer uma solu&ccedil;&atilde;o para realizar esta previs&atilde;o de uma forma f&aacute;cil e r&aacute;pida.</p>
<h2><strong>Entendimento do Neg&oacute;cio</strong></h2>
<p>Conforme demandado pelo CFO na reuni&atilde;o mensal de resultados, uma previs&atilde;o das pr&oacute;ximas 6 semanas de vendas para cada loja deve ser feita para auxiliar em determinar quanto ser&aacute; dedicado de seu faturamento para reforma das lojas.</p>
<h2><strong>Coleta de Dados</strong></h2>
<p>Os dados utilizados para este cen&aacute;rio proposto foram fornecidos em desafio proposto pela Rossmann na plataforma Kaggle e podem ser acessados via este link:<a href="https://www.kaggle.com/competitions/rossmann-store-sales/data"> Rossmann Store Sales</a></p>
<h2><strong>Limpeza dos Dados</strong></h2>
<p>Com os dados extra&iacute;dos inicia-se a etapa de limpeza e descri&ccedil;&atilde;o dos dados, que consiste em determinar como s&atilde;o os dados que estamos trabalhando, sua quantidade, tipos de vari&aacute;veis, quantidade de dados faltantes entre outros aspectos. Segue lista das atividades realizadas:</p>
<ul>
<li aria-level="1"><strong>Descri&ccedil;&atilde;o dos dados</strong>: neste passo foram renomeadas as colunas (para facilitar sua manipula&ccedil;&atilde;o e interpreta&ccedil;&atilde;o), verificada a dimens&atilde;o dos dados (quantidade de linhas e colunas) e quais os tipos de dados que estamos trabalhando.</li>
<li aria-level="1"><strong>Tratamento de dados nulos</strong>: consiste em verificar a quantidade de dados faltantes e adotar uma solu&ccedil;&atilde;o para o preenchimento destes dados.</li>
<li aria-level="1"><strong>Transforma&ccedil;&atilde;o dos tipos dos dados</strong>: altera-se o tipo de alguns dados para facilitar c&aacute;lculos e uso de fun&ccedil;&otilde;es da linguagem utilizada.</li>
<li aria-level="1"><strong>Estat&iacute;stica Descritiva</strong>: resumo da disposi&ccedil;&atilde;o dos dados num&eacute;ricos e categ&oacute;ricos dentro do data set.</li>
<li aria-level="1"><strong>Mindmap de Hip&oacute;teses:</strong> premissas determinadas pelo time de neg&oacute;cio para serem testadas e confirmadas durante o processo de an&aacute;lise dos dados.</li>
<li aria-level="1"><strong>Feature Engineering</strong>: este processo possui a finalidade preparar e extrair informa&ccedil;&otilde;es contidas em vari&aacute;veis selecionadas do data set, como, por exemplo, year, <em>month</em>, <em>day</em>.</li>
<li aria-level="1"><strong>Filtragem das vari&aacute;veis</strong>: removemos as vari&aacute;veis, que ap&oacute;s an&aacute;lise, n&atilde;o possuem relev&acirc;ncia para resolver o problema proposto.&nbsp;</li>
</ul>
<h2><strong>Explora&ccedil;&atilde;o dos Dados</strong></h2>
<p>Este passo procurar mensurar 2 objetivos base, como as vari&aacute;veis impactam o fen&ocirc;meno e qual a for&ccedil;a deste impacto. No problema atual, o fen&ocirc;meno estudado s&atilde;o as vendas das lojas Rossmann e visa produzir insights, validar hip&oacute;teses e determinar quais as vari&aacute;veis mais importantes para o projeto. Seguem as an&aacute;lises realizadas:</p>
<ul>
<li><strong>An&aacute;lise Univariada</strong>: procurar entender os aspectos de somente uma vari&aacute;vel como, valor m&iacute;nimo, valor m&aacute;ximo, distribui&ccedil;&atilde;o no data set, extens&atilde;o de valores entre outros.</li>
<li><strong>An&aacute;lise Bivariada</strong>: verifica como esta vari&aacute;vel impacta na resposta, seja verificando por correla&ccedil;&atilde;o ou valida&ccedil;&atilde;o de hip&oacute;teses. Seguem alguns exemplos de hip&oacute;teses testadas durante o projeto:</li>
</ul>
<h3 data-toc-modified-id="H1-Lojas-com-maior-sortimento-deveriam-vender-mais.-4.2.1"><strong>Hip&oacute;tese 1 -</strong>&nbsp;Lojas com maior sortimento deveriam vender mais</h3>
<p><strong>FALSA:</strong>&nbsp;Lojas com MAIOR SORTIMENTO vendem MENOS</p>
<p>(INSERIR IMAGEM)</p>
<h3 data-toc-modified-id="H2-Lojas-com-competidores-mais-pr&oacute;ximos-deveriam-vender-menos.-4.2.2"><strong>Hip&oacute;tese 2 - </strong>Lojas com competidores mais pr&oacute;ximos deveriam vender menos.</h3>
<p><strong>FALSA:</strong> Lojas que possuem competidores mais pr&oacute;ximos vendem mais.</p>
<p>(INSERIR IMAGEM)</p>
<h3 data-toc-modified-id="H11-Lojas-deveriam-vender-menos-aos-finais-de-semana.-4.2.11"><strong>Hip&oacute;tese 11 -</strong>&nbsp;Lojas deveriam vender menos aos finais de semana.</h3>
<p>(INSERIR IMAGEM)</p>
<ul>
<li><strong>An&aacute;lise Multivariada</strong>: verifica como as vari&aacute;veis se relacionam e analisar&aacute; o impacto da rela&ccedil;&atilde;o entre estas vari&aacute;veis.</li>
</ul>
<h2><strong>Modelagem dos Dados</strong></h2>
<p>Agora inicia o processo de prepara&ccedil;&atilde;o dos dados para os modelos de Machine Learning, pois o aprendizado da maioria de seus algoritmos &eacute; facilitado com dados num&eacute;ricos na mesma escala. Para este passo utilizamos os processos de <em>Rescalling</em>, <em>Encoding,</em> Transforma&ccedil;&atilde;o de Grandeza e Natureza, e Sele&ccedil;&atilde;o de Features.&nbsp;</p>
<ul>
<li><em><strong>Rescalling</strong></em>: utilizado em vari&aacute;veis num&eacute;ricas, para a maioria optou-se por utilizar o m&eacute;todo de <em>Min-Max Scaler</em> e para vari&aacute;veis que possuem outliers de grande intensididade utilizou-se o m&eacute;todo <em>RobustScaler</em></li>
<li><strong><em>Encoding</em></strong>: aplicado em vari&aacute;veis categ&oacute;ricas, foi utilizado o m&eacute;todo <em>LabelEncoder.</em></li>
<li><strong>Transforma&ccedil;&atilde;o de Grandeza</strong>: tem como prop&oacute;sito orientar a vari&aacute;vel resposta para uma distribui&ccedil;&atilde;o mais pr&oacute;xima da normal, neste caso foi utilizado o m&eacute;todo logar&iacute;tmico.</li>
<li><strong>Transforma&ccedil;&atilde;o de Natureza: </strong>visa respeitar&nbsp;a natureza real das vari&aacute;veis, como por exemplo sua periodicidade c&iacute;clica. Neste projeto utilizou-se de tranforma&ccedil;&otilde;es de seno e cosseno.</li>
<li><strong>Sele&ccedil;&atilde;o de Features: </strong>esta estapa consiste em identificar e selecionar as vari&aacute;veis mais relevantes para o modelo, o m&eacute;todo utilizado nesta etapa foi o algoritmo Boruta.</li>
</ul>
<h2><strong>Algoritmos de Machine Learning</strong></h2>
<p>Para este projeto empregou-se o m&eacute;todo de Machine Learning (ML) para aprender o comportamento de vendas das lojas Rossmann para ent&atilde;o generaliz&aacute;-lo para o futuro. Como estamos visando predizer o resultado de um fen&ocirc;meno, constata-se que fun&ccedil;&otilde;es de regress&atilde;o s&atilde;o as mais indicadas para serem empregadas, segue abaixo lista dos algoritmos selecionados para este processo:</p>
<ul>
<li>Linear Regression Model</li>
<li>Linear Regression Regularized Model</li>
<li>Random Forest Regressor Model</li>
<li>XGBoost Regressor Model</li>
</ul>
<p>Logo ap&oacute;s a implementa&ccedil;&atilde;o de cada modelo emprega-se o m&eacute;todo de Cross-Validation, que permite receber a performance real dos algoritmos. Abaixo os resultados dos algoritmos ap&oacute;s a implementa&ccedil;&atilde;o do m&eacute;todo de Cross-Validation:</p>
<table border="1">
<tbody>
<tr>
<td>Model Name</td>
<td>MAE</td>
<td>MAPE</td>
<td>RMSE</td>
</tr>
<tr>
<td>Random Forest Regressor</td>
<td>836.99 +/- 218.08</td>
<td>0.12 +/- 0.02</td>
<td>1255.16 +/- 318.05</td>
</tr>
<tr>
<td>XGBoost Regressor</td>
<td>927.78 +/- 277.33</td>
<td>0.19 +/- 0.01</td>
<td>1389.77 +/- 386.43</td>
</tr>
<tr>
<td>Linear Regression</td>
<td>2081.73 +/- 295.63</td>
<td>0.3 +/- 0.02</td>
<td>2952.52 +/- 468.37</td>
</tr>
<tr>
<td>Linear Regression Regularized</td>
<td>2116.38 +/- 341.5</td>
<td>0.29 +/- 0.01</td>
<td>3057.75 +/- 504.26</td>
</tr>
</tbody>
</table>
<p>O algoritmo que possui a melhor performance foi o Random Forest Regressor, mas devido a sua demora em processamento optou-se pelo XGBoost pois possui resultado similar e um tempo de opera&ccedil;&atilde;o muito menor que favorece a rapidez da entrega de resultados.</p>
<h3><strong>Performance do modelo escolhido</strong></h3>
<p>Determinado o algoritmo a ser utilizado, realiza-se um processo de busca dos melhores valores de seus par&acirc;metros. Para este processo empregamos o m&eacute;todo de Random Search e alcan&ccedil;amos o seguinte resultado:</p>
<table border="1">
<tbody>
<tr>
<td>Model Name</td>
<td>MAE</td>
<td>MAPE</td>
<td>RMSE</td>
</tr>
<tr>
<td>XGBoost Regressor</td>
<td>620.067026</td>
<td>0.089582</td>
<td>910.543822</td>
</tr>
</tbody>
</table>
<h2><strong>Avalia&ccedil;&atilde;o do Algoritmo</strong></h2>
<p>Com base nos resultados obtidos podemos verificar qual a previs&atilde;o gerada pelo modelo e seus cen&aacute;rios utilizando o erro calculado para cada loja. Segue abaixo tabela e gr&aacute;fico para exemplo:</p>
<table style="border-collapse: collapse; width: 100%; height: 108px;" border="1">
<tbody>
<tr style="height: 18px;">
<th style="width: 14.0625%; height: 18px;">store</th>
<th style="width: 14.2045%; height: 18px;">predictions</th>
<th style="width: 15.0568%; height: 18px;">worst_scenario</th>
<th style="width: 14.2045%; height: 18px;">best_scenario</th>
<th style="width: 14.2045%; height: 18px;">MAE</th>
<th style="width: 14.0625%; height: 18px;">MAPE</th>
</tr>
<tr style="height: 18px;">
<td style="width: 14.0625%; height: 18px;">292</td>
<td style="width: 14.2045%; height: 18px;">104080.976562</td>
<td style="width: 15.0568%; height: 18px;">100754.290425</td>
<td style="width: 14.2045%; height: 18px;">107407.662700</td>
<td style="width: 14.2045%; height: 18px;">3326.686138</td>
<td style="width: 14.0625%; height: 18px;">0.554840</td>
</tr>
<tr style="height: 18px;">
<td style="width: 14.0625%; height: 18px;">909</td>
<td style="width: 14.2045%; height: 18px;">237274.953125</td>
<td style="width: 15.0568%; height: 18px;">229721.995436</td>
<td style="width: 14.2045%; height: 18px;">244827.910814</td>
<td style="width: 14.2045%; height: 18px;">7552.957689</td>
<td style="width: 14.0625%; height: 18px;">0.512914</td>
</tr>
<tr style="height: 18px;">
<td style="width: 14.0625%; height: 18px;">876</td>
<td style="width: 14.2045%; height: 18px;">202620.781250</td>
<td style="width: 15.0568%; height: 18px;">198622.608080</td>
<td style="width: 14.2045%; height: 18px;">206618.954420</td>
<td style="width: 14.2045%; height: 18px;">3998.173170</td>
<td style="width: 14.0625%; height: 18px;">0.299266</td>
</tr>
<tr style="height: 18px;">
<td style="width: 14.0625%; height: 18px;">550</td>
<td style="width: 14.2045%; height: 18px;">240955.656250</td>
<td style="width: 15.0568%; height: 18px;">239638.594436</td>
<td style="width: 14.2045%; height: 18px;">242272.718064</td>
<td style="width: 14.2045%; height: 18px;">1317.061814</td>
<td style="width: 14.0625%; height: 18px;">0.250513</td>
</tr>
<tr style="height: 18px;">
<td style="width: 14.0625%; height: 18px;">595</td>
<td style="width: 14.2045%; height: 18px;">393923.781250</td>
<td style="width: 15.0568%; height: 18px;">390267.315535</td>
<td style="width: 14.2045%; height: 18px;">397580.246965</td>
<td style="width: 14.2045%; height: 18px;">3656.465715</td>
<td style="width: 14.0625%; height: 18px;">0.249605</td>
</tr>
</tbody>
</table>
<h3><strong>Performance total</strong></h3>
<p>Abaixo conseguimos verificar a vis&atilde;o geral da soma da previs&atilde;o de vendas de todas as unidades da Rossmann no per&iacute;odo de 6 semanas. Serve para observar a possibilidade bater metas, por exemplo.&nbsp;</p>
<table style="border-collapse: collapse; width: 100%;" border="1">
<tbody>
<tr>
<td style="width: 33.3333%;"><strong>index</strong></td>
<th style="width: 33.2386%;">Scenario</th>
<th style="width: 33.2386%;">Values</th>
</tr>
<tr>
<th style="width: 33.3333%;">0</th>
<td style="width: 33.2386%;">predictions</td>
<td style="width: 33.2386%;">R$283,484,000.00</td>
</tr>
<tr>
<th style="width: 33.3333%;">1</th>
<td style="width: 33.2386%;">worst_scenario</td>
<td style="width: 33.2386%;">R$282,788,590.26</td>
</tr>
<tr>
<th style="width: 33.3333%;">2</th>
<td style="width: 33.2386%;">best_scenario</td>
<td style="width: 33.2386%;">R$284,179,403.04</td>
</tr>
</tbody>
</table>
<h3><strong>Performance&nbsp; de Machine Learning</strong></h3>
<p>Os gr&aacute;ficos em seguida demonstram qual a performance de nosso algoritmo em compara&ccedil;&atilde;o ao cen&aacute;rio real.</p>
<h2><strong>Modelo em Produ&ccedil;&atilde;o</strong></h2>
<p>Verificados os resultados e desempenho do algoritmo gerado nesta primeira vers&atilde;o do ciclo do CRISP-DS, decidiu-se implementar o projeto. Mesmo sendo a primeira vers&atilde;o &eacute; importante para atestar sua usabilidade, precis&atilde;o al&eacute;m de feedback para corre&ccedil;&otilde;es e melhorias.&nbsp;</p>
<p>Para a visualiza&ccedil;&atilde;o r&aacute;pida e &aacute;gil do projeto, optou-se pela solu&ccedil;&atilde;o de criar um bot que informa as previs&otilde;es de vendas para cada lojas atrav&eacute;s do aplicativo Telegram, conforme imagem abaixo:</p>
<p>&nbsp;</p>
<p>Este processo utilizou uma plataforma cloud chamada Heroku gratuitamente para hospedar nosso algoritmo e aplicativo que usa a API (Application Programming Interface) do Telegram.</p>
<p>Caso necessite de mais informa&ccedil;&otilde;es ou possua d&uacute;vidas fico a disposi&ccedil;&atilde;o, al&eacute;m de disponibilizar todos os documentos utilizado para gerar este projeto.</p>
