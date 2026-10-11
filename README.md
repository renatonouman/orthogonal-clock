# Orthogonal Clock

Relógio mundial escultórico com dois braços rígidos a 90°. O braço X indica as horas e o braço Z representa os minutos através de rotações combinadas do conjunto.

## Recursos

- Relógio em tempo real; na vista padrão, as horas seguem um mostrador tradicional (12 acima, 3 à direita, 6 abaixo, 9 à esquerda).
- São Paulo, Nova York, Londres, Paris, Tóquio e Sydney, com fusos e horário de verão via Intl.DateTimeFormat.
- Rotação da câmera por mouse ou toque, zoom, pausa e restauração da vista.
- Studio com cores, seção, proporções, materiais estilizados, iluminação e perspectiva.
- Presets Monolith, Brutalist, Chrome, Glass e Raw Matter.
- Biblioteca pessoal no localStorage: aplicar, editar, duplicar, renomear e excluir.
- Importação e exportação da biblioteca em JSON.

## Executar

Sem instalação de dependências ou etapa de build. Com Python 3:

```sh
python3 -m http.server 8000 --directory dist
```

Abra http://localhost:8000. Para hospedagem estática, publique o conteúdo de `dist/`.

## Estrutura e implementação

- `dist/index.html`: interface responsiva, estilos e controles.
- `dist/app.js`: orientação temporal, geometria 3D, projeção em Canvas 2D, materiais estilizados e persistência.

Esta primeira versão usa JavaScript e Canvas, sem frameworks ou dependências externas. Os materiais são aproximações visuais; não há renderização física de vidro ou metais. A biblioteca é local ao navegador e não sincroniza entre dispositivos. Use a exportação para guardar seus estilos.

Os dois braços recebem a mesma transformação rígida, preservando a perpendicularidade. A leitura dos minutos depende da rotação tridimensional, e não corresponde a um ponteiro independente de mostrador convencional.

A versão hospedada inicialmente em https://orthogonal-clock.daringpig16.chatgpt.site tem acesso privado; tornar este repositório público não altera esse acesso.
