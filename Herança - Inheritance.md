## Herança - Inheritance

Herança é o processo pelo qual uma classe pode herdar propriedades e métodos de outra classe. Isso permite que as classes sejam organizadas em uma hierarquia, com classes mais específicas herdando comportamentos de classes mais gerais.

```
// Exemplo de uma classe que usa herança
class Animal {
   public $nome;

   public function __construct($nome) {
      $this->nome = $nome;
   }

   public function mover() {
      echo "{$this->nome} está se movendo.";
   }
}

class Cachorro extends Animal {
   public function latir() {
      echo "{$this->nome} está latindo.";
   }
}

$rex = new Cachorro("Rex");
$rex->mover(); // Saída: Rex está se movendo.
$rex->latir(); // Saída: Rex está latindo.
```