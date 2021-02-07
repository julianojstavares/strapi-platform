# Strapi application

A seguir serão apresentados textos em inglês e português do Brasil  
Next, texts in English and Brazilian Portuguese will be presented  

Este é o repositório de um projeto Strapi hospedado no Heroku  
This is the repository for a Strapi project hosted on Heroku

Você pode acessá-lo aqui   
You can access it here

https://strapi-platform.herokuapp.com/admin  

Este projeto foi criado e concluído sem custar dinheiro algum, além de bastante tempo de estudo  

O Strapi é grátis  
> (Iniciei ele em modo personalizado após já saber todas as informações da hospedagem remota do MySQL)  
> (tudo que tive que fazer foi executar o comando yarn create strapi-app nome-do-projeto e ir preenchendo o resto)

A hospedagem do Heroku foi gratuita  
> (Para o app não adormecer, dei a ele um pouco de café https://kaffeine.herokuapp.com/ e parece que deu certo)  

A hospedagem do MySQL foi gratuita  
> (Usei o conceito de Banco de Dados como Serviço (DBaaS) e hospedei um banco MySQL gratuitamente no site https://freedb.tech/)  

A hospedagem no GitHub também é gratuita  

O deploy no Heroku está vinculado a este repositório, então ao atualizar aqui no GitHub, atualiza no Heroku também  

***
  
This project was created and completed without costing any money, besides a lot of study time  

Strapi is free  
> (I started it in custom mode after knowing all the information about remote MySQL hosting)  
> (all I had to do was run the command yarn create strapi-app project-name and fill in the rest)  

Heroku hosting was free  
> (For the app not to fall asleep, I gave him some coffee https://kaffeine.herokuapp.com/ and it looks like it worked)

MySQL hosting was free  
> (I used the concept of Database as a Service (DBaaS) and hosted a MySQL database for free at https://freedb.tech/)

GitHub hosting is also free

The Heroku deploy is linked to this repository, so when updating here on GitHub, updates on Heroku too

***

Agora, um pouco de código  
Now, a little bit of code  

As linhas fundamentais para este projeto dar certo são as seguintes:  
The fundamental lines for this project to succeed are the following:  

```javascript
host: process.env.DATABASE_HOST,
port: process.env.DATABASE_PORT,
database: process.env.DATABASE_NAME,
username: process.env.DATABASE_USERNAME,
password: process.env.DATABASE_PASSWORD,
```
> trecho do arquivo database.js que está dentro da pasta config  
> excerpt from the database.js file that is inside the config folder  

Para dar tudo certo é só configurar as variáveis correspondentes no Heroku  
To be all right just set the corresponding variables in Heroku  

Por exemplo, no caso da variável relacionada a hospedagem do banco de dados (DATABASE_HOST), criei no Heroku uma variável de mesmo nome 
e coloquei o valor dela como o endereço do host, no caso **_freedb.tech_**  

For example, in the case of the variable related to database hosting (DATABASE_HOST), I created in Heroku a variable of the same name
and put its value as the host address, in the case **_freedb.tech_**  

Depois é só fazer o mesmo para as outras quatro variáveis  
Then just do the same for the other four variables  

Para saber mais como configurar variáveis no Heroku, acesse  
To learn more about setting variables in Heroku, visit  

https://devcenter.heroku.com/articles/config-vars


***

Se o Strapi está em produção, online no Heroku, como executá-lo localmente, em modo de desenvolvimento?  
Basta criar um arquivo .env no projeto (dentro da pasta raiz) com as mesmas variáveis do banco de dados e seus respectivos valores  

Exemplo:  
> DATABASE_HOST=freedb.tech  

Crie o arquivo .env e preencha com as variáveis, linha por linha  

Depois é só executar yarn develop na linha de comando e trabalhar no que for necessário  

Não esqueça de checar se o arquivo .env consta declarado dentro .gitignore antes de subir as alterações para o GitHub 

***  

If Strapi is in production, online at Heroku, how to run it locally, in development mode?
Just create an .env file in the project (inside the root folder) with the same variables as the database and their respective values

Example:
> DATABASE_HOST = freedb.tech  

Create the .env file and fill in the variables, line by line  

Then just run yarn develop on the command line and work on whatever is necessary  

Don't forget to check if the .env file is declared inside .gitignore before uploading changes to GitHub  

***  
### Se você gosta de atalhos, crie automaticamente o arquivo .env executando o seguinte comando na interface de linha de comando local  
### If you like shortcuts, automatically create the .env file by running the following command on the local command line interface  

```bash
heroku config -a APP -s >> .env
```

> Substitua a palavra APP pelo nome do seu projeto
> Replace the word APP with the name of your project