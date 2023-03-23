## Abstração - Abstraction

Abstração é o processo de identificar as características essenciais de um objeto e ignorar as características não essenciais. Na POO, a abstração é implementada por meio de classes e interfaces. Uma classe é uma representação abstrata de um objeto que contém propriedades e métodos que descrevem as características essenciais do objeto. Uma interface é uma definição abstrata de um conjunto de métodos que um objeto deve implementar.

```
// Exemplo de uma classe que representa um carro
class Carro {
   public $marca;
   public $modelo;
   public $ano;

   public function __construct($marca, $modelo, $ano) {
      $this->marca = $marca;
      $this->modelo = $modelo;
      $this->ano = $ano;
   }

   public function getInfo() {
      return "Este é um carro {$this->marca} {$this->modelo} fabricado em {$this->ano}.";
   }
}

```