# R-universe — maiconcarlospng

Configuração de publicação do pacote R **sisabextrator**, mantido em
[maiconcarlospng/sisab-extrator](https://github.com/maiconcarlospng/sisab-extrator).

O arquivo [`packages.json`](packages.json) identifica o pacote para o R-universe.
A implementação do pacote R está na **raiz** do repositório de origem.

## Primeira publicação no R-universe

- **Configuração criada:** este repositório contém o `packages.json` apontando
  para `maiconcarlospng/sisab-extrator`.
- **Permissão informada pelo mantenedor:** GitHub App do R-universe autorizado
  com acesso a todos os repositórios.
- **Compilação inicial:** a [documentação oficial](https://docs.r-universe.dev/publish/set-up.html#wait-first-build)
  informa que a primeira compilação pode levar **cerca de 1 hora**. Antes de
  concluir, o universo pode mostrar `No packages found for this owner or maintainer`
  e o índice `src/contrib/PACKAGES` pode não estar disponível.
- **Acompanhar:** verifique https://maiconcarlospng.r-universe.dev/ e, somente
  se permanecer vazio depois desse período, investigue os registros do serviço.
  Um check de GitHub Actions aprovado **não** confirma publicação no R-universe.

Depois que o pacote aparecer no R-universe, instale no R:

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

**Nota:** o motor de extração do SISAB é escrito em Python e precisa ser instalado
separadamente quando for necessário executar downloads:

```r
sisab_instalar_motor(python = "python")
```

O pacote permanece experimental. Os relatórios públicos do SISAB contêm dados
agregados, não microdados de pacientes. Algumas opções de consulta ainda precisam
ser validadas diretamente no SISAB.

Documentação oficial: https://docs.r-universe.dev/publish/set-up.html
