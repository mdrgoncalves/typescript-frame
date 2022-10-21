<h1 align="center">
    Alura Frame
</h1>

<p align="center">
 • <a href="#-about">Sobre</a> 
 • <a href="#-tech-stack">Conteúdo Estudado</a>  
</p>

# 💻 Sobre

Alura Frame - Página para estudo de TypeScript.

---

# 🛠 Conteúdo Estudado

<details>

<summary><b><font size="+2">MÓDULO 1 - EVOLUINDO O JAVASCRIPT</font></b></summary>

## TÓPICO 1: Básico do TS

 - **Diferenças do JS para TS**
 
Uma das principais diferenças é que o TS é tipado, ou seja, você precisa definir o tipo de cada variável, função, etc. E isso é muito bom, pois o TS vai te ajudar a evitar erros de digitação, por exemplo, e também vai te ajudar a entender melhor o que cada coisa faz.
<br/><br/>

## TÓPICO 2: Configuração do TS

 - **Instalação do TS**

Para instalar o TS, precisa-se ter o NodeJS instalado na máquina. Depois, basta rodar o comando npm install -g typescript.

 - **Configuração do TS**

Para configurar o TS, precisa-se criar um arquivo chamado tsconfig.json. Nele, se pode definir o diretório de saída do arquivo compilado, o diretório de entrada do arquivo TS, o modo de compilação, etc. 

    {
    "compilerOptions": {
        "outDir": "dist/js", //Diretório de saída do arquivo compilado
        "target": "ES6", //Versão do JS que o TS vai compilarenter code here
        "noEmitOnError": true //Se houver algum erro, não compila o arquivo
    },
    "include": ["app/**/*"] //Diretório de entrada do arquivo TS
    }

 
 - **Modificador PRIVATE**

O modificador PRIVATE é usado para definir que um atributo ou método só pode ser acessado dentro da classe que ele foi declarado. 
<br/><br/>

## TÓPICO 3 - Tipagens

 - **Tipo implícito ANY**

O tipo ANY é um tipo que pode receber qualquer tipo de dado. Ele é muito útil quando você não sabe o tipo de dado que vai receber, mas não é recomendado usá-lo.

Para retirar o tipo ANY, pode-se usar o comando tsc "noImplicitAny": true no tsconfig. Ele vai mostrar todos os erros de tipagem que se tem no código.

- **Tipo HTMLElement**

O tipo HTMLElement é um tipo que representa um elemento HTML. Muito útil para se trabalhar com elementos HTML.
<br/><br/>

## TÓPICO 4 - Avançando em TS

 - **Generics**

Generics em TS são como templates, servem para definir um tipo genérico que pode ser usado em qualquer lugar. Por exemplo: Array<T> é um array que pode receber qualquer tipo de dado.

- **Modificador READONLY**

O modificador READONLY é usado para definir que um atributo só pode ser lido, mas não pode ser alterado. Por exemplo: ReadOnlyArray<T> é um array que só pode ser lido, mas não pode ser alterado.
<br/><br/>

## TÓPICO 5 - Simplificações no TS

- **Declaração no Constructor**

É possível declarar atributos no constructor, sem precisar declarar no escopo da classe. Se no construtor da classe utilizar public ou private antes do atributo, ele vai ser declarado no escopo da classe.

- **Atalho para Array**

Para declarar um array, pode-se usar o atalho T[], no lugar de Array<T>.
Para o modificador READONLY, pode-se usar o atalho readonly T[], no lugar de ReadonlyArray<T>.

- **Getters Públicos**

Se a propriedade de uma classe estiver sendo utilizada apenas para leitura, pode-se declarar no constructor da classe a mesma como pública e utilizando o modificador readonly. Dessa forma, não é necessário criar um getter para a propriedade.

- **Programação Defensiva com Datas**

Pelo Date conter métodos que podem alterar o valor da data quando essa é passada como parâmetro, é recomendado criar uma cópia da data para fornecê-la como getter.
<br/><br/>

</details>

<details>

<summary><b><font size="+2">MÓDULO 2 - AVANÇANDO EM TYPESCRIPT</font></b></summary>

## TÓPICO 1: Manipulação de DOM

- **Templates Declarativos e Dinâmicos**

