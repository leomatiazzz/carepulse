# Contribuindo

Obrigado por considerar contribuir com o CarePulse.

## Fluxo recomendado

1. Faça um fork do repositório.
2. Crie uma branch para a sua alteração.
3. Implemente a mudança com o menor escopo possível.
4. Valide o projeto localmente com as migrações e o servidor de desenvolvimento.
5. Abra um Pull Request com uma descrição clara do problema e da solução.

## Ambiente de desenvolvimento

Use um ambiente virtual e instale as dependências a partir do arquivo `requirements.txt`:

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

## Boas práticas

- mantenha a documentação e os comandos alinhados com o que existe no repositório;
- evite adicionar funcionalidades sem evidência no código ou na arquitetura atual;
- documente mudanças relevantes em `CHANGELOG.md`;
- teste a alteração com `python manage.py test` quando houver cobertura real de testes.

## Observações

Este repositório ainda está em evolução e a documentação pública deve refletir apenas o comportamento atualmente implementado no código.
