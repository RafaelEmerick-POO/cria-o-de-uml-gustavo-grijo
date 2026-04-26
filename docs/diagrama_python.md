

# Diagrama UML - Python

```mermaid
classDiagram
    class Equipamento {
        -_tag : str
        -_descricao : str
        -_ativo : bool
        +__init__(tag : str, descricao : str, ativo : bool)
        +ligar() : void
        +desligar() : void
        +tag : str
        +exibir_resumo() : void
    }

    class SensorTemperatura {
        -_valor_atual : float
        +__init__(tag : str, descricao : str, ativo : bool, valor_atual : float)
        +atualizar_leitura(novo_valor : float) : void
        +exibir_resumo() : void
    }

    Equipamento <|-- SensorTemperatura