Templates declarativos são templates que são declarados no HTML e são utilizados para renderizar elementos HTML. Templates dinâmicos são templates que são declarados no TS e são utilizados para renderizar elementos HTML.

- **Formatação de Datas usando Intl**

Para formatar datas, pode-se usar o Intl, que é um objeto que possui métodos para formatar datas, moedas, números, etc.
<br/><br/>

## TÓPICO 2: Heranças

- **Aplicação do EXTENDS**

O extends é usado para herdar atributos e métodos de uma classe. 

- **Modificador PROTECTED**

O modificador protected é usado para definir que um atributo ou método só pode ser acessado dentro da classe que ele foi declarado ou nas classes que herdam essa classe.

- **Generics em Herança**

É possível utilizar generics em herança. Por exemplo: class ClassePai<T> extends Pai<T>.
O <T> define um tipo genérico, permitindo criar métodos que recebam esse mesmo tipo, aumentando o reaproveitamento de código entre pais e filhos.

- **O ABSTRACT**

O abstract é usado para definir que uma classe não pode ser instanciada, mas pode ser herdada. Uma classe abstrata pode ter métodos abstratos, que são métodos que não possuem implementação, mas que devem ser implementados nas classes filhas.
<br/><br/>

## TÓPICO 3: Enumerations

- **ENUM**

O enum é usado para definir um conjunto de constantes. Por exemplo: enum DiasDaSemana {Segunda, Terça, Quarta, Quinta, Sexta, Sábado, Domingo}. O enum é um tipo de dado, então pode ser utilizado em qualquer lugar que se possa utilizar um tipo de dado.

- **ENUM COM VALORES**

É possível definir valores para cada constante do enum. Isso garante a segurança da ordem do enum, pois se uma constante for adicionada no meio do enum, as outras constantes não serão alteradas. 
<br/><br/>

## TÓPICO 4 - Static e Opcionais

- **Modificador STATIC**

O static é usado para definir que um atributo ou método pertence à classe, e não à instância da classe, sendo assim, não é necessário instanciar a classe para acessar o atributo ou método.

- **Proteção do innerHTML**

Para proteger o innerHTML, pode-se utilizar um escape para evitar que seja inserido a tag script no HTML. Como é o caso utilizando o REGEX: innerHTML = texto.replace(/<script>[\s\S]*?<\/script>/, '');

- **Opcionais**

É possível definir que um atributo ou parâmetro é opcional, utilizando o símbolo de interrogação (?) após o nome do atributo ou parâmetro. Isso permite que o atributo ou parâmetro não seja obrigatório, podendo ser passado ou não.
<br/><br/>

## TÓPICO 5 - Ambientes Rígidos

- **Remoção de Comentários na Compilação**

Para remover comentários na compilação, pode-se utilizar o parâmetro --removeComments no tsconfig.json.

- **StrictNullChecks**

O strictNullChecks é um parâmetro do tsconfig.json que permite que o TS não aceite atribuições de null ou undefined para variáveis que não são do tipo any ou que não possuem o símbolo de interrogação (?) após o nome do atributo ou parâmetro.

- **Casting Explícito**

O casting explícito é uma forma de forçar o TS a aceitar atribuições de null ou undefined para variáveis que não são do tipo any ou que não possuem o símbolo de interrogação (?) após o nome do atributo ou parâmetro. Para isso, pode-se inferir explicitamente o tipo da varíavel, utilizando "... as Tipo" após a declaração da variável ou <Tipo> antes da declaração da variável.
<br/><br/>

</details>

<details>

<summary><b><font size="+2">MÓDULO 3 - TÉCNICAS E BOAS PRÁTICAS</font></b></summary>

## TÓPICO 1: Requisitos Não Funcionais e Decorators

- **Performance Now**

O performance.now() é um método que retorna o tempo em milissegundos desde que a página foi carregada. Esse método é útil para medir o tempo de execução de um trecho de código.

- **Decorators**

Os decorators são funções que podem ser aplicadas a classes, métodos, atributos e parâmetros. Eles são usados para adicionar funcionalidades a esses elementos. Para aplicar um decorator, basta colocar o símbolo @ antes da declaração do elemento. Por exemplo: @logarTempoDeExecução.

- **Compilação do Decorator**

