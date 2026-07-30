## 🎯 Objetivo
Criar uma automação inteligente para capturar diários pessoais enviados por e-mail, processá-los via IA e estruturá-los em um banco de dados no Notion, sem intervenção manual.

## 🛠️ Tecnologias Utilizadas
* **n8n:** Orquestração do fluxo e tratamento de dados.
* **Gmail API:** Trigger de captura (`label:Diário`).
* **Llama 3.1 8B (via Groq):** LLM para análise de sentimento, categorização e resumo.
* **Notion API:** Banco de dados de destino.

## ⚙️ Escopo da Implementação (Arquitetura)
- [x] Configurar `Gmail Trigger` para rodar automaticamente ao receber novos e-mails.
- [x] Desenvolver prompt rigoroso (System Prompt) para a IA retornar um JSON fechado com: Humor, Categoria, Resumo e Tags.
- [x] Implementar tratamento de dados no n8n (Expressões JS + Regex) para limpar formatações Markdown (ex: ````json````) da resposta do Llama.
- [x] Configurar validação de arrays vazios e tipos booleanos para evitar falhas de requisição (HTTP 400) na API do Notion.
- [x] Mapear propriedades e salvar a página estruturada no Notion.

## 🖼️ Evidências / Resultado
<img width="100%" alt="workflow-n8n" src="https://github.com/user-attachments/assets/30559258-5b1c-4bbc-adb3-5fca39baaec2" />


<img width="800" alt="notion-database" src="https://github.com/user-attachments/assets/092acf13-7141-4d52-8c6d-76e1897732f3" />


## 🚀 Status
Implementação finalizada, fluxo rodando em produção de forma 100% autônoma.
