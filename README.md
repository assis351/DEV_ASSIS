# DEV ASSIS — Site de portfólio

Site de uma página só, pronto para publicar de graça no **GitHub Pages**.

## O que tem na pasta

| Arquivo | Para que serve |
|---|---|
| `index.html` | O site inteiro (visual, mural de projetos, textos e contatos) |
| `favicon.ico`, `favicon.png`, `apple-touch-icon.png` | Ícone que aparece na aba do navegador e no celular |
| `icon-192.png`, `icon-512.png` | Ícones em tamanhos maiores (uso futuro) |
| `og-image.jpg` | Imagem que aparece quando alguém compartilha o link no WhatsApp, Instagram etc. |
| `robots.txt` | Avisa o Google que ele pode ler o site e onde está o mapa |
| `sitemap.xml` | Mapa do site para o Google |
| `README.md` | Este guia |

---

## PARTE 1 — Colocar o site no ar (GitHub Pages)

1. Crie uma conta grátis em https://github.com (se ainda não tiver).
2. Clique em **+** (canto superior direito) → **New repository**.
3. Em **Repository name** escreva: `dev-assis`
4. Deixe marcado **Public** e clique em **Create repository**.
5. Na página do repositório, clique em **uploading an existing file**.
6. Abra a pasta do site no seu computador, selecione **todos os arquivos de dentro dela** e arraste para a página do GitHub. (Arraste os arquivos, não a pasta.)
7. Role a página e clique em **Commit changes**.
8. Vá em **Settings → Pages**.
9. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
10. Em **Branch**, escolha **main** e a pasta **/ (root)**. Clique em **Save**.
11. Espere 1 a 3 minutos e atualize a página. Vai aparecer: **"Your site is live at …"**

O endereço do seu site será:

```
https://SEU-USUARIO.github.io/dev-assis/
```

(`SEU-USUARIO` é o nome de usuário que você escolheu no GitHub.)

---

## PARTE 2 — Trocar `SEU-USUARIO` pelo seu usuário (obrigatório)

Esses 3 arquivos têm o endereço do site e precisam do seu usuário real:

- `index.html` (aparece algumas vezes: canonical, og:url, og:image, twitter:image e no bloco de dados `ld+json`)
- `robots.txt`
- `sitemap.xml`

Como trocar direto no GitHub:

1. Clique no arquivo → clique no ícone de **lápis** (Edit).
2. Aperte **Ctrl + F** (ou Cmd + F no Mac) dentro do editor, busque `SEU-USUARIO` e troque cada ocorrência pelo seu usuário.
3. Clique em **Commit changes**.

Se o repositório tiver outro nome que não seja `dev-assis`, troque também essa parte do endereço.

---

## PARTE 3 — Colocar o site no Google

O Google encontra sites sozinho, mas pode demorar. Para acelerar:

1. Entre em https://search.google.com/search-console com a sua conta Google.
2. Clique em **Adicionar propriedade** e escolha **Prefixo do URL**.
3. Cole o endereço completo: `https://SEU-USUARIO.github.io/dev-assis/` e continue.
4. **Verificação:** escolha **Tag HTML**. O Google mostra uma linha parecida com `<meta name="google-site-verification" content="XXXX">`.
   - No GitHub, abra o `index.html` (lápis), ache a linha comentada `<!-- <meta name="google-site-verification" content="COLE-AQUI-O-CODIGO"> -->`.
   - Apague o `<!--` do começo e o `-->` do final, e troque `COLE-AQUI-O-CODIGO` pelo código que o Google deu.
   - Commit changes, volte ao Search Console e clique em **Verificar**.
5. No menu lateral, abra **Sitemaps**, digite `sitemap.xml` e clique em **Enviar**.
6. Abra **Inspeção de URL**, cole o endereço do seu site e clique em **Solicitar indexação**.

**Importante:** aparecer no Google pode levar de alguns dias a algumas semanas, e ninguém consegue garantir a posição nos resultados. Pesquisar por `site:SEU-USUARIO.github.io/dev-assis` no Google mostra se o site já foi incluído.

### Dicas que ajudam a ser encontrado
- Coloque o link do site na bio do Instagram (@dev_assisb) e no WhatsApp Business.
- Crie um **Perfil da Empresa no Google** (grátis, em https://business.google.com).
- Divulgue o link: quanto mais lugares apontarem para o site, mais rápido o Google o descobre.
- Um domínio próprio (por exemplo `devassis.com.br`, no Registro.br) passa mais credibilidade e pode ser ligado ao GitHub Pages depois (Settings → Pages → Custom domain). Se fizer isso, troque o endereço nos 3 arquivos da Parte 2.

---

## PARTE 4 — Como editar o site depois

Tudo fica no `index.html`. No GitHub: abra o arquivo → lápis → edite → **Commit changes**. Em 1 a 2 minutos a mudança entra no ar.

- **Contatos:** no começo do arquivo, no bloco `CONTATO`.
- **Adicionar projetos ao mural:** no bloco `PROJETOS`, copie um dos blocos `{ ... }` e preencha título, categoria, descrição e tecnologias. Depois cadastre o HTML do site em `CODIGOS`, perto do fim do arquivo, usando o mesmo nome em `codigo`.
- **Atenção ao adicionar projetos:** não use sites que tenham nome, logo, telefone ou e-mail de terceiros.
- **Texto "Sobre mim":** procure por `about-text`.
