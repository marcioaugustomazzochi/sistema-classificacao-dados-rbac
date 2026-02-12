# 🖼️ Impressões de Execução

Este documento reúne as evidências visuais (prints) da execução do projeto **Sistema de Classificação de Dados com RBAC**.  
Cada print está acompanhado do comando utilizado e da explicação correspondente.

---

## 1️⃣ Classificação e Risco dos Arquivos (Diretor)

📷 Evidência:  
![Diretor](evidencias/print1.png)<img width="1920" height="936" alt="01_execucao_script_classificacao_rbac png" src="https://github.com/user-attachments/assets/543186cd-d09b-4044-8124-63cf1e12ea29" />


🔹 Comando usado:
python3 main.py

🔹 Explicação:
Executa o programa principal com papel Diretor, permitindo acesso a todos os arquivos.
O sistema exibe a classificação e o risco de cada documento e gera o relatório de risco.

---

## 2️⃣ Auditoria de Acessos Negados (Analista)

📷 Evidência:  
![Analista](evidencias/print2.png)<img width="1920" height="936" alt="02_log_auditoria_acessos_negados" src="https://github.com/user-attachments/assets/1698e600-ac1f-4157-89dd-ee58f7b6053f" />


🔹 Comando usado:
cat reports/audit.log

🔹 Explicação:
Exibe o conteúdo do arquivo de auditoria (audit.log).
Mostra as tentativas de acesso negadas para o papel Analista, incluindo horário, papel e documento acessado.

---

## 3️⃣ Classificação e Risco dos Arquivos (Estagiário)

📷 Evidência:  
![Estagiário](evidencias/print3.png)<img width="1920" height="936" alt="03_estrutura_projeto_completa png" src="https://github.com/user-attachments/assets/f94b46e0-5e1a-45a0-8939-9f7f59305bae" />


🔹 Comando usado:
python3 main.py

🔹 Explicação:
Executa o programa principal com papel Estagiário.
Nesse caso, o sistema nega acesso aos arquivos conforme as regras de RBAC, registrando os eventos no log de auditoria.

---

## 4️⃣ Relatório de Risco

📷 Evidência:  
![Relatório](evidencias/print4.png)<img width="1920" height="936" alt="04_simulacao_role_estagiario" src="https://github.com/user-attachments/assets/3af146da-750e-40d0-a49b-3ba9b652ca5c" />


🔹 Comando usado:
cat reports/relatorio_risco.txt

🔹 Explicação:
Exibe o relatório de risco gerado pelo sistema.
Lista os documentos classificados e seus respectivos níveis de risco, servindo como base para compliance e acompanhamento.

---

## 5️⃣ Auditoria Completa

📷 Evidência:  
![Auditoria](evidencias/print5.png)<img width="1920" height="936" alt="05_simulacao_role_diretor" src="https://github.com/user-attachments/assets/ee6a75a1-b8a5-49ab-8b16-4a281be4e583" />


🔹 Comando usado:
cat reports/audit.log

🔹 Explicação:
Mostra o log completo de auditoria, incluindo todas as tentativas de acesso (permitidas e negadas).
É útil para monitoramento, rastreabilidade e análise de comportamento de usuários.

---

## ✅ Evidências Comprovadas

✔ Classificação automática de documentos  
✔ Avaliação de risco  
✔ Controle de acesso baseado em papéis (RBAC)  
✔ Auditoria e geração de relatórios  
✔ Estrutura organizada para governança de dados
