# 🚀 Service Desk Flow Control - Sede & Anexo

Este projeto é um sistema de gestão de escala e distribuição de chamados em tempo real, desenvolvido para otimizar o fluxo de trabalho em centros de suporte técnico (Service Desk). Ele resolve o problema comum de sobrecarga de técnicos e garante que o encaminhamento de WO/REQ siga regras de negócio estritas.

## 🛠️ Tecnologias Utilizadas
* **HTML5 & CSS3**: Interface responsiva e estruturada.
* **JavaScript (ES6+)**: Lógica de negócio e manipulação de estado.
* **Broadcast Channel API**: Sincronização em tempo real entre diferentes abas/janelas sem necessidade de backend.
* **LocalStorage & SessionStorage**: Persistência de dados e gestão de sessão do atendente.

## ⚙️ Funcionalidades Principais
* **Fila Circular (Round Robin)**: Distribuição equitativa de chamados entre os técnicos ativos.
* **Regra de Disponibilidade Inteligente**:
    * Bloqueio automático 30 min após a entrada (período de setup).
    * Bloqueio 30 min antes do início do intervalo/almoço.
    * Bloqueio 30 min antes do fim do expediente.
* **Sincronismo Total**: Qualquer ação (envio de chamado ou reporte de falha) é refletida instantaneamente em todos os navegadores abertos.
* **Controle Gerencial Protegido**: Área restrita por senha para supervisores realizarem o reporte de falhas e avanço manual da fila.
* **Log de Auditoria**: Registro persistente de quem enviou o chamado, para qual técnico e o número da WO.

## 📋 Escala Implementada (Baseada em Cenário Real)
O sistema já vem configurado com as escalas de duas áreas críticas:
* **SEDE**: Cobertura das 07:00 às 22:00.
* **ANEXO**: Cobertura das 07:00 às 19:00.

## 🚀 Como Executar
1. Clone o repositório.
2. Abra o arquivo `index.html` em qualquer navegador moderno.
3. Para testar o sincronismo, abra o mesmo arquivo em duas abas diferentes.

---
Desenvolvido como projeto de portfólio para demonstração de lógica de sistemas e conformidade com boas práticas de Service Desk (ITIL).
