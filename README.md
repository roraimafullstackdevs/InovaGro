PROJETO CHAMAGRO
1. Descrição do Projeto
ChamAgro
2. Objetivo
O presente projeto visa aprimorar a comunicação entre o Instituto de Assistência Técnica
e Extensão Rural – IATER e os agricultores do estado de Roraima, facilitando a troca de
informações sobre o controle de pragas. Com isso, busca-se proteger o meio ambiente e
aumentar a produtividade agrícola. A plataforma proposta visa reduzir o tempo de
resposta entre a detecção de pragas e a adoção de medidas corretivas, permitindo que o
IATER, e, quando necessário, a Agência de Defesa Agropecuária de Roraima (ADERR),
possam atuar de forma rápida e eficaz.
2. Tecnologias Utilizadas
a) Frontend
Next.js: Framework React que fornece uma interface rápida e amigável ao SEO.
Next Auth: Gerencia autenticação por meio de vários provedores, como e-mail/senha.
React Query: Gerencia a busca de dados e o gerenciamento de estado, proporcionando
uma experiência de usuário fluida.
React Hook Form, Zod e Yup: Utilizados para validação confiável e contínua de
formulários.
Shadcn UI Components: Fornece componentes de interface de usuário consistentes e
acessíveis.
Tailwind CSS: Framework CSS utilizado para estilizar a interface de forma responsiva
e eficiente.
Framer Motion: Biblioteca para animações e transições suaves, aprimorando a
experiência do usuário.
Lucide React Icons: Biblioteca de ícones para melhorar a estética e a usabilidade do
aplicativo.
Date-fns: Biblioteca para manipulação de datas, essencial para recursos de calendário
e agendamento.
JavaScript: Linguagem base usada tanto no frontend quanto no backend.
b) Backend
Node.js: Ambiente de execução JavaScript no servidor, para construção da API.
Express: Framework para Node.js que organiza a estrutura do backend, rotas e
requisições.
Prisma ORM: ORM para facilitar a manipulação de dados no PostgreSQL de forma
segura.
c) Banco de Dados
PostgreSQL: Sistema de banco de dados relacional para armazenar informações sobre
usuários, pragas, notificações e conversas.
Geolocalização e Mapas
Google Maps API / Mapbox: Exibe áreas afetadas em um mapa, auxiliando na análise
de regiões impactadas.
Notificações em Tempo Real
WebSockets (via Socket.IO): Comunicação em tempo real, possibilitando envio de
notificações push e chat entre IATE e agricultores.
Armazenamento de Imagens
Google Firebase / Appwrite: Plataformas para armazenamento seguro de imagens
enviadas pelos agricultores, como fotos de áreas afetadas.
Essas ferramentas combinadas permitem uma aplicação robusta, segura e de fácil
utilização para os usuários.
3. Dependências Necessárias
a) Backend
Node.js: v20.17.0
Express: v4.18.3
Prisma ORM: v5.22.0
Socket.IO: v4.7.2
b) Frontend
Next.js: v14.0.0
Next Auth: v4.22.1
React Query: v5.0.0
React Hook Form: v7.45.0
Zod: v3.22.2
Yup: v1.1.0
Shadcn UI Components: v0.1.0
Tailwind CSS: v3.3.2
Framer Motion: v10.0.0
Lucide React Icons: v0.236.0
Date-fns: v2.30.0
Observação: Certifique-se de usar as versões recomendadas para evitar problemas de
compatibilidade.

4. Variáveis de Ambientes
PORT=5000
DB_PRODUCTION=false
NODE_ENV=production
POSTGRES_URL="postgres://default:bU4mrpoklF3G@ep-royal-math-a4c615f1.us-
east-1.aws.neon.tech:5432/verceldb?sslmode=require"
DB_LOCAL_URL="postgres://postgres:admin@localhost:5432/chamagro_db"
JWT_SALTROUND = 10
JWT_SECRET="2NmORAkTBKcDpxFOMSQMPdKWKqZ4tQq+9XY2jBnB8ywYrd
3NTY9YZn8LHSM="
JWT_ACCESS_EXPIRATION_MINUTES=30
JWT_REFRESH_EXPIRATION_DAYS=30
JWT_RESET_PASSWORD_EXPIRATION_MINUTES=10
JWT_VERIFY_EMAIL_EXPIRATION_MINUTES=10
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USERNAME=devacc2010@gmail.com


5. Como rodar a Aplicação
   5.1 Pré-requisitos
Antes de iniciar, verificar se possui:
Node.js (versão X.X.X ou superior)
NPM ou Yarn (para gerenciar pacotes)
PostgreSQL (banco local ou em nuvem configurado)
Firebase / Appwrite (configurações e conta de armazenamento)
5.2 Instalação
Clone o repositório:
1) git clone [URL do repositório]
2) Instale as dependências:
3) cd [diretório do projeto]
4) npm install # ou yarn install
Configure as variáveis de ambiente: Crie um arquivo. env no diretório raiz e adicione as
chaves necessárias, como credenciais do banco de dados e chaves de autenticação.
Certifique-se de incluir o. env no arquivo. gitignore para proteger suas credenciais
sensíveis:
DATABASE_URL="postgresql://usuario:senha@localhost:5432/chamagro"
GOOGLE_MAPS_API_KEY="sua-chave-google-maps"
FIREBASE_API_KEY="sua-chave-firebase"

Construa o projeto:
npm run build
Inicie o servidor: Para um ambiente de produção, execute:
npm start
Para um ambiente de desenvolvimento, execute:
npm run dev
Por padrão, a aplicação é executada em http://localhost:3000, mas você pode configurar
a porta usando a variável de ambiente PORT no arquivo. env.

