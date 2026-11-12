# FutsalData 20-20 — PWA Android

## Conteúdo
- `index.html`: HTML original com metadados PWA e identidade FutsalData 20-20.
- `manifest.json`: configuração de instalação Android.
- `service-worker.js`: cache offline.
- Arquivo de relatórios: IndexedDB local, acessível no separador **Registos**.
- `icons/`: ícones 192×192 e 512×512.

## Publicar em HTTPS com GitHub Pages
1. Entre em https://github.com/ e crie um repositório, por exemplo `futsaldata-20-20`.
2. Carregue todos os ficheiros deste pacote, mantendo a pasta `icons/`.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`.
5. Depois da publicação, o endereço será semelhante a `https://SEU-UTILIZADOR.github.io/futsaldata-20-20/`.

## Instalar no Android
1. Abra o endereço HTTPS no Chrome do Android.
2. Abra o menu ⋮ e escolha **Instalar aplicação** (ou **Adicionar ao ecrã principal**).
3. Confirme.

## Notas
- O jogo em curso continua guardado em `localStorage`, no próprio dispositivo/navegador.
- Os relatórios guardados na aba **Registos → Arquivo de jogos** ficam em IndexedDB no mesmo dispositivo.
- Use **Cópia de segurança** para exportar todos os relatórios para um ficheiro JSON; **Importar cópia** permite recuperá-los ou transferi-los para outro dispositivo.
- Cada relatório pode ser consultado, exportado individualmente em CSV ou apagado.
- Não existe sincronização automática entre dispositivos. Limpar os dados do Chrome/site pode apagar tanto o jogo em curso como o arquivo local; mantenha cópias de segurança.
- O cache offline fica disponível após a primeira visita online e instalação do service worker.
- Este pacote prepara a publicação, mas não publica automaticamente: é necessário criar/autorizar o alojamento HTTPS.
- A lógica original foi mantida; esta entrega não representa uma auditoria funcional completa do cronómetro ou das substituições.
