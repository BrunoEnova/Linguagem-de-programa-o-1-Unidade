


# Linguagem de programação 1 Unidade

## **O que é linguagem de programação ?**

As linguagens de programação são sistemas estruturados de comunicação com computadores, permitindo a criação de softwares, aplicativos e sistemas automatizados. No contexto atual, dominá-las é essencial para inovação, automação de processos e desenvolvimento de soluções tecnológicas personalizadas.

## **Por que aprender programação hoje?**

- **Inovação e criatividade**: permite transformar ideias em soluções digitais, como aplicativos, jogos e automações.
- **Automação e eficiência**: automatiza tarefas repetitivas, reduz erros e aumenta produtividade em empresas e no cotidiano.
- **Soluções personalizadas**: cria ferramentas sob medida para cada necessidade, desde sistemas de vendas até plataformas de ensino.
- **Segurança**: protege dados e cria sistemas robustos frente a ameaças digitais.
- **Mercado de trabalho**: profissionais que sabem programar têm alta demanda e melhores oportunidades de carreira.

## **JavaScript: Origem e Ambientes de Execução**

Criado por Brendan Eich em 1995 para o navegador Netscape, o JavaScript surgiu como uma linguagem de script para tornar páginas web dinâmicas. Hoje, é executado em:

- **Navegadores**: Manipula elementos HTML/CSS, interage com APIs e valida formulários (ex.: `document.getElementById()`).
- **Node.js**: Ambiente server-side para construir servidores, APIs e aplicações de back-end (ex.: `http.createServer()`).

## **Variáveis em JavaScript**

Variáveis são espaços na memória para armazenar dados temporários (números, textos, objetos etc.).
Declaração:

```javascript
var idade = 25;     // escopo global ou de função
let nome = "Ana";   // escopo de bloco
const PI = 3.14;    // valor constante, não pode ser alterado
```

- **var**: pode ser redeclarada e reatribuída, sofre hoisting (é “elevada” para o topo do bloco de código).
- **let**: pode ser reatribuída, mas não redeclarada no mesmo bloco de código, mais segura para evitar conflitos.
- **const**: deve ser inicializada na declaração, não pode ser reatribuída nem redeclarada, usada para valores fixos.

---

## **Estruturas condicionais**

Permitem tomar decisões no código de acordo com condições.

### **Simples**

```javascript
if (idade >= 18) {
  console.log("Maior de idade");
}
```


### **Composta**

```javascript
if (saldo <= 100) {
  console.log("Compra aprovada");
} else {
  console.log("Saldo insuficiente");
}
```


### **Aninhada**

```javascript
if (nota >= 7) {
  console.log("Aprovado");
} else if (nota >= 5) {
  console.log("Recuperação");
} else {
  console.log("Reprovado");
}
```

Condicionais aninhadas são úteis para múltiplos caminhos de decisão.

### **Switch**

```javascript
let dia = 3;
switch (dia) {
  case 1: console.log("Domingo"); break;
  case 2: console.log("Segunda"); break;
  case 3: console.log("Terça"); break;
  default: console.log("Dia inválido");
}
```

O switch é ideal para comparar uma variável com vários valores possíveis, como menus, dias da semana, etc.

---

## **Operadores em JavaScript**

### **Aritméticos**

- `+` (adição),
- `-` (subtração),
- `*` (multiplicação),
- `/` (divisão),
- `%` (divisão de resto),
- `**` (exponenciação),
- `++` (incremento),
- `--` (decremento).
- **Exemplo**: calcular desconto, somar itens de um carrinho, atualizar pontuação.


### **Atribuição**

- `=` (atribuição)
- **Exemplo**: `var total = 10` atribuir o valor 10 ao total.


### **Comparação (relacionais)**

- `==` (igualdade),
- `!=` (diferente),
- `===` (igualdade estrita),
- `!==` (diferença estrita),
- `>` (maior que),
- `<` (menor que),
- `>=` (maior ou igual),
- `<=` (menor ou igual),
- **Exemplo**: validar senha, comparar idades, filtrar produtos por preço.


### **Lógicos**

- `&&` (E): todas as condições devem ser verdadeiras.
- `||` (OU): pelo menos uma condição precisa ser verdadeira.
- `!` (NÃO): inverte o valor booleano[^10][^20].
- **Exemplo**: liberar acesso só para maiores de idade com cadastro ativo (`idade &gt;= 18 &amp;&amp; ativo`).


### **Ternário**

