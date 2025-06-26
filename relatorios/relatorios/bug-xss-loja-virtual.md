# Relatório de Vulnerabilidade – XSS Refletido

📌 **Título:** XSS Refletido no campo de busca  
🕹️ **Severidade:** P3 – Moderada  
🔐 **Status:** Simulado para fins educacionais

---

## 🐞 Descrição

Identificada vulnerabilidade de Cross-Site Scripting (XSS Refletido) na funcionalidade de busca da aplicação. O campo aceita scripts maliciosos e os reflete na página de resultados sem qualquer sanitização ou validação.

---

## 🔁 Etapas para Reproduzir

1. Acesse a URL de teste: `https://exemplo.com/busca`
2. No campo de busca, insira o seguinte código:

```html
<script>alert('XSS')</script>
