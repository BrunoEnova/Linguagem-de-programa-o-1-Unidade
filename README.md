


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
| 10 | `? :` | Operador ternário |
| 11 | `=`, `+=`, `-=`, etc. | Atribuição e compostos |


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


---

### Resumo

- Sempre que necessário, use parênteses para garantir a ordem desejada.
- Multiplicação, divisão e módulo vêm antes de adição e subtração.
- Comparações vêm antes dos operadores lógicos (`&&`, `||`).
- O operador ternário é avaliado depois dos lógicos.
- Atribuição é sempre a última operação na expressão.

Essas regras ajudam a evitar ambiguidades e bugs em expressões mais complexas.



