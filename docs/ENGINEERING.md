# Engenharia e padrões | VyteTech

[Voltar à apresentação](../README.md)

Este documento descreve diretrizes recomendadas para novos projetos. A adoção é gradual e deve respeitar os contratos, a arquitetura e as necessidades de cada cliente.

## Convenções

- Repositórios de clientes: `client-<identificador>`; produtos: nomes de produto ou de serviço.
- Uma descrição objetiva, website de referência quando aplicável, assuntos (Topics) e README em cada repositório.
- README com: visão geral, funcionalidades, stack, pré-requisitos, desenvolvimento, testes, deploy, segurança e direitos de uso.
- Convenção de commits: `feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`.
- Mudanças de código preferencialmente por branch e Pull Request revisada, com `main` como branch de integração estável.

## Critérios recomendados para PR

1. Escopo bem definido e rastreável.
2. Nenhum segredo, token, credencial real ou dado de cliente no diff.
3. Testes ou verificações relevantes, quando existentes, executados.
4. Migrações e efeitos em dados revisados, com plano de retorno.
5. Sem alterações de infraestrutura produtiva sem aprovação específica.
6. README e documentação operacional atualizados quando necessário.

## Segurança e acesso

- Secrets apenas nos provedores autorizados e fora do Git.
- Menor privilégio em tokens, aplicações e permissões de repositório.
- Secret scanning e Dependabot onde disponíveis; tratar alertas antes de publicar.
- Divulgação responsável de vulnerabilidades pelo canal definido em `SECURITY.md`.
- A natureza pública de um repositório não determina sua licença.

## CI e deploy

Verificações de lint, tipagem, teste e build devem ser introduzidas por projeto **após validar comandos, credenciais e impacto em custos**. Deploy de produção não deve depender da alteração apenas deste guia.

**Observação:** este guia não declara que todas as proteções e verificações já estão ativadas; ele estabelece o padrão-alvo.
