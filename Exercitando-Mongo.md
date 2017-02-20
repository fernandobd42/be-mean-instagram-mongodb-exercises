#Atividades para fixação do conteúdo

##1) Crie um banco de dados chamado biblioteca
- use biblioteca

##2) Crie uma coleção (collection) chamada livros
- db.createCollection('livros')

##3) Crie os sequintes documentos:

título: Introdução a linguagem de marcação HTML
valor: 25.00
Autor: João

- db.livros.insert({titulo: 'Introdução a linguagem de marcação HTML', valor: 25.00, autor: 'João'})


título: NodeJS do básico ao avançado
valor: 280.00
Autor: Jorge

- db.livros.insert({titulo: 'NodeJs do básico ao avançado', valor: 280.00, autor: 'Jorge'})


título: Android - criando apps reais
valor: 290.00
Autor: Jamilton

- db.livros.insert({titulo: 'Android - Criando apps reais', valor: 290.00, autor: 'Jamilton'})


título: PHP e MySQL
valor: 190.00
Autor: Fernando

- db.livros.insert({titulo: 'PHP e MySQL', valor: 190.00, autor: 'Fernando'})


título: Lógica de Programação
valor: 20.00
Autor: Maria

- db.livros.insert({titulo: 'Lógica de Programação', valor: 20.00, autor: 'Maria'})


##4) Crie as seguintes consultas:

Crie uma consulta que retorne apenas os documentos de livros com valores superiores a 200.00
- db.livros.find({valor: {$gt: 200}})

Crie uma consulta que retorne apenas os documentos com valores entre 10 e 30
- db.livros.find({valor:{$gt: 10, $lt: 30}})

Crie uma consulta que retorne todos os documentos, executo aqueles cujo autor seja Fernando
- db.livros.find({autor: {$ne: 'Fernando'}})

##5) Atualize os seguintes documentos:

Atualize o documento cujo o título é PHP e MySQL, passando seu valor de 190.00 para 175.00
- db.livros.update({titulo: 'PHP e MySQL'}, {$set: {valor: 175.00}})

Atualize o documento cujo autor é Jorge, passando seu título para Curso Completo de NodeJS
- db.livros.update({autor: 'Jorge'}, {$set: {titulo: 'Curso Completo de NodeJS'}})

Atualize todos os documentos cujo valor são iguais ou inferiores a 25.00 para o valor 27.00
- db.livros.update({valor: {$lte: 25}}, {$set: {valor: 27}},{multi: true})


##6) Remove os seguintes documentos:

Remova o documento cujo autor é João
- db.livros.remove({autor: 'João'})

Remova todos os documentos cujo valor é superior a 280.00
- db.livros.remove({valor: {$gt: 280}})

Remova todos os documentos cujo valor é inferior a 30.00
- db.livros.remove({valor: {$lt: 30}})
