# 0002: Repositório público na Arven-Labs, licença MIT

**Data:** 2026-11-12

## Contexto
É preciso escolher dono, visibilidade e licença antes do primeiro commit. O projeto é pesquisa sobre colaboração em código aberta e deve poder receber contribuições e integrar projetos existentes.

## Decisão
- Repositório `Arven-Labs/trellis`, **público**.
- Licença **MIT**, titular igual aos demais repos.

## Alternativas descartadas
- Repo privado: só há pesquisa, sem código nem segredo.
- AGPL-3.0: a base pode vir de projetos com outras licenças, e a licença deste repo precisa ser compatível com o que for reaproveitado (a conferir na Etapa 1; não verificado ainda). Se o código derivado de um forge impuser outra licença, um novo ADR trata.
- Conta pessoal em vez da organização: sem motivo.

## Consequências
- Público e MIT são praticamente irreversíveis para o que já foi publicado.
- A MIT não impede fork fechado; aceito, porque o objetivo é adoção.
- Conferir a licença de cada base antes de reaproveitar código (Etapa 1 do `SPEC.md`).
