# Making your first quantum game

To start learning about new computing tools, it is common to hack out simple games. So if you want to learn about quantum computing, making a game could be a good place to start!

## You'll need quantum!

To make a quantum game, you'll need to write quantum software. The basic unit of quantum software is the *circuit*. You can create and manipulate these in Python by using the **Qiskit** framework.
* [Qiskit](https://qiskit.org)

Once you have your quantum software, you need to run it. For complex quantum circuits, the only option is to run it on actual quantum computers. Prototype examples of this quantum hardware are freely available at the **IBM Quantum Experience**. It is a cloud service, where you submit your quantum jobs to run in the IBM Quantum labs. Note that it will take at least a few minutes to get your results back, so the wait time would need to be taken into account in your game.
* [IBM Quantum Experience](https://quantum-computing.ibm.com)

If your quantum circuits are not very complex, you can avoid the need to use real quantum hardware. Instead you can just emulate it on your laptop (or even your phone) using tools bundled in with Qiskit. This is what is done by the vast majority of games that have been made using Qiskit so far (such as [QPong](https://www.youtube.com/watch?v=a1NZC5rqQD8))
* [Qiskit Simulators](https://qiskit.org/overview#simulators)


## You'll need a game engine!

As with making any game, you'll need a game engine. Since Qiskit is written in Python, it is easiest to make a game using a Python-based game engine such as Pygame. However, note that it can be hard for players to be able to install and play such games. See (non-quantum) examples from the [PyWeek game jam](https://pyweek.org/all_games/).
* [PyGame](https://www.pygame.org/wiki/about)

An even easier way to integrate with IBM Quantum resources is to use the **Jupyter Widget Engine**: a game engine designed to run inside the IBM Quantum Experience. It is a very simple engine, giving you a screen of at most ~20x20 pixels. But simplicity can also be helpful if you are mostly making the game to learn about quantum computing.
* [Example game with the Jupyter Widget Engine](https://nbviewer.jupyter.org/github/quantumjim/jupyter-widget-game-engine/blob/master/first-quantum-game.ipynb)
* [How to use the Jupyter Widget Engine](https://nbviewer.jupyter.org/github/quantumjim/jupyter-widget-game-engine/blob/master/jupyter_widget_game.ipynb)

When using this engine, you'll need your players make an account for the IBM Quantum Experience and navigate to the [Quantum Lab](https://quantum-computing.ibm.com/jupyter). After that, it should be easy for them to play. See the following example game jam game made with this engine.
* [Deep Space O'Brien](https://gist.github.com/quantumjim/122f86c34a41e24b9929e924f9d00e85)

You can also use a proper game engine, like Unity or Godot. For this you can try to find some way to integrate Qiskit yourself. Or you can use **MicroQiskit**: a minimal reimplementation of Qiskit in languages such as C++, C# and Lua. This gives the basic functionaly required to create quantum circuits and run them on a simulator.
* [MicroQiskit](https://github.com/qiskit-community/MicroQiskit/blob/master/README.md)


## You'll need an idea!

If you are making the game to teach yourself quantum, one option is simply to learn some very basic quantum computing principles, and then think about how to use them in a game. For example, the first game made for quantum computers, [Battleships for Partial NOT Gates](https://medium.com/qiskit/how-to-program-a-quantum-computer-982a9329ed02), used a single qubit to store the damage taken by each ship. Single qubit gates where then used to implement attacks. No fancy algorithms. Just a basic use of some of the simplest building blocks.

To learn some of these basic quantum concepts for yourself, check out the first few sections of the textbook **Learn Quantum Computation using Qiskit**. The first chapter starts off quite gently, without assuming too much background mathematical knowlege.
* [Qiskit textbook](https://qiskit.org/textbook/preface.html)

If you prefer to learn by playing, there is also a set of interactive puzzles to take you through the basics of qubits and quantum gates.
* [Hello Qiskit puzzles](https://qiskit.org/textbook/ch-ex/hello-qiskit.html)

If you already know quantum, you could make a game to teach other people. Examples of this are the 'Hello Qiskit' puzzles mentioned above, **QiskitBlocks** and many more.
* [QiskitBlocks](https://github.com/JavaFXpert/QiskitBlocks/blob/master/README.md)
* [The History of Games for Quantum Computers](https://medium.com/@decodoku/the-history-of-games-for-quantum-computers-a1de98859b5a)

But perhaps you don't want to be using the machine language of quantum computation at all. Instead you'd rather use more abstract tools, built out of quantum software to provide useful results for the game industry. For that we have **QuantumBlur**: software build on Qiskit for image manipulation, terrain generation and more. It has even been fully integrated into Unity!
* [QuantumBlur](https://github.com/qiskit-community/QuantumBlur/blob/master/README.md)
