![Python](https://img.shields.io/badge/Python-3.13-blue) ![Linux](https://img.shields.io/badge/Linux-Kali-lightgrey) ![Security](https://img.shields.io/badge/Security-RBAC-green)

# 📂 Sistema de Classificação de Dados com RBAC

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
│   └── print4.png
├── README.md
└── EVIDENCIAS.md
📌 Exemplo de execução
1️⃣ Classificação e Risco dos Arquivos (Diretor)
Comando:

python3 main.py
Resultado:

plano_estrategico.docx | Classificação: restrito  | Risco: Crítico | Acesso (diretor): Permitido
salario_2026.xlsx      | Classificação: confidencial | Risco: Alto | Acesso (diretor): Permitido
post_linkedin.txt      | Classificação: interno | Risco: Médio | Acesso (diretor): Permitido

Relatório gerado com sucesso.
Print do resultado:

2️⃣ Auditoria de Acessos Negados
Comando:

cat reports/audit.log
Resultado:

2026-02-11 10:57:58 | ROLE: analista | ARQUIVO: plano_estrategico.docx | ACESSO NEGADO
2026-02-11 10:57:58 | ROLE: analista | ARQUIVO: salario_2026.xlsx | ACESSO NEGADO
Print do resultado:

3️⃣ Classificação e Risco dos Arquivos (Estagiário)
Comando:

python3 main.py
Resultado:

plano_estrategico.docx | Classificação: restrito  | Risco: Crítico | Acesso (estagiario): Negado
salario_2026.xlsx      | Classificação: confidencial | Risco: Alto | Acesso (estagiario): Negado
post_linkedin.txt      | Classificação: interno | Risco: Médio | Acesso (estagiario): Permitido

Relatório gerado com sucesso.
Print do resultado:

4️⃣ Possíveis Evoluções
Implementar alertas automáticos para múltiplas tentativas de acesso negado.

Criar uma interface web para visualização dos relatórios.

Expandir os níveis de classificação (ex.: público, secreto, altamente restrito).

Integrar com criptografia para proteger arquivos críticos.

✅ Conclusão

O projeto demonstra na prática:

Classificação de dados

Avaliação de risco

Controle de acesso baseado em papéis (RBAC)

Auditoria de acessos

Ele fornece uma base sólida para governança de dados em ambiente corporativo seguro.
