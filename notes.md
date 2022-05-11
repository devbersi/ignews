## Basicamente o Next foi desenvolvido para uma melhor indexação nas páginas( SEO )
    - Como os motores de buscas só entendem html, e as SPA ( Single-page Application ) são feitas através do Browser por Javascript, as páginas utilizando as SPA's não seriam possível ser indexadas.
    
## É ai que entra a função do Next: 
    - O next basicamente carrega todo o conteúdo pelo servidor NodeJS dele e já devolve para o Browser seu código em HTML, nisso, fazendo os motores de buscas entenderem a sua página e fazerem uma melhor indexação dela.

## As três formas de renderização no Next:
    - Client Side ( Chamadas realizadas pelo Client (Browser), ou seja, a forma padrão que fazemos do React)
    - SSR ( Server-Side Rendering | Seria uma forma de toda hora ele realiar a chamada pelo Servidor Node do Next porém retornando o dado dinâmico preparado na hora)
    - SSG ( Static Site Generation | Seria uma forma de ele realizar apenas uma chamada a cada determinada hora e retorna para todos os usuários o mesmo conteúdo até dar esse tempo para ele    realizar a chamada novamente)


## Caminho do SPA/React:

    - Browser ( Client ) => Código React ( Bundle.js ) => HTML => Browser ( Client )


## Caminho Next:

    - Browser ( Client ) => Servidor Next => Código React ( Bundle.js ) => Montagem do HTML => Servidor Next => Browser ( Client )


## Estrutura Next
    - Na pasta pages, cada pasta ( page ), vira uma rota ( File System Root ):
        - quando criarmos um componente novo, sempre devemos fazer ele com export default, o next precisa disso.
        - não precisamos fazer nada para criar a rota para esse componente, basta criarmos ele normal e conseguiremos acessar no browser com /"nomeDoComponente"

## Instalando Typescript em projetos React/Next:
    - yarn add typescript @types/react @types/node -D
    - adicionar "AppProps" na page _app.tsx


## Scoped CSS:
    - Scopped css é nada mais nada menos do que um css escopado para um component só.
    - Para usarmos o Scopped css devemos adicionar um .module.css no nome do arquivo que iremos usar
    - E no componente nós usaremos como um StyleSheet, { className={styles."NomeDaClasse"}}
    - Para usarmos sass, basta darmos um yarn add sass e happy coding!!

## Páginas com _ no nome:
    - A _app é simplesmente o App.jsx do projeto React convencional, ele basicamente recebe o componente do qual o browser precisa para ser renderizado
    - O _document seria basicamente nosso index.html lá na pasta public, ele basicamente vai receber nosso conteúdo html, porém com algumas mudanças na sintaxe,
        - as tags head e html do html serão substituídas pelas tags "Head" e "Html" sendo importada do "next/document"
        - nosso componente precisa ter o nome de "MyDocument" e precisa ser feito em classe e não função, importaremos o Document também de next/document para extender o MyDocument de Document.
        - E instalaremos a fonte dentro da Tag "Head" para que consígamos alterar a font padrão

## Title Dinâmico no Next:
    - O Next tem a funcionalidade do title dinâmico, e para isso funcionar devemos fazer:
        - Adicionar um fragment por volta de todo o componente que quisermos adicionar o title dinamico
        - Import Head de next/head
        - e adicionar o a tag Head e a tag html title dentro da tag Head e pronto, happy coding!!