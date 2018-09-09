# Diretrizes gerais de tradução

{!include/aviso-em-construcao.md!}

## Obrigatórias

Estas diretrizes devem ser sempre seguidas, não importando a natureza do texto traduzido.

* Internamente, Steam deve sempre ser referido no masculino — ou seja, **o Steam**;
* Ao encontrar uma string que não tenha tradução (como variáveis ou nomes de arquivos),
    caso não saiba o contexto, sugerimos que deixe para outro tradutor
    com mais experiência no serviço ou jogo em questão;
* Tente manter o tamanho da string próximo ao original;
    * Em textos de páginas web já publicadas, use o inspetor de elementos do navegador
        para testar possíveis traduções _in loco_.
* Traduções só devem possuir maiúsculas no início da primeira palavra de cada frase,
    mesmo que haja maiúscula no início de cada palavra na versão original: 
    * As exceções são nomes próprios e frases escritas em caixa alta, além das exceções delineadas na página específica de cada produto;
* Use o artigo antes de pronomes possessivos que são traduções de adjetivos possessivos (e a crase quando há a preposição "a") quando aplicável, como em _Adicione fundos à sua Carteira Steam_;
    * As únicas exceções são em strings pequenas que iniciem com  pronome, como "Sua conta", "Seus itens" e "Suas informações básicas".
* Remova "por favor" quando o "please" vier no meio de uma frase. Exemplos:
    * "If the problem persists, please contact Steam Support" > "...persistir, contate…";
    * "Cannot connect. Please try again later." > "...conectar-se. Por favor, tente novamente…".
* Todo e qualquer dano é **causado** e **sofrido**;
    * Não use outros termos como _receber_, _infligir_, _tomar_, _levar_ dano ou mesmo _danificar_.
* Caso use de inspiração uma tradução de qualquer outra equipe (como a equipe PT-PT), pedimos que deixe avisado nos comentários;
* Não use aspas simples ou curvadas (__“__ blábláblá __”__), mesmo caso o inglês as possua — troque para aspas duplas retas (__"__ blábláblá __"__);
* Verifique se a string que está sendo traduzida possui espaço antes ou depois dela e, em caso positivo, **mantenha-os**;
* A tradução de gírias e termos populares deve ser feita evitando o uso de regionalismos;
* Use a desinência feminina entre parênteses diretamente após adjetivos que se refiram a uma variável próxima, mesmo que não esteja na mesma string.

## Obrigatórias em textos técnicos

Estas diretrizes devem ser seguidas em textos ditos _técnicos_, como elementos de interface e artigos do Suporte Steam.
Em outros textos, estas regras podem ser flexibilizadas ou ignoradas.

* Não o verbo "ir" como auxiliar ao traduzir frases no futuro. Por exemplo, use "fará" em vez de "irá fazer".
* Evite juntar preposições com artigos indefinidos (como "numa", "dum", "pruma"...), exceto em casos coloquiais, como em legendas e alguns personagens.
* Evite usar _nós_ e _eu_ explicitamente quando o verbo for o bastante Exemplos:
    * Nós entraremos em contato > "Entraremos em contato";
    * "Eu posso lançar mais jogos?" > "Posso lançar mais jogos?".
* Traduza _if_ como **caso**, não **se**.

## Obrigatórias em legendas

Estas diretrizes devem ser seguidas em textos usados como legendas (arquivos de nome `subtitles` e `closedcaptions`).
Muitas destas não se aplicam a outros tipos de texto.

* Sempre siga a norma culta (a não ser em casos onde explicitamente certos artifícios são usados, como a falta de pontuação em falas do Núcleo Espacial), 
mas também não formalize as frases — mantenha a personalidade dos personagens (como a arrogância e o uso deliberado de palavras _feias_ do Francis) intacta.
* Não alongue a tradução: por mais que legendas não tenham limite de espaço na tela na maioria dos jogos da Valve,
  o jogador deve ter tempo de lê-la por completo.