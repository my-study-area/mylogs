# mylogs
![GitHub top language](https://img.shields.io/github/languages/top/my-study-area/mylogs)
![Terraform Version](https://img.shields.io/badge/Terraform-v1.6.4-blue.svg)
[![Repository size](https://img.shields.io/github/repo-size/my-study-area/mylogs)](https://img.shields.io/github/repo-size/my-study-area/mylogs)
[![Last commit](https://img.shields.io/github/last-commit/my-study-area/mylogs)](https://github.com/my-study-area/mylogs/commits/master)

Anotações e registros de atividades

## Anotações
- Gist mylogs: [Gist mylogs](https://gist.github.com/adrianoavelino/313b0be8377e521241819b68a2f7cac4)
- Exemplos de prompts para agente de IA: [Gist prompts](https://gist.github.com/adrianoavelino/3ef49b866ae7c247ce1871ebf137cef1)    
- Link promocional para criar conta no Stackspot AI. [Cadastre-se](https://ai.stackspot.com/?campaignCode=01JXZTQ1S79349E8ZPS03VCW4P)

## Leituras
- OK 15/07/2025 - `#test #testes #unitario #java #spring`: Maratona de Testes Automatizados — Step 1: Testes Unitários: [dev.to](https://dev.to/diegobrandao/maratona-de-testes-automatizados-step-1-testes-unitarios-1kee)
- `#performance #gitlab #backup` Leitura indicada por Maurício Aniche: [Blog do gitlab](https://about.gitlab.com/blog/2025/06/05/how-we-decreased-gitlab-repo-backup-times-from-48-hours-to-41-minutes/)
- OK 05/07/2025 - `#java #exceptions` [Exceptions for Control Flow are Slow](https://www.linkedin.com/pulse/exceptions-control-flow-slow-alexandre-aquiles-3wxef/?trackingId=qrHRGQmYQjSbfO2gqVXQ%2Fg%3D%3D). Relacionado ao assunto: https://wiki.c2.com/?DontUseExceptionsForFlowControl
- playlist Rafael pontes: [Youtube](https://www.youtube.com/playlist?list=PLHMMERsvy9EyWQPru4SrJAYHEGKfkjRgP)

## Template de log
```
### 01/01/2026
`#`
- [text](link)
```
---  




## Logs


### 20/04/2026
`#tool #java #sonar #qube #sonarqube`
- PMD (Programming Mistake Detector): ferramenta de análise estática que verifica o código-fonte para encontrar automaticamente erros de programação, más práticas e vulnerabilidades. PMD é um analisador de código estático multilíngue extensível. Ele encontra falhas comuns de programação, como variáveis não utilizadas, blocos vazios, criação desnecessária de objetos, e assim por diante. [link](https://pmd.github.io/)


### 19/04/2026
`#investimento #financas`
- Regra dos 300 [link](https://youtu.be/TyRO4zc4Fco?si=3V15U6wvyIYkx3ZJ&t=349)
- Regra dos 72 [link](https://youtu.be/2AuPlpRjNsQ?si=ZbkEK_vVJ-MiVlW-&t=126)

**📈 Resumo: Regras da Independência Financeira**

#### 1. Regra dos 300 (O Número da Liberdade)
**Objetivo:** Estimar o patrimônio total necessário para viver de renda.

* **A Lógica:** Baseia-se na "Regra dos 4%", onde você retira 4% ao ano do seu patrimônio sem reduzir o capital principal (corrigido pela inflação).
* **Fórmula:** $$\text{Custo de Vida Mensal} \times 300 = \text{Patrimônio Necessário}$$

##### 💰 Exemplo Prático
Se você quer uma renda de **R$ 4.000,00** por mês:
* $4.000 \times 300 =$ **R$ 1.200.000,00**


#### 2. Regra dos 72 (O Poder dos Juros)
**Objetivo:** Calcular quanto tempo leva para o seu dinheiro **dobrar** de valor.

* **A Lógica:** Uma aproximação matemática rápida para o efeito dos juros compostos.
* **Fórmula:**
$$\frac{72}{\text{Taxa de Juros Anual}} = \text{Anos para Dobrar}$$

##### ⏳ Exemplo Prático
Se o seu investimento rende **12% ao ano**:
* $72 \div 12 =$ **6 anos** (Tempo necessário para transformar R$ 10 mil em R$ 20 mil).





### 28/02/2026
`#anki #plugin #add-on #addon`
- Lista de add-ons: https://ankiweb.net/shared/addons
    - Card Stats in Editor
    - Review Heatmap
    - True Retention
- Consultar os cards do anki que estão com maior dificuldade de aprendizado:
    - acesse o menu Browser (B)
    - na barra de pesquisa digite:
```
deck:AWS::Associate prop:lapses>1
```
Obs: lista os cards que foram avaliados como again (1) mais de uma vez






### 28/01/2026
`#system #design #saga`
- design de sistema blog: https://fidelissauro.dev/category/system-design/


### 24/01/2026
`#english #IA #tool`
- a site to speak with Miles, https://app.sesame.com/


### 14/12/2025
`#estrututuradados #codeinterview`
- Estreia ABSOLUTE_PATH: Aprenda a passar nas entrevistas técnicas: com explicação sobre listas, lista duplamente ligada, conjuntos (set) e dicionário (map): [link no Youtube](https://www.youtube.com/watch?v=R6xXubdcaxI&t=4588s) e exemplo de [código fonte](https://github.com/codigofontetv/entrevistas-tecnicas)
```


### 01/09/2025
`#graalvm #java #compilacaonativa #native`
- corrigindo erro `org.hibernate.bytecode.spi.BytecodeProvider Unable to get public no-arg constructor` ao adicionar spring-data-jpa com compilação nativa

Depois de muitas pesquisa descobri que temos que remover todas as referências para a classe BytecodeProvider e adicionar o seguinte arquivo: src/main/resources/META-INF/native-image/org.springframework/spring-orm/native-image.properties com o seguinte conteúdo:

Args = -H:ServiceLoaderFeatureExcludeServices=org.hibernate.bytecode.spi.BytecodeProvider

fonte: https://github.com/oracle/graal/issues/12207



### 27/09/2025
`#spring #cli #graalvm #aot`
- Spring cli: [doc](https://docs.spring.io/spring-boot/cli/using-the-cli.html)
```bash
spring init --dependencies=web -a artifact -g br.com.estudos -n nomeProjeto --build maven nomeRepositorio
```

- graalvm no asdf:
```bash
# lista as instalações de java com graalvm
asdf list-all java | grep graalvm

# instala graalvm
asdf install java graalvm-community-25.0.0

# para código com reflection execute na vm options:
java -agentlib:native-image-agent=config-output-dir=src/main/resources/META-INF/native-image -jar seu_projeto.jar

# logo após execute os cenário de sucesso e falha para gerar os arquivo em src/main/resources/

# compila em nativo
mvn -Pnative native:compile
```
Acesse o [passo a passo](https://github.com/buildrun-tech/buildrun-java-spring-boot-graalvm-exemplo).


### 11/09/2025
`#spring #datasource #transaction`
- Exemplo de multiplos datasources no mesmo application.properites usando Spring Batch. Controle Transacional no Spring Batch [youtube](https://www.youtube.com/watch?v=iZXYG7fM8jI)
    - arquivo [application.properties](https://github.com/giuliana-bezerra/sb-transactions/blob/main/src/main/resources/application.properties)
    - arquivo de [configuração](https://github.com/giuliana-bezerra/sb-transactions/blob/main/src/main/java/com/example/transactionsmultiplesdbs/DatasourceConfig.java)


### 10/09/2025
`#spring #springbatch #batch #virtualvm #profiling`
- Otimização de desempenho para jobs Spring Batch - Giuliana Silva Bezerra: [udemy](https://www.udemy.com/course/otimizacao-de-desempenho-para-jobs-spring-batch/?couponCode=MT250908G3)



### 08/09/2025
`#java #postgres`
- Vídeo Messaging With PostgreSQL - Rafael Ponte no JavaZone: [vimeo](https://vimeo.com/1115459661)

`#logs #log`    
O que logar numa aplicação? retirado do discord do deveficiente

- Comunicação com sistemas externos
- Alteração de estado no sistema
- Alguma regra de validação que quando não satisfeita interrompe um fluxo
- Exceptions que não são progadas.


### 07/09/2025
`#java #jmeter #thread #virtualthread`
- 🧵 Loom + JMeter — Testes de performance mais leves e escaláveis. Artigo que mostra como o Project Loom (Java 21) melhora a execução de testes no JMeter usando virtual threads. Comparações práticas mostram redução no uso de memória, CPU e número de threads, permitindo simular milhões de usuários com menos recursos. Ideal para entender como otimizar testes de carga em aplicações modernas.[medium](https://medium.com/globant/loom-project-the-revolution-of-jmeter-d321486517a8)

`#node #rinhabackend`
- Post Como Venci a Rinha de Backend 2025 com TypeScript, Node.js e Redis [blog](https://ricassiocosta.me/2025/08/como-venci-a-rinha-de-backend-2025/)
- Vídeo explicando a solução do vencedor, melhor projeto com python, 🐍 O MELHOR PROJETO PYTHON NA RINHA DE BACKEND!!! [Youtube](https://www.youtube.com/watch?v=wBqCR8W-P0g&ab_channel=ProgramadorLhama)

### 31/08/2025
`#java #spring #course #curso`
- Curso Spring Academy gratuito desde 2024: [fonte](https://spring.io/blog/2024/04/10/spring-academy-pro-content-now-free-to-access). Compartilhado no [chat](https://discord.com/channels/700620972604129302/700620973405372478/1411492859013759157) do deveficiente
- VisualVM é uma ferramenta que monitora e analisa aplicações Java em execução: [download](https://visualvm.github.io/download.html)


### 24/08/2025
`#certificação #aws`
- Certificado/badge da AWS para conclusão estilo game para aprender cloud, IA genreativa e outros: [AWS Cloud Quest: Generative AI Practitioner](https://aws.amazon.com/pt/training/digital/aws-cloud-quest/)

### 27/07/2025
`#livro #engenharia #pos #deveficiente`
- indicado no discord do deveficiente sobre curso tecnologia e pós: https://engsoftmoderna.info/

### 27/07/2025
`#rinha #docker`
- Rinha de Backend: como automatizar a publicação de imagens Docker com GitHub Actions: https://www.youtube.com/watch?v=u6dWrkJLYvY&ab_channel=EmilioHeinzmann


### 22/07/2025
`#java #spring`
- Informações sobre Spring compartilhadas no server do discord do deveficiente: [https://www.marcobehler.com/](https://www.marcobehler.com/)


### 06/07/2025
`#java #kubernet`
- [Hands On | Levando uma aplicação Java até o Kubernetes](https://deviniciative.wordpress.com/2020/06/02/hands-on-levando-uma-aplicacao-java-ate-o-kubernetes/)


### 05/07/2025
`#benchmark #java`
- JMH (the Java Microbenchmark Harness): https://www.baeldung.com/java-microbenchmark-harness


### 29/06/2025
`#localstack #aws`
- Aplicação frontend para Localstack: https://github.com/dantasrafael/localstack-web


### 28/06/2025
`#java #design #pattern #leitura`
- [5 Design Patterns Essenciais no Spring Boot — E Como Usá-los com Eficiência](https://deviniciative.wordpress.com/2025/06/20/5-design-patterns-essenciais-no-spring-boot-e-como-usa-los-com-eficiencia/)

---
`#game #jogo #mame #arcade`

Configurar o controle:
- sudo apt install joystick -y
- sudo apt install jstest-gtk -y
- abra o programa jstest-gtk, selecione o controle para testar se o controle está funcionando corretamente.

Vídeo com instruções: https://www.youtube.com/watch?v=3Zej4kdCnpo&ab_channel=DogukanMeral


Instalar mame (arcade):
- instalar pelos gerenciador de programas do Linux
- copiar a pasta .mame do backup

Configurar cheat:
- baixar o [arquivo de cheat](https://mega.nz/file/SxsQUJoT#jBdz6GLm_3J7xC5IbTArVxIwcOmcf11qKQzFGSMms2c) ou [aqui](./arquivos/mame/cheat.7z)
- extrair o cheat.7z
- coloque o arquivo na pasta do cheat definida no seu arquivo `~/.mame/mame.ini`, na linha: 
```
cheatpath                 $HOME/mame/cheat;/usr/local/share/games/mame/cheat;/usr/share/games/mame/cheat;/usr/games
```

Ativar o cheat:
- ao iniciar o mame, acesse a opção Configure Options > Miscellaneous Options > Enable Cheats e ative a opção.
- ao iniciar o jogo, pressione a tecla `Tab` para abrir o menu de opções do mame, vá até a opção Cheat. Na tela que abrir, basta selecionar as opções desejadas como infinity time e infinity Energy.

---
`#panel-attack #game #jogo`
Instalação de panel attack com love: https://panelattack.com/
> Obs: não esquecer de executar `chmod +x panel-attack.AppImage` para dar permissão de execução.


### 08/06/2025
`#pdb #python #debug`

Vídeo: https://www.youtube.com/watch?v=a7qIcIaL4zs&ab_channel=NeuralNine

Lista de comandos para debugar com **pdb** no python na linha de comando.

Exempos de código:
```python
#teste.python


def soma(a, b):
    return a+b

if __name__ == '__main__':
    breakpoint()
    print('main')
    num_1 = 1
    num_2 = 4
    result = soma(num_1, num_2)
    print(result)
    print('fim do main')
```

Depois execute no terminal:
```commandline
python teste.py
```

Opção 2:

```bash
python -m pdb teste.py
```

Lista de comandos:

* `h` - **Help**: Lista todos os comandos disponíveis.
* `n` - **Next line (step over)**: Executa a próxima linha do código, sem entrar em chamadas de função (passa por cima da função).
* `s` - **Step into function**: Entra na próxima chamada de função, permitindo depurar o código dentro da função.
* `c` - **Continue execution**: Continua a execução do programa até o próximo breakpoint, ou até o fim do script.
* `q` - **Quit debugger**: Sai do depurador e encerra a execução do programa.
* `l` - **List source code**: Lista o código fonte ao redor da linha de execução atual.
* `p <expression>` - **Print expression value**: Imprime o valor de uma expressão ou variável.
* `pp <object>` - **Pretty-print object**: Imprime o valor de um objeto de forma formatada (útil para estruturas de dados complexas).
* `b <lineno>` - **Set breakpoint**: Define um breakpoint em uma linha específica do código.
* `w` - **Show call stack**: Mostra a pilha de chamadas (o caminho que o código percorreu para chegar ao ponto atual).


### 06/06/2025
`#icon #emoji #github`
- Repositório com conjunto de códigos emoji para usar no Github markdown :octocat: : https://github.com/ikatyang/emoji-cheat-sheet
- documentação sobre markdown github: https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#footnotes

```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.
```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].

[^1]: My reference.
[^2]: To add line breaks within a footnote, prefix new lines with 2 spaces.
  This is a second line.
  
  



`#aws #cloud`
- :cloud: Aws Educate e Emerging Talent Community para ganhar pontos e ganhar voucher para provas AWS : https://www.awseducate.com/student/s/etc-home





### 05/06/2025
`#pycharm #flatpak`
- Ao executar testes na ide pycharm a variável de ambiente JAVA_HOME ao executar testes não encontra a vaŕiável. Solução cofigurar a variável em ~/.bashrc e  ~/.config/fish/config.fish e depois inciar o pychar na linha de comando.
- Na instalação com flatpak use os comandos:

```bash
flatpak list
flatpak run id-de-aplicativo
#exemplo
flatpak run com.jetbrains.PyCharm-Community &
```

### 04/06/2025
`#pyspark #spark #python #glue #docker`
- Developing and testing AWS Glue job scripts locally: https://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-etl-libraries.html#develop-local-docker-image
- Tutorial acima com o script python: https://aws.amazon.com/pt/blogs/big-data/develop-and-test-aws-glue-version-3-0-jobs-locally-using-a-docker-container/
- imagem docker com libs para aws glue: https://hub.docker.com/r/amazon/aws-glue-libs



### 03/06/2025
`#pyspark #spark #python #pycharm #localstack`
- configuração de spark no pycharm: https://spark.apache.org/docs/latest/api/python/development/setting_ide.html
- configuração com docker glue e pyspark: https://codelovingyogi.medium.com/localstack-for-local-glue-dev-87ab567cff0a

Uso com glue

<details>
<summary>Configuração do glue localmente com pyspark:</summary>
Executar um job PySpark AWS Glue localmente, sem a AWS, significa simular o ambiente do AWS Glue para desenvolver e testar seu código antes de implantá-lo na nuvem. O AWS Glue fornece um conjunto de bibliotecas e funcionalidades que estendem o PySpark padrão, como:

* **`GlueContext`**: Uma wrapper do `SparkContext` que adiciona funcionalidades específicas do Glue (como a leitura e escrita de dados de catálogos do Glue, etc.).
* **DynamicFrames**: Uma abstração de alto nível sobre os DataFrames do Spark, projetada para trabalhar com esquemas em evolução e inferência de esquema, tornando o tratamento de dados semi-estruturados mais fácil.
* **Conectores**: Para várias fontes de dados (S3, JDBC, etc.), que o Glue otimiza.

Para executar isso localmente, você precisará de algumas ferramentas e um ambiente simulado.

### Ferramentas Necessárias:

1.  **Java Development Kit (JDK) 8 ou superior**: Spark e Glue são baseados em Java.
2.  **Python 3.7+**: A linguagem para seus scripts.
3.  **Apache Spark**: Você precisará de uma instalação local do Spark (como no tutorial anterior).
4.  **Bibliotecas AWS Glue para Desenvolvedor (AWS Glue Development Kit - GDK)**: Este é o componente chave que fornece as classes e funcionalidades do Glue (como `GlueContext`, `DynamicFrame`) para seu ambiente local.
5.  **`pyspark`**: A biblioteca Python para interagir com o Spark.
6.  **`awscli`**: Para baixar o GDK.

### Tutorial Passo a Passo: Executando PySpark Glue Job Localmente

#### Passo 1: Pré-requisitos e Instalações Iniciais

1.  **Instale o JDK, Python e Spark**: Se você seguiu o tutorial anterior, você já tem isso. Se não, certifique-se de que `java -version`, `python --version` e `spark-shell` (ou `pyspark`) funcionem no seu terminal.
    * **Lembre-se de configurar `$JAVA_HOME` e `$SPARK_HOME`!**

2.  **Instale `pyspark`**:
    ```bash
    pip install pyspark
    ```

3.  **Instale `awscli`**:
    ```bash
    pip install awscli
    ```
    (Você não precisa configurar credenciais AWS para este tutorial, apenas para poder usar o comando `aws s3 cp` ou `aws s3 sync` para baixar o GDK).

#### Passo 2: Baixar o AWS Glue Development Kit (GDK)

O GDK contém as bibliotecas Java e Python necessárias para executar os jobs do Glue localmente.

1.  **Crie um diretório para o GDK**:
    ```bash
    mkdir -p ~/glue_local/jars
    cd ~/glue_local
    ```

2.  **Baixe o GDK**: A AWS não fornece um link de download direto e estático para o GDK. A forma mais comum é usar o `aws s3 cp` ou `aws s3 sync` de um bucket S3 público da AWS.
    * Verifique a [documentação oficial do AWS Glue](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-programming-etl-libraries.html) para o bucket S3 correto e a versão mais recente dos artefatos. Geralmente, é algo como `s3://aws-glue-artifacts/glue-aws-etl-artifacts-VERSION/`
    * **Exemplo (substitua a versão e região):**
        ```bash
        # Verifique a versão mais recente na documentação da AWS.
        # Por exemplo, para Glue 4.0:
        aws s3 cp s3://aws-glue-artifacts/glue-common/apache-maven-3.6.0-bin.tar.gz . --region us-east-1
        aws s3 cp s3://aws-glue-artifacts/glue-common/gradle-5.6.2-bin.zip . --region us-east-1
        aws s3 cp s3://aws-glue-artifacts/glue-aws-etl-artifacts-4.0/glue-etl-utils-4.0.jar ./jars/ --region us-east-1
        aws s3 cp s3://aws-glue-artifacts/glue-aws-etl-artifacts-4.0/spark-common-4.0.jar ./jars/ --region us-east-1
        aws s3 cp s3://aws-glue-artifacts/glue-aws-etl-artifacts-4.0/AWSGlueETLCommon-4.0.jar ./jars/ --region us-east-1
        # Pode haver mais JARs dependendo da versão do Glue. O mais importante é o AWSGlueETLCommon.jar e os que ele depende.
        ```
        **Dica:** Uma abordagem mais fácil para obter todos os JARs necessários para o GDK é baixar o Docker image da AWS Glue e extrair os JARs de lá, ou usar o script `local-testing/run-job.sh` do repositório de exemplos do Glue, que costuma fazer isso para você.
        Por enquanto, vamos focar nos JARs essenciais:

        ```bash
        # Tente baixar pelo menos estes (substitua '4.0' pela versão do Glue que você quer testar)
        # Se você tiver problema, procure por "AWS Glue Local Testing JARs"
        # e o S3 bucket para a sua região/versão
        aws s3 cp s3://aws-glue-artifacts/glue-aws-etl-artifacts-4.0/AWSGlueETLCommon-4.0.jar ~/glue_local/jars/ --region us-east-1
        aws s3 cp s3://aws-glue-artifacts/glue-aws-etl-artifacts-4.0/spark-common-4.0.jar ~/glue_local/jars/ --region us-east-1
        aws s3 cp s3://aws-glue-artifacts/glue-aws-etl-artifacts-4.0/glue-etl-utils-4.0.jar ~/glue_local/jars/ --region us-east-1
        ```
        Se você tiver dificuldades em baixar esses arquivos, um atalho é encontrar um projeto de exemplo do Glue que já inclua um script para baixar ou empacotar esses JARs.

#### Passo 3: Escrever o Script PySpark AWS Glue

Crie um arquivo Python (ex: `my_glue_job.py`). Este script usará as APIs do Glue.

```python
# my_glue_job.py
import sys
from awsglue.transforms import *
from awsglue.utils import getResolvedOptions
from pyspark.context import SparkContext
from awsglue.context import GlueContext
from awsglue.job import Job
from pyspark.sql.functions import col

# Argumentos (simulando os que o Glue passaria em um job real)
# Aqui estamos apenas definindo-os diretamente para teste local
args = {
    'JOB_NAME': 'my_local_glue_job',
    'SOURCE_PATH': 'file:///tmp/input_data/', # Usaremos um arquivo local
    'OUTPUT_PATH': 'file:///tmp/output_data/' # Saída local
}

# Criar um SparkContext
sc = SparkContext()

# Criar um GlueContext (o ponto de entrada do Glue)
glueContext = GlueContext(sc)

# Criar uma SparkSession (conveniente para usar DataFrames)
spark = glueContext.spark_session

# Criar um objeto Job (opcional para teste local, mas bom para simular o ambiente Glue)
job = Job(glueContext)
# job.init(args['JOB_NAME'], args) # Não precisa para teste local simples

print("Iniciando o job PySpark AWS Glue localmente...")

# --- 1. Preparar Dados de Entrada (simulação) ---
# Vamos criar um arquivo CSV simples para simular a entrada
# Conteúdo para /tmp/input_data/people.csv
# id,name,age
# 1,Alice,30
# 2,Bob,25
# 3,Charlie,35
# Crie este arquivo manualmente ou via script antes de executar.

# Exemplo de leitura de dados usando DynamicFrame
# No Glue real, você usaria o Data Catalog
# Aqui, vamos ler como um DataFrame normal e converter para DynamicFrame
# ou simplesmente usar a API do Spark para simplicidade no teste local.

# Para simplificar o teste local sem depender do GlueContext para leitura complexa
# Vamos ler diretamente com Spark e converter para DynamicFrame
try:
    df_source = spark.read \
        .option("header", "true") \
        .csv(args['SOURCE_PATH'])
    print("\nDados de entrada (DataFrame):")
    df_source.show()

    # Converter DataFrame para DynamicFrame (se você precisar de operações de DynamicFrame)
    dynamic_frame = DynamicFrame.fromDF(df_source, glueContext, "source_data")
    print("\nDados de entrada (DynamicFrame):")
    dynamic_frame.printSchema()

    # --- 2. Processamento de Dados (Exemplo: Filtrar e Adicionar Coluna) ---
    # Convertendo de volta para DataFrame para usar a sintaxe PySpark DataFrame mais familiar
    df_processed = dynamic_frame.toDF() \
        .filter(col("age") > 30) \
        .withColumn("status", col("name") + " is over 30")

    print("\nDados Processados (DataFrame):")
    df_processed.show()

    # Converter de volta para DynamicFrame para escrita com o Glue (opcional para local)
    processed_dynamic_frame = DynamicFrame.fromDF(df_processed, glueContext, "processed_data")

    # --- 3. Escrita dos Dados de Saída ---
    # No Glue real, você usaria o Data Catalog e write_dynamic_frame.
    # Para teste local, vamos escrever para um arquivo CSV simples.
    processed_dynamic_frame.toDF().write \
        .mode("overwrite") \
        .option("header", "true") \
        .csv(args['OUTPUT_PATH'])

    print(f"\nDados de saída escritos em: {args['OUTPUT_PATH']}")

except Exception as e:
    print(f"Erro durante a execução do job: {e}")

finally:
    # Finalizar o job (importante para o ambiente Glue)
    # job.commit() # Comentar para teste local simples, pois job.init() não foi chamado
    print("Job PySpark AWS Glue localmente concluído.")
    # Parar o SparkContext
    sc.stop()

```

#### Passo 4: Preparar o Ambiente para o Script

1.  **Crie o diretório de entrada e o arquivo `people.csv`**:
    ```bash
    mkdir -p /tmp/input_data
    ```
    **Crie o arquivo `/tmp/input_data/people.csv` com este conteúdo:**
    ```csv
    id,name,age
    1,Alice,30
    2,Bob,25
    3,Charlie,35
    4,David,40
    ```
    **No Windows:** Use `C:\tmp\input_data\people.csv` e `C:\tmp\output_data`.

#### Passo 5: Executar o Job PySpark AWS Glue Localmente

Você precisará usar `spark-submit` e passar os JARs do GDK para o classpath do Spark.

1.  **Navegue até o diretório onde você salvou `my_glue_job.py`**.

2.  **Execute o comando `spark-submit`**:

    ```bash
    # Substitua /caminho/para/seus/jars/glue_local/jars
    # pelo caminho real onde você baixou os JARs do GDK.
    # Certifique-se de que o separador de classpath é ':' no Linux/macOS e ';' no Windows.

    # Para Linux/macOS:
    spark-submit \
        --master local[*] \
        --jars ~/glue_local/jars/AWSGlueETLCommon-4.0.jar,~/glue_local/jars/spark-common-4.0.jar,~/glue_local/jars/glue-etl-utils-4.0.jar \
        --conf spark.sql.catalogImplementation=hive \
        --py-files ~/glue_local/jars/AWSGlueETLCommon-4.0.jar,~/glue_local/jars/spark-common-4.0.jar,~/glue_local/jars/glue-etl-utils-4.0.jar \
        my_glue_job.py
    ```

    ```bash
    # Para Windows (observe o ';' no --jars e --py-files e aspas no caminho):
    # Verifique se o caminho para os JARs está correto para o seu sistema.
    # Ex: C:\Users\SeuUsuario\glue_local\jars
    spark-submit ^
        --master local[*] ^
        --jars "C:\Users\SeuUsuario\glue_local\jars\AWSGlueETLCommon-4.0.jar;C:\Users\SeuUsuario\glue_local\jars\spark-common-4.0.jar;C:\Users\SeuUsuario\glue_local\jars\glue-etl-utils-4.0.jar" ^
        --conf spark.sql.catalogImplementation=hive ^
        --py-files "C:\Users\SeuUsuario\glue_local\jars\AWSGlueETLCommon-4.0.jar;C:\Users\SeuUsuario\glue_local\jars\spark-common-4.0.jar;C:\Users\SeuUsuario\glue_local\jars\glue-etl-utils-4.0.jar" ^
        my_glue_job.py
    ```

    **Explicação dos parâmetros:**
    * `--master local[*]`: Roda o Spark localmente usando todos os núcleos disponíveis.
    * `--jars`: Especifica os arquivos JAR do Glue que o Spark precisa carregar no classpath do driver e dos executores. **Essencial para as classes Java do Glue.**
    * `--conf spark.sql.catalogImplementation=hive`: Embora não estejamos usando um metastore Hive real, essa configuração é frequentemente necessária para o Glue funcionar corretamente, pois ele espera uma implementação de catálogo.
    * `--py-files`: Especifica arquivos Python (ou JARs que contenham módulos Python) que devem ser distribuídos para os workers. No caso do Glue, alguns dos JARs podem conter módulos Python que são usados por `awsglue.context` e `awsglue.transforms`.

#### Verificação da Saída:

Após a execução, você deve ver os `print()` e `df.show()` do seu script no terminal. Além disso, verifique o diretório de saída `/tmp/output_data` (ou `C:\tmp\output_data` no Windows). Lá, você deve encontrar arquivos CSV (ou parquet, dependendo do formato de saída) com os dados processados.

### Observações Importantes:

* **Simulação vs. Realidade:** Este é um ambiente de desenvolvimento local. Ele não simula totalmente o Data Catalog da AWS Glue, o AWS Lake Formation, ou a capacidade de escala real de um cluster Glue na AWS. Para isso, você precisaria de serviços como o `localstack` ou executar o job na AWS.
* **DynamicFrames:** No seu script, a conversão de `DataFrame` para `DynamicFrame` e vice-versa é principalmente para ilustrar como você interagiria com eles. Para operações complexas, você usaria os métodos do `DynamicFrame` diretamente.
* **Path dos JARs:** O caminho para os JARs do Glue (`~/glue_local/jars/`) deve ser absoluto ou relativo a onde você está executando o `spark-submit`.
* **Versões:** Certifique-se de que a versão do Spark que você baixou é compatível com a versão do Glue (os JARs do GDK). A documentação da AWS Glue geralmente especifica as compatibilidades. Por exemplo, Glue 4.0 é baseado em Spark 3.3.
* **Depuração:** Se você tiver erros como `ClassNotFoundException` ou `ModuleNotFoundError`, geralmente significa que um JAR ou um módulo Python do Glue não foi carregado corretamente. Verifique os caminhos e os arquivos especificados em `--jars` e `--py-files`.

Este tutorial fornece uma base sólida para começar a desenvolver e testar seus scripts PySpark AWS Glue localmente, acelerando seu ciclo de desenvolvimento.
    
    
</details>


### 01/06/2025
`#certificação #github`
- certificação Github: https://examregistration.github.com/

### 31/05/2025
`#ia #ai #course`
- A free course designed for people with some coding experience, who want to learn how to apply deep learning and machine learning to practical problems: [https://course.fast.ai/](https://course.fast.ai/)

`#notebooklm #open #ia #ai`
- A powerful open-source, AI-powered note-taking/research platform that respects your privacy. Like a notebooklim from Google: (https://www.open-notebook.ai/get-started.html)[https://www.open-notebook.ai/get-started.html]


---
`#draw.io #fluxograma #github #mermaid`
- Exemplo de fluxograma utilizado no markdown de um projeto do Github, os exemplos abaixo não funcionam no gist. [fonte](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams)

Use o código abaixo para verificar a versão suportada:

    ```mermaid
      info
    ```

Exemplo de fluxograma:

    ```mermaid
    graph TD;
        A-->B;
        A-->C;
        B-->D;
        C-->D;
    ```


---
`#intellij #livetemplate #unittest #test`
- Exemplo de livetemplate do intellij:

ctrl + alt + P
```
@org.junit.jupiter.api.Test
@org.junit.jupiter.api.DisplayName("$TEST_NAME$")
void $METHOD_NAME$() {
    $END$
}
```
![image](https://gist.github.com/user-attachments/assets/fae2cd3b-9f58-4b91-8728-4e14aab21844)

![image](https://gist.github.com/user-attachments/assets/069a8dac-ba6e-47c2-a7cd-c6388a9132bd)

---
`#threads #concorrencia`
- palestra indicada por Rafael Pontes: [[PT-BR/EN-US] Java Concurrency from the Trenches - Lessons Learned in the Wild](https://www.youtube.com/watch?v=pV7FDnwxv2I&ab_channel=CarlosNogueira%28DevOps%29)



### 25/05/2025
`#spring #java #h2 #properties`
- exemplo de configuração do `application.properties` usando H2 com configurações para o mysql.
```
spring.datasource.url=jdbc:h2:mem:db;DB_CLOSE_ON_EXIT=FALSE;MODE=MYSQL
```



### 20/04/2025
`#test`
- [testdesiderata: Kent Beck](https://testdesiderata.com/)

### 19/04/2025
`#ia #ai #llm`
- assistente de pesquisa e aprendizado pessoal super inteligente: https://notebooklm.google.com/



### 06/04/2025
`#aws #practitioner #cloud`
Exemplo de contexto para responder perguntas para estudo de prova AWS:
```
Yes, I totally understand! 🧠✨

You want:

✅ A clear, teacher-style explanation like I did for VPC Peering — friendly, easy to understand, like you’re learning from a coach

✅ Then follow it up with your structured format:

Correct Option

Overall Explanation

Exam Alert

Incorrect Options

Reference

Basically, I mix learning + exam prep, so it’s both easy to remember and useful for passing the test. I’ll start with a plain-language explanation to teach the concept, then break it down into your exam format.

Let’s go again! You can resend a question or give me a new one, and I’ll respond with the new combined style. Ready when you are! 💪📚
```


### 20/03/2025
`#pattern #designpattern`
- [padrões de projeto](https://www.youtube.com/playlist?list=PLNHxHgB-_LTt67szNmMsZwqBKq9jH4uKJ)
- 

### 08/03/2025
`#aws #`
- 𝙌𝙪𝙚𝙧 𝙩𝙞𝙧𝙖𝙧 𝙪𝙢𝙖 𝙘𝙚𝙧𝙩𝙞𝙛𝙞𝙘𝙖𝙘̧𝙖̃𝙤 𝘼𝙒𝙎 𝙙𝙚 𝙜𝙧𝙖𝙘̧𝙖? 🚀 
  - https://www.linkedin.com/posts/joaoluizbr_aws-cloud-certificaaexaetoaws-activity-7301982723575877632-Z8BB?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAfm0E8BHZBHyafH5dJvcNZWg08QZfPcTMc
  - https://www.linkedin.com/posts/fernando-garcia-santos_aws-educate-cloud-skills-for-education-activity-7303083149326979072-GoEm?utm_source=share&utm_medium=member_desktop&rcm=ACoAAAfm0E8BHZBHyafH5dJvcNZWg08QZfPcTMc
  - https://www.youtube.com/watch?v=1gIrErgpD_8

### 07/12/2024
`#curtas #filmes #curtametragem #dust`
- [indicações estilo DUST](https://www.youtube.com/watch?v=_ekauaTtwv0)


### 01/12/2024
`#validator #validator #python`
- validadores em python: blog post: https://medium.com/@moraneus/data-validation-in-python-using-pydantic-in-python-95bb36000993
  - [marshmallow](https://marshmallow.readthedocs.io/en/stable/#)
  - [pydantic](https://docs.pydantic.dev/latest/)
  - [cerberus](https://docs.python-cerberus.org/index.html)


### 30/11/2024
`#stepfunction #lambda #aws #localstack`
- [Testar stepfunction aws](https://dev.to/oieduardorabelo/um-guia-pratico-para-testar-o-aws-step-functions-25nj)


### 20/11/2024
`#python #cloud #host`
- [pythonanywhere](https://www.pythonanywhere.com/): hospede, execute e code python na nuvem.

`#aws cre`
- [minha badge do AWS Cloud Quest: Cloud Practitioner](https://www.credly.com/badges/4699b11a-0570-4bcf-b0d8-165485edbae1)


### 19/11/2024
`#microsoft #suporte #mail #outlook`
- [suporte microsoft](https://support.microsoft.com/en-US/home/contact): link para logar quando estiver com erro Too many request no outlook
- 



### 15/11/2024
`#aws #sqs #sns`
- [Filter Messages Published to Topics with Amazon SNS and Amazon SQS TUTORIAL](https://aws.amazon.com/pt/tutorials/filter-messages-published-to-topics/)


### 26/10/2024
`#mermaid #flow #flowchart #fluxograma #tool`
- [Editor Mermaid Online](https://mermaid.live/)

`#drawio #flowchart #tool`
- [tldraw](https://www.tldraw.com/): desenhar fluxogramas online

`#tool #diagram #diagrama #relationship #relacionamento`
- [dbdiagram](https://dbdiagram.io/d): ferramenta para gerar uma visualização de relacionamento entre tabelas de banco de dados.

### 21/10/2024
`#kafka #schema-registry`
- [text](link)
- 
```bash
echo "{\"timestamp\":1637000000000},{\"language\": \"ITALIAN\", \"greeting\": \"Ciao, mondo!\"}" | docker compose exec -T schema-registry \
kafka-avro-console-producer \
--broker-list broker:29092 \
--topic example-stream-avro \
--property key.converter=io.confluent.connect.avro.AvroConverter \
--property value.converter=io.confluent.connect.avro.AvroConverter \
--property value.converter.schema.registry.url=http://schema-registry:8081 \
--property key.converter.schema.registry.url=http://schema-registry:8081 \
--property value.schema='{"type":"record","name":"Hello","doc":"An example Avro-encoded `Hello` message.","namespace":"com.nordstrom.kafka.example","fields":[{"name":"language","type":{"type":"enum","name":"language","symbols":["ENGLISH","FRENCH","ITALIAN","SPANISH"]}},{"name":"greeting","type":"string"}]}' \
--property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
--property parse.key=true \
--property key.separator=,


echo "{\"timestamp\":1637000000000},{\"language\": \"ENGLISH\", \"greeting\": \"Hello, World!\"}" | docker compose exec -T schema-registry \
kafka-avro-console-producer \
--broker-list broker:29092 \
--topic example-stream-avro \
--property key.converter=io.confluent.connect.avro.AvroConverter \
--property value.converter=io.confluent.connect.avro.AvroConverter \
--property value.converter.schema.registry.url=http://schema-registry:8081 \
--property key.converter.schema.registry.url=http://schema-registry:8081 \
--property value.schema='{"type":"record","name":"Hello","doc":"An example Avro-encoded `Hello` message.","namespace":"com.nordstrom.kafka.example","fields":[{"name":"language","type":{"type":"enum","name":"language","symbols":["ENGLISH","FRENCH","ITALIAN","SPANISH"]}},{"name":"greeting","type":"string"}]}' \
--property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
--property parse.key=true \
--property key.separator=,
```

### 18/10/2024
`#transcribe #jpg2text #image2text`
- [converte imagem para texto](https://www.imagetotext.info/)



### 16/10/2024
`#testes #test #linkedin`
- [Linkedin Jordi: O que precisei aprender para ficar Expert em Testes?!](https://www.linkedin.com/pulse/o-que-precisei-aprender-para-ficar-expert-em-testes-silva-dgvnf/?trackingId=FGMIqJq2W%2FqUJ9osh%2FC%2FwA%3D%3D)
- 

### 13/10/2024
`#diagram #flow #draw.io`
- [ferramenta para criar fluxos](https://whimsical.com/) com IU bem amigável e semelhante ao draw.io, mas moderna
- 

### 12/10/2024
`#aws #course #curso #badge`
-  badges recebidas após cursos no https://explore.skillbuilder.aws/learn. Ao concluir visualizar em [https://www.credly.com/earner/dashboard](https://www.credly.com/earner/dashboard)
- https://brasilopenbadge.com.br/ganhador/dashboard
- 


### 11/10/2024
`#markdown #md #github #alert`
- [Criar alertas no markdown do Github](https://docs.github.com/pt/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#alerts)


Código:
```markdown
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```

Resultado:
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.




### 28/09/2024
`#refactory #design-pattern #pattern #java`
- https://medium.com/javarevisited/stop-using-if-else-statements-in-java-57234e13bf9d


`#faker #test #mockmoon`

- https://mockoon.com/tutorials/getting-started/
- https://hub.docker.com/r/mockoon/cli
- Exemplo de arquivo de mock com faker: https://github.com/mockoon/mock-samples/blob/main/samples/generate-mock-data.json
- https://mockoon.com/tutorials/responses-and-rules/
- https://mockoon.com/docs/latest/route-responses/dynamic-rules/
- https://mockoon.com/tutorials/generate-mock-json-data/

Docker-compose:
```yml
services:
  cli:
    volumes:
      # - ${PWD}/sample-data.json:/data/sample-data.json
      - type: bind
        source: ${PWD}/sample-data.json
        target: /data
        # readonly: ro
    ports:
      - '3000:3000'
    image: 'mockoon/cli:latest'
    command: '--data data --port 3000'
```

<details>
<summary>Exemplo de script de configuração:</summary>
 Exemplo:
 
```json
 {
    "uuid": "c7c1e0f8-51fd-4869-b2b7-f872e8812f52",
    "lastMigration": 32,
    "name": "Demo API",
    "endpointPrefix": "",
    "latency": 0,
    "port": 3000,
    "hostname": "",
    "folders": [],
    "routes": [
        {
            "uuid": "02a47816-c840-48c9-a060-c2b99ef706bf",
            "type": "crud",
            "documentation": "Endpoint performing CRUD operations on a data bucket (automatically creates GET, POST, PUT, DELETE routes)",
            "method": "",
            "endpoint": "users",
            "responses": [
                {
                    "uuid": "56b9dbbc-5fed-4f96-9a10-36b17aee9802",
                    "body": "{}",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "Perform CRUD operations on the \"Users\" databucket (\"Data\" tab at the top)",
                    "headers": [],
                    "bodyType": "DATABUCKET",
                    "filePath": "",
                    "databucketID": "kxsw",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": true,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": null
        },
        {
            "uuid": "9ddc06b3-c815-43f2-8efe-f62ce5ed0055",
            "type": "http",
            "documentation": "Generate random body (JSON, text, CSV, etc) with templating",
            "method": "get",
            "endpoint": "template",
            "responses": [
                {
                    "uuid": "d3abe5d3-6aa0-4280-8d01-1456b4cb8b33",
                    "body": "{\n  \"Templating example\": \"For more information about templating, click the blue 'i' above this editor\",\n  \"users\": [\n    {{# repeat (queryParam 'total' '10') }}\n      {\n        \"userId\": \"{{ faker 'number.int' min=10000 max=100000 }}\",\n        \"firstname\": \"{{ faker 'person.firstName' }}\",\n        \"lastname\": \"{{ faker 'person.lastName' }}\",\n        \"friends\": [\n          {{# repeat (faker 'number.int' 5) }}\n            {\n              \"id\": \"{{ faker 'string.uuid' }}\"\n            }\n          {{/ repeat }}\n        ]\n      },\n    {{/ repeat }}\n  ],\n  \"total\": \"{{queryParam 'total' '10'}}\"\n}",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "Creates 10 random users, or the amount specified in the 'total' query param",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": null
        },
        {
            "uuid": "d29d92d3-6506-44a9-960f-4ae0a62bc093",
            "type": "http",
            "documentation": "Use multiple responses with rules",
            "method": "post",
            "endpoint": "content/:param1",
            "responses": [
                {
                    "uuid": "928bef5b-7ed5-4a87-8c4d-4c7dfc6a32ce",
                    "body": "{\n  \"Rules example\": \"Default response. Served if route param 'param1' is not present.\"\n}",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "Default response",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": true,
                    "crudKey": "id",
                    "callbacks": []
                },
                {
                    "uuid": "1ef8d78d-61c4-4463-9fb0-f4c2530e2463",
                    "body": "{\n  \"Rules example\": \"Content XYZ. Served if route param 'param1' equals 'xyz'. (See in 'Rules' tab)\"\n}",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "Content XYZ",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [
                        {
                            "target": "params",
                            "modifier": "param1",
                            "value": "xyz",
                            "invert": false,
                            "operator": "equals"
                        }
                    ],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                },
                {
                    "uuid": "fe0190c5-f405-4500-a504-83dca0117969",
                    "body": "{\n  \"Rules example\": \"Content not found. Served if route param 'param1' is not equal to 'xyz'. (See in 'Rules' tab)\"\n}\n",
                    "latency": 0,
                    "statusCode": 404,
                    "label": "Content not found",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [
                        {
                            "target": "params",
                            "modifier": "param1",
                            "value": "^(?!.*xyz).*$",
                            "invert": false,
                            "operator": "regex"
                        }
                    ],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": null
        },
        {
            "uuid": "6f5b9c70-1a00-4060-a213-d456a9a15c73",
            "type": "http",
            "documentation": "Path supports various patterns",
            "method": "put",
            "endpoint": "path/with/pattern(s)?/*",
            "responses": [
                {
                    "uuid": "eab8ad28-a0e8-40c3-b98e-ebb87d3964f0",
                    "body": "The current path will match the following routes: \nhttp://localhost:3000/path/with/pattern/\nhttp://localhost:3000/path/with/patterns/\nhttp://localhost:3000/path/with/patterns/anything-else\n\nLearn more about Mockoon's routing: https://mockoon.com/docs/latest/api-endpoints/routing/",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "",
                    "headers": [
                        {
                            "key": "Content-Type",
                            "value": "text/plain"
                        }
                    ],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": null
        },
        {
            "uuid": "899962e2-cb20-4045-beff-11554930caa5",
            "type": "http",
            "documentation": "\"Guard\" route protecting all routes starting with /protected/",
            "method": "all",
            "endpoint": "protected/*",
            "responses": [
                {
                    "uuid": "c3480742-5b2c-4d8f-9fd9-769acb48ecdc",
                    "body": "{\n  \"error\": \"Unauthorized\"\n}",
                    "latency": 0,
                    "statusCode": 401,
                    "label": "Requires the presence of an 'Authorization' header",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [
                        {
                            "target": "header",
                            "modifier": "Authorization",
                            "operator": "null",
                            "invert": false,
                            "value": ""
                        }
                    ],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": "FALLBACK"
        },
        {
            "uuid": "3daa5873-a8e9-4812-ba1e-1399aaa8b745",
            "type": "http",
            "documentation": "Protected route",
            "method": "get",
            "endpoint": "protected/path",
            "responses": [
                {
                    "uuid": "7880d9cc-d2ad-4108-b4f9-9c94047f77d4",
                    "body": "You can serve the same responses based on the same rules for all or part of your endpoints by creating global routes using the fallback mode and a wildcard path. \nThis is useful if you want to protect all your endpoints by checking if an Authorization header is present or if you want to verify that all your requests contain a specific property in their body.\nTo learn more: https://mockoon.com/docs/latest/route-responses/global-routes-with-rules/",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "",
                    "headers": [
                        {
                            "key": "Content-Type",
                            "value": "text/plain"
                        }
                    ],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": null
        },
        {
            "method": "get",
            "endpoint": "forward-and-record",
            "documentation": "Can Mockoon forward or record entering requests?",
            "responses": [
                {
                    "uuid": "45fc6e5f-3375-4520-9cd4-da3e71ded687",
                    "body": "Mockoon can also act as a proxy and forward all entering requests that are not caught by declared routes. \nYou can activate this option in the environment settings (\"Settings\" tab at the top). \nTo learn more: https://mockoon.com/docs/latest/server-configuration/proxy-mode/\n\nAll entering requests, and responses from the proxied server will be recorded and can be automatically mocked (\"Logs\" tab at the top).\nTo learn more: https://mockoon.com/docs/latest/logging-and-recording/requests-logging/",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "",
                    "headers": [
                        {
                            "key": "Content-Type",
                            "value": "text/plain"
                        }
                    ],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "uuid": "d2db207f-3649-4b3c-8b93-2a35ebcbc810",
            "type": "http",
            "responseMode": null
        },
        {
            "uuid": "8ecd62ae-16d7-4f7a-8ded-3ef2d6420ccb",
            "type": "http",
            "documentation": "",
            "method": "get",
            "endpoint": "telefones/:id",
            "responses": [
                {
                    "uuid": "bfdb358f-1f0b-47d5-84cc-06bf91643bee",
                    "body": "{\n  \"id\": \"{{urlParam 'id'}}\",\n  \"nome\": \"Adriano\",\n  \"idade\": 40\n}",
                    "latency": 0,
                    "statusCode": 200,
                    "label": "",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": true,
                    "crudKey": "id",
                    "callbacks": []
                },
                {
                    "uuid": "c0633453-7631-48ee-933f-9d7a90e4679d",
                    "body": "{\n  \"message\": \"não encontrado\"\n}",
                    "latency": 0,
                    "statusCode": 404,
                    "label": "",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [
                        {
                            "target": "params",
                            "modifier": "id",
                            "value": "222",
                            "invert": false,
                            "operator": "equals"
                        }
                    ],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                },
                {
                    "uuid": "3b773a4c-6d56-4106-b566-b143043904ff",
                    "body": "{\n  \"erro\": 500\n}",
                    "latency": 0,
                    "statusCode": 500,
                    "label": "",
                    "headers": [],
                    "bodyType": "INLINE",
                    "filePath": "",
                    "databucketID": "",
                    "sendFileAsBody": false,
                    "rules": [
                        {
                            "target": "query",
                            "modifier": "id",
                            "value": "123",
                            "invert": false,
                            "operator": "equals"
                        }
                    ],
                    "rulesOperator": "OR",
                    "disableTemplating": false,
                    "fallbackTo404": false,
                    "default": false,
                    "crudKey": "id",
                    "callbacks": []
                }
            ],
            "responseMode": null
        }
    ],
    "rootChildren": [
        {
            "type": "route",
            "uuid": "02a47816-c840-48c9-a060-c2b99ef706bf"
        },
        {
            "type": "route",
            "uuid": "9ddc06b3-c815-43f2-8efe-f62ce5ed0055"
        },
        {
            "type": "route",
            "uuid": "d29d92d3-6506-44a9-960f-4ae0a62bc093"
        },
        {
            "type": "route",
            "uuid": "6f5b9c70-1a00-4060-a213-d456a9a15c73"
        },
        {
            "type": "route",
            "uuid": "899962e2-cb20-4045-beff-11554930caa5"
        },
        {
            "type": "route",
            "uuid": "3daa5873-a8e9-4812-ba1e-1399aaa8b745"
        },
        {
            "type": "route",
            "uuid": "d2db207f-3649-4b3c-8b93-2a35ebcbc810"
        },
        {
            "type": "route",
            "uuid": "8ecd62ae-16d7-4f7a-8ded-3ef2d6420ccb"
        }
    ],
    "proxyMode": false,
    "proxyHost": "",
    "proxyRemovePrefix": false,
    "tlsOptions": {
        "enabled": false,
        "type": "CERT",
        "pfxPath": "",
        "certPath": "",
        "keyPath": "",
        "caPath": "",
        "passphrase": ""
    },
    "cors": true,
    "headers": [
        {
            "key": "Content-Type",
            "value": "application/json"
        },
        {
            "key": "Access-Control-Allow-Origin",
            "value": "*"
        },
        {
            "key": "Access-Control-Allow-Methods",
            "value": "GET,POST,PUT,PATCH,DELETE,HEAD,OPTIONS"
        },
        {
            "key": "Access-Control-Allow-Headers",
            "value": "Content-Type, Origin, Accept, Authorization, Content-Length, X-Requested-With"
        }
    ],
    "proxyReqHeaders": [
        {
            "key": "",
            "value": ""
        }
    ],
    "proxyResHeaders": [
        {
            "key": "",
            "value": ""
        }
    ],
    "data": [
        {
            "uuid": "9d6fab4c-4dc0-461f-a014-53db58597a7d",
            "id": "kxsw",
            "name": "Users",
            "documentation": "",
            "value": "[\n  {{#repeat 50}}\n  {\n    \"id\": \"{{faker 'string.uuid'}}\",\n    \"username\": \"{{faker 'internet.userName'}}\"\n  }\n  {{/repeat}}\n]"
        }
    ],
    "callbacks": []
}
 
```
</details>

`#fish-shell #shell #fish #linux`
- [selecionar texto no terminal linux para copiar e colar em algum lugar fora do terminal](https://askubuntu.com/a/302286/1077413): ctrl + a e depois ctrl + k no fish shell.


`#vscode #code #ide #shortcut`
- [selecionar texto no terminal linux para copiar e colar em algum lugar fora do terminal](https://askubuntu.com/a/302286/1077413): ctrl + a e depois ctrl + k no fish shell.

Atalhos VS COde:
- ctrl + `\`: divide aba de edição de código no meio
- ctrl + shif + v: visualiza a formatação do arquivo markdown
- ctrl + 1: vai para o grupo de abas 1, se você utilizar a tecla 2 e assim por diante, vai para o grupo de abas 2. Use em conjunto com o comando `ctrl + \` 



### 20/09/2024
`#api`
- jsonplaceholder - api gratuita sem autenticação para testes simples: [https://jsonplaceholder.typicode.com/](https://jsonplaceholder.typicode.com/)

`#md #markdown #anchor #ancora`
- para criar uma ancora no readme do Github gere um título (\# Teste) e gere a ancora da seguinite forma: `[link com ancora](#teste)`. Exemplo: [link com ancora para o final da página](#Teste1) e agora um link com espaço e acento: [teste de ancora com acento](#Teste2-com-espaço)
 

### 19/09/2024
`#aws`

#### Well-Architected Framework:
Another way to remember this could be to think of the acronym "CROPS":
- C - Cost Optimization 
- R - Reliability 
- O - Operational Excellence 
- P - Performance Efficiency 
- S - Security

#### AWS Cloud Adoption Framework (AWS CAF), perspectives:

BUS ina PE GOu PLA S ticO

- BUS: Business
- PE: People
- GO: Govenance
- PLA: Platiform
- S: Security
- O: Operations



#### As "AWS best practices" AWS Trusted Advisor:

Cada Serviço Tem Limites Proibitivos.

- C - Custo (Cost Optimization)
- S - Segurança (Security)
- T - Tolerância a Falhas (Fault Tolerance)
- L - Limites de Serviço (Service Limits)
- P - Performance (Performance Improvement)


Clean Servers Function Like Pros.

Let's break it down:
- C - Cost Optimization
- S - Security
- F - Fault Tolerance
- L - Limit (Service Limits)
- P - Performance (Performance Improvement)



Como Posso Seguir em Frente Sem Limite?

Caralho! Porra! Sai fininho, Safado.

- C: Custo (Otimização de Custos)
- P: Performance (Desempenho)
- S: Segurança (Segurança)
- F: Falhas (Tolerância a Falhas)
- S: Serviço (Limites de Serviço)


### 14/09/2024
`#code #vscode #shortcut`
- [VS Code não funciona TAB ou SHIFT+TAB para identar](https://superuser.com/questions/1445748/tab-key-doesnt-indent-in-vs-code): ao pressionar esses caracteres o focus muda entre os elemenentos visuais da tela como rodapé, barra de ferramentas laterais (plugins, debug, controle de versões e outros) e outros elementos. Isso ocorre ao pressionar `ctrl+m` que habilita o modo **Tab moves focus** (na barra inferior, ao lado da posição da linha e coluna). Basta pressionar novamente e tudo voltara ao normal novamente.

`#jmeter `
- [instalar a versão atualizada manualmente](https://stackoverflow.com/questions/54167710/not-able-to-install-jmeter-plugin-manager-in-linux-mint): no linux mint utilizando asdf e fish shell não abriu usando terminal, mas ao clicar com o mouse funcionou normalmente.
- [Genrenciador de plugin Jmeter](https://jmeter-plugins.org/wiki/PluginsManager/)
- [Paylist sobre Jmeter](https://www.youtube.com/watch?v=EpbIpYfHF58&list=PLPHt--SznmcAAankcwYa5Pdn3t1qAl8Cp&index=63)



/usr/share/jmeter/lib/ext


### 01/09/2024
`#mint #toggle`
- Mutar microfone no Linux Mint [Applet mic mute toggle]([link](https://cinnamon-spices.linuxmint.com/applets/view/343))
- 


### 30/08/2024
`#localstack #aws`
- Configuração de API Gateway com terraform e Localstack. Integrando com uma lambda: [The API Gateway & Lambda Tricky Integration Configs](https://hashnode.localstack.cloud/the-api-gateway-lambda-tricky-integration?source=more_series_bottom_blogs)

`#maven #mvn #asdf`
Comandos do asdf:
asdf plugin list all: lista todos os plugins disponiveis para instalar.

asdf plugin list: lista todos os **plugins instalados**.

asdf list all <plugin>: lista todas as versões disponíveis do plugin. Ex: asdf list all maven

asdf list: lista todos os plugins com suas versões instaladas. Exemplo de saída:
```bash
~ asdf list

java
  adoptopenjdk-8.0.392+8
  corretto-8.412.08.1
 *openjdk-17.0.2
maven
  No versions installed
python
  3.10.13
 *3.12.0
  3.6.15
```

asdf plugin-add <nome-do-plugin>: adiciona um plugin. Ex: `asdf plugin-add maven`
  

asdf install <plugin> <versao>: instala a versão de um plugin. Ex: `asdf install maven 3.5.4`
  
  



### 24/08/2024
`#english`
- [aplicativo via vídeo para estudo de inglês](https://www.twynenglish.com/)
- 


### 18/08/2024
`#anki`
- Para visualizar mais de um deck na estatísticas. Ex: `deck:English::Vocabulary or deck:English::Phrases`. [fonte](https://www.reddit.com/r/Anki/comments/mrk8cy/how_to_see_some_specific_deck_i_want_in_anki/)

- deck:"Practice Test #1 - AWS Certified Cloud Practitioner" or deck:"Practice Test #2 - AWS Certified Cloud Practitioner" or deck:"Practice Test #3 - AWS Certified Cloud Practitioner"

## 23/07/2024
`#tools`
- [Número celular temporário para cadastro e outros (semelhante ao temp-mail)](https://temp-number.org/app/)


## 21/07/2024
`#financas`
- [Curso da B3 sobre ETF](https://edu.b3.com.br/w/aprenda-a-investir-em-etf)

## 23/06/2024
`#testes`
- [AWS Step Functions, Terraform e GitHub Actions: um exemplo prático](https://www.linkedin.com/pulse/aws-step-functions-terraform-e-github-actions-um-exemplo-gleyton-lima-ar9zf/?trackingId=sv1Z3hG93CyuNJRviXEmvA%3D%3D)
- [Deveficiente - Testes](https://dev-eficiente.memberkit.com.br/111379-jornada-dev-eficiente/2676816-bugs-amam-fronteiras)

## 27/05/2024
`#AWS #practitioner`
- [AWS Cloud Practitioner Study Notes (CLF-C02)](https://github.com/kananinirav/AWS-Certified-Cloud-Practitioner-Notes/blob/master/practice-exam/practice-exam-11.md)
- [AWS Certified Cloud Practitioner Sample Question and Answers](https://www.cloudduggu.com/aws/Cloud-Practitioner/Question-Answer-Set-1/)

## 12/02/2024
`#LLM #gpt`
- exemplo de docker-compose com ollama e ollama-gui:
```yml
version: '3'
services:
  ollama:
    image: ollama/ollama
    ports:
      - "11434:11434"
    volumes:
      - ollama_data:/root/.ollama

  ollama-webui:
    image: ghcr.io/ollama-webui/ollama-webui:main
    container_name: ollama-webui
    volumes:
      - ollama_data:/root/.ollama-gui
    depends_on:
      - ollama
    ports:
      - 3000:8080
    environment:
      - OLLAMA_API_BASE_URL=http://172.17.0.1:11434/api
    restart: unless-stopped

volumes:
  ollama_data:
``` 

## 11/02/2024
`#docs #google`
- [abrir google documentos no navegador com doc.new](https://doc.new/)

`#memory #python`
- [Memory Management in Python - The Basics](https://www.youtube.com/watch?v=URNdRl97q_0&t=153s)
- [Python Visually memory allocation](https://pythontutor.com/python-compiler.html#mode=edit)

`#LLM #gpt`
- [Ollama LLM](https://ollama.com/library/codellama)
- [Easiest way to get your own Local AI: Ollama Tutorial](https://fixtse.com/blog/ollama-webui)


## 10/02/2024
`#aws #lambda #logs`
- [Useful Insights queries: consultas comuns para lambdas](https://docs.aws.amazon.com/lambda/latest/operatorguide/useful-queries.html)

```sql
filter @message like /sent to sqs/ 
| fields @message, @report 
| filter @report = "memory usage"
```
Let me break down this query:

1. filter @message like /sent to sqs/: This filters log messages where the @message field contains the substring "sent to sqs."
2. fields @message, @report: This extracts the @message and @report fields from the filtered log messages.
3. filter @report = "memory usage": This further filters the results to include only log messages where the @report field has the value "memory usage."

## 04/02/2024
`#python #profiling`
- [Profiling, identificando problemas de performance - Live de Python #204
](https://www.youtube.com/watch?v=cHraQ2I0Xgk)
    - [slides](https://github.com/dunossauro/live-de-python/blob/main/slides/Live%20de%20Python%20%23204.pdf)
    - [timeit](https://docs.python.org/3/library/timeit.html)
    - [memory profiler](https://pypi.org/project/memory-profiler/)
    - [https://matplotlib.org/](https://matplotlib.org/): visualização de estastisticas
    - [cProfile](https://docs.python.org/3/library/profile.html)
    - [snakeviz](https://jiffyclub.github.io/snakeviz/): facilita visualização do pstats
    - [pyinstrument](https://pyinstrument.readthedocs.io/en/latest/home.html): visualiza os dados no terminal e o tempo em cada método do script
    
## 03/02/2024
`#python #profiling`
- [https://docs.python.org/3/library/profile.html](https://docs.python.org/3/library/profile.html)
- [scalene](https://github.com/plasma-umass/scalene?tab=readme-ov-file): a Python CPU+GPU+memory profiler 

## 06/01/2024
`#linux #pendrive`
- criar pendrive bootavel no linux [ventoy](https://www.ventoy.net/en/download.html)


## 17/12/2023
`#avro #python`
- gera classe python com base num schema (avsc):
    - [fastavro-gen](https://github.com/gudjonragnar/fastavro-gen)


crie o arquivo example.avsc:
```avsc
{
    "namespace": "example.avro",
    "type": "record",
    "name": "User",
    "fields": [
        {"name": "name", "type": "string"},
        {"name": "favorite_number",  "type": ["int", "null"]},
        {"name": "favorite_color", "type": ["string", "null"]}
    ]
}
```
```bash
pip install fastavro-gen

fastavro_gen example.avsc ./example.py --no-black
```

## 10/12/2023
`#podcast`
- podcast os programadores com Willian Azevedo sobre docker, certificações, livros, tecnologias cloud ( & ) e  ( & Docker). [https://open.spotify.com/episode/6PF4ySd9DHqPlz3ECYFMel](https://open.spotify.com/episode/6PF4ySd9DHqPlz3ECYFMel)
- sobre subject com python com multiplos schemas no mesmo tópico:
    - [documentação sobre estratégia de subject no schema registry](https://docs.confluent.io/platform/current/schema-registry/fundamentals/serdes-develop/index.html#subject-name-strategy)   
    - [python avro serializer com confluent-kafka-avro](https://docs.confluent.io/platform/current/clients/confluent-kafka-python/html/index.html#avroserializer)
    - [Exemplo prático no Github](https://github.com/shsethix/python-avro-producer/blob/master/send_record.py)
    - [Outro exemplo Github](https://github.com/my-study-area/poc-kafka-connector-lambda)

`#copyq #linux`
- CopyQ is an advanced clipboard manager with powerful editing and scripting features. [https://github.com/hluk/CopyQ](https://github.com/hluk/CopyQ)

Nas configurações do teclado adicione o comando: `/usr/bin/copyq menu` e adicione um atalho para mostrar o menu com o histórico dos ctrl + c

## 09/12/2023
`#bash #shell-script #bash-script`
- Exemplo de bash script com verificação de aws cli instalado:
```bash
#!/bin/bash

# Ensure AWS CLI is installed
if ! command -v aws &> /dev/null; then
    echo "AWS CLI could not be found. Please install it to continue."
    exit 1
fi

# Variables for AWS CloudWatch Logs
LOG_GROUP="your-log-group-name"
LOG_STREAM="your-log-stream-name"
ENDPOINT_URL="http://localhost:4566"

# Fetch log events from AWS CloudWatch
function fetch_log_events() {
    aws logs get-log-events \
        --log-group-name "$LOG_GROUP" \
        --log-stream-name "$LOG_STREAM" \
        --query 'events[].message' \
        --output text \
        --endpoint-url "$ENDPOINT_URL"
}

# Execute the function and handle any errors
{
    fetch_log_events
} || {
    echo "An error occurred while fetching log events."
    exit 1
}

```

## 07/12/2023
`#git #github`
- renomeia uma tag
```terminal
git tag -l
git tag novonome nomeantigo
git push origin nomeantigo:novonome

#opção 2: envia nova tag e deleta a tag antiga
git push novonome :nomeantigo
```

## 04/12/2023
`#whizlabs #aws`
 - contato de suporte: 
    - e-mail: labsupport@whizlabs.com
    - chat: [https://direct.lc.chat/8761536/](https://direct.lc.chat/8761536/)

## 29/11/2023
- conectar dynamodb localmente com dbeaver `#aws`
  - [https://dbeaver.com/docs/dbeaver/AWS-DynamoDB/](https://dbeaver.com/docs/dbeaver/AWS-DynamoDB/)

## 27/11/2023
- action do gtihub para gerar releases `#github #action`
  - [https://github.com/rymndhng/release-on-push-action](https://github.com/rymndhng/release-on-push-action)
  - [upload de arquivos](https://www.theserverside.com/blog/Coffee-Talk-Java-News-Stories-and-Opinions/How-to-publish-GitHub-Actions-artifacts-example)
  - [action para criar release e adicionar jar](https://github.com/marvinpinto/action-automatic-releases). Ex: [https://github.com/adrianoavelino/kafka-connect-lambda-localstack/commit/83b0f4ee420d5700c7fa0e9c336e9341816e764a](https://github.com/adrianoavelino/kafka-connect-lambda-localstack/commit/83b0f4ee420d5700c7fa0e9c336e9341816e764a)

## 25/11/2023
- view: Toggle Terminal: comando no VScode para realizar toogle do terminal `#vscode`

## 23/11/2023
- tflocal: terraform para usar com localstack, sem passar url_endpoint ou profile.

  - [https://docs.localstack.cloud/user-guide/integrations/terraform/](https://docs.localstack.cloud/user-guide/integrations/terraform/)

- localstack com lambdahotreload. `#localstack #aws`

  - [How to hot reload your Lambda functions locally with LocalStack](https://www.youtube.com/watch?v=DFS3CnB-Z0k&ab_channel=LocalStack)

- Repositório com exemplo de deploy manual de lambda empacotando as dependências
  -   [https://github.com/awsdocs/aws-lambda-developer-guide/tree/master/sample-apps/blank-python](https://github.com/awsdocs/aws-lambda-developer-guide/tree/master/sample-apps/blank-python)



## 21/11/2023
Testfixtures is a collection of helpers and mock objects that are useful when writing automated tests in Python.

`#python #test`
- [https://testfixtures.readthedocs.io/en/latest/utilities.html](https://testfixtures.readthedocs.io/en/latest/utilities.html)

### Exemplo de conector lambda sink produzindo mensagem avro
[https://github.com/Nordstrom/kafka-connect-lambda](https://github.com/Nordstrom/kafka-connect-lambda)
```bash
aws cloudformation create-stack \
--stack-name example-lambda-stack \
--capabilities CAPABILITY_NAMED_IAM \
--template-body file://config/cloudformation.yml --profile sandbox
```

`nano config/connector-avro.json`
```json
{
  "name": "example-lambda-connector-avro",
  "config": {
    "tasks.max": "1",
    "connector.class": "com.nordstrom.kafka.connect.lambda.LambdaSinkConnector",
    "topics": "example-stream-avro",
    "key.converter": "io.confluent.connect.avro.AvroConverter",
    "value.converter": "io.confluent.connect.avro.AvroConverter",
    "value.converter.schema.registry.url": "http://localhost:8081",
    "key.converter.schema.registry.url": "http://localhost:8081",
    "payload.formatter.class": "com.nordstrom.kafka.connect.formatters.JsonPayloadFormatter",
    "aws.region": "us-east-1",
    "aws.lambda.function.arn": "arn:aws:lambda:us-east-1:000000000000:function:example-function",
    "aws.lambda.invocation.timeout.ms": "60000",
    "aws.lambda.invocation.mode": "SYNC",
    "aws.lambda.batch.enabled": "false"
  }
}
```

```bash
curl -XPOST -H 'Content-Type: application/json' http://localhost:8083/connectors -d @config/connector-avro.json

curl http://localhost:8083/connectors/example-lambda-connector/status | jq

docker-compose exec schema-registry bash

kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic example-stream-avro \
  --property key.converter=io.confluent.connect.avro.AvroConverter \
  --property value.converter=io.confluent.connect.avro.AvroConverter \
  --property value.converter.schema.registry.url=http://localhost:8081 \
  --property key.converter.schema.registry.url=http://localhost:8081 \
  --property value.schema='{"type":"record","name":"Hello","doc":"AnexampleAvro-encoded`Hello`message.","namespace":"com.nordstrom.kafka.example","fields":[{"name":"language","type":{"type":"enum","name":"language","symbols":["ENGLISH","FRENCH","ITALIAN","SPANISH"]}},{"name":"greeting","type":"string"}]}' \
  --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property parse.key=true \
  --property key.separator=,



{"timestamp":1637000000000},{"language": "ENGLISH", "greeting": "Hello, World!"}
{"timestamp":1637000000000},{"language": "ENGLISH", "greeting": "Hello, World 2!"}



curl -X DELETE http://localhost:8083/connectors/example-lambda-connector-avro
```




## 18/11/2023
Cofiguração de docker-compose com Kafka connect para criar workr/task ao iniciar containers.

- [https://stackoverflow.com/a/60782426/6415045](https://stackoverflow.com/a/60782426/6415045)

Exemplo:
```yml
    - ../config/connector-localstack.json:/connector-localstack.json
    command: 
      - bash 
      - -c 
      - |
        echo "Launching Kafka Connect worker"
        /etc/confluent/docker/run & 
        #
        echo "Waiting for Kafka Connect to start listening on localhost ⏳"
        while : ; do
          curl_status=$$(curl -s -o /dev/null -w %{http_code} http://localhost:8083/connectors)
          echo -e $$(date) " Kafka Connect listener HTTP state: " $$curl_status " (waiting for 200)"
          if [ $$curl_status -eq 200 ] ; then
            break
          fi
          sleep 5 
        done
        echo -e "\n--\n+> Creating Lambda Sink Connector"
        curl -XPOST -H 'Content-Type: application/json' http://localhost:8083/connectors -d @/connector-localstack.json
        sleep infinity
```



## multi schema in one topic
`#avro #kafka`
- [https://karengryg.io/2018/08/18/multi-schemas-in-one-kafka-topic/](https://karengryg.io/2018/08/18/multi-schemas-in-one-kafka-topic/)
```bash
docker run --rm -p 2181:2181 -p 3030:3030 -p 8081-8083:8081-8083 \
       -p 9581-9585:9581-9585 -p 9092:9092 -e ADV_HOST=127.0.0.1 \
       landoop/fast-data-dev:latest
       
# versin: docker pull landoop/fast-data-dev:3.3       


kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic mykafkatopic \
  --property value.schema.registry.url=http://localhost:8081 \
  --property value.schema='{"type":"record","name":"User","namespace":"io.karengryg","fields":[{"name":"first_name","type":"string","doc":"FirstNameofUser"},{"name":"last_name","type":"string","doc":"LastNameofUser"}],"version":"1"}' \
    --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property parse.key=true \
  --property key.separator=, \
  --property value.subject.name.strategy=io.confluent.kafka.serializers.subject.TopicRecordNameStrategy


{"timestamp":1637000000000},{"first_name": "adriano", "last_name": "avelino"}

kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic mykafkatopic \
  --property value.schema.registry.url=http://localhost:8081 \
  --property value.schema='{"type":"record","namespace":"io.karengryg","name":"Movie","version":"1","fields":[{"name":"movie_name","type":"string","doc":"NameofMovie"},{"name":"genre","type":"string","doc":"GenreofMovie"}]}' \
    --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property parse.key=true \
  --property key.separator=, \
  --property value.subject.name.strategy=io.confluent.kafka.serializers.subject.TopicRecordNameStrategy

{"timestamp":1637000000000},{"movie_name": "A ida dos que foram", "genre": "terror"}



kafka-avro-console-consumer \
  --bootstrap-server localhost:9092 \
  --topic mykafkatopic \
  --from-beginning \
  --property schema.registry.url=http://localhost:8081
```

Outros exemplos:

```bash
# creates a producer with AVRO schema with value
kafka-avro-console-producer --broker-list localhost:29092 --topic greetings --property value.schema='{"type": "record","name":"Greeting","fields": [{"name": "greeting","type": "string"}]}'

# creates a producer with AVRO schema with key and value
kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic greetings \
  --property value.schema='{"type": "record","name":"Greeting","fields": [{"name": "greeting","type": "string"}]}' \
  --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property key.separator=, \
  --property parse.key=true \
  --property schema.registry.url=http://localhost:8081


# creates a producer with AVRO schema with key using avro file
# create avro file using cat command
cat > schema1.avsc
{
  "type": "record",
  "name": "SchemaType1",
  "fields": [
    {"name": "field1", "type": "string"}
  ]
}
# press ctrl + D to close the edition

cat > schema2.avsc
{
  "type": "record",
  "name": "SchemaType2",
  "fields": [
    {"name": "field2", "type": "int"}
  ]
}
# press ctrl + D to close the edition

cat > union_value.avsc
{
  "type": "record",
  "name": "UnionValue",
  "fields": [
    {"name": "schemaType", "type": "string"},
    {"name": "value", "type": ["SchemaType1", "SchemaType2"]}
  ]
}
# press ctrl + D to close the edition

###############schema1
# producer example using avro file
kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic greetings1 \
  --property value.schema="$(< schema1.avsc)" \
  --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property key.separator=, \
  --property parse.key=true \
  --property schema.registry.url=http://localhost:8081

# example of events for schema1.avro
{"timestamp":1637000000000},{"field1": "value1"}
{"timestamp":1637000000000},{"field1": "value2"}


# consumer example using avro file
kafka-avro-console-consumer --bootstrap-server localhost:29092 --topic greetings1 \
  --from-beginning \
  --property print.key=true --property print.value=true



################## schema2
# producer example using avro file
kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic greetings \
  --property value.schema="$(< schema2.avsc)" \
  --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property key.separator=, \
  --property parse.key=true \
  --property schema.registry.url=http://localhost:8081

# example of events for schema1.avro
{"timestamp":1637000000000},{"field2": 1}
{"timestamp":1637000000000},{"field2": 2}


# consumer example using avro file
kafka-avro-console-consumer --bootstrap-server localhost:29092 --topic greetings --from-beginning \
  --property value.schema="$(< schema2.avsc)" \
  --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property key.separator=, \
  --property parse.key=true \
  --property schema.registry.url=http://localhost:8081



kafka-avro-console-consumer --bootstrap-server localhost:29092 --topic greetings \
  --from-beginning \
  --property print.key=true --property print.value=true


{"timestamp":1637000000000},{"field2": 1}
{"timestamp":1637000000000},{"field1": "value1"}



################### union
cat > union2.avsc
{
  "type": "record",
  "name": "UnionRecord",
  "fields": [
    {
      "name": "data",
      "type": [
        {
          "type": "record",
          "name": "Type1",
          "fields": [
            {"name": "field1", "type": "string"}
          ]
        },
        {
          "type": "record",
          "name": "Type2",
          "fields": [
            {"name": "field2", "type": "int"}
          ]
        }
      ]
    }
  ]
}
# press ctrl + D to close the edition



# producer example using more than one avro file
kafka-avro-console-producer   --broker-list localhost:9092 \
--topic greetings-union \
--property value.schema="$(< union2.avsc)" \
--property schema.registry.url=http://localhost:8081

{"data": {"Type1": {"field1": "example"}}}
{"data": {"Type2": {"field2": 100}}}


kafka-avro-console-producer \
  --broker-list localhost:9092 \
  --topic greetings \
  --property value.schema= "$(< union_value.avsc)" \
  --property key.schema='{"type":"record","name":"Header","fields":[{"name":"timestamp","type":"long"}]}' \
  --property key.separator=, \
  --property parse.key=true \
  --property schema.registry.url=http://localhost:8081


kafka-avro-console-consumer --bootstrap-server localhost:29092 --topic greetings-union \
  --from-beginning \
  --property print.key=true --property print.value=true

```

Examples to API schema Registry:
```bash
# list all schemas
curl -X GET http://localhost:8081/subjects

#
curl -X GET http://localhost:8081/subjects/greetings-value/versions/latest

# Delete the key schema
curl -X DELETE http://localhost:8081/subjects/greetings-key

# Delete the value schema
curl -X DELETE http://localhost:8081/subjects/greetings-value
```



## comandos kafka kafka connect aws-cli 
#kafka #kafka-connect #aws-cli #cloudformation
```bash
# consome mensagens avro no container schemaregistry
kafka-avro-console-consumer --bootstrap-server kafka:29092 \
--topic topic3 --property schema.registry.url=http://schemaregistry:8081 \
--from-beginning



aws cloudformation create-stack \
  --stack-name example-lambda-stack \
  --capabilities CAPABILITY_NAMED_IAM \
  --template-body file://config/cloudformation.yml \
  --endpoint-url http://localhost:4566


aws lambda invoke --function-name example-function \
--cli-binary-format raw-in-base64-out \
--payload '{"value": "my example"}' --output text result.txt \
--endpoint-url http://localhost:4566


curl -s http://localhost:8083/connector-plugins | jq .[].class



curl -s http://localhost:8083/connectors | jq


# mostra os logs da lambda
aws logs tail /aws/lambda/example-function --follow --endpoint-url http://localhost:4566

# conector 1
curl -X POST -H "Content-Type:application/json" -d @config/connector.json http://localhost:8083/connectors

curl -X DELETE http://localhost:8083/connectors/example-lambda-connector -v


# conector 2 - json
curl -XPOST -H 'Content-Type: application/json' http://localhost:8083/connectors -d @config/connector-json-formatter.json

{"value": "my example"}

curl -X DELETE http://localhost:8083/connectors/example-lambda-connector-json -v

# mostra o status do conector
curl -v http://localhost:8083/connectors/example-lambda-connector-json/status | jq


# produz mensagem string
docker-compose run --rm broker bash

kafka-console-producer --broker-list localhost:19092 --topic example-stream
{"value": "my example"}


docker-compose exec schema-registry bash


kafka-avro-console-producer \
--broker-list localhost:19092 \
--topic example-stream \
--property schema.registry.url http://localhost:8081 \
--property value.schema='{"type":"record","name":"example","fields":[{"name":"nome","type":"string"},{"name":"idade","type":"int"}]}'


{"nome": "Adriano", "idade": 30}
{"nome": "Carlos", "idade": 27}
{"nome": "Maria", "idade": 25}

# list logs in cloudwatch with localstack

descobrir log group
# lista os log groups criados
aws logs describe-log-groups --endpoint-url http://localhost:4566


aws logs tail /aws/lambda/example-function --follow --endpoint-url http://localhost:4566


LOG_GROUP=/aws/lambda/example-function
LOG_STREAM=`aws logs describe-log-streams --log-group-name $LOG_GROUP --max-items 1 --order-by LastEventTime --descending --query logStreams[].logStreamName --output text --endpoint-url http://localhost:4566 | head -n 1`
aws logs get-log-events --log-group-name $LOG_GROUP --log-stream-name $LOG_STREAM --query events[].message --output text --endpoint-url http://localhost:4566


set LOG_GROUP "/aws/lambda/example-function"
set LOG_STREAM (aws logs describe-log-streams --log-group-name $LOG_GROUP --max-items 1 --order-by LastEventTime --descending --query logStreams[].logStreamName --output text --endpoint-url http://localhost:4566 | head -n 1)


Fonte: https://stackoverflow.com/a/56743650/6415045

```

## example to create topíc sqs aws cli:
```bash
aws sns create-topic --name teste1 --profile sandbox
aws sqs create-queue --queue-name q4 --profile sandbox
aws sqs set-queue-attributes --queue-url https://sqs.us-east-1.amazonaws.com/000000000000/q4 --attributes file://sns.json --profile sandbox
{"Policy":"{\"Version\": \"2012-10-17\",\"Id\": \"arn:aws:sqs:us-east-1:000000000000:undefined/SQSDefaultPolicy\",\"Statement\":[{\"Sid\": \"topic-subscription-arn:aws:sns:us-east-1:000000000000:teste1\",\"Effect\": \"Allow\",\"Principal\": {\"Service\": \"sns.amazonaws.com\"},\"Action\": \"SQS:SendMessage\",\"Resource\": \"arn:aws:sqs:us-east-1:000000000000:q4\",\"Condition\": {\"ArnEquals\": {\"aws:SourceArn\": \"arn:aws:sns:us-east-1:000000000000:teste1\"}}}]}"}
aws sns subscribe --topic-arn arn:aws:sns:us-east-1:000000000000:teste1 --protocol sqs --notification-endpoint arn:aws:sqs:us-east-1:000000000000:q4 --profile sandbox
aws sns publish --topic-arn arn:aws:sns:us-east-1:000000000000:teste1 --message "Hello from SNS 1!" --profile sandbox
aws sqs receive-message --queue-url https://sqs.us-east-1.amazonaws.com/000000000000/q4 --profile sandbox
```


Estudo idempotencia api idempotentes e tolerante a falhas

- https://www.youtube.com/watch?v=-50uDb_hExw&ab_channel=MaurodeBoni
- https://www.youtube.com/watch?v=U0DyJx68oCY&ab_channel=CristianoCunha
- https://www.infoq.com/br/news/2013/05/idempotent/
- https://xuenqui.medium.com/idempot%C3%AAncia-uma-boa-pr%C3%A1tica-a-se-utilizar-em-servi%C3%A7os-rest-633c38f4d7c0
- https://developer.mozilla.org/pt-BR/docs/Glossary/Idempotent
- https://opensource.zalando.com/restful-api-guidelines/#149
- https://stripe.com/docs/api/idempotent_requests
- https://stripe.com/docs/videos/developer-foundations?video=idempotency-and-retries&lang=java
- https://github.com/zup-academy/materiais-publicos-treinamentos/blob/main/crud-basico-com-java-hibernate/idempotencia-em-rest-apis.md
- https://developers.openpix.com.br/docs/concepts/idempotence
- https://dev.to/oieduardorabelo/fundamentos-de-api-serverless-idempotencia-2d5m
- https://www.readysetcloud.io/blog/allen.helton/api-essentials-idempotency/
- https://asyncq.com/how-to-implement-idempotent-api-part-1
- https://aws.amazon.com/pt/builders-library/making-retries-safe-with-idempotent-APIs/?did=ba_card&trk=ba_card
- https://www.tedinski.com/2019/02/20/idempotence.html
- https://datatracker.ietf.org/doc/draft-ietf-httpapi-idempotency-key-header/
- https://qasimalbaqali.medium.com/achieving-idempotency-in-the-aws-serverless-space-d0671a521479
- https://www.youtube.com/watch?v=uSXAln1cfqU&ab_channel=DXLab


Exemplos práticos:
- https://javadeveloperzone.com/spring-boot/spring-boot-etag-header-example/
- 


- [AWS Lambda Container Image tutorial](https://www.youtube.com/watch?v=23fE57EFRK4&ab_channel=SrceCde): tutorial para execução de labda dentro do container docker. Código fonte disponível em: [https://github.com/srcecde/aws-tutorial-code/tree/master/lambda/container-image](https://github.com/srcecde/aws-tutorial-code/tree/master/lambda/container-image)
- [LocalStack: usando S3, AWS Secret Manager, AWS Parameter Store e Spring Boot com a API Oficial da Marvel](https://thomsdacosta.medium.com/localstack-usando-s3-aws-secret-manager-aws-parameter-store-e-spring-boot-com-a-api-oficial-da-9e944f43a591) #secrets #localstack #medium
- [Creating Lambda container images](https://docs.aws.amazon.com/lambda/latest/dg/images-create.html#images-create-from-base)
- [testes de mock pytest no postgres](https://github.com/TriageCapacityPlanning/Triage-Backend/blob/main/api/tests/test_database_interaction.py) #python #pytest #mock
- [testes de mock pytest no postgres](https://stackoverflow.com/a/35144096/6415045)
- [mock python com stub](https://github.com/stelligent/python-testing/blob/master/test/unit/test_stubber.py) #python #mock 
- [template de lambda trigada por log group](https://github.com/awsdocs/aws-lambda-developer-guide/blob/main/sample-apps/error-processor/template.yml) #cloudformation #aws #lambda
- [Exemplo de estrutura do event recebido por umalambda trigada pelo log group](https://docs.aws.amazon.com/lambda/latest/dg/samples-errorprocessor.html)
```yml
{
    "messageType": "DATA_MESSAGE",
    "owner": "123456789012",
    "logGroup": "/aws/lambda/lambda-error-processor-randomerror-1GD4SSDNACNP4",
    "logStream": "2019/04/04/[$LATEST]63311769a9d742f19cedf8d2e38995b9",
    "subscriptionFilters": [
        "lambda-error-processor-subscription-15OPDVQ59CG07"
    ],
    "logEvents": [
        {
            "id": "34664632210239891980253245280462376874059932423703429141",
            "timestamp": 1554415868243,
            "message": "2019-04-04T22:11:08.243Z\t1d2c1444-efd1-43ec-b16e-8fb2d37508b8\tERROR\n"
        }
    ]
}
```
#aws #lambda
- [Python versões de dependência no requirement.txt](https://youtu.be/KxvKCSwlUv8?t=906) #python #pip
   
 # Teste1
    
# Teste2 com espaço    
