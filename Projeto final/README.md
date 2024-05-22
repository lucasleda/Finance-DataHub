Projeto de Pipeline de Dados
Descrição
Este projeto constrói um pipeline de dados que realiza extração, tratamento, armazenamento e validação de dados financeiros obtidos da API do Brasil API.

Etapas do Projeto
Escolha da API

Utilizamos a API do Brasil API, que fornece dados sobre bancos, corretoras e participantes do PIX.
Extração de Tabelas

Extraímos dados de três tabelas diferentes: bancos, corretoras e participantes do PIX.
Tratamento de Dados

Realizamos a conversão de tipos de dados, renomeação de colunas e preenchimento de valores ausentes para garantir a qualidade e consistência dos dados.
Armazenamento em Banco de Dados

Os dados tratados foram armazenados em um banco de dados SQLite para facilitar a consulta e análise.
Validação das Tabelas

Validamos as tabelas verificando a integridade dos dados, garantindo a ausência de duplicatas e o preenchimento correto de todas as colunas.
