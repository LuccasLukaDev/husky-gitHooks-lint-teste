# Husky + ESLint + lint-staged

Projeto de estudo sobre **Git Hooks** e automação de validações no fluxo de commits.

## Tecnologias

- ESLint
- Husky
- lint-staged
- Git
- Node.js

## Fluxo

```text
git add
   ↓
arquivos staged
   ↓
git commit
   ↓
Husky (pre-commit)
   ↓
lint-staged
   ↓
ESLint
   ↓
Commit permitido ou bloqueado
```

## Instalação

```bash
npm install
```

Inicialize o Husky:

```bash
npx husky init
```

## Teste

Adicione os arquivos ao staging:

```bash
git add .
```

Faça o commit:

```bash
git commit -m "feat: primeiro commit"
```

O Husky executará o `lint-staged`, que aplicará o ESLint somente nos arquivos staged.

## Estrutura

```text
├── .husky/
│   └── pre-commit
├── src/
├── eslint.config.js
├── package.json
└── package-lock.json
```

## Objetivo

Demonstrar a integração entre **ESLint, lint-staged e Husky** para automatizar a validação do código antes dos commits.
