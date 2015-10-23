#### Unoesc Chapecó
#### Pós-graduação em Desenvolvimento Web, Cloud e dispositivos móveis - WebMob
#### Disciplina: HTML5+CSS3
#### Professor: Jean Carlo Nascimento
#### Acadêmico(a): Marcos Aurélio Pinheiro
### Artigo de revisão de CSS3

##### Funcionalidade: **calc()**
##### O que é?
Finalidade incumbida de fazer operações aritméticos simples de modo direto no css.
##### Onde usar:
Qualquer propriedade com valor numérico `(<length>, <frequency>, <angle>, <time>, <number>, or <integer>)`.
##### Como usar:
```css
	[propriedade]: calc([expressão]) 
```
##### Exemplo de uso

```css
	div {
		width: calc(100% - 80px);
	}
```
### Referencia:
[https://developer.mozilla.org/en-US/docs/Web/CSS/calc](https://developer.mozilla.org/en-US/docs/Web/CSS/calc)
[http://tutorialzine.com/2013/10/12-awesome-css3-features-you-can-finally-use/](http://tutorialzine.com/2013/10/12-awesome-css3-features-you-can-finally-use/)

##### Funcionalidade: **gradients**
##### O que é?
Possibilita que os desenvolvedores e designers de web  produzam tranferência mais delicadas dentre as tonalidades de cores, sem ter de recorrer para imagens.
##### Onde usar:
Qualquer propriedade com valor de cor.
##### Como usar:
```css
// gradiente linear:
[propriedade]: linear-gradient([direction<to bottom, to top, to right, to left, to bottom right, etc.>, color-stop1, color-stop2, ...]);
```
##### Exemplo de uso

```css
	div {
		background: linear-gradient(to bottom, blue, white);
	}
```
### Referencia:
[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Images/Using_CSS_gradients)
[http://www.w3schools.com/css/css3_gradients.asp](http://www.w3schools.com/css/css3_gradients.asp)

#####Funcionalidade: Box Shadow
#####O que é?
Esta modificação implanta sombreados em box’s, seja qual for o elemento, desde que seja em uma página html.
#####Onde usar:
Em qualquer elemento.
#####Como usar:
É necessário informar os parâmetros indicando o deslocamento horizontal e vertical da sombra, esfumaçado e cor da sombra.
```css
seletor { propriedade: none|h-shadow v-shadow blur spread color |inset|initial|inherit; }
```
#####Exemplo de uso:
A sintaxe geral para aplicar sombreamento em caixas é mostrada a seguir.
```css
seletor {
    box-shadow: 5px 5px 0 #333;
   -webkit-box-shadow: 5px 5px 0 #333;
   -moz-box-shadow: 5px 5px 0 #333;
}
```
#####Referência:
[http://www.linhadecodigo.com.br/artigo/3633/entendendo-o-atributo-box-shadow-nas-css3.aspx] (http://www.linhadecodigo.com.br/artigo/3633/entendendo-o-atributo-box-shadow-nas-css3.aspx)
[http://www.w3schools.com/cssref/css3_pr_box-shadow.asp] (http://www.w3schools.com/cssref/css3_pr_box-shadow.asp)

##### Funcionalidade: **columns**
##### O que é?
A construção do layout em colunas já faz parte da construção do css. Previamente usavam-se métodos não adequados, até mesmo ao lado servidor para separar o conteúdo em colunas.  Até agora não possui suporte total dos navegadores.
##### Onde usar:
Elementos de container.
##### Como usar:
```css
[seletor] {
	// shorthand
	columns: [auto|column-width column-count|initial|inherit];
	// ou definido as subpropriedades
	column-count: [number|auto|initial|inherit];
	column-fill: [balance|auto|initial|inherit];
	column-gap: [length|normal|initial|inherit];
	column-rule: [column-rule-width column-rule-style column-rule-color|initial|inherit];
	column-rule-color: [color|initial|inherit];
	column-rule-style: [none|hidden|dotted|dashed|solid|double|groove|ridge|inset|outset|initial|inherit];
	column-rule-width: [medium|thin|thick|length|initial|inherit];
	column-span: [1|all|initial|inherit];
	column-width: [auto|length|initial|inherit];
}

```
##### Exemplo de uso

```css
div {
   -webkit-column-width: 100px; /* Chrome, Safari, Opera */
    column-width: 100px;
}
```
### Referencia:
[http://www.w3schools.com/css/css3_multiple_columns.asp](http://www.w3schools.com/css/css3_multiple_columns.asp)
[http://www.w3schools.com/css/css3_multiple_columns.asp](http://www.w3schools.com/css/css3_multiple_columns.asp)

##### Funcionalidade: **web fonts**
##### O que é?
Norma que autoriza o uso de tipografias que não estão instaladas na máquina do usuário.
##### Onde usar:
Todos os elementos html.
##### Como usar:
```css
@font-face {
    font-family: [name]; // nome da fonte
    src: url([url_arquivo_fonte]); //url para o arquivo da fonte.
    font-stretch: [normal|condensed|ultra-condensed|extra-condensed|semi-condensed|expanded|
				   semi-expanded|extra-expanded|ultra-expanded];
	font-style:	 [normal|italic|oblique];
	font-weight: [normal|bold|100|200|300|400|500|600|700|800|900];
	unicode-range:	[unicode-range] // quais caracteres UNICODE a font suporta. 
}
```
##### Exemplo de uso

```css
@font-face {
    font-family: fonteLegal;
    src: url(fonte_legal.ttf);
    font-weight: bold;
}

p { font-family: fonteLegal; }

```
### Referencia:
[http://www.w3schools.com/css/css3_fonts.asp](http://www.w3schools.com/css/css3_fonts.asp)
[http://www.maujor.com/tutorial/css3-@font-face.php](http://www.maujor.com/tutorial/css3-@font-face.php)

##### Funcionalidade: **3D Transforms**
##### O que é?
Possibilita modificar elementos utilizando transformações 3D.
##### Onde usar:
Todos os elementos html. 
##### Como usar:
```css
seletor {
	// rotação
    -webkit-transform: [rotateX([angulo_rotacao]) | rotateY([angulo_rotacao]) | rotateZ([angulo_rotacao])]; /* Chrome, Safari, Opera */
    transform: [rotateX([angulo_rotacao]) | rotateY([angulo_rotacao]) | rotateZ([angulo_rotacao])] ;

    // transformação em perspectiva
    -webkit-perspective: [length|none];
    perspective: [length|none];


}
```
##### Exemplo de uso

```css
div {
	// rotação
    -webkit-transform: rotateY(130deg); /* Safari */
    transform: rotateY(130deg);

    // perspectiva
    -webkit-perspective: 500px; /* Chrome, Safari, Opera */
    perspective: 500px;
}
```
### Referencia:
[http://www.w3schools.com/css/css3_3dtransforms.asp](http://www.w3schools.com/css/css3_3dtransforms.asp)

##### Funcionalidade: **animation**
##### O que é?
É um atributo que possibilita a elaboração de animações com css, eliminando em algumas situações o uso de outra sistema para animar estilos de elementos. 
##### Onde usar:
Todos os elementos html.
##### Como usar:
```css
//definir uma animação: (onde 'name' é o nome da animação)
@keyframes[name] {
	[keyframes-selector(from=0%,to=100%,0-100%)] {
		[css-styles]
	}
}

[classe,id,elemento] {
	animation: [name duration timing-function delay iteration-count direction fill-mode play-state];
	// ou cada sub-propriedade:
	animation-name: [name|none|initial|inherit];
	animation-duration: [time|initial|inherit];
	animation-timing-function: [linear|ease|ease-in|ease-out|cubic-bezier(n,n,n,n)|initial|inherit];
	animation-delay: [time|initial|inherit];
	animation-iteration-count: [number|infinite|initial|inherit];
	animation-direction: [normal|reverse|alternate|alternate-reverse|initial|inherit];
	animation-fill-mode: [none|forwards|backwards|both|initial|inherit];
	animation-play-state: [paused|running|initial|inherit];
}
```
##### Exemplo de uso

```css

@keyframes diagonal-slide {
  from {
    left: 0;
    top: 0;
  }
  to {
    left: 100px;
    top: 100px;
  }
}

div {
  animation-name: diagonal-slide;
  animation-duration: 5s;
  animation-iteration-count: 10;
}

```
### Referencia:
[http://www.w3schools.com/cssref/css3_pr_animation.asp](http://www.w3schools.com/cssref/css3_pr_animation.asp)
[http://www.w3.org/TR/css3-animations/#animation](http://www.w3.org/TR/css3-animations/#animation)

##### Funcionalidade: **text-overflow**
##### O que é?
Identifica a forma que um conteúdo que tenha excedido sua dimensão deve ser exposto(cortado, com reticências.)
##### Onde usar:
Todos os elementos html. 
##### Como usar:
```css
seletor {
    text-overflow: [clip|ellipsis|string|initial|inherit];
}
```
##### Exemplo de uso

```css
// o texto presente nesta div mostrará reticencias no final se o tamanho do conteúdo for maior que seu tamanho.
div {
     text-overflow: ellipsis; 
}
```
### Referencia:
[http://www.w3schools.com/cssref/css3_pr_text-overflow.asp](http://www.w3schools.com/cssref/css3_pr_text-overflow.asp)

#####Funcionalidade: Cores RGBA
#####O que é?
Esta ferramenta RGBA têm o objetivo de delimitar as cores e transparência através do uso de valores RGB (sistema de cores formado por **R**ed, **G**reen e **B**lue).
#####Onde usar:
Em qualquer elemento que possui propriedades de cor. Exemplos: color, background, border-color, etc.
#####Como usar:
```css
seletor { propriedade: rgba(R, G, B, A); }
```
#####Exemplo de uso:
A sintaxe geral para aplicar cores e transparência RGB é mostrada a seguir.
```css
seletor { 
      background: rgba(0, 0, 0, 1);
}
```
#####Referência:
[http://www.maujor.com/tutorial/interativo-css3/inc/rgba.php] (http://www.maujor.com/tutorial/interativo-css3/inc/rgba.php)

##### Funcionalidade: **novos seletores por atributo**
##### O que é?
Além de outros seletores adicionados, este viabiliza eleger elementos apoiado nos seus atributos. 
##### Onde usar:
Todos os elementos html.
##### Como usar:
```css
	[elemento][attr^=val] // todos os elementos com atributo 'attr' e valor iniciando em 'val'
	[elemento][attr$=val] // todos os elementos com atributo 'attr' e valor terminando em 'val'
	[elemento][attr*=val] // todos os elementos com atributo 'attr' e valor contendo em 'val'
```
##### Exemplo de uso

```css
	//selecionando todas as imagens com a extensão jpg.
	img[src$=".jpg"]  {
		...
	}
```
### Referencia:
[http://www.w3schools.com/cssref/css_selectors.asp](http://www.w3schools.com/cssref/css_selectors.asp)
