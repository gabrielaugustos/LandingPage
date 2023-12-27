![image](https://github.com/gabrielaugustos/LandingPage/assets/101292040/22e61935-c04e-4ffa-82b3-7de8643a06c4)


Primeiramente iremos construir todo o nosso HTML, posteriormente implementaremos o CSS.

- HTML
    
    O projeto HTML será dividido em 3 partes principais: o `header`, o `main` e o `footer`.
    
    Inicialmente teremos o cabeçalho, que é a tag `header` contendo toda a barra com a logo, o texto com o nome das páginas, e o github.
    
    Como ela será nossa barra de navegação então faremos uma implementação `nav` que terá um `span` com o titulo da página: BalleCoffe.
    
    Para o nome das páginas faremos uma lista de elementos não ordenados, com a tag `ul`. Para essas páginas teremos um link, com a tag `a`.
    
    Para o link do github faremos apenas uma âncora, com a tag `a`.
    
    Então a nossa `header` estará assim:
    
    ```html
    <header>
            <nav>
                <span>BalleCoffe</span>
                <ul>
                    <li><a href="">Home</a></li>
                    <li><a href="">Receitas</a></li>
                    <li><a href="">Novidades</a></li>
                    <li><a href="">Melhor Avaliados</a></li>
                </ul>
            </nav>
    </header>
    ```
    
    Feito isso vamos implementar a nossa `main`, ela está separada em duas seções `section`: a hero, que é a parte apresentável da página (ela é importante para saber se o usuário irá ou não ficar na página); e teremos a seção do conteúdo de fato, com as receitas.
    
    Então começaremos pelo hero, que também será dividido em duas partes: uma com o cabeçalho do hero (parte escrita) e a outra com as imagens.
    
    Para nossa hero faremos uma tag `header` dentro da `section`, com o conteúdo da hero. Podemos observar que temos uma linha separando o título do restante do conteúdo, para este título poderíamos usar uma imagem, mas utilizaremos a tag `hr/`.
    
    Para nossas imagens faremos uma tag `div` dentro da `section`, a qual teremos uma `figure` e dentro dela teremos a nossa tag `img` com o caminho da imagem.
    
    ```html
    <main>
            <section>
                <header>
                    <span>Novidade</span>
                    <h1>Encontre a receita perfeita!</h1>
                    <hr/>
                    <h2>Explore dezenas de variações da bebida favorita entre os devs ao redor mundo!</h2>
                </header>
                <div>
                    <figure> <img src="assets/image-1.png"/></figure>
                    <figure> <img src="assets/image-2.png"/></figure>
                    <figure> <img src="assets/image-3.png"/></figure>
                    <figure> <img src="assets/image-10.png"/></figure>
                    <figure> <img src="assets/image-11.png"/></figure>
                    <figure> <img src="assets/image-12.png"/></figure>
                    <figure> <img src="assets/image-13.png"/></figure>
                    <figure> <img src="assets/image-14.png"/></figure>
                    <figure> <img src="assets/image-15.png"/></figure>
                    <figure> <img src="assets/image-16.png"/></figure>
                    <figure> <img src="assets/image-17.png"/></figure>
                    <figure> <img src="assets/image-18.png"/></figure>
                </div>
            </section>
    ```
    
    Temos um botão que separa a hero e o conteúdo. Adicionaremos mais uma `section`, entre os dois, que terá um `button` com uma `img`.
    
    ```html
    <section>
    		<button>
    				<img src="assets/button.svg"/>
    		</button>
    </section>
    ```
    
    Por fim, vamos implementar nossa última `section`, que a do conteúdo. Ela tem um cabeçalho `header`, dentro desse cabeçalho tem um `span`, um `h2`, e um parágrafo `p`.
    
    Teremos 4 cards, que serão separados por `div`. Eles tem um cabeçalho com um `span` e um `h3` que colocaremos dentro de uma `div` para separar o conteúdo do cabeçalho pois teremos um parágrafo também no cabeçalho. Saindo do cabeçalho teremos um parágrafo. Ainda dentro da primeira `div` teremos uma outra `div` para separar as informações do autor, com imagem e nome. Este será o procedimento para os outros 3 cards restantes.
    
    ```html
    <section>
                <header>
                    <span>Receitas</span>
                    <h2>Confira as ultimas receitas</h2>
                    <p>Dê uma olhada nas receitas mais amadas!</p>
                </header>
                <div>
                    <div>
                        <header>
                            <div>
                                <span>Em alta 🔥</span>
                                <h3>Cappuccino</h3>
                            </div>
                            <p>Extraordinário · 4/4</p>
                        </header>
                        <p>Uma bebida ideal para os amantes de doce e cremosidade. 😍</p>
                        <div>
                            <img src="https://avatars.githubusercontent.com/u/101292040?v=4"/>
                            <span>Gabriel Augusto</span>
                        </div>
                    </div>
                </div>
            </section>
    ```
    
    Agora faremos nosso rodapé o `footer`, que terá somente dois parágrafos. Usamos o comando `&lt;` para simbolizar o menor que (<) e o comando `&gt;` para simbolizar o maior que (>).
    
    ```html
    <footer>
    		<p>Copyright &lt;CODEFEE /&gt; 2023</p>
    		<p>Feito com muito ❤ e café por Rafaella Ballerini</p>
    </footer>
    ```
    
    Nosso HTML está finalizado, vamos fazer a parte do CSS.
    
- CSS
    
    Agora vamos implementar o CSS. 
    
    Inicialmente faremos o *import* de nossa fonte, que virá do google fonts. 
    
    `@import url('https://fonts.googleapis.com/css2?family=**Inter:wght@400;500**&family=**Teko:wght@600**&display=swap');`
    
    A primeira implementação que faremos será resetar algumas configurações padrão. Como o `margin`, `padding` e o `box-sizing`.
    
    Com `box-sizing: border-box`, q**uando definido como border-box, a largura do elemento na página permanece estática, com a borda e o preenchimento ocupando espaço *dentro* do elemento.**
    
    ```css
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    ```
    
    Iremos resetar nossa tag âncora, a fim de que seja somente texto
    
    ```css
    a {
        text-decoration: none;
    }
    ```
    
    Também iremos resetar a configuração padrão para lista, a tag `ul`, para que não esteja pontuada.
    
    ```css
    ul {
        list-style: none;
    }
    ```
    
    Faremos agora nossa tag `body` que pega toda a estrutura do HTML. Nela teremos nosso `background`, cor de fundo. Teremos nossa `color`, cor das letras.
    
    ```css
    body {
        background: #1F1517;
        color: #FFFFFF;
    }
    ```
    
    Vamos colocar por padrão do HTML a fonte Inter
    
    ```css
    html {
        font-family: Inter, sans-serif;
        font-weight: 500;
    }
    ```
    
    Feito todo o reset, agora vamos adentrar de fato na nossa implementação.
    
    Ao invés de trabalharmos somente com pixels (px), utilizaremos em alguns momentos a unidade de medida *rem*.
    
    Inicialmente faremos na tag `nav` mantendo uma largura máxima de 1120 pixels da viewport. Terá uma `margin` definida como `auto`. 
    
    Vamos definir o `padding` que terá 1.5rem (em cima e em baixo) e 10 rem (nas laterais).
    
    Para colocarmos nossos elementos em posições específicas, vamos utilizar o Flexbox.
    
    Então vamos colocar primeiramente um `display:flex`. Um `flex-direction:row`, ou seja, na horizontal.
    
    Vamos colocar um `justify-content: space-between;`, é a separação dos conteúdos. Com o *space-between* separamos os três conjuntos de elementos (logo, menu e github), criando um espaço entre os elementos.
    
    Ao fazermos um `align-items: center;` eles ficarão alinhados no eixo central.
    
    ```css
    nav {
        max-width: 1120px;
        margin: auto;
        padding: 1.5rem 10rem;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }
    ```
    
    Vamos definir uma classe para o título, que é a logo. Vamos estilizar a fonte, definir o tamanho e principalmente colocar em maiúscula (ao definir com maiúscula diretamente no html, pode ser que o leitor de tela interprete de forma errada).
    
    ```css
    .logo {
        font-family: Teko;
        font-size: 2rem;
        font-weight: 600;
        text-transform: uppercase;
    }
    ```
    
    Para o menu com os links, temos que deixa-los dispostos na horizontal, usaremos o `display: flex;` e faremos um `flex-direction: row;`.
    
    Para fazermos o espaçamento entre eles faremos um `gap: 1.5rem;`.
    
    ```css
    .menu {
        display: flex;
        flex-direction: row;
        gap: 1.5rem;
        color: #FFF2E780;  
    }
    ```
    
    No github também mudaremos a cor e o tamanho da fonte.
    
    ```css
    .github {
        color: #FFF2E7;
        font-weight: 600;
    }
    ```
    
    Agora que já fizemos toda a estilização do `header`, vamos trabalhar no nosso `main`.
    
    Como as seções estão dispostas na vertical vamos fazer um `flex-direction: column;`.
    
    ```css
    main {
        display: flex;
        flex-direction: column;
    }
    ```
    
    Nossa primeira `section` é a hero. Ela terá uma div chamada principal, a qual tem uma cor de fundo um pouco diferente, um tom mais escuro. Terá uma largura máxima de 1120px e uma altura, mas essa altura terá uma unidade de medida o vh, que é o tamanho da viewport (da tela). Terá um `display: flex;` e faremos um `flex-direction: row;`, para alinharmos na horizontal e teremos um `justify-content: space-between;` e um `gap: 6rem;` para que haja um espaço entre os elementos.
    
    ```css
    .principal {
        background-color: #181012;
    }
    
    .hero {
        max-width: 1120px;
        height: 60vh;
    
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        gap: 6rem;
    }
    ```
    
    Faremos uma classe, chamada *hero-conteudo* especificaremos a header do *main*.
    
    Precisamos alinhar os elementos dispostos em coluna, com um `gap:1rem;` entre eles.
    
    ```css
    .hero-conteudo {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    ```
    
    E teremos nossa div *hero-images-container* que terá nossas figuras. Nela nossas imagens ocuparão no máximo 45% da tela em que estão dispostas, terá 4 colunas de imagens e um gap entre essas imagens.
    
    ```css
    .hero-images-container {
        max-width: 45%;
        column-count: 4;
        column-gap: 1rem;
        margin: -1rem;
    }
    ```
    
    Para estilizarmos as imagens, vamos fazer uma abordagem em que mencionamos uma tag que fica dentro de uma outra tag com classe, no caso o elemento *img* dentro de *figure* que fica dentro de um elemento que tenha a classe *hero-images-container*. 
    
    Teremos um `width: 100%;`, um `border-radius: 0.5rem;`
    
    ```css
    .hero-images-container>figure>img {
        width: 100%;
        border-radius: 0.5rem;
    }
    ```
    
    Podemos observar que nossas imagens estão saindo do container em que elas estão. Então, voltaremos na hero e colocaremos a propriedade `overflow: clip;` que fará com que as imagens estejam nos limites da container em que elas estão.
    
    Então, vamos agora personalizar a parte do conteúdo, para isso criaremos a classe para o *span*, chamada de *destaque*. 
    
    ```css
    .destaque {
        font-family: Epilogue;
        font-size: 1rem;
        font-weight: 500;
        text-transform: uppercase;
    }
    ```
    
    No entanto, teremos vários spans que terão as mesmas propriedades variando somente na cor, então podemos usar essa mesma classe destaque para evitar duplicação de código. O que faremos de diferente em cada uma delas é criar uma segunda classe apenas com o nome da cor. Por exemplo:
    
    ```html
    <header class="hero-conteudo">
    		<span class="destaque marrom">Novidade</span>
    ```
    
    Então, colocaremos a nossa cor como marrom
    
    ```css
    .marrom {
        color: #A45A49;
    }
    ```
    
    Agora, vamos implementar o nosso h1
    
    ```css
    h1 {
        font-family: Montserrat;
        font-size: 3.5rem;
        font-weight: 800;
    }
    ```
    
    Feito isso, vamos estilizar o nosso *hr*
    
    ```css
    hr{
        border-color: #A45A49;
    }
    ```
    
    Faremos também uma nova classe para o h2 que contém nosso subtítulo, chamaremos de *hero-subtitulo*
    
    ```css
    .hero-subtitulo {
        color: #C7BAB3;
        font-family: Inter;
        font-size: 1.5rem;
        font-weight: 400;
    }
    ```
    
    Agora, para que os elementos fiquem todos centralizados, voltaremos no nossa classe hero e faremos um `align-items: center;`.
    
    Pronto, nossa primeira section está pronta. Agora, vamos estilizar nossa section que contém nosso botão.
    
    Para isso faremos uma classe *botao-container*.
    
    ```css
    .botao-container{
        width: 100%;
        max-width: 1120px;
        margin: auto;
        transform: translate("0, -50%");
    }
    ```
    
    No botão tiraremos a borda, definiremos um padding de 1 rem e um border-radius.
    
    ```css
    button {
        border: none;
        padding: 1rem;
        border-radius: 0.5rem;
        background: #A45A49;
    }
    ```
    
    Pronto, finalizamos a section do botão. Agora, faremos nossa última section com a parte das receitas.
    
    ```css
    .receitas {
        display: flex;
        flex-direction: column;
    
        max-width: 1120px;
        padding: 3rem 2rem;
        margin: auto;
    }
    ```
    
    No header criaremos uma classe *receitas-cabecalho*
    
    ```css
    .receitas-cabecalho {
        display: flex;
        flex-direction: column;
    
        gap: 0.5rem;
    }
    ```
    
    Agora, temos que editar cada um desses elementos, para isso, no span, vamos criar a classe *destaque* também com a segunda classe *marrom*.
    
    Teremos uma classe para nosso titulo das receitas
    
    ```css
    .receitas-titulo {
        font-family: Montserrat;
        font-size: 32px;
        font-weight: 700;
        color: #FFF2E7;
    }
    ```
    
    Teremos a nossa classe *receitas-subtitulo* para nosso parágrafo *p*.
    
    ```css
    .receitas-subtitulo {
        color: #C7BAB3;
        font-family: Inter;
        font-size: 1rem;
        font-weight: 400;
    }
    ```
    
    Agora, vamos estilizar nossos cards. Primeiramente faremos nosso padding. O *flex-direction* como *row*, porque primeiro colocaremos tudo na horizontal e depois quebraremos os nossos cards com a propriedade `flex-wrap: wrap;`
    
    ```css
    .receitas-card-container {
        padding: 0rem 10rem;
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 2rem;
    }
    ```
    
    Feito isso, vamos estilizar os nossos cards de fato. Essa div é separada pelo *header*, pela descrição e nossa imagem do autor. Então, podemos fazer um `display:flex` para agrupar essas três coisas.
    
    ```css
    .receitas-card {
        background: #241A1C;
        padding: 2rem;
        border-radius: 0.5rem;
        display: flex;
        flex-direction: column;
        gap: 2rem;
        flex-basis: 29rem;
    }
    ```
    
    Agora, nossa header *receitas-card-cabecalho* será disposta na horizontal e alinhada ao fim do conteúdo, com um espaço entre eles.
    
    ```css
    .receitas-card-cabecalho-detalhes {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
    }
    ```
    
    Nosso span terá a classe *destaque* porém dessa vez ela será amarela.
    
    O titulo também terá uma classe *receita-titulo*
    
    ```css
    .receita-titulo {
        color: #FFF2E7;
        font-family: Montserrat;
        font-size: 1.5rem;
        font-weight: 700;
    }
    ```
    
    Também teremos a parte das avaliações, que é o parágrafo p. 
    
    ```css
    .receita-avaliacao {
        color: #756A67;
        font-family: Inter;
        font-size: 1rem;
        font-weight: 500;
    }
    ```
    
    E termos nossa descrição
    
    ```css
    .receita-descricao {
        color: #C7BAB3;
        font-family: Inter;
        font-size: 1rem;
        font-weight: 400;
    }
    ```
    
    Feito tudo isso, agora precisamos estilizar a parte do autor, com a imagem e o nome.
    
    Primeiramente, criaremos uma classe que será *receita-autor* e faremos um *display* para agrupar os dois na horizontal, alinhados ao centro com um espaço entre eles
    
    ```css
    .receita-autor {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 0.5rem;
    }
    ```
    
    A imagem será implementada da seguinte forma
    
    ```css
    .receita-autor>img {
        border-radius: 20rem;
        width: 1.5rem;
    }
    ```
    
    E o nome de autor
