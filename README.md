# API N703 - Técnicas de Integração de Sistemas

## Descrição
API REST de agregação que consulta informações geográficas e climáticas para cidades brasileiras.
O usuário informa apenas o **nome da cidade**. A aplicação obtém coordenadas e busca dados climáticos via APIs públicas externas.

## Endpoints

### Health Check
- `GET /api/v1/health`

### Clima por Cidade
- `GET /api/v1/clima/{nome_cidade}`

### Listagem de Cidades por Estado
- `GET /api/v1/cidades/{sigla_uf}?limite=10`

## Como rodar

### Pré-requisitos
- Python 3.10+
- pip

### Instalação
```bash
pip install fastapi uvicorn requests
pip install pytest fastapi.testclient
uvicorn src.main:app --host 0.0.0.0 --port 3000 --reload
pytest -q
