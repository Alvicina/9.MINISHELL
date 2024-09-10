The aim of this project is for us to create our own shell, taking as reference bash. The following guide is top-notch to understand how to implement a shell, therefore kudos to its author and I will share it below:
https://m4nnb3ll.medium.com/minishell-building-a-mini-bash-a-42-project-b55a10598218

Basically the project can be divided in four parts:
1) Parser
2) Execution
3) Built-ins
4) Signals

At least this is how we divided the work. The execution part in our case was done using a AST tree:
https://en.wikipedia.org/wiki/Abstract_syntax_tree
And using recursive descent to solve the AST. Once the user input is parsed, the input is send to the AST module that builts up the AST tree. This logic tree then is solved using recursive descent due two the fact that both concepts (AST && Recursive descent) work pretty well together. The built-ins are just bash commands such as cd or export that will not be executed using the binary in the bin directory through execve. This commands need to be implemented handmade by ourselves (in the project requirements are stated which ones).

By far one one of the toughest projects so far.

This project was first done and finished in a different repo to this one (42 camps provides us with independent repos for each project). Once finished, the project was then copied to my personal repo in gitHub.

In the following pdf you can find the project requirements as specified by 42 campus: [README_MINISHELL.pdf](https://github.com/Alvicina/MINISHELL/files/15310207/README_MINISHELL.pdf)

The following snapshot is proof that the project was succesfully done: 
![Screenshot from 2024-09-10 18-33-16](https://github.com/user-attachments/assets/27ddfaad-84d3-44e6-9c84-13e241fa1ccb)
