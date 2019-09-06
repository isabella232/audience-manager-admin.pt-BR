---
source-git-commit: b76aa4a35a5216aabd60d07352a7c4bd2b3e6e32
translation-type: tm+mt

---
# Instruções

**Observação: Esta página (ou qualquer página readme. md) não será publicada na documentação voltada para o cliente**

## Sumário

+ `TOC.md` na raiz do guia do usuário fornece a organização dos tópicos contidos no guia para esta solução.
+ Cada guia do usuário terá seu próprio único, `TOC.md`no qual você pode ordenar todas as páginas/tópicos conforme necessário.
+ A primeira página de todos os guias do usuário `overview.md`é.

## Guia do usuário

+ A introdução ao guia do usuário é chamada `overview.md`
+ Cada tópico no guia do usuário tem seu próprio diretório distinto.
   + Se houver um tópico no guia chamado *Implementação*, o diretório correspondente é `/implementation`
+ Todos os ativos de imagem são armazenados na `/assets` raiz do guia do usuário.
   + Todas as imagens no `/assets` diretório serão localizadas.
   + Nenhuma imagem no `/no-localize` diretório será localizada (há uma surpresa!) Isso pode ser usado para garantir em versões loc que os ativos específicos não serão reproduzidos desnecessariamente.

## Metadados de nível do guia do usuário

+ Os metadados que descrevem o guia do usuário são armazenados no `TOC.md`. Isso inclui:
   + produto - nome do produto/recurso.
   + nuvem - nuvem à qual este produto pertence.
   + público-alvo: público-alvo ou arquivema no qual o guia é direcionado.
   + guia do usuário - nome do guia do usuário.

## Metadados de nível de página

+ Os metadados necessários para descrever um documento são armazenados como parte de cada página individual. Isso inclui:
   + título - título da página.
   + descrição - descrição da página.
   + seo-title - título alternativo seo.
   + seo-description - título alternativo para fins de SEO.
   + abreviado - (campo opcional).
   + index - sim/não - a página será indexada pela plataforma de pesquisa da Adobe.
   + traduzir - sim/não - essa página será localizada.
   + versão - usada principalmente para o AEM e Campanha, para indicar a versão do produto.
   + private-feature-pack - usado principalmente para o AEM.
   + beta - este produto é beta?
   + redirecionar - pode ser usado para criar um ref para uma nova página, se necessário.
   + doc-type: reference (padrão)/troubleshooting/developer/tutorial/kb/whitepaper.

## Mais Informações

Para obter mais instruções de publicação, guias de estilo, amostras e outros recursos, visite a [Documentação colaborativa de Repo](https://git.corp.adobe.com/AdobeDocs/collaborative-doc-instructions)
