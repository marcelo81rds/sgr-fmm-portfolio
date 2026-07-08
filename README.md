> 🔒 **Nota de Confidencialidade:** Por questões de direitos autorais, segurança e conformidade de dados com a instituição de ensino parceira, o código-fonte integral deste projeto é privado. Esta documentação serve como um estudo de caso técnico de engenharia e arquitetura de software para o meu portfólio.

# sgr-fmm-portfolio
Sistema autônomo de gestão de filas para refeitórios escolares utilizando Raspberry Pi 3, Python, Flask e SQLite.
Tela do Administrador – Organiza a ordem de acesso das turmas ao refeitório.
<img width="1384" height="1414" alt="image" src="https://github.com/user-attachments/assets/2a8a5f5c-505d-4a29-8f3f-4debc7dd047c" />
Tela do Inspetor - Avisa e Libera o acesso ao Refeitório.
Tela do Painel - Telas espalhadas pela escola que informam que o acesso ao refeitório está próximo ou liberado.
<img width="2872" height="1418" alt="image" src="https://github.com/user-attachments/assets/b92d6402-268e-42a4-862c-6f1a8d2c9593" />
Telas do Inspetor e do Painel - Apresentando o status de almoço encerrado.
<img width="2864" height="1504" alt="image" src="https://github.com/user-attachments/assets/007b6ca8-dda8-45e1-86f9-da1655e6383a" />


# 🍽️ Sistema Automatizado de Gestão de Refeitório Escolar

Uma solução robusta e leve desenvolvida para otimizar o fluxo de alunos em refeitórios escolares, eliminando filas e automatizando a comunicação entre inspetores de pátio e o telão central.

---

## 🚀 Funcionalidades Principais

*   **Painel do Inspetor Autônomo:** Interface mobile simplificada para que os inspetores acionem o status das turmas ("Avisar" / "Liberar") direto do smartphone.
*   **Telão do Pátio Inteligente:** Painel estático projetado para SmartTVs/monitores que exibe de forma síncrona quais turmas devem se dirigir ao refeitório.
*   **Grid Adaptável:** O layout do telão se ajusta automaticamente em colunas caso haja acúmulo de turmas, eliminando barras de rolagem.
*   **Encerramento Automatizado (Timeout):** Sistema inteligente rodando no servidor que finaliza o status da turma 15 minutos após a liberação, garantindo operação 100% autônoma caso o operador esqueça de encerrar.
*   **Painel Administrativo:** Gerenciamento, ordenação dinâmica da fila via prioridades e reinicialização diária do fluxo.

---

## 🛠️ Tecnologias Utilizadas

*   **Servidor Local:** Raspberry Pi 3.
*   **Backend:** Python 3 + Flask (Estrutura de API RESTful)
*   **Banco de Dados:** SQLite (Armazenamento leve e relacional com persistência local)
*   **Frontend:** HTML5, CSS3 (CSS Grid/Flexbox moderno com unidades dinâmicas `vw`/`vh`) e JavaScript Vanilla (Consumo assíncrono via `fetch` API)

---

## 📦 Arquitetura do Projeto

O projeto foi estruturado seguindo o padrão minimalista do ecossistema Flask:

```text
├── app.py                  # Servidor central e regras de expiração de tempo (Backend)
├── static/                 # Assets visuais e identidades da instituição
└── templates/              # Camadas de visualização (Pátio, Inspetor, Admin)
\```

---

## 💡 Motivação e Resultados

Este projeto foi desenhado sob medida para resolver o gargalo de comunicação logística na troca de turnos de almoço de uma instituição de ensino. A automação no backend reduziu a necessidade de intervenção humana contínua, permitindo que a equipe de inspeção foque exclusivamente na segurança dos alunos, enquanto o sistema gerencia o tempo de permanência e a limpeza visual dos painéis.
