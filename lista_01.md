# Instruções
- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 8 questões objetivas assinalando a alternativa correta e **justificando sua resposta.**
- Resolva as 2 questões dissertativas escrevendo no próprio arquivo .md
- Lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com o uso de ChatGPT (e similares), pois entregar algo só para ganhar nota não fará você aprender. Não seja dependente da máquina!
- Ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas
**1) Considerando a execução do código abaixo, indique a alternativa correta e justifique sua resposta.**
```javascript
console.log(x);
var x = 5;
console.log(y);
let y = 10;
```
Correta: a) A saída será undefined seguido de erro 
Justificativa: pela leitura do javascript ser de cima para baixo, o código não le o let y = 10 e nem o var = 5 previamente deles serem expostos pelos console.logs. a forma correta seria adicionando o console log após a definição de cada variavel, para o códio ser lido e exposto.

b) A saída será 5 seguido de 10

c) A saída será undefined seguido de undefined

d) A saída será erro em ambas as linhas que utilizam console.log


**2) O seguinte código JavaScript tem um erro que impede sua execução correta. Analise e indique a opção que melhor corrige o problema. Justifique sua resposta.**

```javascript
function soma(a, b) {
    if (a || b === 0) {
        return "Erro: número inválido";
    }
    return a + b;
}
console.log(soma(2, 0));
```

a) Substituir if (a || b === 0) por if (a === 0 || b === 0)

Correta: b) Substituir if (a || b === 0) por if (a === 0 && b === 0)
Justificativa: A verificação a || b === 0 sempre indica o numero como invalida pois a soma define o b como 0, sendo assim, executando a logica, a OU b sendo 0 o numero sera invalido. alterando agora para uma verificação separada, analisando a de forma isolada e depois determinando que b TAMBÉM deve ser zero, exclui o erro de apenas um numero ser 0 e invalidar o outro.

c) Substituir if (a || b === 0) por if (a && b === 0)

d) Remover completamente a verificação if (a || b === 0)

______
**3) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
function calcularPreco(tipo) {
    let preco;

    switch(tipo) {
        case "eletrônico":
            preco = 1000;
        case "vestuário":
            preco = 200;
            break;
        case "alimento":
            preco = 50;
            break;
        default:
            preco = 0;
    }

    return preco;
}

console.log(calcularPreco("eletrônico"));
```

a) O código imprime 1000.

Correta: b) O código imprime 200.
Justificativa: o código executando a estrutura condiciona switch 'Switch' e alterando o let preço, verifica os casos eletronico, vestuario e alimento. o console log chama a função calcular preço que aciona o switch case, a condicional é executada verificando o case eletronico, porém não é parado, é apenas finalizado no caso vestuário que possui um break e no final imprimindo 200. Para corrigir isso deve ser adicionado um break após eletronico.

c) O código imprime 50.

d) O código gera um erro.

______
**4) Ao executar esse código, qual será a saída no console? Indique a alternativa correta e justifique sua resposta.**
```javascript
let numeros = [1, 2, 3, 4, 5];

let resultado = numeros.map(x => x * 2).filter(x => x > 5).reduce((a, b) => a + b, 0);

console.log(resultado);
```
a) 0

b) 6

c) 18

Correta: d) 24
Justificativa: o Let numeros cria a primeira array, definindo a sequencia de numeros indicada. o numeros.map cria um novo array, multiplicando todos os numeros do array anterior por 2. o .filter filtra todos os numeros da array criada, apenas mostrando todos os numeros maiores que 5, trazendo o resultado 6, 8, 10. o .reduce soma todos os valores do array criado pelo .filter, iniciando por 0 sendo assim: 0 + 6; 0 + 8; 14 + 10; finalizando o console log final com 24.
______
**5) Qual será o conteúdo do array lista após a execução do código? Indique a alternativa correta e justifique sua resposta.**

```javascript
let lista = ["banana", "maçã", "uva", "laranja"];
lista.splice(1, 2, "abacaxi", "manga");
console.log(lista);
```

a) ["banana", "maçã", "uva", "abacaxi", "manga", "laranja"]

b) ["banana", "abacaxi", "manga"]

Correta: c) ["banana", "abacaxi", "manga", "laranja"]
Justificativa: O .splice que foi usado tem a função de remover e substituir elementos dentro de um array. no exemplo mostrado, o array inicial é definido, após isso o lista.splice o remove o elemento 1 e 2, respectivamente "maça" e "uva", pois o elemento 0 seria "banana". e substitui os dois elementos retirados por "abacaxi" e "manga". Por fim, o console nome exibe a nova lista. com os elementos substituidos.

d) ["banana", "maçã", "uva", "abacaxi", "manga"]
______
**6) Abaixo há duas afirmações sobre herança em JavaScript. Indique a alternativa correta e justifique sua resposta**

I. A herança é utilizada para compartilhar métodos e propriedades entre classes em JavaScript, permitindo que uma classe herde os métodos de outra sem a necessidade de repetir código.  
II. Em JavaScript, a herança é implementada através da palavra-chave `extends`.


a) As duas afirmações são verdadeiras, e a segunda justifica a primeira.

Correta: b) As duas afirmações são verdadeiras, mas a segunda não justifica a primeira.
Justifica: A primeira afirmação está correta sobre o conceito de herança e sua função, porém a segunda afirmação mesmo que verdadeira, não justifica o funcionamento de herança no Javascript, mas sim mostra como usa-lo.

c) A primeira afirmação é verdadeira, e a segunda é falsa.

d) A primeira afirmação é falsa, e a segunda é verdadeira.
______
**7) Dado o seguinte código. Indique a alternativa correta e justifique sua resposta.**

```javascript
class Pessoa {
  constructor(nome, idade) {
    this.nome = nome;
    this.idade = idade;
  }

