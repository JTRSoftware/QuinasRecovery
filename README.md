# Quinas Recovery Page

Página estática para receber um token no fragmento HTTPS e abrir a aplicação Quinas através do esquema `quinas://`. Não contém segredos nem valida tokens; essa validação continua a ser feita pelo servidor Quinas.

## Publicar com GitHub Pages

1. Cria no GitHub um repositório **público** chamado `QuinasRecovery`.
2. Coloca `index.html` na raiz do branch `main`.
3. Em **Settings > Pages**, escolhe **Deploy from a branch**, branch `main` e pasta `/ (root)`.
4. Aguarda a publicação e confirma `https://jtrsoftware.github.io/QuinasRecovery/`.
5. Testa com um token falso de 64 caracteres hexadecimais; não uses um token real no teste.

O link de produção esperado será `https://jtrsoftware.github.io/QuinasRecovery/#TOKEN`. Se escolheres outro nome de repositório, o caminho da página também muda.

Depois de a página estar publicada, o servidor deverá enviar esse URL em vez de incluir diretamente `quinas://` no e-mail. O link HTTPS abre a página; o utilizador carrega no botão para passar o token à app. O fragmento não é enviado ao alojamento GitHub Pages.

A aplicação Android já declara o esquema personalizado. A associação do esquema no pacote iOS continua a ser necessária para abrir a app no iPhone/iPad.
