# CodeQuinta #1 - Arquitetura Flux com Redux do zero

Exemplo criado durante a [RocketLive #1](https://www.youtube.com/watch?v=69e1MoUWE1g)

## Ferramentas

- [react](https://github.com/facebook/react) através do [create-react-app](https://github.com/facebook/create-react-app)
- [redux](https://github.com/reduxjs/redux)
- [react-redux](https://github.com/reduxjs/react-redux)

## Conceitos

![Diagrama](docs/diagrama.png)
*Créditos na imagem*

**Qual a diferença entre gerenciar estados por componente ou com Redux?**

Por componente há a limitação de o estado estar somente naquele componente, se seus filhos se for necessário, porém podemos tornar aquele estado como global, sendo acessível em qualquer lugar da aplicação através do Redux.

**Actions no Javascript**

Eventos são ações ou ocorrências que acontecem no sistema que estamos desenvolvendo, no qual este te alerta sobre essas ações para que você possa responder de alguma forma, se desejado. Por exemplo, se o usuário clica em um botão numa pagina web, você pode querer responder a esta ação mostrando na tela uma caixa de informações.

_Fonte: [MDN web docs](https://developer.mozilla.org/pt-BR/docs/Aprender/JavaScript/Elementos_construtivos/Events)_

## Desafio

### Qual o papel dos seguintes items na estrutura do redux?

**View**

No React, é o HTML, podendo ser várias divs, ou um input, um botão, e o que acontece na view é ter ações do usuário, como um clique, ou um hover.

**Actions**

É um objeto que ele indica o redux qual ação deve ser feita no nosso estado. Contendo de base um nome para indicar qual action esta sendo disparada. A partir disso esta action é ouvida pelo redux pelos middlewares

**Middleware**

Interceptor de dois pontos, pegando o conteúdo interior, sendo assim o único local que pode transformar o mesmo. Por exemplo, capturando uma ID e buscando na API seu conteúdo.

**Reducer**

Ouve actions, podendo vários reducers podem ouvir a mesma action, ou o contrário. Por exemplo, uma action de propósito de adicionar um conteúdo, pode haver um reducer para adicionar o conteúdo numa lista, e outro para notificar o sucesso ou erro daquela inserção. Lembrando que reducers agem somente sobre um estado, qualquer outro tipo de intenção deve ser feita pro fora do escopo do redux, como na action ou middleware.

---

**Observação:** todo o estudo foi tirado da Live, portanto, todos os méritos são para o professor do mesmo.