# R-universe — maiconcarlospng

Configuração de publicação do pacote R **sisabextrator**, mantido em
[maiconcarlospng/sisab-extrator](https://github.com/maiconcarlospng/sisab-extrator).

O arquivo [`packages.json`](packages.json) identifica o pacote para o R-universe.
A implementação do pacote R está na **raiz** do repositório de origem.

## Ativar a publicação

1. Instale o [GitHub App do R-universe](https://github.com/apps/r-universe/installations/new)
   na conta GitHub `maiconcarlospng`, concedendo acesso a este repositório e a
   `sisab-extrator` (ou a todos os repositórios).
2. Verifique as compilações em https://maiconcarlospng.r-universe.dev/
3. Depois de uma compilação bem-sucedida, instale no R:

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
