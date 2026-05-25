# 🎨 Visualy AI

**Plataforma inteligente de design gráfico com IA para profissionais e iniciantes**

Visualy AI é um aplicativo especializado que utiliza inteligência artificial para ajudar criadores de conteúdo, pequenos empreendedores, freelancers e profissionais de design a criar:

- ✨ Posts e Stories para redes sociais
- 🎯 Flyers e Banners profissionais
- 📝 Legendas e Textos de venda otimizados
- 🎨 Identidade visual e branding
- 📸 Melhorias em fotos de produtos
- 💡 Ideias criativas personalizadas
- 📦 Modelos prontos por nicho de mercado

## 🎯 Características Principais

### IA Integrada
- Geração de imagens com OpenAI DALL-E 3
- Análise e sugestões de design
- Otimização de textos e legendas
- Ideias criativas baseadas em IA

### Editor Visual
- Canvas editor profissional
- Biblioteca de templates por nicho
- Edição em tempo real
- Exportação em múltiplos formatos

### Gerenciamento de Projetos
- Histórico de criações
- Versioning de designs
- Organização por campanhas
- Compartilhamento de projetos

## 🏗️ Stack Tecnológico

### Backend
- **Framework:** Python FastAPI
- **Banco de Dados:** PostgreSQL
- **Autenticação:** JWT
- **IA/ML:** OpenAI API (DALL-E 3)
- **Cache:** Redis
- **Fila:** Celery + RabbitMQ
- **Processamento:** Pillow, OpenCV

### Frontend
- **Framework:** React 18+
- **UI:** TailwindCSS + Shadcn/ui
- **Editor:** Fabric.js
- **State Management:** Redux Toolkit
- **HTTP Client:** Axios

### Infraestrutura
- **Containerização:** Docker + Docker Compose
- **CI/CD:** GitHub Actions
- **Variáveis de Ambiente:** .env

## 🚀 Quick Start

### Pré-requisitos
- Python 3.10+
- Node.js 18+
- PostgreSQL 14+
- Redis
- Git

### Setup Local (Sem Docker)

**1. Clone o repositório:**
```bash
git clone https://github.com/IsadoraBenites/visualy-ai-app.git
cd visualy-ai-app
```

**2. Backend:**
```bash
cd backend
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
# Configure as variáveis de ambiente em .env
python -m uvicorn app.main:app --reload
# Backend rodando em http://localhost:8000
```

**3. Frontend:**
```bash
cd frontend
npm install
cp .env.example .env
npm run dev
# Frontend rodando em http://localhost:5173
```

### Setup Local (Com Docker)

```bash
git clone https://github.com/IsadoraBenites/visualy-ai-app.git
cd visualy-ai-app

# Copiar arquivo de ambiente
cp .env.example .env

# Iniciar todos os containers
docker-compose up -d

# Verificar status
docker-compose ps

# Ver logs
docker-compose logs -f backend
```

**Acessos:**
- Frontend: http://localhost:5173
- Backend: http://localhost:8000
- API Docs: http://localhost:8000/docs
- RabbitMQ: http://localhost:15672 (user: visualy, password: visualy_password)

## 🔑 Variáveis de Ambiente

### Backend (.env)
```
ENVIRONMENT=development
DATABASE_URL=postgresql://visualy_user:visualy_password@localhost:5432/visualy_db
JWT_SECRET_KEY=your-super-secret-key-change-in-production
OPENAI_API_KEY=sk-your-openai-api-key
REDIS_URL=redis://localhost:6379
CORS_ORIGINS=["http://localhost:5173","http://localhost:3000"]
```

### Frontend (.env)
```
VITE_API_URL=http://localhost:8000
VITE_APP_NAME=Visualy AI
```

## 🎨 Design Visual

**Paleta de Cores:**
- 🌸 Rosa Claro: `#F8E9F3` (background, highlights)
- ⚫ Grafite: `#2C3E50` (text, dark elements)
- ⚪ Branco: `#FFFFFF` (clean, spacious)
- ✨ Champagne/Prata: `#E8D7C3` / `#C0C0C0` (accents, premium feel)

## 📁 Estrutura do Projeto

```
visualy-ai-app/
├── backend/                 # API Backend (FastAPI)
│   ├── app/
│   │   ├── api/            # Rotas da API
│   │   ├── models/         # ORM Models
│   │   ├── schemas/        # Pydantic schemas
│   │   ├── services/       # Lógica de negócio
│   │   ├── tasks/          # Celery tasks
│   │   ├── core/           # Configurações
│   │   ├── db/             # Database
│   │   └── main.py         # Entry point
│   ├── tests/              # Testes
│   ├── Dockerfile
│   ├── requirements.txt
│   └── .env.example
├── frontend/                # Frontend React
│   ├── src/
│   │   ├── components/     # Componentes reutilizáveis
│   │   ├── pages/          # Páginas (rotas)
│   │   ├── hooks/          # Custom React hooks
│   │   ├── services/       # Chamadas à API
│   │   ├── store/          # Redux store
│   │   ├── styles/         # Estilos globais
│   │   └── App.jsx
│   ├── Dockerfile
│   ├── package.json
│   ├── tailwind.config.js
│   └── .env.example
├── docker-compose.yml
├── .github/workflows/       # CI/CD
├── .env.example
└── README.md
```

## 🧪 Testes

```bash
# Backend
cd backend
pytest

# Frontend
cd frontend
npm test
```

## 📚 Documentação

Documentation em `/docs`:
- [API Documentation](docs/API.md)
- [Setup Guide](docs/SETUP.md)
- [Architecture](docs/ARCHITECTURE.md)

## 🤝 Contribuindo

Contribuições são bem-vindas! Por favor:
1. Faça um fork
2. Crie uma branch (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📝 Licença

MIT License

## 📞 Suporte

Para suporte, abra uma issue no GitHub.

---

**Feito com ❤️ por Isadora Benites**

Versão: 1.0.0 (Early Access)
