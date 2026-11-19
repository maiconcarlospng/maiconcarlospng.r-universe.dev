# Publicação do SISAB Extrator no R-universe

Este repositório serve para **publicar o pacote R `sisabextrator`**. Ele não contém o programa principal.

O código-fonte e as instruções para usar a ferramenta estão aqui:

**[SISAB Extrator — ver projeto e como usar no RStudio](https://github.com/maiconcarlospng/sisab-extrator)**

## Como instalar no RStudio?

Assim que o pacote aparecer no [R-universe de maiconcarlospng](https://maiconcarlospng.r-universe.dev/), execute:

```r
install.packages(
  "sisabextrator",
  repos = c(
    "https://maiconcarlospng.r-universe.dev",
    "https://cloud.r-project.org"
  )
)

library(sisabextrator)
```

## Por que ainda pode não aparecer?

A primeira publicação pode levar **cerca de uma hora**, conforme a [documentação do R-universe](https://docs.r-universe.dev/publish/set-up.html#wait-first-build). Nesse intervalo, a página pode mostrar **“No packages found”**.

Se o pacote continuar ausente depois desse período, é necessário verificar o processamento pelo R-universe. O fato de passar nos testes do GitHub **não significa** que a publicação no R-universe tenha terminado.

## Para que serve o `packages.json`?

É um arquivo que indica ao R-universe onde encontrar o pacote R, no repositório [`maiconcarlospng/sisab-extrator`](https://github.com/maiconcarlospng/sisab-extrator).

O GitHub App do R-universe já foi autorizado com acesso aos repositórios, segundo o mantenedor.

**Observação:** o pacote ainda está em desenvolvimento, e a extração real do SISAB precisa ser validada.
