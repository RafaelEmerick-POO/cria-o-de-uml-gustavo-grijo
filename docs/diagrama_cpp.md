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

#Jusificativa#
A classe SensorTemperatura herda de Equipamento, identificado pelo uso de : Equipamento(...) no construtor.
Os atributos e métodos foram extraídos diretamente do código fonte.
O método exibirResumo() é sobrescrito na classe derivada, caracterizando polimorfismo.
Os atributos são privados e acessados por métodos públicos, garantindo encapsulamento.
- quais operacoes merecem destaque no diagrama;
- por que seu UML representa corretamente o codigo em `C++`.

## 5. Evidencias

Cole aqui a saida do terminal, prints ou observacoes da execucao do codigo em `C++`.