- Sintaxe: `condição ? valorSeVerdadeiro : valorSeFalso`
- **Exemplo**:

```javascript
let status = idade >= 18 ? "Adulto" : "Menor";
```


### **De uso prático**

- **Matemáticos**: calcular notas, médias, descontos.
- **Relacionais**: decidir se um aluno passou, se um produto está disponível.
- **Lógicos**: validar múltiplos critérios de acesso, filtrar dados em sistemas.
- 


## Precedência dos Operadores em JavaScript

A precedência dos operadores determina a ordem em que as operações são realizadas em uma expressão. Operadores com maior precedência são avaliados antes dos de menor precedência. Isso é fundamental para evitar erros e garantir que as expressões sejam interpretadas corretamente pelo JavaScript.

### Ordem de Precedência

| Prioridade | Operadores | Descrição |
| :-- | :-- | :-- |
| 1 | `()` | Parênteses (forçam avaliação) |
| 2 | `!` | Operador lógico NOT |
| 3 | `**` | Exponenciação |
| 4 | `*`, `/`, `%` | Multiplicação, divisão, módulo |
| 5 | `+`, `-` | Adição e subtração |
| 6 | `>`, `>=`, `<`, `<=` | Operadores relacionais |
| 7 | `==`, `!=`, `===`, `!==` | Igualdade e diferença |
| 8 | `&&` | Operador lógico E |
| 9 | `\|\|`  | Operador lógico OU |


---

### Exemplos Práticos

#### 1. **Atribuição**

- `=` (atribuição): atribui valor a uma variável.

```javascript
var total = 10; // total recebe 10
```


#### 2. **Comparação (Relacionais)**

- `==`, `!=`, `===`, `!==`, `>`, `<`, `>=`, `<=`

```javascript
let idade = 18;
console.log(idade == "18");   // true  (valor igual, tipo ignorado)
console.log(idade === "18");  // false (valor igual, tipo diferente)
console.log(idade > 16);      // true
console.log(idade <= 17);     // false
```


#### 3. **Lógicos**

- `&&` (E): todas as condições devem ser verdadeiras.
- `||` (OU): ao menos uma condição deve ser verdadeira.
- `!` (NÃO): inverte o valor booleano.

```javascript
let maiorDeIdade = idade >= 18;
let ativo = true;
console.log(maiorDeIdade && ativo); // true
console.log(maiorDeIdade || false); // true
console.log(!ativo);                // false
```


#### 4. **Ternário**

- Sintaxe: `condição ? valorSeVerdadeiro : valorSeFalso`

```javascript
let status = idade >= 18 ? "Adulto" : "Menor"; // "Adulto"
```


---

### Como a Precedência Afeta o Resultado

#### Sem Parênteses:

```javascript
let resultado = 3 + 4 * 2; // Multiplicação primeiro: 3 + 8 = 11
```


#### Com Parênteses:

```javascript
let resultado2 = (3 + 4) * 2; // Soma primeiro: 7 * 2 = 14
```


#### Operador NOT com E Lógico:

```javascript
let a = true;
let b = false;
console.log(!a && b); // !a é false, então false && false = false
```


#### Operador Ternário após Lógicos:

```javascript
let idade = 20;
let status = idade >= 18 ? "Adulto" : "Menor"; // condição avaliada antes do ?
```


#### Atribuição é a Última:

```javascript
let x = 10 + 5 * 2; // 5*2 = 10, 10+10 = 20, depois atribui a x
```

### Resumo

- Sempre que necessário, use parênteses para garantir a ordem desejada.
- Multiplicação, divisão e módulo vêm antes de adição e subtração.
- Comparações vêm antes dos operadores lógicos (`&&`, `||`).
- O operador ternário é avaliado depois dos lógicos.
- Atribuição é sempre a última operação na expressão.

Essas regras ajudam a evitar ambiguidades e bugs em expressões mais complexas.

---

## **Estruturas de repetição**

Permitem executar um bloco de código várias vezes.

### **while**

Executa enquanto a condição for verdadeira:

```javascript
let i = 0;
while (i &lt; 3) {
  console.log(i);
  i++;
}
```

Usado quando não se sabe quantas vezes será necessário repetir[^11].

### **do...while**

Garante ao menos uma execução:

```javascript
let senha;
do {
  senha = prompt("Digite a senha:");
} while (senha !== "1234");
```

Útil para validação de entrada de usuário[^12].

### **for**

Estrutura mais usada, especialmente quando se sabe o número de repetições:

