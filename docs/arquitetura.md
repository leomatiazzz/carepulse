# Arquitetura do projeto

## Visão geral

O projeto é uma aplicação Django monolítica, com um único app principal chamado `pacientes`.

## Componentes

- `core/`: configuração principal do projeto Django.
- `pacientes/`: domínio da aplicação, incluindo modelos, views, URLs e templates.
- `templates/`: templates globais compartilhados.
- `media/`: uploads de fotos e vídeos.

## Fluxo principal

1. O usuário acessa a rota principal de pacientes.
2. O app lista os pacientes cadastrados.
3. O usuário pode visualizar um paciente e registrar uma consulta.
4. A consulta pode ser compartilhada por link público, condicionado ao status de pagamento do paciente.

## Observações

- Não há API REST separada.
- Não há serviço de fila, broker ou backend distribuído.
- O banco padrão é SQLite.
