# Começando com Python

Python é uma linguagem de programação popular, e bastante poderosa! Ela é usada para muitas coisas diferentes, desde o desenvolvimento de aplicações web, jogos, robôs, e muito mais. Além de tudo, ela é também uma linguagem muito idiomática, e simples, o que é ótimo, pois escrevemos códigos que podem ser compreendidos muito bem por humanos.

O nome da linguagem, caso você que está lendo esteja curioso, ou curiosa, é uma homenagem a uma famosa série de comédia chamada [Monty Python](https://pt.wikipedia.org/wiki/Monty_Python%27s_Flying_Circus).

A linguagem Python foi criada inicialmente com o seguinte propósito: ser uma linguagem fácil e intuitiva enquanto que ainda sendo tão poderosa quanto as maiores competidoras, que fosse de código aberto, para que qualquer um possa contribuir para o desenvolvimento, um código que fosse tão inteligível quanto inglês e que fosse adequada para tarefas diárias, permitindo um tempo de desenvolvimento mais curto.

A essência da linguagem é passada em um poema, O Zen do Python, por Tim Peters. Assim que instalada, podemos executa-la direto em nosso terminal. Para ler o Zen do Python usamos o comando:

```bash
import this
```

O poema é impresso no próprio terminal, traduzindo para português, temos algo como:

```
Bonito é melhor que feio.
Explícito é melhor que implícito.
Simples é melhor que complexo.
Complexo é melhor que complicado.
Linear é melhor do que aninhado.
Esparso é melhor que denso.
Legibilidade conta.
Casos especiais não são especiais o bastante para quebrar as regras.
Ainda que praticidade vença a pureza.
Erros nunca devem passar silenciosamente.
A menos que sejam explicitamente silenciados.
Diante da ambiguidade, recuse a tentação de adivinhar.
Deveria haver um — e preferencialmente só um — modo óbvio para fazer algo.
Embora esse modo possa não ser óbvio a princípio a menos que você seja holandês.
Agora é melhor que nunca.
Embora nunca frequentemente seja melhor que já.
Se a implementação é difícil de explicar, é uma má idéia.
Se a implementação é fácil de explicar, pode ser uma boa idéia.
Namespaces são uma grande ideia — vamos ter mais dessas!
```
# Seu primeiro programa em Python

Vamos começar a desenvolver nossos primeiros programas em Python. Lembrando que por definição, um programa é uma sequência de instruções que especifica como executar uma operação de computação.

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

Reza a lenda que ao aprender uma nova linguagem de programação precisamos exibir um Olá mundo ou sofreremos para sempre com a maldição de nunca aprender a linguagem.

```python
print('Olá mundo')
```
O Python consegue fazer muitas coisas, como por exemplo operações matemáticas. Digite uma operação simples e veja o que acontece:
```python
1 + 1
```
