# Fake Shop

## Variável de Ambiente
--------------------------------------------------------------
DB_HOST	=> Host do banco de dados PostgreSQL.
DB_USER => Nome do usuário do banco de dados PostgreSQL.
DB_PASSWORD	=> Senha do usuário do banco de dados PostgreSQL.
DB_NAME	=>	Nome do banco de dados PostgreSQL.
DB_PORT	=>	Porta de conexão com o banco de dados PostgreSQL.

# INSTRUÇÕES FAZER DEPLOY POR PIPELINE CI-CD
1 - ABRIR ABA ACTIONS
2 - UTILIZAR TEMPLATE COMO PONTO DE PARTIDA OU CRIAR (SET UP WORKFLOW YORSELF)
OBS: CRIAMOS O NOSSO PROPRIO WORKFLOW
3 - BOAS PRATICAS DE CRIAÇÃO É FAZER UMA PRIMEIRA VERSÃO-FAKE (PORTUGOL) DOS PROCESSOS CI E CD
NOSSO EXEMPLO:
--------------------------------------------------------------
# Fake-lista-dos-comandos
# name: CI-CD
# on:
#  push:
#    branches: ["main"]
#  workflow_dispatch:
#  
# jobs:
#    CI:
#      runs-on: ubuntu-latest
#      steps:
#        - run: echo "Obter codigo"
#        - run: echo "Fazer Login no Docker Hub"
#        - run: echo "Executar o Docker build"
#        - run: echo "Enviar imagem Docker para o Docker Hub"
#    CD:
#      needs: [CI]
#      runs-on: ubuntu-latest
#      steps:
#        - run: echo "Obter codigo"
#        - run: echo "Configurar o kubeconfig"
#        - run: echo "Executar o apply"
--------------------------------------------------------------
4 - UTILIZAR MARKETPLACE DE ACTIONS (https://github.com/marketplace?type=actions)
5 - UTILIZAR VARIÁVEIS DO TIPO SECRET SEMPRE QUE PRECISAR PASSAR DADOS CONFIDENCIAIS, TOKENS DE CERTIFICADOS, SENHAS, ECT.
6 - ACTIONS UTILIZADAS:
# CI
6.1 - CHECKOUT
6.2 - DOCKER LOGIN
6.3 - BUILD AND PUSH DOKER IMAGES
6.4 - BUILD AND PUSH DOKER IMAGES
# CD
6.5 - CHECKOUT
6.6 - KUBERNETS SET CONTEXT
6.7 - DEPLOY TO KUBERNETES CLUSTER

