# 💰 Finance-DataHub

Um projeto desenvolvido por **Lucas Leda**, focado na **integração, tratamento e análise de dados financeiros** do Brasil.  
O sistema consome informações da **Brasil API**, tratando e armazenando dados de **bancos, corretoras e participantes do PIX** em um **banco de dados SQLite**.

---

## 🧠 Descrição do Projeto

O **Finance-DataHub** tem como objetivo criar um pipeline completo de dados (ETL) para o setor financeiro brasileiro, realizando as seguintes etapas:

### 🛰️ Escolha da API
Foi utilizada a **Brasil API**, uma API pública que disponibiliza dados atualizados sobre instituições financeiras do Brasil, incluindo:
- **Bancos**
- **Corretoras**
- **Participantes do PIX**

### 📦 Extração de Tabelas
O sistema coleta dados de **três endpoints distintos** da Brasil API:
- `/banks/v1` – informações sobre bancos brasileiros;
- `/cvm/corretoras/v1` – lista de corretoras registradas na CVM;
- `/pix/v1/participants` – instituições participantes do sistema PIX.

Cada tabela contém dados específicos sobre as entidades financeiras.

### 🧹 Tratamento de Dados
Após a extração, o sistema realiza diversas etapas de limpeza e padronização:
- Conversão de tipos de dados (strings, numéricos, datas);
- Renomeação de colunas para manter consistência;
- Remoção de duplicatas e preenchimento de valores ausentes.

### 🗄️ Armazenamento em Banco de Dados
Os dados tratados são armazenados em um **banco de dados SQLite (`finance_data.db`)**, permitindo consultas rápidas e organizadas.  
Isso possibilita a integração futura com sistemas de relatórios, dashboards ou análise de dados.

### ✅ Validação
O sistema valida os dados antes do armazenamento, garantindo:
- Ausência de duplicações;
- Integridade das colunas e tipos;
- Estrutura consistente em todas as tabelas.

---

## 🏦 Estrutura das Tabelas

| Tabela | Descrição |
|--------|------------|
| **bancos** | Contém informações sobre instituições bancárias, como nome, código, ISPB e tipo. |
| **corretoras** | Lista de corretoras registradas na CVM, com nome, CNPJ e status de operação. |
| **pix_participantes** | Entidades participantes do sistema PIX (bancos, fintechs, cooperativas etc.). |

---

## 🧩 Tecnologias Utilizadas

- **Python 3**
- **Requests** – para acessar a API Brasil API  
- **Pandas** – para tratamento e manipulação de dados  
- **SQLite3** – para armazenamento local  
- **dotenv** – para variáveis de ambiente  
- **logging** – para controle de logs e execução

---

## ⚙️ Como Executar o Projeto

### 1️⃣ Clone o repositório:
```bash
git clone https://github.com/lucasleda/Finance-DataHub.git
cd Finance-DataHub
2️⃣ Crie um ambiente virtual:
bash
Copiar código
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # Linux/Mac
3️⃣ Instale as dependências:
bash
Copiar código
pip install -r requirements.txt
4️⃣ Execute o script principal:
bash
Copiar código
python src/main.py
📊 Resultados Esperados
Ao final da execução, você terá:

Três tabelas organizadas em um banco SQLite (finance_data.db);

Dados limpos e validados de bancos, corretoras e participantes do PIX;

Um pipeline de ETL completo, pronto para uso em análises financeiras.

👨‍💻 Autor e Direitos
Desenvolvido por Lucas Leda

📫 Contato
📧 weidner.lucas@gmail.com
🌐 github.com/lucasleda
