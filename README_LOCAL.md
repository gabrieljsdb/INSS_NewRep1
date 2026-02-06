# Instruções para Execução Local - Agendamento INSS

Este pacote contém o código-fonte atualizado e o banco de dados do projeto.

## Pré-requisitos
- Node.js (v18 ou superior)
- pnpm (`npm install -g pnpm`)
- MySQL Server 8.0

## Configuração do Banco de Dados
1. Crie um banco de dados no seu MySQL:
   ```sql
   CREATE DATABASE agendamento_inss;
   ```
2. Importe o dump incluído neste pacote:
   ```bash
   mysql -u seu_usuario -p agendamento_inss < database_backup_updated.sql
   ```

## Configuração do Projeto
1. Instale as dependências:
   ```bash
   pnpm install
   ```
2. Configure o arquivo `.env` com suas credenciais locais do MySQL:
   ```env
   DATABASE_URL="mysql://usuario:senha@localhost:3306/agendamento_inss"
   # Outras variáveis conforme necessário
   ```

## Execução
Para rodar em modo de desenvolvimento:
```bash
pnpm dev
```

A aplicação estará disponível em `http://localhost:3000` (ou na porta configurada).

---
*Backup gerado em 05/02/2026*
