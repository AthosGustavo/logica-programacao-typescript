# logica-programacao_typescript
<details>
  <summary>Lógica de programação</summary>

  # Lógica de programação
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
  
  
</details>
