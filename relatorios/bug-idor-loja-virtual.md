# 🛡️ Relatório de Vulnerabilidade – IDOR

🔐 **Título:** Acesso não autorizado a pedidos de outros usuários  
🚨 **Severidade:** P2 – Alta  
📌 **Status:** Simulado para fins educacionais

---

## 🔎 Descrição

Foi identificada uma falha de **IDOR (Insecure Direct Object Reference)** na URL de visualização de pedidos da loja. A aplicação permite a modificação do parâmetro `id` na URL, possibilitando o acesso a dados de outros usuários sem verificação de autorização.

---

## 🧪 Etapas para Reproduzir

1. Logar como usuário válido (ex: `cliente01@loja.com`)
2. Acessar a URL:  
3. Modificar a URL manualmente para:  
https://loja.com/pedido/1024
4. Confirmar que dados de outro usuário foram expostos.

---

## ✅ Resultado Esperado

A aplicação deveria retornar um erro de autorização (403) ou redirecionar, impedindo acesso ao recurso de outro usuário.

---

## 🩹 Recomendação

- Implementar verificação no backend para validar se o `id` do pedido pertence ao usuário logado.
- Adotar controle de acesso baseado em sessão ou token.

---

## 📎 Evidências

- Testado em ambiente simulado.
- Prints omitidos por fins educacionais.

