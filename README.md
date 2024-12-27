# Questão 3 - Murano

<h1> A) Classificações de Padrões de Projeto </h1>
<p> Os padrões de projeto, conhecidos pelo inglês <i> design patterns </i>, são soluções reutilizáveis para problemas comuns no design de software. 
<h2> 1. Padrões Criacionais </h2>
<p> São esses os que fornecem mecanismos de criação de objetos que aumentam a flexibilidade e a reutilização de código. focando em como os objetos são instanciados e inicializados. </p>
<p> Alguns exemplos de padrões criacionais são: </p>
<h3> 1.1. Singleton </h3>
<p> Tipo de objeto que pode apenas ser instanceado uma vez, fornecendo um ponto global de acesso ao mesmo. </p>
<h3> 1.2. Builder </h3>
<p> Criação de um objeto passo-a-passo, pela utilização de métodos. Permite que o mesmo processo de construção crie diferentes representações.</p>
<h3> 1.3. Factory </h3>
<p> Definição de uma interface para criar objetos. </p>

<h2> 2. Padrões Estruturais </h2>
<p> São esses os que permitem montar objetos e classes em estruturas maiores, ainda mantendo tais estruturas flexíveis e eficientes.</p>
<p> Alguns exemplos de padrões estruturais são: </p>
<h3> 2.1. Facade </h3>
<p> Fornece uma interface simplificada para um conjunto complexo de classes. É util quando o usuário precisa integrar sua aplicação com uma biblioteca complexa, mas precisa apenas de dados específicos delas.</p>
<h3> 2.2. Adapter </h3>
<p> Permite que classes com interfaces incompatíveis trabalhem juntas, converte a interface de um dos objetos para que o outro consiga entender. </p>
<h3> 2.3. Proxy </h3>
<p> Permite que o usuário forneça um substituto para outro objeto. Tal substituto é chamado de proxy, e adiciona uma camada intermediária entre o usuário e o objeto real. </p>

<h2> 3. Padrões Comportamentais </h2>
<p> Focam na comunicação e interação entre os objetos, especificando como eles colaboram para realizar tarefas específicas. </p>
<p> Alguns exemplos de padrões comportamentais são: </p>
<h3> 3.1. Observer </h3>
<p> Permite com que um objeto notifique automaticamente outros objetos observadores quando ocorre uma mudança em seu estado. </p>
<h3> 3.2. Strategy </h3>
<p> Permite que uma família de algoritmos seja definida, encapsulada e intercambiável. </p>
<h3> 3.3. State </h3>
<p> Permite que um objeto altere seu comportamento quando seu estado interno muda. </p>

<h1> B) Melhorias ao Pseudocódigo: </h1>
<p> O código pode ser melhorado utilizando o padrão criacional Factory, que foi explicado anteriormente, para evitar a dependência direta de múltiplas fábricas (como Factory_A e Factory_B) no código principal. O objetivo seria centralizar a lógica de criação em uma interface comum, e permitir que subclasses decidam qual botão criar, simplificando o código. Para isso, podemos criar uma interface comum para os botões (IButton), e depois uma interface comum para construir botões (IButtonFactory). A partir disso, podemos criar fábricas específicas para cada sistema operacional, com cada uma criando uma instância do botão correspondente. Teríamos algo como: </p>

![image](https://github.com/user-attachments/assets/889ff2dd-ade2-40dc-9092-86a60f771408)

<p> Assim, podemos modificar a classe Site para depender apenas da interface da fábrica, sem a necessidade de verificar o tipo de sistema operacional diretamente. Utilizando a ferramenta PLantUML, é possível realizar o seguinte digrama de classes: </p>

![image](https://github.com/user-attachments/assets/3d83ed03-f01d-4fda-b5c9-18e4399dd8d7)
