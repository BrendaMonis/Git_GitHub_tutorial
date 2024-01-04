# Git_GitHub_tutorial
Olá!

Neste tutorial será abordado sobre:
- O uso do Git e GitHub pelo terminal do RStudio visando facilitar o gerenciamento de arquivos. 

Espero que gostem do conteúdo preparado!



Atenciosamente, Brenda Monis Moreno. 🙂

## O que o Git e GitHub fazem? 
Essas ferramentas são responsáveis por gerenciar os arquivos e atualizar as suas versões, ou seja, são um `sistema de Controle de Versão`, 
visto que permite o acompanhamento das mudanças de seus códigos. Assim sendo, tal ferramenta é essencial para o armazenamento/ restauração
de versões, gerenciamento de backups e trabalhos colaborativos. Mas qual a diferença entre eles? 🤔

### 1. Git:
- É um software livre e muito utilizado no desenvolvimento de softwares onde diversas pessoas estão contribuindo simultaneamente, 
podendo criar e editar arquivos. Logo, para esta aula será necessário realizar o Download do [Git.](https://git-scm.com/downloads)
<img src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png">

### 2. GitHub:
-  GitHub é uma plataforma onde você pode armazenar seus projetos. É como se fosse uma `rede social`, só que de códigos, onde seus 
desenvolvedores podem disponibilizá-los para outras pessoas verem. Portanto, para essa aula será necessário ter uma conta no [GitHub.](https://github.com)
<img src="https://cdn-icons-png.flaticon.com/512/25/25231.png">

## Etapas para obter atualizações remotas do seu código do RStudio:
1. Fazer o Download do [Git.](https://git-scm.com/downloads);
2. RStudio → File → New Project; 
<img src="https://media.discordapp.net/attachments/1080588468301877271/1080929056180146266/Screenshot_2023-03-02_at_16-01-31_Design_sem_nome.png">
3. Version Control → Git;
<img src="https://media.discordapp.net/attachments/1080588468301877271/1080932176310304778/Screenshot_2023-03-02_at_16-15-02_Design_sem_nome.png">
<img src="https://media.discordapp.net/attachments/1080588468301877271/1080932320485310484/Screenshot_2023-03-02_at_16-15-40_Design_sem_nome.png">
4. GitHub → Criar um novo repositório → Copiar URL;
<img src="https://media.discordapp.net/attachments/1080588468301877271/1080931473328189490/Screenshot_2023-03-02_at_16-12-13_Design_sem_nome.png">
5. RStudio → Git → Colar URL;

- OBS: nesta parte poderá pedir para fazer o login no GitHub.
<img src="https://media.discordapp.net/attachments/1080588468301877271/1080932476735725598/Screenshot_2023-03-02_at_16-16-14_Design_sem_nome.png">

Após isso, será necessário criar um SSH key e um personal access token 

6. SSH key: 

- RStudio: Tools → Global Options → Git/SVN → Create SSH key → Apply → View public key → copiar → ok. 
- GitHub: Settings → SSH e GPT keys → New SSH → Add title → Colar Key. 

7. Personal access token:

- GitHub: Settings → Developer Settings → Personal access tokens  → tokens (classic) → Generate New Token (classic) → Colocar Note → habilitar repo → Generate token → Copiar código. 
- RStudio: 1. credentials::set_github_pat("colar seu token aqui"); 2. rodar isso no RStudio; 3. instalar os pacotes exigidos; 4. rodar aquele código novamente.

8. Fazer alterações no documento; 
<img src="https://media.discordapp.net/attachments/1080588468301877271/1080938159812116521/Screenshot_2023-03-02_at_16-38-53_Design_sem_nome.png">


### Sincronizando através do terminal: 
<img src="https://media.discordapp.net/attachments/1080588468301877271/1082293190335418368/Screenshot_2023-03-06_at_10-18-28_testes_minicurso_Testes_minicurso_RStudio_Server.png">

1. `echo "# testes_minicurso" >> README.md`

2. `git init`

3. `git add README.md`


4. `git commit -m "first commit"`


5. `git branch -M main`


6. `git remote add origin https://github.com/BrendaMonis/testes_minicurso.git`

- Deve substituir esse link pelo seu link do repositório do GitHub; 
7. `git push -u origin main`

### Sincronizando através do Git:
<img src="https://media.discordapp.net/attachments/1080588468301877271/1082297471092396042/Screenshot_2023-03-06_at_10-40-08_testes_minicurso_Testes_minicurso_RStudio_Server.png">

- OBS: Antes de iniciar esta etapa deve salvar os Scripts. 

1. `Commit`
<img src="https://media.discordapp.net/attachments/1080588468301877271/1082305512630128670/Screenshot_2023-03-06_at_11-12-02_Design_sem_nome.png">

2. `Selecionar os arquivos`

3. `Escrever algo em Commit`

4. `Clicar em Commit`
<img src="https://media.discordapp.net/attachments/1080588468301877271/1082321911821893733/Screenshot_2023-03-06_at_12-17-02_Design_sem_nome.png?width=969&height=155">

5. `Clicar em Push` 
<img src="https://media.discordapp.net/attachments/1080588468301877271/1082322710505476197/Screenshot_2023-03-06_at_12-20-26_Design_sem_nome.png">

- OBS: pode pedir seu login no GitHub.

Após isso, os seus códigos já estarão disponíveis no seu repositório do GitHub! 🙏
