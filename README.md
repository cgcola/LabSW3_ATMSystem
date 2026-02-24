# Lab Seatwork 3 - ATM System

<h3><strong>Problem:</strong></h3>
<p>We will design an ATM system for BPI (Bank of the Philippine Islands) that dispenses cash in denominations of 1000 pesos, 500 pesos, 200 pesos, 100 pesos, 50 pesos, and 20 pesos bills. The system should follow the Chain of Responsibility design pattern to handle the dispensing of cash requests efficiently.</p>

<p>In this implementation, ATMDispenseChain class handles the dispensing logic for BPI's ATM system with denominations of 1000, 500, 100, 50, and 20 peso bills. The BPI_Atm class allows users to adjust (hard-coded) an amount and initiates the dispensing process using the Chain of Responsibility pattern.</p>

<p>This design ensures that the ATM system dispenses cash in the specified denominations according to the requested amount.</p>

<p>In the provided example, the elements of the Chain of Responsibility pattern can be identified as follows:</p>
<ol>
  <li><strong>Handler: </strong>The handler objects are the concrete classes that implement the CurrencyDispenser abstract class. In this case, there are three handlers: <code>Peso1000Dispenser</code>, <code>Peso500Dispenser</code>, <code>Peso200Dispenser</code>, <code>Peso100Dispenser</code>, <code>Peso50Dispenser</code>, and Peso20Dispenser. Each handler is responsible for dispensing a specific denomination of currency.</li>

  <li><strong>Chain: </strong>The chain is represented by the <code>ATMDispenserChain</code> class. It sets up the sequence of handlers by linking them together using the <code>setNextChain()</code> method. The chain is responsible for passing the request along the sequence of handlers until one of them handles it.</li>

  <li><strong>Request: </strong>The request is represented by the <code>dispense()</code> method call made on the first handler in the chain. In this case, the request is to dispense a specific amount of currency.</li>

  <li><strong>Client: </strong>The client is the <code>ATMDispenseChain</code> class that creates and initializes the chain of handlers. It sends the request to the first handler in the chain by calling the <code>dispense()</code> method.</li>

  <li><strong>Context: </strong>The context includes the <code>ATMDispenseChain</code> class, which manages the chain of handlers and ensures that the request is passed along the chain until it is handled.</li>
</ol>

<hr>

### UML Diagram:
