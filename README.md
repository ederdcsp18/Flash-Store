🚀 Flash Store - Arquitetura de Microserviços com Kubernetes
A Flash Store é uma plataforma de e-commerce baseada em microserviços, desenvolvida como projeto acadêmico para o curso de Análise e Desenvolvimento de Sistemas (ADS). O projeto demonstra a implementação prática de containerização, orquestração de clusters e escalabilidade automatizada.

🏗️ Estrutura do Ecossistema
O projeto é dividido em quatro microserviços independentes escritos em Python, localizados no diretório /app:

API Gateway: Ponto de entrada centralizado que gerencia o roteamento das requisições (localizado em ./app/api-gateway).

Estoque: Responsável pelo gerenciamento de produtos e inventário (localizado em ./app/estoque).

Pagamentos: Processa as transações financeiras da plataforma (localizado em ./app/pagamentos).

Pedidos: Controla o ciclo de vida das ordens de compra (localizado em ./app/pedidos).

🛠️ Tecnologias e Ferramentas
Linguagem de Programação: Python (v3.14+).

Containerização: Docker.

Orquestração: Kubernetes (K8s).

Infraestrutura: Terraform e Docker Compose.

Imagens Públicas: Hospedadas no Docker Hub sob o usuário eduratoo.

📋 Pré-requisitos
Para rodar este projeto localmente, você precisará de:

Docker Desktop com suporte a Kubernetes habilitado.

kubectl configurado para interagir com o cluster local.

Acesso à internet para baixar as imagens públicas.

🚀 Como Executar o Projeto
1. Clonar o Repositório

git clone https://github.com/eduratoo/Flash_Store.git

cd Flash_Store

2. Implantar no Kubernetes

Aplique todos os manifestos localizados na pasta /k8s (incluindo Deployments, Services e HPA):

kubectl apply -f ./k8s/

3. Verificar a Execução

Certifique-se de que todos os pods atingiram o status Running:

kubectl get pods

📈 Escalabilidade (HPA)
O projeto inclui arquivos de configuração Horizontal Pod Autoscaler (HPA) no diretório /k8s, permitindo que o Kubernetes aumente ou diminua o número de réplicas dos serviços automaticamente com base no consumo de recursos.