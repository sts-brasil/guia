# Guia de estilo e organização do guia

Esta página trata de como colaboradores devem redigir páginas do guia
e organizá-las em relação a outras páginas.

Caso seja novato(a) em Markdown, consulte [este guia](https://www.markdownguide.org/getting-started).

{!include/aviso-em-construcao.md!}

## Organização

### Divisão de seções

O guia é dividido em 5 seções principais:

* **Essencial** aborda regras gerais para tradutores do Steam Translation,
    assim como dicas para novatos;
* **Recursos/Jogos** abordam regras e dicas específicas para cada recurso
    e jogo disponível para tradução;
* **Candidatos** aborda diretrizes específicas para membros da Comunidade Steam
    que desejam participar da equipe;
* **Tradutores externos** é composto por um miniguia para tradutores externos,
    desenvolvedores brasileiros, membros da imprensa, etc. que desejam seguir
    a nossa terminologia ao trabalhar em textos que citam recursos, serviços
    e/ou jogos traduzidos no Steam Translation.

Além disso, cada entrada das seções **Recursos** e **Jogos** deve conter, no mínimo,
as seções:

* **Informações gerais**: Descrição breve, link para página na loja
    e/ou informações gerais, etc;
* **Diretrizes de tradução**: Regras e dicas de tradução que vão além de simples terminologia.
    Como deve ser traduzida a fala de certos personagens? Padrões ocultos que o
    tradutor deve ficar atento?
* **Glossário**: Como o próprio nome diz, contém listas simples de termos do produto
    e as suas respectivas traduções.

## Elementos de uma página

### Título

Toda página deve incluir um título, definido com um elemento de cabeçalho nível 1
na primeira linha do arquivo. Para páginas relativas a recursos e jogos,
é aconselhável que o título termine com _sobre o/do jogo X_ (para jogos) ou
_sobre o/do X_ (para outros recursos diversos),
como **Informações gerais sobre o jogo Artifact** ou
**Diretrizes de tradução do Steam Link**.

### Subseções

Páginas podem ser subseções, que, para este projeto, devem usar o estilo de cerquilhas
e não o de sublinhado:

```Markdown
# Seção

Faça assim

## Subseção

e assim
```

```Markdown
Seção
=====

Não assim

Subseção
--------

nem assim
```

### Tabelas

Tabelas no arquivo-fonte devem estar organizadas, com alinhamento de colunas
e um espaço entre o conteúdo de uma célula e as suas extremidades.

```Markdown
| Termo             | Tradução        |
|-------------------|-----------------|
| name              | nome            |
| really long term  | termo bem longo |
```

Não deixe as tabelas assim:

```markdown
|Termo|Tradução|
|-----|---------|
|name|nome|
|really long term|termo bem longo|
```

### Avisos

Avisos podem ser adicionados ao guia por meio da extensão Admonition. Consulte
[este link](https://squidfunk.github.io/mkdocs-material/extensions/admonition/)
para saber como usá-los e os estilos disponíveis.

Decidiremos, com o progresso do guia, que tipos de avisos serão recomendados e o
quanto deverão ser usados, mas por enquanto, fica a cargo do editor, mas não abuse.

Exemplo:

```Markdown
!!! info "Aviso de exemplo"
    Um aviso de exemplo.

    Perceba que as linhas dentro do aviso precisam ter
    quatro espaços antes.

??? tip "Clique em mim!"
    Esta dica fica oculta porque começa com ??? e não !!!.
```

!!! info "Aviso de exemplo"
    Um aviso de exemplo.

    Perceba que as linhas dentro do aviso precisam ter
    quatro espaços antes.

??? tip "Clique em mim!"
    Esta dica fica oculta porque começa com ??? e não !!!.

## Elementos repetidos pelo guia

Caso haja algum bloco de conteúdo que precise ser repetido em várias seções e páginas do guia,
o melhor é usar o recurso de **inclusão** (oferecido pela extensão [Markdown Include](https://github.com/cmacmackin/markdown-include)),
facilitando a inclusão do conteúdo em páginas e evitando possíveis inconsistências
caso venha a ter que alterá-lo no futuro.

Todo arquivo de inclusão deve estar na pasta `docs/include` e ter um nome descritivo.
É permitida a criação de subpastas para agrupar arquivos de temas similares.

Por exemplo, você precisa adicionar um pouco de _lero-lero_ a várias páginas do guia.
A saída simples seria sair copiando e colando o texto em cada uma delas...
mas e caso outra pessoa encontre um erro ou precise adicionar conteúdo ao lero-lero,
terá que verificar todas as páginas para achar as com lero-lero e atualizá-las?
Há ferramentas para buscar e substituir pedaços de texto em vários arquivos de uma vez,
mas seria mais uma coisa para se atentar.

Assim, crie um arquivo `lero-lero.md` na pasta `include` e insira nele o lero-lero.
Depois, em cada página que receberá o lero-lero, adicione a linha a seguir:

<code>&#123;!include/lero-lero.md!&#125;</code>

!!! warning "Não se esqueça das exclamações antes **e** depois do caminho!"

O que resultará na sua substituição pelo conteúdo do arquivo:

{!include/lero-lero.md!}

## Páginas específicas

### Informações gerais

Esta é uma página básica, que deve informar:

* **Nome do jogo**;
* **Link para página na Loja Steam**;
* **Desenvolvedor**;
* **Data de lançamento**;
* **Situação de tradução**.

### Diretrizes

As diretrizes são compostas por regras e indicativos que vão além de simples termos.
Por exemplo, regras de maiúsculas ou minúsculas, padrões que podem ser difíceis
de se notar simplesmente traduzindo, etc.

Caso tenha diretrizes curtas (cerca de duas ou três frases por diretriz)
e não interligadas, faça uma lista em tópicos.
Para diretrizes mais complicadas e/ou que sejam interligadas (como, por exemplo,
regras relacionadas a legendas), crie uma subseção própria.

### Glossários

Glossários são listas simples de termos e as suas respectivas traduções no contexto
em que o glossário está inserido.

Glossários devem sempre estar em tabelas de duas colunas, denominadas **Termo** e **Tradução**.

Exemplo básico:
<pre><code>&#123;!include/aviso-maiuscula-minuscula-glossario.md!&#125;<br/>
| Termo             | Tradução        |
|-------------------|-----------------|
| name              | nome            |
| really long term  | termo bem longo |</code></pre>

Resulta em:

{!include/aviso-maiuscula-minuscula-glossario.md!}

| Termo             | Tradução        |
|-------------------|-----------------|
| name              | nome            |
| really long term  | termo bem longo |

#### Maiúsculas e minúsculas

Um termo na coluna **Tradução** deve conter letras maiúsculas _apenas se estas devem ser mantidas nas traduções_.
Em caso contrário, use apenas letras minúsculas.

Exemplo:

| Termo                 | Tradução                             |
|-----------------------|--------------------------------------|
| Steam Library Sharing | compartilhamento de biblioteca Steam |
| Steam Workshop        | Oficina Steam                        |

Devido a esta regra, inclua o alerta sobre maiúsculas e minúsculas antes de qualquer glossário do guia.
Isso é feito ao adicionar a linha <code>&#123;!include/aviso-maiuscula-minuscula-glossario.md!&#125;</code> antes da tabela.