# 📄 Documentação Técnica  
## Sistema de Classificação de Dados com RBAC

---

## 📌 1. Visão Geral

O **Sistema de Classificação de Dados com RBAC (Role-Based Access Control)** foi desenvolvido com o objetivo de simular um ambiente de governança de dados, aplicando:

- Classificação automática de documentos
- Avaliação de risco
- Controle de acesso baseado em papéis
- Auditoria de acessos
- Geração de relatorios

O projeto demonstra conceitos fundamentais de Segurança da Informação aplicados de forma prática.

---

## 🎯 2. Objetivo do Projeto

Implementar um sistema capaz de:

✔ Classificar documentos por nível de sensibilidade  
✔ Avaliar o risco associado a cada documento  
✔ Restringir acesso com base em papéis (RBAC)  
✔ Registrar eventos em log de auditoria  
✔ Gerar relatório estruturado para compliance  

---

## 🏗️ 3. Arquitetura do Sistema

O sistema é composto por:

- `main.py` → Script principal de execução
- `data/` → Diretório contendo os arquivos simulados
- `reports/` → Diretório onde são gerados:
  - `audit.log`
  - `relatorio_risco.txt`

Fluxo de funcionamento:

1. Usuário executa o sistema
2. Papel (role) é identificado
3. Documentos são classificados
4. Risco é avaliado
5. RBAC verifica permissão
6. Evento é registrado no log
7. Relatório é gerado

---

## 👥 4. Controle de Acesso (RBAC)

O sistema utiliza três papéis:

### 🔹 Diretor
- Acesso total aos documentos
- Visualiza todas as classificações
- Pode gerar relatórios completos

### 🔹 Analista
- Acesso parcial
- Pode consultar determinados arquivos
- Tentativas indevidas são registradas

### 🔹 Estagiário
- Acesso restrito
- A maioria das tentativas é negada
- Eventos registrados em log

---

## 🔐 5. Classificação de Dados

Os documentos são classificados em níveis como:

- Público
- Interno
- Confidencial
- Restrito

A classificação impacta diretamente no nível de risco atribuído e nas permissões de acesso.

---

## ⚠️ 6. Avaliação de Risco

O sistema atribui níveis de risco com base na sensibilidade da informação.

Exemplo:
- Documento Restrito → Alto Risco
- Documento Público → Baixo Risco

O relatório consolidado permite análise de exposição de dados.

---

## 📝 7. Auditoria

Todos os eventos são registrados em:

reports/audit.log


O log inclui:
- Data e hora
- Papel do usuário
- Documento acessado
- Status (Permitido / Negado)

Isso garante:
✔ Rastreabilidade  
✔ Monitoramento  
✔ Conformidade  

---

## 📊 8. Relatório de Risco

Gerado automaticamente em:

reports/relatorio_risco.txt


Contém:
- Lista de documentos
- Classificação
- Nível de risco

Pode ser utilizado como base para auditorias internas.

---

## 🛡️ 9. Boas Práticas Aplicadas

✔ Princípio do Menor Privilégio  
✔ Separação de responsabilidades  
✔ Registro de eventos (Accountability)  
✔ Estrutura organizada de diretórios  
✔ Simulação de ambiente corporativo  

---

## 🚀 10. Possíveis Melhorias Futuras

- Implementação de autenticação real
- Integração com banco de dados
- Interface web
- Criptografia de arquivos sensíveis
- Exportação de relatórios em PDF

---

## 📌 11. Conclusão

O projeto demonstra de forma prática a aplicação de conceitos de:

- Governança de Dados
- Segurança da Informação
- Controle de Acesso
- Auditoria e Compliance

Servindo como base para evolução em arquiteturas mais robustas.
