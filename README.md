Neste notebook, faremos uma análise exploratória de um dataset sobre perfil de freelancers na área de tecnologia retirado do kaggle. Extrairemos insights a partir de perguntas previamente formuladas e tiraremos conclusões a partir desses insights.

**Perguntas a serem respondidas:**

- Perfil dos freelancers e sua relação com os ganhos
1. Quais categorias de trabalho geram os maiores e menores ganhos para os freelancers?
2. Como o nível de experiência impacta a média de ganhos e o sucesso nas plataformas? <br>
3. Qual a distribuição dos ganhos por hora entre freelancers? Existe alguma discrepância entre plataformas ou níveis de experiência? <br>
- Plataformas e modelos de contratação**
1. Qual plataforma oferece os melhores ganhos médios para freelancers?
2. Freelancers que trabalham com projetos por hora ganham mais do que os que trabalham com preço fixo? <br>
- Duração dos trabalhos e seu impacto**
1. Projetos mais longos resultam em maiores ganhos? Qual a relação entre Job_Duration_Days e Earnings_USD?
2. Existe alguma relação entre duração do projeto e taxa de sucesso ou satisfação dos clientes?

Vamos primeiro entender o **Perfil dos freelancers e sua relação com os ganhos**

Antes de obter o ganho médio por categoria de trabalho, vamos analisar se existem outliers que podem distorcer a média.

![image](https://github.com/user-attachments/assets/1ce7ec81-9709-45b2-a3bc-f57ca6a986b4)

Os números de ganhos em USD são bem distribuídos e não possuem outliers.

Dessa forma, podemos utilizar a média de ganhos por categoria de trabalho para identificar as categorias que mais pagam.

![image](https://github.com/user-attachments/assets/ae34d67d-6d77-4ca3-bd5e-e121be8fe8be)

Podemos dizer que a categoria de trabalho que obtém mais ganhos em média é a App Development. Por outro lado, a que obtém menos ganhos em média é a de SEO.

Agora, vamos responder à pergunta: **Como o nível de experiência impacta a média de ganhos e o sucesso nas plataformas?**

Primeiramente, vamos, por precaução, analisar a coluna 'Job_Success_Rate' para entender se há outliers que distorçam a média.

![image](https://github.com/user-attachments/assets/66f8d4e7-1e4e-456c-bea0-7a9a70522064)

De acordo com o gráfico do boxplot, os dados de sucesso do trabalho estão distribuídos de maneira semelhante, tendo em vista o nível de experiência. Também podemos concluir que não há outliers. Deste modo, podemos continuar com a análise utilizando a média sem preocupações.

![image](https://github.com/user-attachments/assets/9ee2de6c-6875-4dd6-b84b-aae8a3f189ad)

A partir desses gráficos, podemos observar que o nível "Expert" ganha menos em média e também tem a menor taxa de sucesso. Essa é uma observação notável a se fazer, porque intuitivamente o nível "Expert" deveria ser o que mais ganha e o que mais obtém sucesso em seus trabalhos, visto o nível de experiência. Faz-se necessária uma investigação sobre este fenômeno.

Hipóteses:

1. Profissionais de níveis "Beginner" e "Intermediate" aceitam trabalhos menos desafiadores, e por isso a taxa de sucesso é maior;
2. Por serem trabalhos menos desafiadores, levam menos tempo para conclusão e, por conseguinte, tais profissionais se tornam mais produtivos e aumentam seus ganhos médios;
2. Profissionais de nível "Expert" aceitam menos trabalhos.

Para testar essas hipóteses, realizaremos as seguintes análises:

- Distribuição de Ganhos por Hora
- Trabalhos completados 
- Taxa de Sucesso por Tipo de Projeto
- Volume de trabalhos aceitos

![image](https://github.com/user-attachments/assets/1e8e08e8-08f8-4e47-b031-64c6dfd1fc71)

Os freelancers iniciantes completam mais trabalhos, e os intermediários e experts empatam neste quesito.<br>
**O fato dos freelancers iniciantes completarem mais trabalhos pode estar relacionado com o maior ganho bruto em USD anteriormente observado.**<br>
<br>Quanto aos ganhos por hora, os freelancers intermediários superam os experts. Por que isso acontece?<br>
Vamos explorar a diferença da quantidade de freelancers x ganhos entre as plataformas:

![image](https://github.com/user-attachments/assets/a384d822-8234-444a-9e45-3b0fd29613f9)
![image](https://github.com/user-attachments/assets/e4a90ebc-344e-4104-881a-49d9c197e62b)

A plataforma upwork é a que há mais freelancers na amostra, e também a plataforma que mais paga os freelancers intermediários.
- O ganho por hora dos freelancers intermediários na plataforma upwork é o maior entre os níveis de experiência
- Para o nível Expert, a plataforma que melhor valoriza esses profissionais é a "PeoplePerHour"
- Para o nível Beginner, a melhor oportunidade está na "Fiverr"

Freelancers que trabalham com projetos por hora ganham mais do que os que trabalham com preço fixo? Vamos checar.

![image](https://github.com/user-attachments/assets/f6671d8c-16f7-499d-ae02-46c5a65eb273)

Podemos concluir que, independente da plataforma, os ganhos por hora são ligeraimente maiores em projetos com contratos fixos.

# Verificação de correlações

Vamos verificar se os dados numéricos possuem alguma correlação.

![image](https://github.com/user-attachments/assets/b2ad773e-89ba-4d6b-b48b-13a57013c02e)

De acordo com a correlação de Pearson, os dados possuem uma correlação insignificante. Vamos demonstrar isso com gráficos de dispersão fazendo os seguintes questionamentos:

1. Projetos mais longos resultam em maiores ganhos?
2. Existe alguma relação entre a duração do projeto e a taxa do sucesso do trabalho / satisfação do cliente?

![image](https://github.com/user-attachments/assets/b3bd3084-d390-4035-befe-bca257b71623)

Os dados desse dataset não possuem correlações significativas.

# Conclusões

- As plataformas oferecem diferentes oportunidades de acordo com os níveis de experiência.
- Os ganhos médios e taxa de sucesso não estão diretamente relacionados com o nível de experiência
- Os freelancers do nível "Beginner" possuem um volume de trabalhos completos maior, o que gera um maior ganho.
- Os dados do dataset são limpos, não possuem outliers e não possuem correlação entre si, o que indica que são dados artificialmente gerados.