```javascript
for (let i = 0; i < 5; i++) {
  console.log(i); // 0 a 4
}
```



## **4. Objeto Literal: Funcionalidades Básicas**

Objetos literais são estruturas que armazenam dados e funcionalidades relacionadas.

### **Propriedades e Métodos**

```javascript
const pessoa = {
  nome: "Ana", // propriedade
  idade: 30,
  cumprimentar: function() { // método
    return `Olá`;
  }
};
console.log(pessoa.cumprimentar()); // "Olá"
```


### **Atualização Dinâmica**

```javascript
pessoa.profissao = "Engenheira"; // Adiciona nova propriedade
delete pessoa.idade; // Remove propriedade
```


### **Shorthand Notation**

```javascript
const nome = "Carlos";
const idade = 25;
const usuario = { nome, idade }; // { nome: "Carlos", idade: 25 }
```


### **Métodos Simplificados**

```javascript
const calculadora = {
  somar(a, b) { // Sintaxe simplificada
    return a + b;
  }
};
console.log(calculadora.somar(2,3)); // 5
```

Este material cobre desde os conceitos básicos até exemplos práticos, preparando você para aplicar JavaScript em situações do mundo real.

<div style="text-align: center">⁂</div>

[^1]: https://universidadedatecnologia.com.br/o-que-e-linguagem-de-programacao/

[^2]: https://pt.linkedin.com/pulse/importância-das-linguagens-de-programação-mundo-moderno-kelly-costa-zsrpf

[^3]: https://developer.mozilla.org/pt-BR/docs/Glossary/JavaScript

[^4]: https://clauboaventura.com.br/historia-da-linguagem-java-script/

[^5]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Grammar_and_types

[^6]: https://cursos.alura.com.br/forum/topico-diferencas-const-let-e-var-200251

[^7]: https://www.treinaweb.com.br/blog/estruturas-condicionais-e-estruturas-de-repeticao-em-javascript

[^8]: https://awari.com.br/javascript-switch-case-tomando-decisoes-com-switch-case-em-javascript/

[^9]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Expressions_and_operators

[^10]: https://awari.com.br/operadores-logicos-em-javascript-guia-completo-para-iniciantes/

[^11]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Loops_and_iteration

[^12]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/do...while

[^13]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Working_with_objects

[^14]: https://blog.rocketseat.com.br/javascript-entendendo-objetos-propriedades-e-metodos/

[^15]: https://rockcontent.com/br/blog/linguagem-de-programacao/

[^16]: https://www.dio.me/articles/a-importancia-da-programacao-nos-dias-atuais

[^17]: https://www.azion.com/pt-br/blog/a-historia-do-javascript/

[^18]: https://www.devmedia.com.br/javascript-variaveis-e-constantes/41012

[^19]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/if...else

[^20]: https://www.dio.me/articles/desvendando-os-operadores-em-javascript-potencialize-seu-codigo

[^21]: https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/Scripting/Object_basics

[^22]: https://www.lenovo.com/br/pt/glossary/programming-language/

[^23]: https://www.dio.me/articles/variaveis-javascript

[^24]: https://rocketseat.com.br/blog/artigos/post/estruturas-condicionais-javascript

[^25]: https://blog.rocketseat.com.br/loops-em-javascript-um-guia-basico-para-iniciantes/

[^26]: https://tableless.github.io/iniciantes/manual/js/objetos.html

[^27]: https://pt.wikipedia.org/wiki/Linguagem_de_programa%C3%A7%C3%A3o

[^28]: https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/Scripting/Variables

[^29]: https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/Scripting/Conditionals

[^30]: https://fia.com.br/blog/linguagem-de-programacao/

[^31]: https://www.alura.com.br/artigos/linguagem-programacao

[^32]: https://www.dio.me/articles/a-importancia-de-aprender-uma-linguagem-de-programacao-para-o-futuro

[^33]: https://www.godaddy.com/resources/br/artigos/voce-sabe-o-que-e-linguagem-de-programacao

[^34]: https://canaltech.com.br/mercado/a-importancia-da-linguagem-de-programacao-c-na-evolucao-da-computacao-214210/

[^35]: https://pm3.com.br/blog/programacao-basica-o-que-e-principais-conceitos-e-linguagens/

[^36]: https://idocode.com.br/blog/programacao/o-que-e-programacao/

[^37]: https://hub.asimov.academy/blog/linguagem-de-programacao-o-que-e/

[^38]: https://napratica.org.br/linguagem-de-programacao/

