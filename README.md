# Projeto com Flask e UV Astral

Este projeto consiste em uma aplicação web simples desenvolvida em Python com o micro-framework **Flask**, utilizando o **UV Astral** para gerenciamento de dependências e ambientes virtuais.

## 📁 Estrutura do Projeto

Para organizar o projeto, crie a seguinte estrutura de arquivos e diretórios:

* **`projeto_com_Flask/`**: Diretório raiz do projeto.
  * **`app.py`**: Arquivo principal da aplicação Python.
  * **`templates/`**: Pasta destinada aos arquivos HTML do projeto.
    * **`ola.html`**: Arquivo HTML para renderização de páginas.

## 🚀 Instalação e Configuração do UV (PowerShell)

O **UV** é um gerenciador de pacotes e ambientes virtuais para Python rápido e moderno.

### 1. Instalação

Execute o comando abaixo no PowerShell para realizar a instalação:

```
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 2. Comandos do UV para Gerenciamento do Projeto

* **Verificar versão do UV instalada:**
  ```

  jp
  uv -V
  ```

* **Inicializar a estrutura do projeto:**
  ```
  uv init
  ```

* **Verificar e instalar a versão do Python (3.15.0):**
  ```
  python -V
  uv python install 3.15.0
  ```

* **Criar o ambiente virtual (`venv`):**
  ```
  uv venv
  ```

* **Adicionar o micro-framework Flask:**
  ```
  uv add Flask
  ```

* **Sincronizar pacotes e dependências:**
  ```
  uv sync
  ```

## 💻 Código da Aplicação (`app.py`)

No arquivo `app.py`, importamos os módulos do `Flask` e `markupsafe` (`Flask`, `request`, `render_template`, `escape`), configuramos a rota principal e a inicialização da aplicação:

```python
from flask import Flask, request, render_template
from markupsafe import escape

app = Flask(__name__)

@app.route("/")
def ola_mundo():
    return "<p>Olá, Mundo!</p>"

if __name__ == "__main__":
    app.run(debug=False, port=5000)
```

## 🎨 Utilização de Templates (`templates/ola.html`)

Ao invés de retornar apenas snippets de código HTML diretamente na função, utilizamos a pasta `templates/` com arquivos HTML para renderização dinâmica de conteúdo.

### Exemplo em `ola.html`:

```html
{% if nome %}
    <h1>Olá, {{ nome }}!</h1>
{% else %}
    <h1>Olá, Flask</h1>
{% endif %}
```

> **Nota:** Blocos condicionais iniciados com `{% if %}` devem ser explicitamente finalizados utilizando `{% endif %}`.

## ▶️ Como Executar o Projeto

Para rodar a aplicação Flask através do UV, utilize o comando:

```
uv run flask run
```
