# Prova de Conceito: Media Queries

## Descrição
Este projeto demonstra o uso de Media Queries no CSS para criar layouts responsivos que se adaptam a diferentes dispositivos e tamanhos de tela, melhorando a experiência do usuário. O site exibe uma galeria de imagens e um texto formatado em colunas, com comportamento visual adaptado conforme as características do dispositivo ou da janela de visualização.
## Estrutura do Projeto
O projeto é composto por um arquivo HTML principal e uma folha de estilo CSS que contém regras de Media Queries para diferentes tipos de dispositivos e orientações.
## Layout Responsivo com Media Queries
O site foi desenvolvido para se ajustar dinamicamente a diferentes larguras de tela e orientações. Abaixo estão as diferentes Media Queries usadas no projeto.
## No código HTML, foi implementado um menu de navegação utilizando a tag <nav>, contendo um link que leva à página "Explicação". A estrutura básica do menu é simples, utilizando a tag <a> para criar o link de navegação.
``` css
<nav>
    <a href="explicativo.html">Explicação</a>
</nav>
```
# 1. Media Query: Dispositivos Móveis (até 600px de largura)
```css
@media (max-width: 600px) {
  nav a {
    display: block;
    padding: 10px;
    text-align: center;
  }

  .gallery img {
    flex: 1 1 60%; 
    max-width: 100%; 
  }
}
```
Nesta faixa de largura, os links de navegação são exibidos em blocos empilhados, melhorando a usabilidade em telas pequenas. As imagens da galeria são redimensionadas para ocupar 60% da largura disponível, ajustando-se de maneira flexível.
# 2.Media Query: Tablets (601px a 1024px de largura)
``` css
@media (min-width: 601px) and (max-width: 1024px) {
  .gallery img {
    flex: 1 1 calc(12% - 10px); 
    max-width: 100%;
  }
}
```
Em dispositivos intermediários como tablets, as imagens são redimensionadas para ocupar um espaço maior na tela, mantendo uma disposição equilibrada.
# 3.Media Query: Desktop (1025px e acima)
``` css
@media (min-width: 1025px) {
  .gallery img {
    flex: 1 1 calc(5% - 10px); 
    max-width: 100%;
  }
}
```
Nos desktops, as imagens são exibidas em uma grade mais densa, ocupando uma porção menor da tela, garantindo que várias imagens sejam visíveis simultaneamente.
# 4.Media Query: Orientação Landscape
``` css
@media (orientation: landscape) {
  .gallery img {
    flex: 1 1 calc(5% - 10px); 
    max-width: 100%;
  }

  .text-columns {
    column-count: 2;
    column-gap: 20px;
  }
}
```
Quando o dispositivo está em modo paisagem, o conteúdo textual é exibido em duas colunas para aproveitar melhor a largura extra, enquanto a galeria de imagens se adapta com um espaçamento adequado.
# 5.Media Query: Orientação Portrait
``` css
@media (orientation: portrait) {
  .gallery img {
    flex: 1 1 100%; 
    max-width: 100%;
  }

  .text-columns {
    column-count: 1;
  }
}
```
Em dispositivos em modo retrato (vertical), as imagens ocupam 100% da largura disponível e o texto é exibido em uma única coluna para melhor legibilidade.
# 6.Media Query: Estilo de Impressão
``` css
@media print {
  nav, footer, .gallery {
    display: none;
  }

  .content {
    font-size: 14pt;
    line-height: 1.5;
    color: black;
  }

  .text-columns {
    column-count: 1;
    column-gap: 0;
  }
}
```
Ao imprimir a página, elementos não essenciais, como a navegação e a galeria de imagens, são ocultados. O conteúdo principal é otimizado para impressão com fontes maiores e espaçamento ajustado.


## Autores
- Guilherme Sampaio Silva - 10443768
- Felipe Melantonio - 10443843
- Arthur Eduardo - 10437356
