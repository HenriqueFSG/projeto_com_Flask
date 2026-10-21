## Projeto com Flask



#### Como instalar e configurar o uv na sua máquina virtual pelo PowerShell



* Usar o comando: powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex" para instalar na máquina
* Digite: uv initi para inicializar o uv
* Para verificar a versão do python digite: python -V 
* Se a versão for inferior a 3.15.0 instale utilizando: uv python install 3.15.0
* Inicialize o ambiente virtual colocando: uv venv
* Para analisa os pacotes do uv e do python que 
* Digite: uv add Flask para instalar o micro-framework Flask


#### Utilização do uv em python 

* Importamos os módulos Flask e markupsafe, e utilizamos as funções Flask, render_template, request, escape para utilizar em um arquivo em python 
* Usamos a função route para fazer diferentes rotas do cabeçalho de uma URL
* Criamos uma pasta chamada: Templates para utilizar uma pagina HTML ao invés de só utilizar snippets de código HTML  

