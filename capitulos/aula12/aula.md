# Banco de dados

Um banco de dados ou base dados é uma coleção de dados relacionados entre si, como uma grande caixa em que armazenamos e organizamos todas as nossas informações de forma muito simples e inteligente. Cada banco de dados tem suas características e conceitos, mas geralmente todos são criados com o propósito de armazenar e organizar dados para que possamos acessar nossas informações de forma eficiente.

Vamos estudar um tipo de banco que chamamos de relacional, não se prenda nesse conceito agora, com o tempo isso vai ficar mais claro. Nesse banco, os dados são organizados em tabelas interligadas. Essas tabelas são formadas por linhas e colunas. 

Para trabalhar com as tabelas, usamos uma linguagem chamada SQL, que significa Linguagem de consulta estruturada. Basicamente, para criar novos bancos, novas tabelas, manipular dados de tabelas existentes, e mais algumas outras coisas, usamos comandos do SQL.

Vamos usar como exemplo nessa aula o FavelaFlix, uma aplicação fictícia que oferece serviços sobre o cinema produzido na favela. O FavelaFlix exibe uma lista de filmes que a pessoa pode assistir em casa através de sua plataforma. Através da nossa aplicação, consultas são feitas ao nosso banco de dados.

## Criando um banco de dados

O problema, é que nosso banco de dados não existe ainda, então vamos cria-lo! Para isso usamos o comando CREATE DATABASE, a sintaxe fica assim:

```
CREATE DATABASE FavelaFlix; 
```

## Criando uma tabela

Nosso banco precisa também de tabelas, onde armazenaremos nossos dados, vamos criar uma tabela que armazena os dados dos filmes. Precisamos armazenar em uma tabela os dados referentes ao titulo, genero e ano de cada filme, no SQL usamos o comando CREATE TABLE, a sintaxe completa fica assim:
```
CREATE TABLE filmes (
    titulo varchar(255),
    genero varchar(255),
    pais varchar(255),
    nota tinyint,
    ano year
); 
```
Cada uns dos atributos do filme possui um tipo de dado específico, . Por exemplo, título e gênero são valores textuais enquanto a nota é um número inteiro. Abaixo destacamos os tipos de dados mais utilizados.

**Tipos de data e Hora:**

DATE – armazena datas (YYYY-MM-DD)
DATETIME – armazena data e hora (YYYY-MM-DD HH:MM:SS)
TIME – armazena hora (hh:mm:ss)
YEAR – armazena ano no formato (YYYY)

**Tipos numéricos:**
TINYINT: armazena de -128 até 127 ou de 0 até 255
SMALLINT: armazena de -32768 até 32767 ou de 0 até 65535
MEDIUMINT: armazena de -8388608 até 8388607 ou de 0 até 16777215
INT: armazena de -2147483648 até 2147483647 ou de 0 até 4294967295
BIGINT: armazena de -9223372036854775808 até 9223372036854775807 ou de 0 até 2^64-1

**Tipos string:**
CHAR(M): string de tamanho fixo que é sempre preenchida a direita com espaços até o tamanho especificado quando armazenado
VARCHAR(M): string de tamanho variável

Para identificar cada filme, precisamos adicionar um id, com a propriedade *AUTO_INCREMENT*, dessa forma o próprio banco de dados cria esse ID de forma automática. Outra propriedade que precisamos adicionar também é *PRIMARY KEY*, e adicionar a ela o valor da nossa chave primaria, geralmente o id, assim o id é a nossa primeira chave, que podemos usar para identificar cada filme.
```
CREATE TABLE filmes (
    id int AUTO_INCREMENT,
    titulo varchar(255),
    genero varchar(255),
    pais varchar(255),
    nota tinyint,
    ano year,
    PRIMARY KEY (id)
); 
```

Caso uma propriedade seja abrigatória, inclua *NOT NULL*.
```
CREATE TABLE filmes (
    id int AUTO_INCREMENT,
    titulo varchar(255) NOT NULL,
    genero varchar(255),
    pais varchar(255),
    nota tinyint,
    ano year,
    PRIMARY KEY (id)
); 
```

## Adicionando dados
```
INSERT INTO filmes (titulo, genero, ano, pais, nota)
VALUES ('Neguinho e Kika','Ficção', 2013, 'Brasil', 10);

INSERT INTO filmes (titulo, genero, ano, pais, nota)
VALUES ('Central do Brasil', 'Drama', 1998, 'Brasil', 3);

INSERT INTO filmes (titulo, genero, ano, pais, nota)
VALUES ('The Matrix', 'Ficçao Cientifica', 1999, 'Brasil', 5);

INSERT INTO filmes (titulo, genero, ano, pais, nota)
VALUES ('Jurassic Park', 'Ficçao Cientifica', 1993, 'Estados Unidos', 7);

INSERT INTO filmes (titulo, genero, ano, pais, nota)
VALUES ('O Senhor dos Aneis - A Sociedade do Anel', 'Fantasia', 2001, 'Estados Unidos', 10);

INSERT INTO filmes (titulo, genero, ano, pais, nota)
VALUES ('Oldboy', 'Drama', 2003, 'Coreia do Sul', 6);
```

## Selecionando dados

Para selecionar os dados, usamos o comando SELECT, e indicamos uma ou mais colunas e qual tabela queremos selecionar.
```
SELECT titulo FROM filmes;
```

É possível também ao invés de especificar as colunas, selecionar todas as colunas de uma tabela, para isso usamos o seletor universal * fica assim:
```
SELECT * FROM filmes;
```

Para realizar uma busca mais específica podemos utilizar o WHERE e os operadores OR, AND e NOT
```
SELECT * FROM filmes WHERE pais = 'Brasil';
SELECT * FROM filmes WHERE pais = 'Brasil' AND nota >= 5;
SELECT * FROM filmes WHERE NOT pais = 'Brasil';
SELECT * FROM filmes WHERE genero = 'Drama' OR genero = 'Ficção Científica';
```

Podemos também utilizar o ORDER BY para ordenar os nosso resultados
```
SELECT * FROM filmes ORDER BY pais;
SELECT * FROM filmes ORDER BY pais, nota;
SELECT * FROM filmes WHERE genero = 'Drama' OR genero = 'Ficção Científica' ORDER BY nota DESC;
```

Pesquisar valores máximos e mínimos com MAX e MIN
```
SELECT MAX(nota) FROM filmes;
SELECT MIN(ano) FROM filmes;
SELECT MAX(nota) FROM filmes WHERE genero = 'Drama' OR genero = 'Ficção Científica';
```

Contar quantas linhas atingiram nosso critério de pesquisa com COUNT
```
SELECT COUNT(nota) FROM filmes WHERE genero = 'Drama' OR genero = 'Ficção Científica';
```

Pesquisar um valor dentro de uma lista de valores com IN
```
SELECT COUNT(nota) FROM filmes WHERE genero IN('Drama', 'Ficção Científica');
```

E limitar o tamanho do resultado com LIMIT
```
SELECT titulo, nota FROM filmes ORDER BY nota DESC LIMIT 3;
```
