# MNSR Digital - Guia Interativo e Inteligente

Aplicacao movel gamificada e inteligente para o Museu Nacional Soares dos Reis (Porto).

---

## 1. Visao do Produto
- PARA os jovens, familias e turistas culturais que visitam a cidade do Porto,
- QUE procuram uma experiencia museologica dinamica, personalizada e interativa,
- A APP MNSR DIGITAL e uma aplicacao movel inteligente e gamificada,
- QUE oferece roteiros personalizados pelo tempo disponivel, caca ao tesouro por QR Code, guia conversacional de IA para responder a duvidas sobre as obras e um painel de gestao de fluxos para a administracao do museu,
- AO CONTRARIO DOS guias audio estaticos e brochuras em papel tradicionais,
- O NOSSO PRODUTO aumenta o envolvimento do visitante, promove o regresso do publico local e permite gerir eficientemente o fluxo e lotacao nas salas do museu.

---

## 2. Equipa e Papeis (Marco M0)
- Ana Azevedo 
- Luis Monteiro 
- Rodrigo Ribeiro 
- Rodrigo Rocha

---

## 3. Carta de Utilizacao de IA Generativa (Marco M0)
A equipa compromete-se a cumprir os principios de integridade academica e transparencia no uso de IA Generativa durante o desenvolvimento do projeto:
- Uso Permitido (Zona Verde/Amarela): Apoio na escrita de documentacao, geracao de dados ficticios para testes, revisao/refactoring de codigo e apoio no diagnostico de erros.
- Mecanismos de Validacao: Nenhuma saida de IA sera incorporada sem revisao critica, execucao previa e testes automatizados.
- Registo de Transparencia: Todas as interacoes relevantes com assistentes de IA (ferramenta, tarefa, validacao efetuada e decisoes) serao registadas na pasta /docs/ai-log.md.
- Avaliacao Presencial: O codigo e as decisoes arquiteturais serao totalmente dominados pela equipa para defesa oral.

---

## 4. Stakeholders (Marco M1)
1. Visitante / Turista Cultural: Procura otimizar o tempo de visita e compreender as obras de forma envolvente.
2. Jovem / Estudante: Interessa-se por elementos interativos, desafios gamificados e caca ao tesouro.
3. Equipa de Gestao do Museu / Curadores: Pretendem monitorizar o afluxo de visitantes por sala, gerir o acervo de obras e analisar estatisticas de visitas.
4. Administrador de Sistemas: Pretende gerir permissoes de acesso e assegurar a estabilidade do sistema.

---

## 5. Backlog Inicial de Requisitos - User Stories (Marco M1)

### Alta Prioridade (Must Have)
- US01 - Roteiro Personalizado por Tempo
  * User Story: Enquanto visitante, quero indicar o meu tempo disponivel no museu para que a app gere um roteiro com as obras mais relevantes ajustadas a essa duracao.
  * Criterios de Aceitacao:
    * Permite escolher intervalos de tempo pre-definidos (ex.: 30 min, 1h, 2h).
    * Apresenta a lista sequencial de obras e o caminho recomendado no mapa do museu.

- US02 - Leitura de QR Code para Obras
  * User Story: Enquanto visitante, quero ler o QR Code associado a uma obra para aceder de imediato aos seus detalhes e conteudos multimedia.
  * Criterios de Aceitacao:
    * A camara da app deve reconhecer o QR Code em menos de 2 segundos.
    * Apresenta a ficha da obra, audio explicativo e opcao de interagir com o assistente.

### Media Prioridade (Should Have)
- US03 - Caca ao Tesouro Gamificada
  * User Story: Enquanto jovem visitante, quero participar na caca ao tesouro lendo QR Codes nas salas para resolver enigmas e ganhar medalhas.
  * Criterios de Aceitacao:
    * A leitura do QR Code correto valida o enigma atual e desbloqueia a pista seguinte.
    * A app regista o progresso e mostra o resultado final ao completar o desafio.

- US04 - Guia Conversacional de IA para Obras
  * User Story: Enquanto visitante curioso, quero colocar questoes em texto sobre uma obra ao guia virtual para obter respostas adaptadas ao meu nivel de conhecimento.
  * Criterios de Aceitacao:
    * O utilizador pode escolher o tom/nivel de detalhe (Geral, Criancas ou Especialista).
    * O assistente responde exclusivamente com base na base de conhecimento oficial fornecida pelo museu.

### Baixa Prioridade / Extensao (Could Have - Valorizacao Admin)
- US05 - Gestao e Alerta de Lotacao de Salas (Administracao)
  * User Story: Enquanto gestor do museu, quero visualizar a taxa de ocupacao das salas para reencaminhar novos roteiros e evitar sobrelotacao.
  * Criterios de Aceitacao:
    * O painel indica o estado das salas (Verde, Amarelo, Vermelho) com base no numero de utilizadores ativos nessa zona.

- US06 - Gestao do Catalogo de Obras e Gerador de QR Codes
  * User Story: Enquanto curador, quero criar e editar fichas de obras e gerar os respetivos QR Codes para impressao.
  * Criterios de Aceitacao:
    * Permite inserir titulo, autor, ano, descricao e imagem da obra num formulario Web/Admin.
    * O sistema gera automaticamente o ficheiro do QR Code associado ao ID da obra.

- US07 - Dashboard de Analytics de Visitas
  * User Story: Enquanto gestor do museu, quero consultar graficos com as obras mais visitadas e o tempo medio de permanencia nas salas para otimizar as exposicoes.
  * Criterios de Aceitacao:
    * Apresenta um grafico com o top das obras mais escaneadas por dia ou semana.
    * Exibe o tempo medio de permanencia dos visitantes por sala.

---

## 6. Requisitos Nao-Funcionais (RNF)
- RNF01 - Desempenho: A aplicacao deve carregar os detalhes de uma obra via QR Code em menos de 2 segundos.
- RNF02 - Seguranca e Privacidade: Nenhuns dados pessoais sensiveis dos visitantes serao armazenados.
- RNF03 - Seguranca e Autenticacao: As funcionalidades de gestao e administracao (US05, US06 e US07) exigem autenticacao com login e palavra-passe.
- RNF04 - Usabilidade e Acessibilidade: A interface deve seguir padroes de elevado contraste e permitir ajuste de tamanho de letra para facilitar a leitura no telemovel.
