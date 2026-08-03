# O Meu Portefólio Pessoal

Este é o repositório do meu site pessoal/portefólio, construído com [Jekyll](https://jekyllrb.com/) e alojado gratuitamente no GitHub Pages.

---

## 🛠️ Como preparar o ambiente de desenvolvimento (Setup do Zero)

Se estiveres num computador novo e quiseres editar o site localmente, segue estes passos rigorosamente.

### 1. Pré-requisitos (O que instalar)

Antes de descarregares o código, precisas das ferramentas base no teu sistema:

- **Git:** Instalar o [Git for Windows](https://git-scm.com/download/win).
- **Ruby + Devkit:** Fazer o download do [RubyInstaller with Devkit](https://rubyinstaller.org/downloads/) (versão recomendada com MSYS2). Durante a instalação, deixa as opções padrão selecionadas e no final corre o terminal que aparece para instalar o MSYS2 base.

### 2. Configurar o Projeto Localmente

Abre o terminal (PowerShell) na pasta onde queres guardar o projeto e executa:

1. **Clonar o repositório:**

   ```powershell
   git clone [https://github.com/RAGilSimoes/RAGilSimoes.github.io.git](https://github.com/RAGilSimoes/RAGilSimoes.github.io.git)
   ```

2. **Entrar na pasta do projeto:**

   ```powershell
   cd RAGilSimoes.github.io
   ```

3. **Instalar as dependências do Jekyll (Gemas):**

   ```powershell
   bundle install
   ```

4. **Correr o Servidor Local:**
   ```powershell
   bundle exec jekyll serve --config _config.yml,_config.dev.yml
   ```

## ⚠️ Troubleshooting (Resolução de Problemas Comuns no Windows)

#### Erro de Certificado SSL (SSL_connect returned=1 errno=0 peeraddr=...):

Se ao correres um comando do bundle ou tentares arrancar o servidor o Ruby reclamar de certificados SSL, tens de forçar o caminho do certificado manualmente.

1. Faz o download do ficheiro cacert.pem (por exemplo em https://curl.se/ca/cacert.pem).

2. Guarda-o numa pasta segura.

3. No terminal (PowerShell), antes de correres o comando do Jekyll, define a variável de ambiente:
   ```powershell
   $env:SSL_CERT_FILE="C:\Caminho\Para\O\Teu\cacert.pem"
   ```

#### Erro ao instalar a gema wdm:

O wdm costuma falhar a compilação nas versões mais recentes do Ruby no Windows. Apenas ignora ou remove essa linha do Gemfile, pois o Jekyll tem um método de fallback para ler as alterações aos ficheiros sem necessitar dessa gema.

---

## 📄 Licença e Direitos de Autor

Este repositório contém uma mistura de código aberto e conteúdo estritamente pessoal. Por favor, respeita as seguintes regras de licenciamento:

- **O Código e o Tema (Open Source):** A estrutura web (HTML, CSS, Liquid) é baseada num tema de código aberto. Estás à vontade para clonar, estudar e usar o código estrutural para construíres o teu próprio site, respeitando a licença original do criador do tema.
- **O Conteúdo Pessoal (Todos os Direitos Reservados):** Todo o conteúdo escrito (artigos do blog, descrições de projetos, secção "Sobre Mim"), fotografias pessoais, currículo e certificados **são da minha autoria exclusiva (© Ricardo André Simões)**. Não tens permissão para copiar, reproduzir ou utilizar a minha identidade, textos ou imagens nos teus próprios projetos.
