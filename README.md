# SafeAlert Backend

Backend do sistema SafeAlert, uma plataforma inteligente de monitoramento, previsão e alerta para proteção de cidades contra eventos ambientais extremos.

## Autor

**Roan Ferreira de Sá**

## Tecnologias Utilizadas

- Next.js 14
- TypeScript
- PostgreSQL
- Prisma ORM
- NextAuth.js
- OpenAI API
- Tailwind CSS

## Requisitos

- Node.js 18+
- PostgreSQL
- DBeaver (ou outro cliente SQL)
- Conta na OpenAI (para API key)

## Configuração do Ambiente

1. Clone o repositório
```bash
git clone [url-do-repositorio]
cd safealert-back
```

2. Instale as dependências
```bash
npm install
```

3. Configure as variáveis de ambiente
```bash
cp .env.example .env
```
Edite o arquivo `.env` com suas configurações:
- DATABASE_URL: URL de conexão com o PostgreSQL
- NEXTAUTH_SECRET: Chave secreta para o NextAuth
- OPENAI_API_KEY: Chave da API da OpenAI
- Credenciais dos provedores OAuth (opcional)

4. Configure o banco de dados
```bash
npx prisma migrate dev
```

5. Inicie o servidor de desenvolvimento
```bash
npm run dev
```

## Endpoints da API

### Autenticação
- POST /api/auth/[...nextauth] - Endpoints de autenticação

### Cidades
- GET /api/cities - Lista todas as cidades
- POST /api/cities - Cria uma nova cidade

### Alertas
- GET /api/alerts - Lista todos os alertas
- POST /api/alerts - Cria um novo alerta

### Previsões
- POST /api/predictions - Gera uma nova previsão usando IA

### Dados Ambientais
- GET /api/environmental-data - Lista dados ambientais (com filtros)
- POST /api/environmental-data - Adiciona novos dados ambientais

## Estrutura do Banco de Dados

- Users: Usuários do sistema
- Cities: Cidades monitoradas
- Alerts: Alertas gerados
- Predictions: Previsões geradas pela IA
- EnvironmentalData: Dados ambientais coletados

## Contribuição

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
# SafeAlertBack