[^39]: https://geosemfronteiras.org/blog/como-se-produz-uma-linguagem-de-programacao-quais-sao-as-mais-populares-hoje-em-dia/

[^40]: https://esr.rnp.br/desenvolvimento-de-sistemas/a-importancia-da-programacao-para-o-futuro-do-trabalho/

[^41]: https://www.hostinger.com.br/tutoriais/linguagens-de-programacao-mais-usadas

[^42]: https://www.fundacaotelefonicavivo.org.br/noticias/linguagem-programacao-mercado-trabalho/

[^43]: https://www.resilia.com.br/blog/javascript-o-que-e-como-surgiu-e-onde-utilizar/

[^44]: https://pt.wikipedia.org/wiki/JavaScript

[^45]: https://www.locaweb.com.br/blog/temas/codigo-aberto/evolucao-do-javascript/

[^46]: https://www.youtube.com/watch?v=k8SAA979zAk

[^47]: https://support.microsoft.com/pt-br/topic/como-habilitar-o-javascript-no-windows-88d27b37-6484-7fc0-17df-872f65168279

[^48]: https://www.w3schools.com/nodejs/nodejs_intro.asp

[^49]: https://www.cpt.com.br/cursos-informatica-desenvolvimentodesoftwares/artigos/linguagem-de-programacao-javascript-um-breve-historico

[^50]: https://caffeinealgorithm.com/blog/configuracao-de-ambiente-em-javascript

[^51]: https://www.treinaweb.com.br/blog/trabalhando-com-javascript-no-navegador

[^52]: https://nodejs.org/en

[^53]: https://www.youtube.com/watch?v=uf9uTUC4Qqs

[^54]: https://www.alura.com.br/artigos/node-js

[^55]: https://www.dio.me/articles/var-let-const-qual-usar

[^56]: https://tableless.github.io/iniciantes/manual/js/variaveis.html

[^57]: https://www.youtube.com/watch?v=nsqf51K-xVc

[^58]: https://www.dio.me/articles/const-let-e-var-em-javascript-qual-a-melhor-escolha

[^59]: https://blog.lsantos.dev/mas-praticas-javascript/

[^60]: https://dev.to/rodrigozan/introducao-ao-javascript-variaveis-tipos-de-dados-e-operadores-2fpd

[^61]: https://www.freecodecamp.org/portuguese/news/var-let-e-const-qual-e-a-diferenca/

[^62]: https://www.dio.me/articles/sintaxe-basica-em-javascript-variaveis-vetores-objetos-estruturas-condicionais-e-funcoes

[^63]: https://www.covildodev.com.br/article/variaveis-javascript

[^64]: https://pt.stackoverflow.com/questions/206117/var-const-ou-let-qual-usar

[^65]: https://vivendodeprogramacao.com.br/aprendendo-variaveis-e-tipos-dados-com-javascript

[^66]: https://www.youtube.com/watch?v=ZsSKPpUOvO8

[^67]: https://ebaconline.com.br/blog/if-em-javascript-seo

[^68]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/switch

[^69]: https://www.devmedia.com.br/javascript-estrutura-condicional-if/40611

[^70]: https://www.youtube.com/watch?v=2u3W6jycNto

[^71]: https://www.homehost.com.br/blog/javascript/switch-javascript/

[^72]: https://www.hashtagtreinamentos.com/como-usar-condicionais-em-javascript

[^73]: https://www.ibm.com/docs/pt-br/cics-ts/5.6?topic=instructions-nested-ifthenelse

[^74]: https://www.hashtagtreinamentos.com/switch-case-em-javascript

[^75]: https://www.youtube.com/watch?v=TXOOSaMF2R8

[^76]: https://pt.stackoverflow.com/questions/21992/desempenho-em-javascript-switch-ou-if-aninhado

[^77]: https://www.devmedia.com.br/javascript-switch/39761

[^78]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Data_structures

[^79]: https://www.escoladnc.com.br/blog/operadores-aritmeticos-em-javascript-guia-completo/

[^80]: https://www.youtube.com/watch?v=5ESHpHXFa4M

[^81]: https://caffeinealgorithm.com/blog/operadores-aritmeticos-em-javascript

[^82]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators

[^83]: https://blog.betrybe.com/desenvolvimento-web/operadores-logicos-javascript/

[^84]: https://www.youtube.com/watch?v=LXjhhENoeMk

[^85]: https://www.youtube.com/watch?v=vOrtQOSa9WY