  apresentar() {
    console.log(`Olá, meu nome é ${this.nome} e tenho ${this.idade} anos.`);
  }
}

class Funcionario extends Pessoa {
  constructor(nome, idade, salario) {
    super(nome, idade);
    this.salario = salario;
  }

  apresentar() {
    super.apresentar();
    console.log(`Meu salário é R$ ${this.salario}.`);
  }
}
```


I) A classe Funcionario herda de Pessoa e pode acessar os atributos nome e idade diretamente.  
II) O método `apresentar()` da classe Funcionario sobrepõe o método `apresentar()` da classe Pessoa, mas chama o método da classe pai usando `super`.  
III) O código não funciona corretamente, pois Funcionario não pode herdar de Pessoa como uma classe, já que o JavaScript não suporta herança de classes.

Quais das seguintes afirmações são verdadeiras sobre o código acima?

Correta: a) I e II são verdadeiras.
Justificativa: a alternativa III está incorreta porque o javascript suporta herança de classes.

b) I, II e III são verdadeiras.

c) Apenas II é verdadeira.

d) Apenas I é verdadeira.

______

**8) Analise as afirmações a seguir. Indique a alternativa correta e justifique sua resposta.**

**Asserção:** O conceito de polimorfismo em Programação Orientada a Objetos permite que objetos de diferentes tipos respondam à mesma mensagem de maneiras diferentes.  
**Razão:** Em JavaScript, o polimorfismo pode ser implementado utilizando o método de sobrecarga de métodos em uma classe.

a) A asserção é falsa e a razão é verdadeira.

Correta: b) A asserção é verdadeira e a razão é falsa.
Justificativa: O javascript não suporta a sobrecarga de metodos, definindo multiplos metodos com parametros diferentes, no JavaScript, o polimorfismo é implementado principalmente através de herança e sobrescrita de métodos, ou seja, uma classe filha pode sobrescrever um método da classe pai para fornecer uma implementação específica.

c) A asserção é verdadeira e a razão é verdadeira, mas a razão não explica a asserção.

d) A asserção é verdadeira e a razão é verdadeira, e a razão explica a asserção.

______

# Questões dissertativas
9) O seguinte código deve retornar a soma do dobro dos números de um array, mas contém erros. Identifique os problema e corrija o código para que funcione corretamente. Adicione comentários ao código explicado sua solução para cada problema.

```javascript
function somaArray(numeros) {

    for (i = 0; i < numeros.size; i++) {
        soma = 2*numeros[i];
    }
    return soma;
}
console.log(somaArray([1, 2, 3, 4]));
```

```javascript
let numeros // definindo a var numeros

function somaArray(numeros) {
    let soma = 0; 
    numeros = [3, 6, 9, 12]; // Adicionando os numeros que serão multiplicados e somados

    for (let i = 0; i < numeros.length; i++) { // numeros.size substituido por numeros.lenght 
        soma += 2*numeros[i]; // o soma = 2*numeros[i] foi substituido por soma += 2*numeros[i]
    }
    return soma;
}

console.log(somaArray(numeros)); // referenciando diretamente a var numeros ao inves de colocar os numeros
```
______
10) Crie um exemplo prático no qual você tenha duas classes:

- Uma classe `Produto` com atributos `nome` e `preco`, e um método `calcularDesconto()` que aplica um desconto fixo de 10% no preço do produto.
- Uma classe `Livro` que herda de `Produto` e modifica o método `calcularDesconto()`, aplicando um desconto de 20% no preço dos livros.

Explique como funciona a herança nesse contexto e como você implementaria a modificação do método na classe `Livro`.

para a implementação das classes e o desconto, usei herança ao fazer a classe Livro estender Produto, aproveitando seus atributos e métodos. No construtor, chamei super(nome, preco) para herdar corretamente os valores. Além disso, criei calculardesconto(), usando super.calculardesconto() para aplicar 10% de desconto e subtraindo mais 10% do preço original, garantindo um total de 20% sem sobrescrever completamente o método da classe pai.

```javascript
class Produto {
  constructor(nome, preco) { // Criando a classe produto com os atributos nome e preço
    this.nome = nome; // Atribuindo o valor do parametro nome ao atributo nome
    this.preco = preco; // Atribuindo o valor do parametro preco ao atributo preco
  }
  calculardesconto() { // metodo criado para aplicar um desconto de 10% no preço do produto
    return this.preco * 0.9; // Criando a lógica para aplicar o desconto de 10%
  }
}

class Livro extends Produto{ // Criando a classe Livro que herda os atributos da classe Produto
    constructor(nome, preco){ // Criando o construtor da classe
        super(nome, preco); // chamando os parametros da classe pai
    }

    calculardesconto() { //alterando o metodo calculardesconto da classe pai para 20$
        return super.calculardesconto() - this.preco * 0.1; // Logica que calcula o desconto, preço atual com 10% de desconto - 10% do valor original
    }
}

const produto = new Produto('Livros', 30); // Cria o produto dentro da classe Produto
console.log("Seu produto com 10% de desconto:", produto.calculardesconto()); //Chama a função de 10% de desconto

const livro = new Livro('Aprendendo Javascript', 30);// Cria o livro dentro da classe Livro
console.log("Seu livro com 20% de desconto:", livro.calculardesconto()); //Chama a função de 20% de desconto
```
