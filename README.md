![Python](https://img.shields.io/badge/Python-3.13-blue) 
![Linux](https://img.shields.io/badge/Linux-Kali-lightgrey) 
![Security](https://img.shields.io/badge/Security-RBAC-green)
![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-yellow)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

# 📂 Sistema de Classificação de Dados com RBAC
> Governança de dados e segurança da informação aplicada em Python.

Este projeto implementa um modelo simples de governança de dados em Python, rodando em ambiente Linux. Ele combina **classificação de documentos**, **avaliação de risco**, **controle de acesso baseado em papéis (RBAC)** e **auditoria de acessos**.

---

## 🔑 Funcionalidades

### 1️⃣ Classificação de arquivos
Arquivos são automaticamente classificados em níveis:
- Interno
- Confidencial
- Restrito

### 2️⃣ Avaliação de risco
Cada documento recebe uma classificação de risco:
- Médio
- Alto
- Crítico

### 3️⃣ Controle de acesso por papéis (RBAC)
- **Diretor:** acesso permitido a todos os documentos.  
- **Analista:** acesso negado a arquivos confidenciais e restritos.  
- **Estagiário:** acesso negado a todos os arquivos, inclusive internos.  

### 4️⃣ Auditoria e relatórios
- **Logs:** `audit.log` registra tentativas de acesso com horário, papel e resultado.  
- **Relatórios de risco:** `relatorio_risco.txt` permite acompanhamento e compliance.

---

## 📂 Estrutura do Projeto

```bash
classificador-dados-seguros/
├── main.py
├── classification.py
├── rbac.py
├── risk.py
├── data/
│   ├── plano_estrategico.docx
│   ├── salario_2026.xlsx
│   └── post_linkedin.txt
├── reports/
│   ├── relatorio_risco.txt
│   └── audit.log
├── evidencias/
│   ├── print1.png
│   ├── print2.png
│   ├── print3.png
│   ├── print4.png
│   └── print5.png
├── README.md
└── IMPRESSOES.md

📌 Exemplos de execução
1️⃣ Classificação e Risco dos Arquivos (Diretor)
Comando:

python3 main.py
📷 Evidência:

Explicação: Executa o programa principal com papel Diretor, permitindo acesso a todos os arquivos e exibindo classificação e risco.

2️⃣ Auditoria de Acessos Negados (Analista)
Comando:

cat reports/audit.log
📷 Evidência:

Explicação: Exibe o arquivo de auditoria, mostrando tentativas de acesso negadas para o papel Analista.

3️⃣ Classificação e Risco dos Arquivos (Estagiário)
Comando:

python3 main.py
📷 Evidência:

Explicação: Executa o programa com papel Estagiário, negando acesso a todos os arquivos, inclusive internos.

4️⃣ Relatório de Risco
Comando:

cat reports/relatorio_risco.txt
📷 Evidência:

Explicação: Exibe o relatório de risco gerado, listando documentos classificados e seus níveis de risco.

5️⃣ Auditoria Completa
Comando:

cat reports/audit.log
📷 Evidência:

Explicação: Mostra o log completo de auditoria, incluindo todas as tentativas de acesso (permitidas e negadas).

🔮 Possíveis Evoluções
Implementar alertas automáticos para múltiplas tentativas de acesso negado.

Criar uma interface web para visualização dos relatórios.

Expandir os níveis de classificação (ex.: público, secreto, altamente restrito).

Integrar com criptografia para proteger arquivos críticos.

🚀 Instalação e Uso
# Clonar o repositório
git clone https://github.com/seuusuario/classificacao-dados-rbac.git

# Entrar na pasta do projeto
cd classificacao-dados-rbac

# Executar o script principal
python3 main.py
📜 Licença
Este projeto está licenciado sob os termos da licença MIT.
Você pode usar, modificar e distribuir livremente, desde que mantenha os créditos.

🤝 Contribuição
Contribuições são bem-vindas!
Para colaborar, faça um fork do repositório, crie uma branch com sua melhoria e abra um pull request.

✅ Conclusão
O projeto demonstra na prática:

Classificação de dados

Avaliação de risco

Controle de acesso baseado em papéis (RBAC)

Auditoria de acessos

Ele fornece uma base sólida para governança de dados em ambiente corporativo seguro.
