# Minicord APK (via GitHub Actions)

O app é um "invólucro" (Capacitor) que abre o seu servidor Minicord. O servidor precisa estar rodando e acessível por **https**.

1. Crie um repositório no GitHub e suba **todo o conteúdo desta pasta** (incluindo a pasta oculta `.github`).
2. No repositório: aba **Actions** > **Build APK** > **Run workflow**, e cole o endereço https do seu servidor.
3. Quando terminar (uns 5 a 10 min), abra a execução e baixe **minicord-apk** em *Artifacts*. É um zip com o `app-debug.apk`.
4. Passe o APK para o celular e instale (precisa permitir "fontes desconhecidas"). Na primeira chamada, aceite a permissão do microfone.

Se o endereço do servidor mudar (ex.: o túnel gera outro link), rode o workflow de novo com o novo endereço.

Obs.: é um APK de depuração (assinado com chave de debug), serve para uso pessoal. No Android, compartilhar a tela costuma não funcionar dentro do app; chamada, mic e sons funcionam.

## Se a pasta .github não subir
Pastas que começam com ponto ficam ocultas e alguns jeitos de enviar (arrastar pelo site, por exemplo) podem esquecê-la. Se a aba **Actions** não mostrar o "Build APK", crie o arquivo à mão: no repositório, **Add file > Create new file**, digite o nome `.github/workflows/apk.yml` (as barras criam as pastas) e cole o conteúdo do `apk.yml` desta pasta. Pelo GitHub Desktop ou pelo `git`, ela sobe normal.
