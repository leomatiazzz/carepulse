# 🩺 CarePulse (Consulta Pacientes)

O **CarePulse** é uma aplicação web desenvolvida em **Python** e **Django** criada para facilitar a gestão de atendimentos clínicos e psicológicos. O sistema permite o cadastramento e acompanhamento de pacientes, agendamento e registro de consultas, definição de tarefas e anexação de mídias relevantes (fotos e vídeos) para suporte ao acompanhamento do paciente.

---

## 📌 Funcionalidades

- 👤 **Gestão de Pacientes**: Cadastro completo de pacientes, incluindo dados de contato, foto de perfil, histórico e queixa principal.
- 📅 **Agendamento de Consultas**: Registro e acompanhamento de sessões e consultas de forma organizada.
- 📋 **Gestão de Tarefas**: Atribuição de atividades e tarefas terapêuticas/clínicas para acompanhamento da evolução do paciente.
- 🌐 **Consulta Pública / Compartilhável**: Visualização pública/simplificada de informações ou tarefas do paciente via link específico.
- 🖼️ **Suporte a Mídias**: Upload e armazenamento de imagens e vídeos de suporte na ficha do paciente.

---

## 🛠️ Tecnologias Utilizadas

- **Linguagem**: [Python 3.11+](https://www.python.org/)
- **Framework web**: [Django 5.1+](https://www.djangoproject.com/)
- **Banco de dados**: SQLite3 (desenvolvimento/local)
- **Manipulação de imagens**: Pillow (PIL)
- **Frontend**: HTML5, CSS3 / Bootstrap (Templates Django)

---

## 📂 Estrutura do Repositório

```text
.
├── core/                  # Configurações do projeto Django (settings, urls, wsgi/asgi)
├── pacientes/             # App Django de gestão de pacientes, consultas e tarefas
│   ├── migrations/        # Migrações do banco de dados
│   ├── templates/         # Páginas HTML (pacientes, consulta pública, etc.)
│   ├── models.py          # Modelos de dados (Pacientes, Consultas, Tarefas)
│   ├── views.py           # Lógica de controle e regras de negócio
│   └── urls.py            # Rotas específicas do app de pacientes
├── media/                 # Arquivos de mídia enviados (fotos de perfil, vídeos)
├── templates/             # Templates globais (ex: base.html)
├── db.sqlite3             # Banco de dados SQLite local
└── manage.py              # Script de gerenciamento do Django
```

---

## 🚀 Execução do Projeto

### Pré-requisitos

* Python 3.11 ou superior instalado.

### Passo-a-passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/CarePulse.git
   cd CarePulse
   ```

2. **Crie e ative o ambiente virtual (`venv`):**
   * **Linux/macOS:**
     ```bash
     python3 -m venv venv
     source venv/bin/activate
     ```
   * **Windows:**
     ```bash
     python -m venv venv
     venv\Scripts\activate
     ```

3. **Instale as dependências:**
   ```bash
   pip install django pillow
   ```

4. **Execute as migrações do banco de dados:**
   ```bash
   python manage.py migrate
   ```

5. **Inicie o servidor de desenvolvimento:**
   ```bash
   python manage.py runserver
   ```

6. **Acesse a aplicação:**
   Abra o navegador e acesse `http://127.0.0.1:8000/`.

---

## 📝 Boas Práticas (.gitignore)

Recomenda-se não versionar o ambiente virtual (`venv/`), arquivos compilados do Python (`__pycache__`), o banco local (`db.sqlite3`) e arquivos de mídia pessoais enviados durante os testes.

Exemplo de `.gitignore`:

```gitignore
venv/
__pycache__/
*.pyc
db.sqlite3
media/
```

---

## 📜 Licença

Este projeto está sob a licença MIT. Sinta-se à vontade para utilizar, modificar e distribuir.
