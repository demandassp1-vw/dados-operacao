# Ficha de Proposta

Página única (`index.html`), sem dependências de servidor, que transforma o texto exportado do sistema em uma ficha de proposta pronta para conferir/enviar.

## Como usar
1. Abra a página.
2. Cole o texto copiado do sistema no campo da esquerda.
3. Aperte **Enter** (ou clique em "Gerar ficha") — a ficha à direita se monta sozinha.
4. Preencha "Retorno" e "Vencimento" manualmente (esses dois não vêm no texto colado).
5. Use "Copiar resumo" para copiar um resumo em texto puro (bom para mandar por WhatsApp, por exemplo).

## Campos reconhecidos automaticamente
A página procura, linha por linha, por estes rótulos e usa a linha seguinte como valor:

- `Proposta`
- `Data Inclusão`
- `CPF`
- `Nome`
- `Status da Proposta`
- `Código Plano`
- `Vcto do Plano`
- `Valor Veículo`
- `Valor Entrada`
- Qualquer parcela no formato `Nx` (ex.: `60x`, `48x`)

O **Crédito** é calculado automaticamente (Valor Veículo − Valor Entrada).

Se o texto colado tiver rótulos com grafia um pouco diferente do esperado, ajuste as expressões regulares no início do `<script>` do `index.html` (constante `LABELS`).

## Como colocar no GitHub (GitHub Pages)

1. Crie um repositório novo no GitHub (pode ser público ou privado, mas o Pages gratuito exige público em contas free).
2. Suba o arquivo `index.html` para a raiz do repositório (pode arrastar e soltar pela interface web do GitHub, em "Add file → Upload files").
3. Vá em **Settings → Pages**.
4. Em "Build and deployment", escolha **Deploy from a branch**.
5. Selecione a branch `main` e a pasta `/ (root)`, depois clique em **Save**.
6. Aguarde 1-2 minutos. O GitHub mostrará o link, algo como:
   `https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`

Pronto — é só acessar esse link de qualquer computador ou celular para usar a ficha.

## Rodar localmente antes de subir
Basta abrir o `index.html` direto no navegador (duplo clique) — não precisa de servidor nem instalação.
