# ScanKadosh

App web (um único `index.html`) que escaneia etiquetas de roupas pela câmera do celular e gera uma planilha Excel (.xlsx).

## O que faz
- Lê **código de barras** ao vivo (BarcodeDetector nativo, com ZXing como alternativa).
- Lê o **texto da etiqueta** por OCR (Tesseract.js, português + inglês) e extrai: marca, tamanho, cor, composição, origem, CNPJ, RN, referência, preço e lavagem.
- Você revisa/corrige os campos antes de salvar cada item.
- Ao final, **"Finalizar e baixar Excel"** gera um `.xlsx` com uma linha por item.
- A lista fica salva no navegador, então não se perde se a página recarregar.

## Como usar no celular (sem instalar nada)
A câmera só funciona em **HTTPS**. Ative o GitHub Pages:
1. Repositório → **Settings → Pages**
2. Source: **Deploy from a branch**, branch `main`, pasta `/ (root)`
3. Abra `https://<seu-usuario>.github.io/scankadosh/` no celular.

Precisa de internet na primeira vez (as bibliotecas de OCR, Excel e leitura de código vêm de CDN).

Se a câmera ao vivo não abrir, o botão "Usar foto da galeria/câmera" abre a câmera nativa do celular.