Para ativar a compilação dos decorators no código, é necessário adicionar o parâmetro "experimentalDecorators": true no tsconfig.json.

- **Parâmetros do Decorator**

```typescript
    function decorator() {

        return function(
            target: any, 
            /*
                Se colocar o decorator em um método estático, o target é a função construtora
                Se colocar o decorator em um método de instância, o target é o prototype da função construtora
            */
            propertyKey: string,
            /*
                Se colocar o decorator em um atributo, o propertyKey é o nome do atributo
                Se colocar o decorator em um parâmetro, o propertyKey é o nome do método
            */
            descriptor: PropertyDescriptor
            /*
                Se colocar o decorator em um método, o descriptor dá acesso ao método
            */
        )
    }
```
<br/><br/>

## TÓPICO 2: Decorators de Métodos

- **Template do Decorator**

```typescript
    export function decorator() {

        return function(
            target: any,
            key: string,
            descriptor: PropertyDescriptor
        ) {
            const metodoOriginal = descriptor.value;

            descriptor.value = function(...args: any[]) {

                const retorno = metodoOriginal.apply(this, args);
                return retorno;
            };

            return descriptor;
        }
    }
```

- **Simplificando um Decorator**

Se um decorator não tiver nenhum parâmetro, não é necessário chamar um wrapper. Por exemplo:

```typescript
    return decorator(
        target: any,
        key: string,
        descriptor: PropertyDescriptor
    ) {
        const metodoOriginal = descriptor.value;

        descriptor.value = function(...args: any[]) {

            const retorno = metodoOriginal.apply(this, args);
            return retorno;
        };

        return descriptor;
    }
```
<br/><br/>

## TÓPICO 3: Decorators de Propriedades

- **Getters Dinâmicos**

Para que seja possível o decorator acessar o atributo através de alguma instância da classe, é necessário criar um getter dinâmico para o atributo. Para isso, basta criar um getter para o atributo, que retorna o valor do atributo da instância da classe.

- **Redefinir Getter**

Para redefinir o getter, é necessário utilizar o Object.defineProperty. Este sobrescreverá o getter original, criando uma nova referência no prototype, permitindo que o decorator acesse o atributo através de alguma instância da classe.

- **Cache Decorator Copy**

Para evitar que o decorator seja aplicado várias vezes ao mesmo atributo, é necessário criar um cache para o decorator. Para isso, cria-se uma verificação no decorator para verificar se o atributo já foi decorado. Caso não tenha sido, o decorator é aplicado ao atributo. Caso já tenha sido, o decorator não é aplicado novamente.
<br/><br/>

## TÓPICO 4: API Externa e Interface

- **Interfaces**

As interfaces são formas de definir um contrato para uma classe. Elas são úteis para definir o que uma classe deve ter, mas não como ela deve ter. Para criar uma interface, basta utilizar a palavra interface seguida do nome da interface. 

- **Implementando uma Interface**

Para implementar uma interface, basta utilizar a palavra implements seguida do nome da interface. 

- **Services**

Os services são classes que contém métodos que acessam uma API externa. Eles são úteis para isolar a lógica de acesso a uma API externa, permitindo que a lógica de negócio da aplicação não seja afetada caso a API externa mude.
<br/><br/>

## TÓPICO 5: Evoluindo Interfaces

- **Polimorfismo**

O polimorfismo é um conceito que permite que uma classe tenha métodos com o mesmo nome, mas que façam coisas diferentes. Para isso, pode-se utilizar interfaces. 

- **Interfaces com Generics**

As interfaces podem ser parametrizadas, permitindo que sejam utilizadas com diferentes tipos de dados. Para isso, basta utilizar o símbolo <T> antes do nome da interface.

- **Estendendo Interfaces**

Para estender uma interface, basta utilizar a palavra extends seguida do nome da interface. As interfaces podem ser estendidas um número ilimitados de vezes, ao contrário das classes.

- **SourceMap**

O sourceMap é um arquivo que mapeia o código transpilado para o código original. Ele é útil para debugar o código original, mesmo que o código transpilado esteja sendo executado. Para gerar o sourceMap, basta adicionar o parâmetro "sourceMap": true no tsconfig.json. Para o debug ocorrer de forma correta, tanto o código compilado quanto a ser compilado devem estar na mesma estrutura de pastas.

</details>