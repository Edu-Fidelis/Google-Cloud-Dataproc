# Google-Cloud-Dataproc
Criando um Ecossistema Hadoop Totalmente Gerenciado com Google Cloud Dataproc

Descrição do Desafio
Sua missão será criar um ecossistema de Big Data usando o Google Cloud Platform (GCP). 
Para isso, o expert te ensinará a configurar o Google Cloud Dataproc, 
um Hadoop totalmente gerenciado, usando seus créditos gratuitos da GCP.

## Passo 1

### Criando a conta no GCP

##### Entrar:
console.cloud.google.com


##### Clicar em:

1 - Selecione um projeto
2 - Novo projeto


##### Criando o projeto

1 - Nome do projeto
2 - Colocar numa pasta/organização, se preciso
3 - Criar projeto
4 - Selecionar projeto => Abre o "dashboard"


##### Ativando a conta

1 - Clique em ativar lá em cima da página do dashboard do projeto
2 - Escolhe o país e concorda com os termos
3 - Pessoa física, CPF, nascimento, endereço, cartão de crédito
4 - "Iniciar minha teste gratuito"
5 - Responder as perguntas do GCP
6 - Concluído


##### Orçamentos e alertas

1 - Clique em "Orçamentos e alertas"
2 - Clique em Criar Orçamento
3 - Nome, Projetos, Serviços (Pode selecionar todos para monitoramento)
4 - Valor, pode colocar valor específico (recomendado) ou gasto do mês anterior
5 - Ações, pode usar até as Cloud Functions
6 - Concluir


## Passo 2

### Compute Engine

##### Entrando no Compute Engine

1 - Menu (três barras horizontais)
2 - Compute Engine
3 - Instâncias de VM
4 - Vai na API, clique em ativar
5 - Abre os menus da Compute Engine, na parte de máquinas virtuais

##### Criando instância

1 - No menu da Compute Engine, clique em criar instância
2 - Nome, marcadores, região, configurações de máquina
3 - Criar

##### Acessando a máquina

1 - Ocultar painel de informações
2 - SSH

###### Ou

1 - Cloud Shell (Canto superior direito, lá no ícone)


##### Excluindo

1 - Selecionar no quadrado em branco
2 - Mais opções (três bolinhas uma em cima da outra)
3 - Excluir

## Passo 3

### Dataproc

##### Ativando o Dataproc

1 - Menu (três barras horizontais)
2 - Lá no Big Data, clique em Dataproc
3 - Ativar a API do Dataproc


##### Criando um Bucket

1 - Menu (três barras horizontais)
2 - Cloud Storage
3 - Criar intervalo
4 - Nomear (Com nome único no mundo), escolher onde armazenar os dados, classe de armazendamento, controle de acesso a objetos, configurações avançadas
5 - Criar


##### Criando o cluster

1 - Pesquisar por Dataproc
2 - Clique em Criar cluster
3 - Configurar conforme necessário
4 - Criar

##### No cluster

1 - Clica no nome em azul do cluster para ver mais sobre ele


##### Job

1 - Menu (três barras horizontais)
2 - Lá no Big Data, clique em Dataproc
3 - Clique em Job (barra à esquerda)
4 - Em arquivos .jar => file://usr/lib/spark/examples/jars/spark-examples.jar
5 - Enviar
4 - Clique em enviar job


## Resolvendo o desafio

GitHub: https://github.com/marcelomarques05/dio-desafio-dataproc

1 - Abre GCP
2 - Cloud shell
3 - git clone https://github.com/marcelomarques05/dio-desafio-dataproc.git
4 - cd dio-desafio-dataproc/
5 - gsutil ls
6 - vim contador.py
7 - gs://desafio-dataproc-edu/livros.txt
8 - gsutil cp contador.py livro.txt gs://desafio-dataproc-edu/
9 - Vá no cluster e clique em Jobs
10 - Nome: job-desafio-edu
11 - Tipo de Job: PySpark
11 - Arquivo Python principal: gs://desafio-dataproc-edu/contador.py
12 - Enviar
13 - Menu (três barras horizontais)
14 - Cloud Storage
15 - desafio-dataproc-edu
