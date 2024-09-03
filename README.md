# Exemplo de como criar uma layer em uma função lambda com terraform.

Esse exemplo utiliza a layer `got` para fazer requisições HTTP em uma função lambda.

## Requisitos

* Terraform 1.1.0 ou superior.
* AWS CLI configurado.
* Localstack (opcional).

## Como usar

1. Clone o repositório
2. Execute `terraform init` para inicializar o diretório de trabalho do terraform.
3. Execute `terraform validate` para verificar se o arquivo `main.tf` esta correto.
4. Execute `terraform plan` para verificar como sera a infraestrutura antes de aplicar.
3. Execute `terraform apply --auto-approve` para criar a infraestrutura.
4. Execute `terraform destroy --auto-approve` para destruir a infraestrutura.
5. Dentro da pasta `lambdas/cat-api`, execute `npm install` para instalar as dependências do npm (ou `npm ci` se você quiser usar o cache do npm).
6. Dentro da pasta `layers/got/nodejs`, execute `npm install` para instalar as dependências do npm (ou `npm ci` se você quiser usar o cache do npm).

## Arquivos

* `layers/got/package.json`: Arquivo de configuração do npm para a layer `got`
* `lambdas/cat-api/index.js`: Arquivo de código da função lambda que utiliza a layer `got`
