# FAQ

## Como instalar o projeto?

Crie um ambiente virtual, instale as dependências e rode as migrações:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Como acessar a tela de administração?

Acesse:

```text
http://127.0.0.1:8000/admin/
```

## O projeto suporta produção?

Não no estado atual. O projeto possui configuração de desenvolvimento local, com `DEBUG = True`, `ALLOWED_HOSTS = []` e banco SQLite.

## Onde ficam os uploads de mídia?

Os uploads são armazenados em `media/`, com subpastas `fotos/` e `video/`.
