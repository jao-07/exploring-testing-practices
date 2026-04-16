# Explorando Práticas de Teste

Neste exercício, vamos explorar práticas de teste em sistemas reais utilizando a ferramenta [TestMiner](https://andrehora.github.io/testminer).

O TestMiner permite visualizar e analisar testes de software em repositórios do GitHub, fornecendo dados sobre como os projetos organizam seus testes, como eles evoluem entre versões e quais bibliotecas de teste são utilizadas.
Explore a ferramenta antes de começar para se familiarizar com seu funcionamento.

---

## Passo 1: Selecionar um repositório

Escolha um repositório real que possua testes escritos na linguagem de sua preferência.
Abaixo estão alguns links para ajudá-lo a encontrar projetos interessantes:

- **Python:** https://github.com/topics/python?l=python
- **JavaScript:** https://github.com/topics/javascript?l=javascript
- **TypeScript:** https://github.com/topics/typescript?l=typescript
- **Java:** https://github.com/topics/java?l=java

## Passo 2: Explorar o repositório selecionado

Busque o repositório escolhido no [TestMiner](https://andrehora.github.io/testminer) e analise os dados de teste gerados pela ferramenta.

## Passo 3: Explicar uma prática de teste

Com base nos dados obtidos, selecione uma prática ou dado de teste relevante e explique-o com suas próprias palavras.

---

## Instruções de entrega

1. Faça um `fork` deste repositório (saiba mais sobre forks [aqui](https://docs.github.com/pt/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)).
2. Responda às questões abaixo diretamente neste arquivo `README.md` do seu fork. Pode adicionar imagens para enriquecer sua explicação.
3. No Moodle, submeta apenas a URL do seu fork.

---

## Respostas

**1. Repositório selecionado:** https://github.com/facebook/react

**2. Explicação:** 
  Escolhi o repositório do React. Com o TestMiner, pudi perceber que da versão 16 para a 19, houve um aumento significativo no número de testes e principalmente na quantidade de fixtures, na qual, na versão 16 não haviam fixtures e já na 19, existem mais de 3500.
  Isso se dá pois na época do React 16, a renderização da página ocorria quase inteiramente no navegador, então para isso, testes unitários simples já eram suficientes para testar a aplicação.
  No React 18 e 19, foi introduzido o React Server Components e os motores do Server-Side Rendering (SSR) foram reescritos, de forma a melhorar a forma como a página feita em React é renderizada. Isso faz com que, para testar os Server Components, que são componentes que rodam e ficam no servidor, é necessário um ambiente mais complexo, na qual é necessário um processo de build, um ambiente de servidor, como Node.js e um ambiente de cliente para testar o hydration e a transferência dos dados. Para resolver esse problema, foi necessário criar milhares de fixtures para atuarem como pequenos apps, que configuram um servidor, renderiza o componente e verificam como o cliente reage.
  Por isso, o React, que antes usavam apenas testes unitários simples, passou a utilizar testes mais complexos usando fixtures. Essa filosofia continuou a ser implementada para outras features, como o React Concurrent e o React Compiler, que também são difíceis de serem testados sem um ambiente adequado.

  <img width="723" height="417" alt="image" src="https://github.com/user-attachments/assets/710af4f9-b989-4e68-bce3-f4941c60a644" />
  <img width="721" height="419" alt="image" src="https://github.com/user-attachments/assets/4b0ae773-09f1-4de4-a2c6-e1b8ce58f8fe" />


