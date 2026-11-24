# Rolezando

App de iPhone para descobrir rolês em Brasília num mapa, com eventos por categoria e lista de favoritos.

Projeto acadêmico (HackaTruck) · iOS 17.5+ · 2025

Projeto final do HackaTruck, do Instituto Eldorado e da IBM.

## O que faz
- Mostra os eventos como pinos num mapa de Brasília, com ícone e cor por categoria (restaurante, cultura, esportes e festa).
- Filtra o mapa por categoria.
- Tem uma gaveta "Em alta no momento" com os lugares da região.
- Abre a página de cada evento, com tags, descrição e endereço.
- Tem três abas: mapa, lista de eventos e eventos salvos.

## Meu papel
Projeto do HackaTruck feito em turma. O repositório tem só commits meus (upload de 24/05/2025), mas os arquivos do Xcode mostram dois usuários de máquina da turma, então não foi um trabalho só meu. O tamanho do time não está registrado.

## Como foi feito
- SwiftUI com `TabView` e `NavigationStack`; mapa com `Map` e `Annotation` do MapKit em `MapView.swift`.
- Os dados vêm de um serviço Node-RED na rede do curso: o `ViewModel` lê a lista (`/leitura`) e tem o envio de favorito (`/enviarLocalFavorito`).
- O modelo `Local` guarda categoria, data, tags, endereço, latitude e longitude, e se o evento está salvo.
- Há um teste de unidade e um de interface criados pelo Xcode.

## Tecnologias
Swift, SwiftUI, MapKit, URLSession, Codable e Node-RED (backend do curso).

## Como rodar
1. Abra `Desafio10 2/Desafio10.xcodeproj` no Xcode (iOS 17.5 ou mais novo).
2. O endereço do serviço Node-RED está fixo em `ViewModel.swift`, num IP da rede do curso. Fora dessa rede, o app abre sem eventos. Para ver dados, troque o endereço por um serviço seu com as mesmas rotas.

---
Feito por Cauê Crillanovick · [portfólio](https://cauecarneiro.github.io/portfolio/) · [LinkedIn](https://www.linkedin.com/in/cau%C3%AA-carneiro)
