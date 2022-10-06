# Prueba tecnica

## Tecnologías

node
typescript
serverlees
dynamodb
diversos plugins

## Requerimientos

Tener una un access key y secret key a aws, para el despliegue de los lambda
configurarlo en la maquina host con aws-cli

npm install -g serverless # Herramienta de despliegue a aws
npm install #instalar los paquetes

## Estructura

src : se ubica los metodos lambda
    addToken
    getToken

middleware : se ubica el validador pk del Header su valor actual es de: "pk_test_LstJoiskhHytsmksjgakKhs"

persistence
    dynamodb

## Ejecución

    Despues de configurar el aws-cli, hay dos modo de ejecución uno desde aws y otro de manera local
    Desde aws se despliega con 
        serverless deploy 
    Esto creara el stack, que posee las funciones y la tabla dynamo donde se almacena

## Evidencia

postman

serverless invoke local --function addToken --path data/data1.json
serverless invoke local --function addToken --path data/data2.json
serverless invoke local --function getToken --path data/dataGet.json
