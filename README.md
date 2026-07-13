# Site MáfiaBR — Saint Seiya Awakening

Site estático de consulta de cavaleiros: o usuário digita/seleciona o nome
e o site mostra a progressão de habilidade (Mínimo / Média / Ideal) e a
sugestão de cosmos (Central, Vermelho, Amarelo, Azul).

## Arquivos
- `index.html` — o site (HTML/CSS/JS puro, sem dependências de build)
- `cavaleiros.json` — "banco de dados" com 104 cavaleiros, gerado a partir
  da planilha `Paramentros_CV.xlsx`

## Como publicar no GitHub Pages
1. Crie um repositório novo (ex: `mafiabr-saint-seiya`).
2. Suba os dois arquivos (`index.html` e `cavaleiros.json`) na raiz do repositório.
3. Vá em **Settings → Pages**, selecione a branch `main` e a pasta `/ (root)`.
4. O site ficará disponível em `https://SEU-USUARIO.github.io/mafiabr-saint-seiya/`.

O `index.html` carrega `cavaleiros.json` com `fetch('cavaleiros.json')` — os
dois arquivos precisam estar na mesma pasta do repositório.

## Atualizando os dados
Para atualizar cavaleiros, edite `cavaleiros.json` diretamente pelo GitHub
(ou gere novamente a partir de uma planilha atualizada) e dê commit — o site
lê o arquivo em tempo real, sem precisar recompilar nada.

## Pontos de atenção nos dados originais
Ao converter a planilha percebi duas inconsistências que valem revisar na
fonte original:

1. **"Hasgard" aparece duas vezes** nas abas HABILIDADES e COSMOS, com
   valores diferentes em cada linha. Usei a última linha de cada aba —
   vale conferir qual está correta.
2. **Grafia "Seya" vs "SEIYA"**: a aba LISTA/HABILIDADES usa "Seya de
   Sagitário" e "Seya Divino", enquanto a aba COSMOS usa "SEIYA de
   Sagitário" e "SEIYA Divino". Tratei como o mesmo cavaleiro para juntar
   os dados, mas o ideal é padronizar a grafia na planilha.