[^86]: https://www.youtube.com/watch?v=tSJVntWx3RY

[^87]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Operator_precedence

[^88]: https://dev.to/joaopedrov0/4-operadores-entendendo-o-javascript-20hm

[^89]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Logical_AND

[^90]: http://www.nce.ufrj.br/ginape/js/conteudo/variaveis/operadores.htm

[^91]: https://www.devmedia.com.br/curso/javascript-estruturas-de-repeticao/2396

[^92]: https://developer.mozilla.org/pt-BR/docs/Web/HTML/Element/em

[^93]: https://www.youtube.com/watch?v=SYMxV4HM224

[^94]: https://www.devmedia.com.br/javascript-while-e-do-while/41015

[^95]: https://docs.pipz.com/central-de-ajuda/learning-center/guia-basico-de-markdown

[^96]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/while

[^97]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Statements/for

[^98]: https://pt.linkedin.com/pulse/estruturas-de-repetição-laços-testes-em-javascript-edmundo

[^99]: https://www.homehost.com.br/blog/javascript/while-javascript/

[^100]: https://www.locaweb.com.br/ajuda/wiki/for-javascript/

[^101]: https://franciscochaves.com.br/assets/img/blog/2024/01/logo-estrutura-de-repeticao-em-javascript.png?sa=X\&ved=2ahUKEwisi-_wqfiMAxU-B7kGHYwUEkQQ_B16BAgLEAI

[^102]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Object_initializer

[^103]: https://dev.to/vitorrios1001/classes-vs-objetos-em-javascript-entendendo-as-diferencas-fundamentais-5f59

[^104]: https://www.youtube.com/watch?v=ddOOJJwbuLY

[^105]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Property_accessors

[^106]: https://web.dev/learn/javascript/objects

[^107]: https://www.javascriptprogressivo.net/2019/01/Classe-Objeto-Propriedade-Metodos-JS.html

[^108]: https://www.devmedia.com.br/curso/javascript-objeto-literal-e-colecao-de-objetos/2405

[^109]: https://ebaconline.com.br/blog/linguagem-de-programacao

[^110]: https://www.azion.com/pt-br/learning/jamstack/historia-e-evolucao-do-javascript/

[^111]: https://www.treinaweb.com.br/blog/contexto-de-execucao-javascript

[^112]: https://support.runescape.com/hc/pt-br/articles/115003779409-Ativar-o-JavaScript-no-seu-navegador

[^113]: https://nodejs.org/en/about

[^114]: https://www.alura.com.br/apostila-html-css-javascript/38CA-eventos-com-javascript

[^115]: https://academiatech.blog.br/tipos-de-dados-javascript/

[^116]: https://dev.to/collabcode/como-funciona-o-var-let-e-const-do-javascript-178p

[^117]: https://www.treinaweb.com.br/blog/conhecendo-variaveis-e-constantes-no-javascript

[^118]: https://www.javascriptprogressivo.net/2018/08/IF-ELSE-Aninhados-Tutorial-JavaScript.html

[^119]: https://www.devmedia.com.br/javascript-if-else-criando-scripts-com-estruturas-condicionais/39686

[^120]: https://celsokitamura.com.br/if-aninhado-estrutura-de-decisao-em-javascript/

[^121]: https://www.dio.me/articles/usando-expressoes-matematicas-em-js

[^122]: https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/Scripting/Math

[^123]: https://evandrofalleiros.github.io/docs/js-linguagem/tipos/operadores-relacionais

[^124]: https://www.alura.com.br/artigos/operadores-matematicos-em-javascript

[^125]: https://awari.com.br/javascript-operadores-logicos-and-e-or/

[^126]: https://dev.to/acaverna/lacos-de-repeticao-em-javascript-50hj

[^127]: https://www.hashtagtreinamentos.com/loops-em-javascript

[^128]: https://www.freecodecamp.org/portuguese/news/lacos-em-javascript-explicados-lacos-for-while-do-while-e-mais/

[^129]: https://developer.mozilla.org/pt-BR/docs/Learn_web_development/Core/Structuring_content/Headings_and_paragraphs

[^130]: https://pt.stackoverflow.com/questions/445508/o-que-são-tipos-literais-em-javascript

[^131]: https://www.locaweb.com.br/blog/temas/codigo-aberto/objeto-literal-colecao-de-objetos/

[^132]: https://tableless.com.br/javascript-objetos-literais-vs-funcoes-construtoras/

[^133]: https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Guide/Grammar_and_types








