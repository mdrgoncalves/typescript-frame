<h1 align="center">
    Aparecida Nutrição
</h1>

<p align="center">
 • <a href="#-about">Sobre</a> 
 • <a href="#-tech-stack">Conteúdo Estudado</a>  
</p>

## 💻 Sobre

Alura Frame - Página para estudo de TypeScript.

---

## 🛠 Conteúdo Estudado

## MÓDULO 1

 - **Diferenças dos JS para TS**
 
Uma das principais diferenças é que o TS é tipado, ou seja, você precisa definir o tipo de cada variável, função, etc. E isso é muito bom, pois o TS vai te ajudar a evitar erros de digitação, por exemplo, e também vai te ajudar a entender melhor o que cada coisa faz.

## MÓDULO 2

 - **Instalação do TS**

Para instalar o TS, você precisa ter o NodeJS instalado na sua máquina. Depois, basta rodar o comando npm install -g typescript.

 - **Configuração do TS**

Para configurar o TS, você precisa criar um arquivo chamado tsconfig.json. Nele, você pode definir o diretório de saída do arquivo compilado, o diretório de entrada do arquivo TS, o modo de compilação, etc. 

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
