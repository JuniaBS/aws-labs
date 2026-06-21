# Arquitetura Fan-Out com SNS, SQS e Lambda

## Objetivo

Implementar uma arquitetura orientada a eventos utilizando Amazon SNS, Amazon SQS e AWS Lambda, aplicando o padrão **Fan-Out** para distribuir mensagens entre múltiplos consumidores de forma assíncrona. O laboratório também aborda filtros de assinatura, tratamento de falhas com Dead-Letter Queue (DLQ) e monitoramento através do Amazon CloudWatch.

## Serviços Utilizados

* Amazon SNS
* Amazon SQS
* AWS Lambda
* Amazon CloudWatch
* AWS IAM

## Arquitetura

A arquitetura implementada utiliza o Amazon SNS como um hub central para distribuir mensagens para múltiplos consumidores utilizando o padrão Fan-Out. O fluxo inclui processamento paralelo com AWS Lambda, integração com Amazon SQS para análise de fraude e utilização de Dead-Letter Queue (DLQ) para tratamento de falhas.

![Arquitetura](./images/sns-sqs-lambda-fanout-architecture.jpg)

## Funcionalidades

* Implementação do padrão Fan-Out utilizando Amazon SNS.
* Distribuição de mensagens para múltiplos consumidores.
* Configuração de filtros de assinatura (Subscription Filter Policy).
* Processamento assíncrono com Amazon SQS.
* Criação de Dead-Letter Queue (DLQ) para tratamento de falhas.
* Desenvolvimento de funções AWS Lambda em Python.
* Integração entre SNS, SQS e Lambda.
* Processamento paralelo de diferentes etapas do fluxo de pedidos.
* Monitoramento das execuções através do Amazon CloudWatch Logs.
* Gerenciamento de permissões utilizando IAM Roles.

## Aprendizados

* Arquitetura orientada a eventos (Event-Driven Architecture).
* Implementação do padrão Fan-Out.
* Integração entre Amazon SNS e Amazon SQS.
* Processamento assíncrono utilizando filas.
* Desenvolvimento de aplicações Serverless com AWS Lambda.
* Configuração de filtros de mensagens com SNS.
* Tratamento de falhas utilizando Dead-Letter Queue (DLQ).
* Gerenciamento de permissões com IAM.
* Monitoramento e troubleshooting utilizando CloudWatch Logs.
* Construção de arquiteturas desacopladas e escaláveis.

## Evidências

### SNS - Assinaturas do Tópico

![SNS Subscriptions](./images/sns-subscriptions.jpg)

### SQS com Dead-Letter Queue (DLQ)

![SQS DLQ](./images/sqs-dlq-configuration.jpg)

### Logs da Lambda de Inventário

![CloudWatch Inventory](./images/cloudwatch-inventory-logs.jpg)

### Logs da Lambda de Pagamento

![CloudWatch Payment](./images/cloudwatch-payment-logs.jpg)

## Resultado

Neste laboratório foi possível implementar uma arquitetura orientada a eventos utilizando Amazon SNS, Amazon SQS e AWS Lambda, aplicando o padrão Fan-Out para distribuir mensagens para múltiplos consumidores de forma desacoplada.

A solução permitiu processar diferentes etapas de um fluxo de e-commerce em paralelo, incluindo atualização de inventário, processamento de pagamento, notificação ao cliente e análise de fraude. Além disso, foi implementado um mecanismo de resiliência através de Dead-Letter Queue (DLQ), garantindo maior confiabilidade no tratamento das mensagens.

A prática permitiu aplicar conceitos fundamentais de mensageria, arquiteturas serverless, processamento assíncrono, monitoramento e integração entre serviços AWS, simulando um cenário próximo ao encontrado em aplicações distribuídas e ambientes corporativos.
