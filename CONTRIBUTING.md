# Contribuindo com o guia
_Due to the nature of this repository, this documentation is aimed to Portuguese-speakers only._

Para contribuir com este guia, é necessário ter conhecimento de Markdown
e um pouco de conhecimento tanto de Git quanto da plataforma GitHub.

Como podemos ter, entre possíveis colaboradores, usuários não familiarizados com sistemas
de controle de versão e outras ferramentas mais voltadas ao desenvolvimento de _software_,
alguns dos passos de colaboração serão demarcados com **usuários avançados**. Esses passos
não são obrigatórios, mas auxiliam nos testes e verificação de contribuições.


## 1&ordm; passo: Escolha do que contribuir

A plataforma GitHub permite a adição e acompanhamento de problemas e pendências conhecidas
do projeto por meio da seção [issues](https://github.com/sts-brasil/guia/issues).
Por meio dela é possível tanto indicar novos problemas, como escolher no que trabalhar.

### Achei algo para corrigir ou adicionar

Neste caso, acesse a página de [novo _issue_](https://github.com/sts-brasil/guia/issues/new).
Informe um título breve e detalhe, na descrição, o que deve ser adicionado, removido, corrigido, etc.

No caso de correções simples, é recomendável que já emende com um [_pull request_](#) com a correção
já aplicada.

### Quero contribuir, mas não sei com o quê
Veja as _issues_ abertas e escolha uma!

## 2&ordm; passo: Bifurcação (_fork_) do repositório
Depois de escolher o que fazer, realize uma bifurcação do repositório para a sua conta.
Para tal, acesse [esta página](https://github.com/sts-brasil/guia/fork)
e siga as instruções.

## 3&ordm; passo A: Edição em máquina local

### i. Clonagem do repositório
Para colaboradores no Windows ou macOS, este processo pode ser realizado de forma mais fácil
com o uso do aplicativo [GitHub Desktop](https://desktop.github.com/).

Depois de instalar o aplicativo e abri-lo, clique em _Clone a repository_ e selecione o repositório
bifurcado.

Para colaboradores no Linux e/ou com maior afinidade com git,
[instale o git](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git),
abra o terminal/prompt de comando, navegue até a pasta onde deseja clonar o repositório
e clone-o.

### ii. Criação de novo ramo
Crie um novo ramo para melhor organizar as suas alterações. Caso esteja usando o GitHub Desktop,
clique em _Current branch_ no topo e depois no botão _New branch_. Para usuários do git em
linha de comando, navegue até a raiz do repositório e execute o comando:

```bash
git checkout -b [nome-do-ramo]
```

O nome do ramo fica à sua escolha, mas é recomendável usar um nome que comece com a numeração
do _issue_ no GitHub seguido de algumas poucas palavras que descrevem o _issue_.
Exemplo: `10-adicionar-glossario-tf2`

### iii-a. Edição de páginas
Para editar páginas, basta abrir o arquivo .md correspondente e começar a editá-lo, seguindo o nosso
[guia de estilo](guia-de-estilo.md). Um editor recomendado é o [Visual Studio Code](https://code.visualstudio.com/),
com extensões para Markdown (o próprio editor recomendará alguns) e para correção ortográfica.

### iii-b. Adição de páginas
Para adicionar páginas, primeiro defina onde ela ficará localizada segundo o índice.
O local do respectivo arquivo deve então seguir esta mesma localização.

Ex: Páginas associadas ao jogo Ricochet 2 devem estar na pasta `docs/jogos/ricochet2`.

O nome do arquivo deve ser baseado no título da página, com a extensão .md,
a não ser que seja a página principal daquela seção; 
este caso, o nome do arquivo deve ser `index.md`.

Ex: Para criar duas páginas do jogo Ricochet 2, uma de informações gerais (que será a página principal)
e uma de glossário, criaremos dois arquivos:

```
docs/jogos/ricochet2/index.md
docs/jogos/ricochet2/glossario.md
```

Por último, adicione as páginas ao índice. Abra o arquivo [mkdocs.yml](mkdocs.yml) e, na seção
`# Listagem de páginas`, adicione os nomes no índice e caminhos para os novos arquivos.
No caso de jogos, lembre-se de sempre mantê-lo em ordem alfabética com outros jogos.
Tirando isso, use a ordenação que achar melhor.

Ex: Para os dois arquivos criados acima, as entradas a seguir são adicionadas:

```yaml
 #Listagem de páginas
 pages:
# Outras entradas...
   - Jogos:
    # Mais entradas de jogos...
       - Ricochet 2:
         - 'Informações gerais': 'jogos/ricochet2/index.md'
         - 'Glossário': 'jogos/ricochet2/glossario.md'
     # Mais outras entradas...
```

### iv. Testes locais (opcional)
Quando tiver terminado de realizar as suas alterações, realize um teste das páginas
para ver se a formatação está correta e os links no índice estão funcionando.

Para isso, é necessário instalar o Python na sua máquina. Recomendamos usar uma instalação
via gerenciador de pacotes (ex: [Chocolatey no Windows](https://chocolatey.org/packages/python))
para que configure o PATH automaticamente.

Depois de instalado, [crie e ative um novo ambiente virtual](https://docs.python.org/3/tutorial/venv.html)
onde preferir, depois acesse a pasta raiz do repositório pelo terminal/prompt de comando e execute:

```bash
pip install -r requirements.txt
mkdocs serve
```

Depois, abra a página http://127.0.0.1:8000 &mdash; o guia deverá carregar, com as suas alterações.
Tente acessar as páginas criadas e editadas e confirme que tudo está nos conformes. Caso precise
alterar mais alguma coisa, basta editar que a página será recarregada automaticamente.

### v. Efetivação das alterações
Caso esteja no GitHub Desktop,

## 3&ordm; passo B: Edição via GitHub

Esta opção não é recomendada devido 

# Código de Conduta para Colaboradores
## Nossa promessa

Com o interesse de fomentar uma comunidade aberta e acolhedora,
nós, como colaboradores e administradores deste projeto, comprometemo-nos
a fazer a participação deste projeto uma experiência livre de assédio
para todos, independentemente da aparência pessoal, deficiência,
etnia, gênero, idade, identidade ou expressão de gênero, identidade
ou orientação sexual, nacionalidade, nível de experiência, porte físico,
raça ou religião.

## Nossos padrões

Exemplos de comportamentos que contribuem a criar um ambiente positivo incluem:

* Usar linguagem acolhedora e inclusiva
* Respeitar pontos de vista e experiências diferentes
* Aceitar crítica construtiva com graça
* Focar no que é melhor para a comunidade
* Mostrar empatia com outros membros da comunidade

Exemplos de comportamentos inaceitáveis por parte dos participantes incluem:

* Uso de linguagem ou imagens sexuais e atenção ou avanço sexual indesejada
* Comentários insultuosos e/ou depreciativos e ataques pessoais ou políticos (*Trolling*)
* Assédio público ou privado
* Publicar informação pessoal de outros sem permissão explícita, como, por exemplo, um endereço eletrônico ou residencial
* Qualquer outra forma de conduta que pode ser razoavelmente considerada inapropriada num ambiente profissional

## Nossas responsibilidades

Os administradores do projeto são responsáveis por esclarecer os padrões de
comportamento e deverão tomar ação corretiva apropriada e justa em resposta
a qualquer instância de comportamento inaceitável.

Os administradores do projeto têm o direito e a responsabilidade de
remover, editar ou rejeitar comentários, commits, código, edições
na wiki, erros ou outras formas de contribuição que não estejam de
acordo com este Código de Conduta, bem como banir temporariamente ou
permanentemente qualquer colaborador por qualquer outro comportamento
que se considere impróprio, perigoso, ofensivo ou problemático.

## Escopo

Este Código de Conduta aplica-se dentro dos espaços do projeto ou
qualquer espaço público onde alguém represente o mesmo ou a sua
comunidade. Exemplos de representação do projeto ou comunidade incluem
usar um endereço de email oficial do projeto, postar por uma conta de
mídia social oficial, ou agir como um representante designado num evento
online ou offline. A representação de um projeto pode ser ainda definida e
esclarecida pelos administradores do projeto.

## Aplicação

Comportamento abusivo, de assédio ou de outros tipos pode ser
comunicado contatando a equipe do projeto por meio do
[grupo na Comunidade Steam](https://steamcommunity.com/groups/STSBrasil).
Todas as queixas serão revistas e investigadas e
resultarão numa resposta necessária e apropriada à situação.
A equipe é obrigada a manter a confidencialidade em relação
ao elemento que reportou o incidente. Demais detalhes de
políticas de aplicação podem ser postadas separadamente.

Administradores do projeto que não sigam ou não mantenham o Código
de Conduta em boa fé podem enfrentar repercussões temporárias ou permanentes
determinadas por outros membros da liderança do projeto.

## Atribuição

Este Código de Conduta é adaptado do [Contributor Covenant](https://www.contributor-covenant.org),
versão 1.4, disponível em https://www.contributor-covenant.org/pt-br/version/1/4/code-of-conduct.html