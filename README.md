# logica-programacao_typescript
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

  ## Manipulação de Arrays
  *Iniciando um array vazio*
  ```javascript
  let arrayVazio:number[] = [];
  ```
  
</details>
