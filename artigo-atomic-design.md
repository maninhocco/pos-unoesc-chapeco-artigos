####Universidade do Oeste de Santa Catarina – Unoesc
####Pós-Graduação em Desenvolvimento Web, Cloud e Dispositivos Móveis - WebMob
####Disciplina: HTML5+CSS3
####Professor: Jean Carlo Nascimento
####Acadêmico: Marcos Aurélio Pinheiro
###Atomic Design

#####Resumo
Na sociedade do mundo conteporâneo, a utilização de softwares têm tomado cada vez mais espaço na vida das pessoas. Seja trabalho ou lazer, é notória a importância do desses sistemas para a vida social das pessoas. Sendo assim, tornou-se uma carência cada dia mais primordial, e que para suprir tal necessidade,observa-se que uma das técnicas que vem assumindo espaço é denominada de Atomic Design, que trouxe a proposição de átomos, moléculas, organismos, templates e páginas. Assim, a técnica orienta a reutilização da estrutura, a fim de otimizar tempo quando, e se preciso fazer mudanças na interface, pois sugere que a modificação aconteça apenas em um local. #####1. 
O que é?
O método do design atômico é constituída através da criação de componentes reutilizáveis durante a construção de um sistema (web, mobile, etc). Desenvolvida pelo webdesigner Brad Frost, fundamenta-se em conferir da química conceitos elaborados sobre átomos, moléculas e organismos, que associados criam a substância final (ou seja, sistema pronto entregue ao cliente).</br></br>
A metodologia de design atômico é articular, partindo do pressuposto que as páginas são concomitantes elementos "colados" que constroem uma perspectiva final inteira. Brad Frost, baseado em aulas de química,  concluiu que as estruturas de uma página web operam de forma igual aos átomos, moléculas e organismos, constituídos por um grupo de princípios (tags HTML, por exemplo), que podem ser (re)empregados de diversas maneiras e de diversas vezes formando várias páginas web desiguais.
#####2. Como funciona
Consiste em dividir o sistema em cinco partes, conforme descritas abaixo:</br></br>
**2.1 Átomos (atoms)**: são as partes mínimas de cada página, mas que sozinhas não são úteis. Exemplos: inputs, buttons, labels de formulários, etc.</br></br>
**2.2 Moléculas (molecules)**: são agrupamentos de átomos. Nesse ponto, o conteúdo começa a fazer sentido para quem está usando. Exemplo: um label de formulário, um input e um botão, quando agrupados, criam um formulário que pode efetuar alguma operação.</br></br>
**2.3 Organismos (organisms)**: são grupos de moléculas, que formam partes maiores (ou sessões) de uma página. Norteiam a navegação de leitura do conteúdo da interface. A criação de organismos torna possível o reuso de componentes, pois um organismo pode ter moléculas de vários tipos diferentes.</br></br>
**2.4 Modelos (templates)**: são grupos de organismos “costurados” (ou seja, organizados) para formar as páginas. A partir dessa etapa, o cliente já pode visualizar as páginas com funcionalidades dispostas em ação, com o desenho em fase final.</br></br>
**2.5 Páginas (pages)**: são instâncias específicas dos templates. Nessa etapa o conteúdo final é formado para dar uma visão exata do que o usuário acabará por ver. É tipicamente o local aonde a maioria das pessoas envolvidas no projeto do sistema passará o tempo, buscando problemas e/ou melhorias. Se for necessário algum ajuste, deve-se voltar às moléculas, organismos e templates para resolver.</br></br>
Existe uma ferramenta criada juntamente com a técnica do design atômico, chamada Pattern Lab. Esta ferramenta é utilizada para construir a interface, agrupando os átomos, moléculas e organismos. Também serve como biblioteca central para criação/alteração de novos componentes.</br></br>
O Pattern Lab também é utilizado para validar os componentes em vários browsers e também é possível fazer refresh (atualizar) automático a cada mudança em de componente (imagem, css, etc). Um exemplo demonstrativo da biblioteca pode ser encontrado em [http://demo.patternlab.io] (http://demo.patternlab.io).
#####3. Por que usar
*	Esse é o jeito o qual nós já estamos pensando no design e implementação desses elementos, mas talvez não de forma consciente e não de forma tão específica.
*	Os membros do time de desenvolvimento e do cliente conseguem visualizar melhor o sistema de design, sem precisar ver os layouts salvos em frente a eles.
*	O sistema passa a ter maior escalabilidade e coerência enquanto mostra simultaneamente as coisas em seu contexto final. Não existem breakpoints ou devices específicos para montar a interface, e sim elementos que se comportam adequadamente a todos eles.
*	Agilidade na alteração de componentes: como é baseado em componentes, qualquer alteração pode ser feita uma única vez e todos os templates que usam esse componente já estarão alterados.
*	Centralização de informações: ao utilizar o Pattern Lab, o time de desenvolvimento tem em mãos uma biblioteca centralizada com informações de cada componente. Isso torna fácil o acesso às funcionalidades.

#####4. Onde usar
Em projetos de médio a grande porte. Não faz sentido criar toda uma biblioteca (Pattern Lab) centralizada de componentes se o projeto tiver apenas um ou dois templates. A técnica do design atômico mostra seu propósito quando existem vários componentes que serão usados em uma grande quantidade de templates e páginas.</br></br>
Vale destacar que o time precisa ter bastante confiança entre si, pois nem tudo será documentado. Por exemplo: o componente que monta um *header* na página inicial será o mesmo para as demais páginas, não sendo necessário documentar cada parte do *header* em cada template de página.
#####5) Exemplos:

5.1 Átomos:
São os elementos mais simples que sozinhos não teriam significado importante.
```html
<!--Um simples label-->
<label>Apenas um label</label>

<!--Um simples input-->
<input type="button" name="Button" value="Button">
```
5.2 Moléculas:
São combinações de átomos, dando algum sentido à eles.
```html
<form>
	<label>Apenas um label</label>
	<<input type="text" name="busca" value="busca" placeholder="busca">
	<input type="button" name="Button" value="Button">
</form>
```
5.3 Organismos:
São combinações de moléculas, isto já é algo concreto.
```html
<!--Combina as moléculas de busca e navegação-->
<header>
	<img src="logo.png">
	<<nav>
		<ul>
			<li><a href="" title=""></a></li>
			<li><a href="" title=""></a></li>
			<li><a href="" title=""></a></li>
		</ul>
	</nav>
	<div>
		<label>Busca no site</label>
		<input type="button" name="Button" value="Button">
	</div>
</header>
```
5.4 Templates:
Onde a analogia com a química acaba :/ 
Um modelo de página concreta.

![Template](01.jpg)

5.4 Páginas:

Uma página pronta, a visão de algo tangível.

![Página](02.jpg)
#####6. Referências
[http://bradfrost.com/blog/post/atomic-web-design/] (http://bradfrost.com/blog/post/atomic-web-design/)</br>
[http://tableless.com.br/o-que-e-design-atomic/] (http://tableless.com.br/o-que-e-design-atomic/)</br>
[http://patternlab.io/] (http://patternlab.io/)</br>
[http://www.frontendbrasil.com.br/tutoriais/atomic-design-como-funciona/] (http://www.frontendbrasil.com.br/tutoriais/atomic-design-como-funciona/)</br>
[http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/] (http://arquiteturadeinformacao.com/mobile/atomic-design-redesenhando-os-entregaveis-de-designers-e-desenvolvedores/)</br>
