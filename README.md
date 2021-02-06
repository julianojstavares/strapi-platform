# Strapi application

Este é o repositório de um projeto Strapi hospedado no Heroku  
This is the repository for a Strapi project hosted on Heroku

Você pode acessá-lo aqui   
You can access it here

https://strapi-platform.herokuapp.com/admin  

Este projeto foi criado e concluído sem custar dinheiro algum, além de bastante tempo de estudo  

A hospedagem do Heroku foi gratuita  
> (Para o app não adormecer, dei a ele um pouco de café https://kaffeine.herokuapp.com/ e parece que deu certo)  

A hospedagem do MySQL foi gratuita  
> (Usei o conceito de Banco de Dados como Serviço (DBaaS) e hospedei um banco MySQL gratuitamente no site https://freedb.tech/)  

A hospedagem no GitHub também é gratuita  

O deploy no Heroku está vinculado a este repositório, então ao atualizar aqui no GitHub, atualiza no Heroku também  

***
  
This project was created and completed without costing any money, besides a lot of study time

Heroku hosting was free  
> (For the app not to fall asleep, I gave him some coffee https://kaffeine.herokuapp.com/ and it looks like it worked)

MySQL hosting was free  
> (I used the concept of Database as a Service (DBaaS) and hosted a MySQL database for free at https://freedb.tech/)

GitHub hosting is also free

The Heroku deploy is linked to this repository, so when updating here on GitHub, updates on Heroku too

***

Agora, um pouco de código  

As linhas fundamentais para este projeto dar certo são as seguintes:  

```javascript
host: process.env.DATABASE_HOST,
port: process.env.DATABASE_PORT,
database: process.env.DATABASE_NAME,
username: process.env.DATABASE_USERNAME,
password: process.env.DATABASE_PASSWORD,
```
> config/database.js  

Para dar tudo certo é só configurar as variáveis correspondentes no Heroku  

Por exemplo, no caso da variável relacionada a hospedagem do banco de dados, criei no Heroku uma variável chamada DATABASE_HOST
e coloquei o valor dela como o endereço do host, no caso **_freedb.tech_**
