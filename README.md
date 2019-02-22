# tarefaspendendes
Uma aplicação feita em HTML e JavaScript para Tarefas Pendentes


O programa consiste em um CRUD(Create,Read,Update and Delete) de uma lista de tarefas, além de marcar as tarefas que foram concluídas. Podendo, assim, adicionar, excluir, alterar e marcar com um CheckBox as tarefas concluídas.

Na parte de "Adicionar" a tarefa foi construída uma função em JavaScript que é chamada quando apertado o botão "Adicionar":


	      var tarefa = document.getElementById("tarefaid").value;  ---------- Cria-se uma variavel com o nome "tarefa" e atribui a ela o valor do campo texto do HTML. 
  	    var lista  = document.getElementById("lista").innerHTML; ---------- Cria-se uma variável com o nome "lista" e atribui a ela o valor da lista criada no HTML.
  	    lista = lista+ "li"+tarefa+" input type='checkbox'" +"/li"; ---------- Na variável "lista" é adicionada ela mesma e a tarefa desejada com um checkbox.
	      document.getElementById("lista").innerHTML = lista; --------- O elemento HTML de id "lista" toma como valor a variável lista da função.

Na parte de "Excluir" a tarefa foi construída uma função em JavaScript que é chamada quando apertado o botão "Excluir":


	      var list = document.getElementById("lista"); ---------- Cria-se uma variável com o nome "list" e atribui a ela o valor da lista criada no HTML.
	      var ele = document.getElementById("excluirid").value; ---------- Cria-se uma variável com o nome "ele" e atribui o valor do campo texto do HTML, elemento a ser excluido
	      list.removeChild(list.childNodes[ele]); ---------- Remove o elemento da lista.

Na parte de "Alterar" a tarefa foi construída uma função em JavaScript que é chmada quando apertado o botão "Alterar":


	      var novo = document.getElementById("alterarname").value; -------- Cria-se uma variável com o nome "novo" e atribui a ela o valor do campo texto do HTML e pega o valor.
	var textnode = document.createTextNode(novo); -------- Cria-se uma variável com o nome "textnode" e atribui a ela o valor do novo como TextNode.
	      var ele = document.getElementById("alterarid").value; ------- Cria-se uma variável com o nome ele atribui a ela o valor do index do elemento a ser mudado.
	      var item = document.getElementById("lista").childNodes[ele];  ------- Cria-se uma variável com o nome "item" e atribui a ela o valor do elemento da lista com o index "ele".
	      item.replaceChild(textnode,item.childNodes[0]); ------- Reposiciona o elemento textnode no lugar do selecionado com o ID.
