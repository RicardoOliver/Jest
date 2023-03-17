# Jest


Jest é um framework de teste em JavaScript desenvolvido pelo Facebook. É usado principalmente para testes unitários e de integração de aplicativos escritos em React, Node.js e outras bibliotecas e frameworks de JavaScript. O Jest se destaca por ser fácil de configurar, rápido e ter uma sintaxe simples que permite escrever testes de forma legível e fácil de manter.

Neste tutorial, mostrarei como configurar o Jest e escrever testes simples para um aplicativo React.
Instalação

Você pode instalar o Jest por meio do npm usando o seguinte comando:

css
npm ´´´
npm install --save-dev jest
´´´
Configuração

Para configurar o Jest, crie um arquivo chamado jest.config.js na raiz do seu projeto. Aqui, você pode especificar as opções de configuração para o Jest. Por exemplo, se você tiver arquivos de teste em uma pasta chamada __tests__, poderá adicionar o seguinte ao seu arquivo de configuração:

javascript

module.exports = {
  testMatch: ['**/__tests__/**/*.js?(x)', '**/?(*.)+(spec|test).js?(x)'],
};

Isso indicará ao Jest que procure arquivos de teste que contenham os seguintes padrões de arquivo: **/__tests__/**/*.js?(x) e **/?(*.)+(spec|test).js?(x).
Escrevendo testes

Para escrever testes no Jest, crie um arquivo de teste que termine com .test.js ou .spec.js em sua pasta de teste. Por exemplo, crie um arquivo chamado sum.test.js na pasta __tests__ com o seguinte conteúdo:

javascript

function sum(a, b) {
  return a + b;
}

test('adds 1 + 2 to equal 3', () => {
  expect(sum(1, 2)).toBe(3);
});

Neste exemplo, estamos definindo uma função chamada sum que recebe dois argumentos e retorna a soma de ambos. Em seguida, definimos um teste que verifica se sum(1, 2) é igual a 3. Para fazer isso, usamos a função expect e a função toBe do Jest.
Executando testes

Para executar os testes, basta executar o seguinte comando em seu terminal:

npx jest

Isso procurará arquivos de teste em sua pasta __tests__ e executará todos os testes que encontrar.
Conclusão

O Jest é uma ferramenta muito útil para escrever testes em JavaScript. É fácil de configurar e escrever testes no Jest é bastante simples. Espero que este tutorial tenha ajudado você a começar com o Jest.
