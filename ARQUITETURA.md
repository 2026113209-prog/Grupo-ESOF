# Arquitetura do Sistema — App MNSR Digital

## 1. Arquitetura em 3 Camadas
O sistema está dividido em três camadas independentes para separar o ecrã da lógica e dos dados:

| Camada | O que faz | Exemplos no nosso projeto |
| :--- | :--- | :--- |
| **1. Apresentação (UI / Controllers)** | Recebe os pedidos do utilizador e mostra os resultados no ecrã. | `RoteiroController`, `QRCodeController` |
| **2. Lógica de Negócio (Services)** | Contém as regras, cálculos e validações do museu. | `ServicoRoteiro`, `ValidadorQRCode`, `CalculadorAfluencia` |
| **3. Persistência (Repositories)** | Guarda e lê os dados das obras e salas na base de dados local. | `RepositorioObra`, `RepositorioSala` |

---

## 2. Diagrama de Classes (Estrutura)
Este diagrama mostra os objetos principais do museu e como se ligam entre si:

```mermaid
classDiagram
    class Obra {
        +String id
        +String titulo
        +String autor
        +int duracaoMinutos
        +getDetalhes()
    }

    class Roteiro {
        +String id
        +int tempoMaximo
        +adicionarObra(Obra o)
    }

    class ServicoRoteiro {
        +gerarRoteiro(int tempo, String perfil) Roteiro
    }

    Roteiro "1" *-- "*" Obra : contem
    ServicoRoteiro ..> Roteiro : cria
