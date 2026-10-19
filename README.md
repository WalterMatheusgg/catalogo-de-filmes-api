<div align="center">

# 🎬 Movie API
### CRUD de filmes com Django REST Framework

![Python](https://img.shields.io/badge/Python-3-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![DRF](https://img.shields.io/badge/DRF-REST%20API-A30000?style=for-the-badge)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white)

</div>

## 🎯 Visão geral

API de estudo desenvolvida com **Django e Django REST Framework**, expondo operações CRUD para um catálogo de filmes. O código utiliza **generic class-based views** e serialização de modelos.

> Projeto educacional da trilha Django, originalmente baseado em exercício da [Mate Academy](https://github.com/mate-academy/py-task-guideline). Não possui suíte de testes própria implementada em `cinema/tests.py`.

## ✨ Recursos

O modelo `Movie` possui os campos **`title`**, **`description`** e **`duration`** (minutos).

| Método | Rota | Operação |
|---|---|---|
| GET | `/api/cinema/movies/` | Listar filmes |
| POST | `/api/cinema/movies/` | Cadastrar filme |
| GET | `/api/cinema/movies/{id}/` | Consultar filme |
| PUT | `/api/cinema/movies/{id}/` | Atualizar filme |
| DELETE | `/api/cinema/movies/{id}/` | Remover filme |

## 🏗️ Estrutura

```text
cinema/
├── models.py         # Entidade Movie
├── serializers.py    # Serialização DRF
├── views.py          # ListCreate / RetrieveUpdateDestroy
├── urls.py           # Rotas
└── migrations/       # Migração do modelo
cinema_service/       # Configurações Django
manage.py             # Gerenciamento
cinema_service_db_data.json # Fixture
```

## 🚀 Como executar localmente

Utilize **Python compatível com as dependências do projeto** e um ambiente virtual limpo:

```bash
git clone https://github.com/WalterMatheusgg/py-movie-api.git
cd py-movie-api
python3 -m venv .venv-local
source .venv-local/bin/activate
python -m pip install django djangorestframework
python manage.py migrate
python manage.py runserver
```

Acesse `http://127.0.0.1:8000/api/cinema/movies/`. Para adicionar os dados de exemplo:

```bash
python manage.py loaddata cinema_service_db_data.json
```

**Importante:** versões não estão fixadas em um arquivo de dependências próprio. O repositório inclui `venv/`, `db.sqlite3` e `__pycache__` versionados; recomenda-se removê-los do Git futuramente e adicionar `requirements.txt` e `.gitignore` — isso **não foi alterado** nesta atualização de documentação.

## 🧠 Conceitos praticados

Modelagem Django, serializers, views genéricas, URLs, CRUD REST, migrations e fixtures.

## 👨‍💻 Autor

**Walter Matheus Soares da Silva** · [GitHub](https://github.com/WalterMatheusgg)
