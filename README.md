# Shakers – Semana 2 – Landing Page de Loções
### Autor: André Lucas Cunha de Almeida
## Descrição do desafio

Desenvolvimento de uma landing page exclusiva para campanha de loções utilizando Shopify e Liquid, com template, section e schema configuráveis pelo Admin.

Este projeto demonstra o fluxo completo de desenvolvimento Shopify: 
  template → section → schema → validação no tema → versionamento em Git.

---

## O que foi implementado

### Template da página

Arquivo:
````
templates/page.lotion-lp.json
````
Responsável por renderizar a section da landing page.

---

### Section da landing page

Arquivo:
````
sections/lotion-lp.liquid
````
#### Esta section:
Exibe o título da página usando:
````
{{ page.title }}
````
Exibe o conteúdo da página usando:
````
{{ page.content }}
````
Exibe um produto em destaque selecionável pelo Admin:
````
section.settings.featured_product
````
Mostrando:
````
product.title
product.price | money
product.featured_image
product.url
````
Exibe uma coleção selecionável pelo Admin
````
section.settings.lotions_collection
````
Loop em:
````
collection.products
````
Para cada produto:
````
product.title
product.price | money
product.featured_image
product.url
````
#### Schema configurável

O schema permite selecionar no Editor de Temas:
- Produto em destaque
- Coleção de loções

Sem necessidade de alterar o código.

#### Objetos Shopify utilizados:
- page
- product
- collection
- section.settings
---
### Link da landing page
(necessita de uma senha)
````
https://andre-theme-dev-2.myshopify.com/pages/lotion 
````
---

### Como testar localmente
Rodar o tema com Shopify CLI:
````
shopify theme dev
````
Abrir no navegador:
````
/pages/lotion
````
### Como configurar no Admin
- Ir em Online Store → Customize
- Selecionar Pages → Lotion
- Na section "Lotion LP": Selecionar Produto em destaque e selecionar Coleção de loções
- Salvar

---
## Estrutura do projeto
shakers-semana-2-lp-lotions
├── README.md
├── templates/
│ └── page.lotion-lp.json # Template da página que carrega a section
└── sections/
└── lotion-lp.liquid # Section principal da landing page 

---
### Branch utilizada
```
feat/lotion-landing-page
```
### Pull Request
```
https://github.com/andreLuAlmeida/shakers-semana-2-lp-lotions/pull/1#issue-3942102446
```
### Vídeo
```
https://youtu.be/tZV7oF7ZE-I
```
---
