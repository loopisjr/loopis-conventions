# Loopis Conventions

## Commits

### Estrutura de commit:

```
tipo[escopo opcional]: descrição
[corpo opcional]
[rodapé opcional]
```


### Exemplo de commit:

```
fix: corrige pequenos erros de digitação no código
veja o ticket para detalhes sobre os erros de digitação corrigidos
closes issue #12
```

### Lista de tipos permitidos
- feat: Uma funcionalidade
- fix: Um ajuste de erro/bug
- view: Criação ou modificações em arquivos estáticos (ccs, html, assets)
- refactor: Mudança de código que não adiciona funcionalidade ou arruma um erro
- test: Novos testes ou correção de antigos
- build: Mudanças que afetam o build ou dependências externas (yarn, npm, mvn)
- env: Mudanças referentes ao ambiente do projeto (variáveis de ambiente, docker)
- revert: Reversão de um commit
- config: Configurações de dependências do projeto (bancos de dados, rotas, serviços externos)

A única exceção é o primeiro commit, que deve ser "Commit inicial"

## Versionamento

Ao criar uma nova tag de versão deve seguir o formato  MAJOR.MINOR.PATCH

Exemplos: v. 1.0.0, v. 2.1.3

- Major: Atualizada quando gera incompatibilidade com versões anteriores 
- Minor: Atualizada quando uma nova funcionalidade é incorporada a última versão
- Patch: Atualizado quando um bug é corrigido, ou outra alteração menor


## Padrão de branches
O padrão a ser seguido ao criar uma nova branch é informar o tipo entre: feature, fix e release.

O nome da branch deve ser definido com base no nome do projeto, o identificador da issue ao qual ela se refere e a funcionalide que ela irá implementar. Por exemplo, em um projeto chamado Ouvidoria Colégio Polivalente, que tenha uma issue de id 4 descrevendo a necessidade de que o sistema cadastre informações de funcionários, geraria uma branch "feature/OCP-04-Cadastrar-Funcionarios".

Merges com a Master devem sempre ser feitos através de pull requests.
```
Master
│   ├── feature/FeatureName
│   │   └──fix/BugToFix
│   ├── fix/BugToFix
│   ├── release/ReleaseName
```

## Funções
De maneira geral todos os nomes de funções em qualquer projeto devem ser escritos em inglês, seguindo as demais convenções da linguagem.

- Funções que lidam com eventos devem conter informações do tipo de evento e a ação. EX: handleRegister(), handleSubmit().
- Funções que retornam booleano  devem começar com ‘is’ seguido da característica que a função verifica. EX: isInteger(), isEmpty(), isStaff().

## Padrões de pastas

A seguir os detalhes de como as pastas de projetos devem ser organizadas

### Node

```
Project
├── src
│   ├── index.js
│   ├── Router.js
│   ├── routes
│   │   └── UserRoutes.js
│   │   └── ...
│   ├── controllers
│   │   └── UserController.js
│   │   └── …
│   ├── services (optional)
│   │   └── UserService.js
│   │   └── ...
│   ├── database
│   │   └── Connection.js
│   │   └── UserSchema.js (optional)
│   │   └── ...
│   ├── config (optional)
│   │   └── ...
│   ├── utils (optional)
│   │   └── …
└── .gitignore
```

### React

```
Project
├── src
│   ├── index.js
│   ├── App.js
│   ├── routes.js
│   ├── pages
│   │   └── Login
│   │   │   └── index.js
│   │   │   └── style.css
│   │   │   └── components (optional) 
│   │   └── ...
│   ├── services
│   │   └── api.js
│   │   └── ... 
│   ├── global.css (optional)  
│   ├── assets (optional)
│   │   └── ...
│   ├── config (optional)
│   │   └── ...
│   ├── components (optional)
│   │   └── ...
│   ├── utils (optional)
│   │   └── …
└── .gitignore

```

### React Native
 ```
 Project
├── src
│   ├── App.js
│   ├── routes.js
│   ├── pages
│   │   └── Login
│   │   │   └── index.js
│   │   │   └── style.css
│   │   │   └── components (optional) 
│   │   └── ...
│   ├── services
│   │   └── api.js
│   │   └── ... 
│   ├── global.css (optional)  
│   ├── assets (optional)
│   │   └── ...
│   ├── config (optional)
│   │   └── ...
│   ├── components (optional)
│   │   └── ...
│   ├── utils (optional)
│   │   └── …
├── index.js
└── .gitignore

 ```
