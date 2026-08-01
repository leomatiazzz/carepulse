# CarePulse

**CarePulse** é uma aplicação web desenvolvida em Python com Django para gestão, cadastro e acompanhamento de pacientes, registro de consultas e gerenciamento de tarefas para atendimentos clínicos e psicológicos.

Repositório oficial: [https://github.com/leomatiazzz/carepulse](https://github.com/leomatiazzz/carepulse)

---

## 🚀 Funcionalidades

- **Gestão de Pacientes**: Cadastro completo com nome, e-mail, telefone, queixa inicial, foto de perfil e controle de status de pagamento.
- **Prontuário e Consultas**: Registro detalhado de consultas com acompanhamento de humor, anotações clínicas, upload de vídeos explicativos e vinculação de tarefas.
- **Planos de Ação e Tarefas**: Associação de tarefas personalizadas a cada consulta com instruções e frequência definida.
- **Link Público de Consulta**: Geração de link externo para compartilhamento de informações da consulta com o paciente (com bloqueio automático se o pagamento estiver em atraso).
- **Painel de Administração**: Integração nativa com o Django Admin para gerenciamento completo dos dados.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: Python 3.11+
- **Framework Web**: Django 5.1.6
- **Banco de Dados**: SQLite
- **Manipulação de Mídia**: Pillow
- **Frontend**: HTML5, CSS3, Templates Django e Tailwind CSS (via CDN)

---

## 📁 Estrutura do Projeto

```text
carepulse/
├── core/                        # Configurações globais do projeto Django
│   ├── settings.py              # Definições de ambiente, apps e middlewares
│   ├── urls.py                  # Roteamento raiz da aplicação
│   ├── asgi.py                  # Interface ASGI
│   └── wsgi.py                  # Interface WSGI
├── pacientes/                   # Aplicação principal de pacientes
│   ├── admin.py                 # Registro dos modelos no Django Admin
│   ├── apps.py                  # Configuração do app pacientes
│   ├── models.py                # Modelos de dados (Pacientes, Consultas, Tarefas)
│   ├── tests.py                 # Suíte de testes unitários
│   ├── urls.py                  # Roteamento do módulo de pacientes
│   ├── views.py                 # Regras de negócio e rotas das telas
│   ├── migrations/              # Histórico de migrações do banco de dados
│   └── templates/               # Templates HTML das páginas do app
├── docs/                        # Documentações técnicas do sistema
│   ├── arquitetura.md           # Visão geral da arquitetura
│   └── faq.md                   # Perguntas frequentes
├── templates/                   # Templates HTML globais (base.html)
├── media/                       # Armazenamento de arquivos enviados (fotos/vídeos)
├── db.sqlite3                   # Banco de dados local
├── manage.py                    # Script de gerenciamento do Django
└── requirements.txt             # Dependências Python do projeto
```

---

## 🗄️ Modelos de Dados

- **Pacientes**: Armazena informações cadastrais (`nome`, `email`, `telefone`, `queixa`, `foto`, `pagamento_em_dia`).
- **Consultas**: Registra o atendimento (`humor`, `registro_geral`, `video`, `paciente`, `tarefas`, `data`).
- **Tarefas**: Define atividades e orientações para o paciente (`tarefa`, `instrucoes`, `frequencia`).

---

## ⚙️ Instalação e Configuração

### 1. Clonar o repositório
```bash
git clone https://github.com/leomatiazzz/carepulse.git
cd carepulse
```

### 2. Criar e ativar o ambiente virtual

- **Windows (PowerShell):**
  ```powershell
  python -m venv venv
  .\venv\Scripts\activate
  ```

- **Linux / macOS:**
  ```bash
  python3 -m venv venv
  source venv/bin/activate
  ```

### 3. Instalar as dependências
```bash
pip install -r requirements.txt
```

### 4. Executar as migrações do banco de dados
```bash
python manage.py migrate
```

### 5. Iniciar o servidor de desenvolvimento
```bash
python manage.py runserver
```

Acesse a aplicação em: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

---

## 📌 Principais Rotas

| Rota | Descrição |
| :--- | :--- |
| `/pacientes/` | Painel principal, listagem e cadastro de pacientes |
| `/pacientes/<id>/` | Ficha do paciente e registro de novas consultas |
| `/pacientes/atualizar_paciente/<id>/` | Atualização do status de pagamento do paciente |
| `/pacientes/excluir_consulta/<id>/` | Remoção de registro de consulta |
| `/pacientes/consulta_publica/<id>/` | Página pública de visualização da consulta |
| `/admin/` | Painel de administração nativo do Django |

---

## 📚 Documentação Complementar

- [CONTRIBUTING.md](CONTRIBUTING.md) — Guia de contribuição e boas práticas.
- [CHANGELOG.md](CHANGELOG.md) — Histórico de versões e alterações.
- [SECURITY.md](SECURITY.md) — Política de segurança e reporte de vulnerabilidades.
- [docs/arquitetura.md](docs/arquitetura.md) — Detalhes da arquitetura da aplicação.
- [docs/faq.md](docs/faq.md) — Dúvidas frequentes de desenvolvimento e uso.
