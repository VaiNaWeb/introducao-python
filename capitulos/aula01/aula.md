# Começando com Python

Python é uma linguagem de programação popular, e bastante poderosa! Ela é usada para muitas coisas diferentes, desde o desenvolvimento de aplicações web, jogos, robôs, e muito mais. Além de tudo, ela é também uma linguagem muito idiomática, e simples, o que é ótimo, pois escrevemos códigos que podem ser compreendidos muito bem por humanos.

O nome da linguagem, caso você que está lendo esteja curioso, ou curiosa, é uma homenagem a uma famosa série de comédia chamada [Monty Python](https://pt.wikipedia.org/wiki/Monty_Python%27s_Flying_Circus).

A linguagem Python foi criada inicialmente com o seguinte propósito: ser uma linguagem fácil e intuitiva, poderosa, e de código aberto, para que todos possam aprender a programar.

# Seu primeiro programa em Python

Vamos começar a desenvolver nossos primeiros programas em Python. Por definição, um programa é uma sequência de instruções que especifica como executar uma operação de computação.

Como aprendemos em outro módulo, o código em HTML precisa de um navegador para interpreta-lo. O Python tem seu próprio interpretador, um programa que lê e executa o código Python.

Para começar, nós queremos abrir o Python em um terminal, para fazer isso é só digitar o comando python, ou python3 e apertar enter.

```cmd
python3
```

Quando o interpretador iniciar, você deverá ver algo como:

```cmd
Python 3.6.3 (...)
Type "help", "copyright", "credits" or "license" for more information.
>>>
```

Esses símbolos >>> significam que o interpretador do Python está pronto para você digitar o código. Se precisar sair dele digite exit() e aperte enter. Mas não é isso que queremos fazer.

O Python consegue fazer muitas coisas, como por exemplo operações matemáticas. Digite uma operação simples e veja o que acontece:
```python
1 + 1
```

Legal, não é?! Você pode tentar outros comandos como multiplicação, subtração, e divisão:

```python
4 * 10
```

```python
10 - 1
```

```python
15 / 3
```
Também tem o operador para trabalhar com exponenciação, exemplo:
```python
2 ** 4
```

# A Maldição do olá mundo e as letras

Reza a lenda que ao aprender uma nova linguagem de programação precisamos exibir um Olá mundo ou sofreremos para sempre com a maldição de nunca aprender a linguagem.

```python
print('Olá mundo')
```
Você acabou de usar um comando um pouco mais avançado da linguagem e nem percebeu. O Python assim como outras linguagens de programação tem uma estrutura que chamamos de função, não se preocupe em entender sobre isso agora, mas saiba que  existem funções que já são nativas da linguagem, e outras que vamos aprender a criar em um futuro próximo. 

A função nativa que você usou é a <code>print()</code> que serve basicamente para mostrar coisas na tela. Uma coisa legal sobre funções é que elas recebem coisas dentro dela, no exemplo que usamos a função recebeu a frase Olá mundo entre aspas. Tente substituir o conteúdo das aspas por outra palavra que você deseje, como por exemplo seu nome e veja o que acontece!

As aspas indicam que esse dado que você está usando é uma palavra, chamamos esse tipo de dado de String. O Python também permite fazer operações usando palavras, faça o teste:
```python
print(' ilari' * 3 + ' ê, oh oh oh')
```

# Errar pode ser divertido

O que será que acontece se você tirar as aspas da frase?
```python
print(ola mundo)
  File "<stdin>", line 1
    print(ola mundo)
                  ^
SyntaxError: invalid syntax
```
Seu primeiro erro! SyntaxError: invalid syntax indica que você cometeu um erro de sintaxe, já aprendemos sobre isso, é quando escrevemos a estrutura da instrução de uma forma diferente da que a linguagem foi projetada para usar. Geralmente acontece quando esquecemos algum símbolo, como aspas, ou uma vírgula, por exemplo.

Sabendo disso, você já sabe como descobrir o que está fazendo de errado. Ler os erros que o próprio interpretador apresenta no terminal pode ser muito útil, pois você pode copia-lo e pesquisar sobre ele. Aqui mora a magia em programar, procurar sobre erros e corrigi-los pode ser um desafio muito legal.

# Guardando coisas em Variáveis

Uma variável é um espaço com um nome reservado para guardar alguma coisa. Usamos variáveis para guardar dados, elas também são úteis para fazer códigos mais fáceis de ler.

```python
nome = "Dali"
```
Pronto, você já criou uma varíável e atribuiu a ela um valor como String. Ou seja, guardamos uma palavra dentro dessa variável! Agora digite nome e tecle enter, você vai poder ver esse valor que ela guardou:

```python
nome
```
Você também pode guardar um novo valor dentro da mesma variável. Exemplo:

```python
nome = "Anna"
```
Uma variável pode guardar vários tipos de dados diferentes, como números, listas, datas! Exemplo usando números:

```python
nome = "Hebert"
idade = 20
```

Você pode usar a função print para exibir essas variáveis na tela!
```python
print(nome, idade)
```

Python pode ser muito divertido! Você pode continuar testando as instruções que você aprendeu hoje no interpretador. Gostaríamos que você continuasse praticando mais um pouco para que você também possa perceber como programar pode ser uma coisa muito legal e divertida.
