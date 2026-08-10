# Swepay — Organization Meta Repository

> Meta-repositório da organização Swepay no GitHub. Hospeda os artefatos que a
> convenção do GitHub exige neste repo: o README público da organização
> (`profile/README.md`), workflows reutilizáveis e community health files padrão
> (SECURITY, CONTRIBUTING, LICENSE) herdados pelos demais repositórios da org.

## Conteúdo

### [`profile/README.md`](profile/README.md)

README público exibido em `github.com/swepay` (página da organização).

### [`.github/workflows/`](.github/workflows/)

Workflows reutilizáveis consumidos pelos repos da org:

```yaml
jobs:
  build:
    uses: swepay/.github/.github/workflows/swepay-build-dotnet-lib.yml@v1
    with:
      dotnet-version: "10.0.x"
      package-projects: "src/NativeMediator/NativeMediator.csproj"
      coverage-paths: "./tests/**/coverage.cobertura.xml"
    secrets:
      NUGET_API_KEY: ${{ secrets.NUGET_API_KEY }}
      CODECOV_TOKEN: ${{ secrets.CODECOV_TOKEN }}
```

- **`swepay-build-dotnet-lib.yml`** — build + test + coverage + pack + security-scan +
  publish (tags). Versionado por tags `v1`, `v2`, …; breaking changes de `inputs`/`secrets`
  exigem bump de major.

### Community health files

`SECURITY.md` (disclosure coordenado via `security@swepay.com.br`), `CONTRIBUTING.md` e
`LICENSE` valem como default para os repositórios públicos da organização.

## Bibliotecas públicas

[`native-mediator`](https://github.com/swepay/native-mediator) ·
[`native-fluent-validation`](https://github.com/swepay/native-fluent-validation) ·
[`native-lambda-router`](https://github.com/swepay/native-lambda-router) ·
[`native-source-generator`](https://github.com/swepay/native-source-generator) ·
[`native-open-api`](https://github.com/swepay/native-open-api) ·
[`native-aws-api-gateway-local-proxy`](https://github.com/swepay/native-aws-api-gateway-local-proxy) ·
[`native-passkey-sdk`](https://github.com/swepay/native-passkey-sdk) ·
[`dotnet-lambda-template`](https://github.com/swepay/dotnet-lambda-template)
