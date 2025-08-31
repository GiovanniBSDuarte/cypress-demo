# Ambiente de Testes Automatizados com Cypress no Codespaces

Este repositório contém a configuração necessária para rodar o **Cypress** com interface gráfica diretamente no **GitHub Codespaces**, sem precisar instalar nada localmente.  

Cada aluno poderá abrir este repositório no Codespaces e executar os testes de forma interativa.

---

## O que está incluído
- **Cypress** já instalado (`npx cypress open` disponível).
- **Ambiente gráfico XFCE** acessível via navegador.
- **Servidor VNC + noVNC** para visualizar o desktop remoto.
- **Exemplo de teste simples**: validar título da página de A/B Testing no site *The Internet*.

---

## Como usar

### 1. Abrir no Codespaces
1. Clique no botão **"Code"** verde neste repositório.  
2. Selecione a aba **Codespaces**.  
3. Clique em **"Create codespace on main"**.  

---

### 2. Iniciar o ambiente gráfico
No terminal do Codespaces, execute:

```bash
npm run desktop
