# Diagrama de Casos de Uso - App MNSR Digital

Este documento mostra de forma simples quem usa a app e o que cada pessoa pode fazer nela.

---

## O Diagrama (O que a app faz)

```mermaid
graph LR
    %% Quem usa a app
    v[Visitante]
    j[Jovem / Estudante]
    c[Curador / Admin]

    %% O que se faz na App do Telemovel
    subgraph App no Telemovel
        UC01((UC01: Criar Roteiro por Tempo))
        UC02((UC02: Ver Obra por QR Code))
        UC03((UC03: Jogar Caca ao Tesouro))
        UC04((UC04: Falar com o Guia de IA))
    

    %% O que se faz no Site de Gestao
    subgraph Site do Museu (Admin)
        UC05((UC05: Ver Lotacao das Salas))
        UC06((UC06: Adicionar Obras e QR Codes))
        UC07((UC07: Ver Estatisticas de Visitas))
    

    %% Ligacoes: Quem faz o que
    v --> UC01
    v --> UC02
    v --> UC04

    j --> UC01
    j --> UC02
    j --> UC03
    j --> UC04

    c --> UC05
    c --> UC06
    c --> UC07
