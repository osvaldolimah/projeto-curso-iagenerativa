# 📈 B3 Expert - Chatbot de Investimentos

O **B3 Expert** é um assistente virtual inteligente desenvolvido para facilitar a consulta de cotações da bolsa de valores brasileira (B3). Ele utiliza Inteligência Artificial Generativa para interpretar perguntas em linguagem natural e retornar dados financeiros precisos.

---

## 🚀 Demonstração
O projeto está disponível para testes em: https://osvaldolimah.github.io/projeto-curso-iagenerativa/

---

## ⚙️ Funcionalidades
- **NLU (Natural Language Understanding):** Extração de tickers a partir de nomes comuns (ex: "Magalu" -> MGLU3).
- **Dados em Tempo Real:** Integração com a API Brapi para cotações atualizadas.
- **Lógica de Calendário:** Identificação automática de fechamento de mercado em fins de semana e feriados.
- **Filtro de Escopo:** O bot identifica e evita responder sobre assuntos fora do domínio financeiro.
- **Interface Humanizada:** Respostas personalizadas e objetivas.

---

## 🛠️ Stack Tecnológica
- **Backend:** [n8n](https://n8n.io/) (Self-hosted)
- **LLM:** Google Gemini 1.5 Flash
- **API Financeira:** [Brapi](https://brapi.dev/)
- **Frontend:** HTML/CSS/JS (Hospedado no GitHub Pages)

---

## 🧠 Arquitetura da Solução
O fluxo de dados segue a seguinte lógica:
1. **Entrada:** O usuário envia uma mensagem via Webhook.
2. **Classificação:** O primeiro nó do Gemini identifica se há uma intenção de consulta e extrai o ticker.
3. **Enriquecimento:** O n8n realiza uma requisição HTTP para a API Brapi.
4. **Processamento:** O segundo nó do Gemini recebe a pergunta original + dados da API e sintetiza a resposta final.
5. **Saída:** A resposta é retornada ao frontend com tratamento de erros (Graceful Degradation).

---

## 📝 Como executar o projeto
1. Importe o arquivo JSON do workflow no seu **n8n**.
2. Configure sua `API_KEY` do Google Gemini e o seu token da **Brapi**.
3. Aponte a URL do seu Webhook no arquivo JavaScript do seu frontend.

---

## 👤 Autor
**Osvaldo Holanda**
