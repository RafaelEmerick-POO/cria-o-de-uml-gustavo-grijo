# # Diagrama UML - C++

```mermaid
classDiagram
    class Equipamento {
        -tag : string
        -descricao : string
        -ativo : bool
        +Equipamento(tagEquipamento : string, descricaoEquipamento : string, ativoInicial : bool)
        +ligar() : void
        +desligar() : void
        +getTag() : string
        +estaAtivo() : bool
        +exibirResumo() : void
    }

    class SensorTemperatura {
        -valorAtual : double
        +SensorTemperatura(tagSensor : string, descricaoSensor : string, ativoInicial : bool, valorInicial : double)
        +atualizarLeitura(novoValor : double) : void
        +getValorAtual() : double
        +exibirResumo() : void
    }

    Equipamento <|-- SensorTemperatura

