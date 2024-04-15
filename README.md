# AWS Lambda Workflows

Faça o deploy do seu código Python no AWS Lambda.

## Como usar?

```yaml
name: Deploy Python to AWS Lambda
on: [push]

jobs:
  deploy:
    uses: gh-actions-workflows/aws-lambda-workflows/.github/workflows/deploy-lambda.yaml@1.6
    with:
      function_name: my_function
      handler: my_handler.handler # Nome do arquivo "." nome da função que será o entrypoint do Lambda 
    secrets:
      aws_access_key_id: ${{ secrets.AWS_ACCESS_KEY_ID }}
      aws_secret_access_key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
      aws_region: ${{ secrets.AWS_REGION }}
```

Para mais detalhes sobre o funcionamento consulte o arquivo: [deploy-lambda.yaml](https://github.com/gh-actions-workflows/aws-lambda-workflows/blob/master/.github/workflows/deploy-lambda.yaml).
