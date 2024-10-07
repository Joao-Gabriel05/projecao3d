
# Guia para desenvolvedores

## Configurando seu ambiente de trabalho

Execute estas instruçõess imediatamente após criar seu projeto com o cookiecutter.

1. Navegue para o diretório que você criou

        cd my_awesome_project

2. Crie um ambiente virtual para seu desenvolvimento:

        conda create -n my_awesome_project python=3.12
        conda activate my_awesome_project

3. (opcional) Instale o aplicativo `gh` para criar automaticamente seu repositório no GitHub:

        conda install gh --channel conda-forge
        gh auth login

4. Instale seu módulo em modo editável:

        pip install -e .

5. Verifique que a ferramenta de linha de comando está funcionando:

        my_awesome_project-cli --help

## Sincronizando com Github

### Com o aplicativo `gh`

Na pasta-raiz de seu projeto recém-criado:

    git init
    git add *
    git commit -m "Commit inicial"
    gh repo create projecao3d --public --push --source .

### Sem o aplicativo `gh`

1. Em seu navegador, vá para o [GitHub](https://www.github.com) e faça login como Joao-Gabriel05
1. Crie um novo repositório (vazio, sem README inicial, sem gitignore, etc) chamado projecao3d (lembre-se de respeitar maiúsculas, minúsculas, etc).
1. Execute os comandos abaixo na pasta-raiz de seu projeto recém-criado:


        git init
        git add *
        git commit -m "Commit inicial"
        git remote add origin https://github.com/Joao-Gabriel05/projecao3d.git
        git push --set-upstream origin main


