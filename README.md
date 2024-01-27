# Lógica de programação em TypeScript
<details>
  <summary>Comandos e montagem de ambiente</summary>
  
  ## Configurando o arquivo tsconfig.json
  ### module:
   - Define o tipo de importação commonjs ou ESNext

  ### outDir
   - Pasta onde os arquivos .js serão compilados
  `"outdir": "./dist"`

  ### rootDir
   - Pasta que ficarão os arquivos .ts
  `"rootDir": "./src"`
  
  ### Comando para instalar o TypeScript globalmente
   - npm install -g typescript
  
  ### Comando para compilar o TypeScript
   - tsc nomeArquivo.ts

  ### Comando para criar o arquivo tsconfig.json
   - tsc --init



  
</details>
<details>
  <summary>Lógica de programação</summary>

  # Lógica de programação
  ## Tipos de dados utilizados
   - Number
   - String
   - Boolean
  ### Tipo Any
   - Usado para representar uma variável que pode ter qualquer tipo de valor.
   - Desabilita a verificação de tipo estático para a variável, permitindo que ela aceite qualquer valor sem gerar erros de compilação.

  ### Union Type
   - Adiciona tipagem dupla a uma variável ou função
   - A variável ou função passa a aceitar dois tipos de dados

  *EXEMPLO*
  ```javascript
  let id: number | string
  id = 1;
  id = "1"
  ```
  **

  *Declarando uma variável do tipo Any*
  ```javascript
  let valorQualquer: any = 5;
  valorQualquer = "texto";
  valorQualquer = { objeto: true };
  ```
  *Declarando uma função do tipo Any*
  ```javascript
  function retornaQualquerCoisa(): any {
    return "qualquer coisa";
  }

  let resultado: any = retornaQualquerCoisa();
  ```
  
  ## Declaração de variáveis
  ### Inferência x annotaion
  **Inferência**
   - A inferência é uma habilidade usada pelo compilador para definir o tipo de variável pelo valor que ela guarda.
   - A inferência ocorre geralmente com variáveis `let` e `const`

  *EXEMPLO*
  ```javascript
  let nome = "athos"  //O compilador infere que a variável nome seja do tipo String devido o valor que ela assume.
  nome = 12;          //Ocorre erro de tipagem, pois a variável foi inferida como String
  ```
  *annotation*
   - Usada para sinalizar a tipagem de uma variável `const` ou `let`

  *EXEMPLO*
  ```javascript
  let nome:String = "Athos"
  ```
  
  ## Convertendo variáveis - Type Assertions(cast)
   - Usa-se o `as` para converter o tipo
  *Convertendo um tipo Any em uma string*
  ```javascript
  let valor: any = "Isso é uma string";
  let comprimentoDaString: number = (valor as string).length;

  console.log(comprimentoDaString); // Saída: 18
  ```
  
  ## Declarando funções
  ### Declaração padrão
  ```javascript
  function nomeFuncao(a: tipoParametro, b:tipoParametro): tipoRetorno {
    return
  }
  ```
  ### Declaração Expresão de função
  ```javascript
  let nomeFuncao = function(a: tipoParametro, b: tipoParametro): tipoRetorno{
    return
  }
  ```
  ### Declaração de função Arrow Function
  ```javascript
  let nomeFuncao = (a: tipoParametro, b: tipoParametro): tipoRetorno => {
    return 
  }
  ```
  ### Declaração de função com parâmetros opcionais
  ```javascript
  function saudacao(nome: string, sobrenome?: string): string{
    if(sobrenome){
      return `Olá, ${nome} ${sobrenome}`!;
    }else{
      return `Olá, ${nome}!`
    }
  }
  ```
  ### Declaração de função com parâmetro Default
  ```javascript
  function potencia(base: number, expoente: number = 2): number {
    return Math.pow(base, expoente);
  }
  ```
  
  ## Manipulação de Arrays
  *Iniciando um array vazio*
  ```javascript
  let arrayVazio:number[] = [];
  ```

  *Adicionando valores no final do array*
  ```javascript
  let meuArray: number[] = [];
  meuArray.push(4,5);
  ```

  *Adicionando valores em um array de forma direta*
  ```javascript
  let meuArray: number[] = [1,2,3]
  meuArray[3] = 4;
  ```
  ## Objetos Types
   - Coleção de dados simples no formato de objeto com par chave-valor
  ```javascript
  type User = {
    nome: string;
    idade: number:
    email: string;
  }
  const user: User = {
    nome: "athos",
    idade: "22",
    email: "athos@.com"
  }
  ```
  
  ## Map
   - Coleção de dados no formato chave-valor
   - possui ordem de inserção
  *SINTAXE*
  ```javascript
  let nomeMapa: Map<TipoDaChave, TipoDoValor> = new Map();
  ```
  ### Métodos
  `set`: Define um par chave-valor
  ```javascript
  variavel.set(chave, valor);
  ```
  `get`: Retorna o valor de uma chave
  ```javascript
  variavel.get(chave)  //retorna valor
  ```
  `has`: Verifica se uma chave está presente no mapa
  ```javascript
  let verificaChave: boolean = meuMapa.has("Carro");
  console.log(verificaChave)  //Retorna true ou false
  ```
  `delete`: Remove um par chave-valor
  
  `clear` : Remove todas as chaves do map
  
  `size`  : Retorna o número de chaves do map

  
</details>
<details>
  <summary>Orientação a Objetos</summary>
  
</details>
