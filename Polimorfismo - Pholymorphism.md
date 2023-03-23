## Polimorfismo - Polymorphism

Polimorfismo é a capacidade de uma classe responder ao mesmo método de maneiras diferentes, dependendo do contexto em que é chamada. Isso permite que diferentes objetos sejam tratados de maneira uniforme, independentemente de suas diferenças específicas.

```
interface Forma {
    public function calcularArea();
}

class Retangulo implements Forma {
    private $altura;
    private $largura;

    public function __construct($altura, $largura) {
        $this->altura = $altura;
        $this->largura = $largura;
    }

    public function calcularArea() {
        return $this->altura * $this->largura;
    }
}

class Circulo implements Forma {
    private $raio;

    public function __construct($raio) {
        $this->raio = $raio;
    }

    public function calcularArea() {
        return pi() * pow($this->raio, 2);
    }
}

function mostrarArea(Forma $forma) {
    return "A área da forma é " . $forma->calcularArea() . ".";
}

$retangulo = new Retangulo(10, 5);
$circulo = new Circulo(3);

echo mostrarArea($retangulo); // Saída: A área da forma é 50.
echo mostrarArea($circulo); // Saída: A área da forma é 28.274333882308.
```