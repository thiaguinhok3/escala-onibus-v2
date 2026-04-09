# EscalaOnibus - Sistema de Gestão de Escalas de Motoristas

Aplicativo mobile (Expo/React Native) para gerenciamento de escalas de motoristas de ônibus, com sincronização em tempo real via API em nuvem.

## 🚀 Características

- ✅ **Autenticação em Nuvem**: Login via API remota com fallback local
- ✅ **Múltiplos Usuários**: Suporte para Admin e Motoristas
- ✅ **Escalas Remotas**: Criar, editar, aprovar e negar escalas
- ✅ **Ponto Eletrônico**: Registro de entrada/saída com foto e localização
- ✅ **Ocorrências**: Registro de problemas durante o turno
- ✅ **CNH Virtual**: Gestão de carteira de habilitação fictícia
- ✅ **Multas e Pontos**: Sistema de pontuação e infrações
- ✅ **Dashboard**: Estatísticas e relatórios para admin
- ✅ **Acesso Remoto**: Funciona em qualquer lugar com internet

## 📋 Pré-requisitos

- Node.js 18+ e npm/pnpm
- Expo CLI (`npm install -g expo-cli`)
- PostgreSQL em nuvem (Neon.tech) - já configurado
- Conta no Render para deploy do backend

## 🔧 Instalação

### 1. Clonar o repositório

```bash
gh repo clone seu-usuario/bus_driver_schedule
cd bus_driver_schedule
```

### 2. Instalar dependências

```bash
pnpm install
```

### 3. Configurar variáveis de ambiente

Criar arquivo `.env` na raiz do projeto:

```env
DATABASE_URL=postgresql://neondb_owner:SEU_PASSWORD@ep-aged-feather-amazlq0g.c-5.us-east-1.aws.neon.tech/neondb?sslmode=require
PORT=3000
NODE_ENV=development
EXPO_PUBLIC_API_URL=http://localhost:3000
```

Para produção (`.env.production`):

```env
DATABASE_URL=postgresql://neondb_owner:SEU_PASSWORD@ep-aged-feather-amazlq0g.c-5.us-east-1.aws.neon.tech/neondb?sslmode=require
PORT=3000
NODE_ENV=production
EXPO_PUBLIC_API_URL=https://seu-app.onrender.com
```

### 4. Inicializar banco de dados

```bash
pnpm run db:push
```

## 🏃 Executar Localmente

### Modo Desenvolvimento (Frontend + Backend)

```bash
pnpm run dev
```

Isso inicia:
- Backend em `http://localhost:3000`
- Metro bundler para o app mobile em `http://localhost:8081`

### Apenas Backend

```bash
pnpm run dev:server
```

### Apenas Frontend

```bash
pnpm run dev:metro
```

## 📱 Testar no Celular

### Via Expo Go

1. Instale o app **Expo Go** no seu celular (iOS/Android)
2. Execute `pnpm run qr` para gerar QR code
3. Escaneie o QR code com a câmera ou Expo Go

### Via Emulador

```bash
pnpm run android    # Android Emulator
pnpm run ios        # iOS Simulator (macOS only)
```

## 🚀 Deploy

### Backend no Render

1. Crie uma conta em [render.com](https://render.com)
2. Conecte seu repositório GitHub
3. Crie um novo Web Service
4. Configure:
   - **Build Command**: `pnpm install && pnpm build`
   - **Start Command**: `pnpm start`
   - **Environment Variables**: Adicione `DATABASE_URL` e `NODE_ENV=production`

### Frontend (Expo)

O app é testado via Expo Go. Para build de produção:

```bash
eas build --platform all
```

## 👤 Usuários Padrão

| Usuário | Senha | Papel |
|---------|-------|-------|
| admin | admin123 | Administrador |

Novos motoristas devem ser criados pelo admin.

## 📊 Estrutura do Projeto

```
├── app/                    # Telas do app (Expo Router)
│   ├── (admin)/           # Telas do administrador
│   ├── (driver)/          # Telas do motorista
│   ├── (auth)/            # Telas de autenticação
│   └── index.tsx          # Roteamento principal
├── server/                # Backend Node.js
│   ├── api.ts             # Rotas da API
│   ├── db-config.ts       # Configuração do banco
│   └── _core/index.ts     # Inicialização do servidor
├── lib/                   # Utilitários
│   ├── api-client.ts      # Cliente HTTP
│   ├── auth-context.tsx   # Contexto de autenticação
│   └── database.ts        # Tipos TypeScript
├── drizzle/               # Migrações do banco
└── package.json
```

## 🔐 Segurança

- Senhas são armazenadas em hash no banco de dados
- JWT para autenticação de API
- CORS configurado para múltiplas origens
- Validação de entrada em todas as rotas

## 🐛 Troubleshooting

### Erro de conexão com banco de dados

Verifique se a URL do PostgreSQL está correta em `.env`:

```bash
psql "postgresql://user:password@host/database?sslmode=require"
```

### App não conecta ao backend

1. Certifique-se que o backend está rodando: `pnpm run dev:server`
2. Verifique a URL em `EXPO_PUBLIC_API_URL`
3. Tente `http://localhost:3000` no emulador ou IP da máquina no celular

### Erro ao fazer build

```bash
pnpm install --force
pnpm run check  # Verificar tipos TypeScript
```

## 📞 Suporte

Para suporte, entre em contato via WhatsApp: **(19) 99560-5536**

## 📄 Licença

Propriedade privada - Todos os direitos reservados

## 🤝 Contribuições

Contribuições são bem-vindas! Abra uma issue ou pull request.

---

**Desenvolvido com ❤️ para EscalaOnibus**
