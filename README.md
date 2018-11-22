# Taller de desarrollo de aplicaciones descentralizadas en la Blockchain de Ethereum

Este año, como Proyecto de Fin de Máster me he pegado con el desarollo de aplicaciones descentralizadas ([ÐApps](https://en.wikipedia.org/wiki/Decentralized_application)) con contratos inteligentes ([Smart Contracts](https://en.wikipedia.org/wiki/Smart_contract)) en la Blockchain de [Ethereum](https://www.ethereum.org/).

En este taller pretendo hacer una pequeña aplicación descentralizada con un pequeño contrato inteligente, y enseñar todo lo que yo he aprendido a base de golpes.

Veremos un poco de [Solidity](https://solidity.readthedocs.io/en/v0.4.24/), un lenguaje para programar contratos inteligentes. Utilizaremos también [Truffle](http://truffleframework.com/), un framework para desarrollar y testear aplicaciones descentralizadas. Necesitaremos usar [web3js](https://github.com/ethereum/web3.js/) para llamar desde nuestra web a la Blockchain. Usaremos [MetaMask](https://metamask.io/) para interactuar con la aplicación. Y para minar nuestras transacciones de prueba levantaremos una instancia de [Ganache](http://truffleframework.com/ganache/).

[Charla en el Commit Conf](https://www.koliseo.com/events/commit-2018/r4p/5630471824211968/agenda#/5116072650866688/5423890473943040)

<a href="https://www.koliseo.com/events/commit-2018/r4p/5630471824211968/agenda#/5116072650866688/5423890473943040">
  <img src="./slides/img/commit-conf-blockchain.png" alt="Charla en el Commit Conf"/>
</a>


## Recursos

### Slides de la charla

[Slides de la charla](https://asanzdiego.github.io/commit-conf-taller-blockchain/)

<a href="https://asanzdiego.github.io/commit-conf-taller-blockchain/">
  <img src="./slides/img/slides-sombra.png" alt="Slides de la charla"/>
</a>

## Ejecución de la ÐApp

### Prerequisitos

Instalar NodeJS https://nodejs.org/

Instalar MetaMask https://metamask.io/

### Clonar el repositorio

Ejecutar:

~~~
git clone git@github.com:asanzdiego/commit-conf-taller-blockchain.git
cd commit-conf-taller-blockchain
~~~

### Instalar dependencias globales

Ejecutar:

~~~
npm install -g truffle
npm install -g ganache-cli
npm install -g @angular/cli
~~~

### Instalar dependencias del proyecto

Ejecutar en la carpeta del proyecto:

~~~
npm install
~~~

### Ejecutar ganache (nodo privado)

Ejecutar en la carpeta del proyecto en una consola separada:

~~~
ganache-cli --gasLimit 7000001
~~~

### Compilar y migrar los contratos al nodo privado

Ejecutar en la carpeta del proyecto en una consola separada:

~~~
truffle compile && truffle migrate
~~~

### Testear los contratos contra el nodo privado

Ejecutar en la carpeta del proyecto en una consola separada:

~~~
truffle test
~~~

### Arrancar el front

Ejecutar en la carpeta del proyecto en una consola separada:

~~~
ng serve
~~~

### Abrir la aplicación

En un navegador con MetaMask instalado abrir: <http://localhost:4200/>

### Para desarrollar

Recomiendo [Visual Studio Code](https://code.visualstudio.com/) con el [plugin de Solidity de Juan Blanco](https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity)