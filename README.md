# github-pages-vue

2/11/2024 wpp

O comando git add dist -f significa o seguinte:

git add dist → adiciona o diretório chamado dist (ou arquivo, se fosse um arquivo) à área de staging, ou seja, prepara esse conteúdo para o próximo commit.

-f → é a abreviação de --force, e serve para forçar a adição de arquivos que normalmente o Git ignoraria.

💡 Em resumo:
👉 git add dist -f força o Git a adicionar a pasta dist, mesmo que ela esteja listada no .gitignore.

git subtree push --prefix dist origin gh-pages

🧩 Quebra do comando:

git subtree → é um recurso do Git que permite tratar uma subpasta de um repositório como se fosse um repositório separado.

push → envia (faz push) o conteúdo para um branch remoto.

--prefix dist → indica que a pasta dist/ é o “subprojeto” que você quer enviar.

origin → é o nome do repositório remoto (padrão no GitHub).

gh-pages → é o nome do branch remoto para onde o conteúdo será enviado.

💡 Em outras palavras:

Esse comando pega o conteúdo da pasta dist e o envia para o branch gh-pages do repositório remoto (normalmente o GitHub).
É muito usado em projetos frontend (React, Vue, Angular, etc.) para publicar o site no GitHub Pages.

🔧 Exemplo prático:

Suponha que você tenha um projeto React.

Você roda o build:

npm run build

Isso cria a pasta dist com os arquivos do site.

Aí você faz o deploy:

git subtree push --prefix dist origin gh-pages

O Git então envia só o conteúdo de dist/ para o branch gh-pages, que o GitHub Pages usa para exibir o site.

# RESUMO

2- dentro da pasta -> npm run build 

3- git add dist -f 

4- git commit -m"adding dist"

5- git subtree push --prefix dist origin gh-pages

How to Deploy Your Vite App to Github Pages
https://www.youtube.com/watch?v=yo2bMGnIKE8

publicPath: '/menu-completo',

https://github.com/jaquemoura/menu-completo.git

0:45

1- Create a new repository -> deploying-vite-project-example -> create repository

2- git init

3- git add .

4- git commit -m"first commit"

5- git branch -M main

6- git remote add origin ...

7- git push -u origin main

Let's Start Deploying!

vue.config.js

base: '/deploying-vite-project-example/',

2- dentro da pasta -> npm run build 

3- git add dist -f 

4- git commit -m"adding dist"

5- git subtree push --prefix dist origin gh-pages

no painel do github

6- trocar main por gh-pages https://prnt.sc/MLya7DyFCi-D

7- Settings - Pages - source - Branch: gh-pages - save

https://jaquemoura.github.io/menu-completo/

https://learnvue.co/articles/deploy-vue-to-github-pages

gh-pages Nosso objetivo final é que este branch contenha apenas nossa pasta build – que para muitos projetos será dist.
