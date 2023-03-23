## Encapsulamento - Encapsulation

Encapsulamento é a técnica de ocultar o estado interno de um objeto e expor uma interface pública para interagir com o objeto. Isso garante que o objeto só possa ser modificado por meio de métodos definidos em sua classe, o que evita que seu estado seja alterado acidentalmente ou de forma maliciosa.

```
// Exemplo de uma classe que usa encapsulamento para proteger seus dados
class ContaBancaria {
   private $saldo;

   public function depositar($valor) {
      $this->saldo += $valor;
   }

   public function sacar($valor) {
      if ($valor <= $this->saldo) {
         $this->saldo -= $valor;
         return true;
      } else {
         return false;
      }
   }

   public function getSaldo() {
      return $this->saldo;
   }
}

```