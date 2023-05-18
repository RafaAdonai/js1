<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset='utf-8'>
    <meta http-equiv='X-UA-Compatible' content='IE=edge'>
    <meta name='viewport' content="width=device-width, initial-scale=1.0">
    <title>Todo Avançado</title>
    <!---Css do projeto-->
    <link rel="stylesheet" href="style/style.css">
    <!---Fonte Awesome-->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
        integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw=="
        crossorigin="anonymous" referrerpolicy="no-referrer" />


    <!--Js Projeto-->

</head>

<body>
    <div class="todo-container">
        <!--a div todo container inicia-->
        <header>
            <h1> Todo Avançado</h1>
        </header>


        <form id="todo-form">
            <p>Adicione a sua tarefa</p>
            <div class="form-control">
                <input type="text" id="todo-input" placeholder="O que vai fazer? ">
                <button type="submit">
                    <i class="fa-thin fa-plus"></i>
                </button>
            </div>
        </form>

        <form id="edit-form" class="hide">
            <p>Edite sua tarefa:</p>
            <div class="form-control">
                <input type="text" id="edit-input">
                <button type="submit">
                    <i class="fa-solid fa-check-double"></i>
                </button>
            </div>
            <button id="cancel-edit-btn">Cancelar</button>
        </form>

        <div id="toolbar">
            <div id="search">
                <h4>Pesquisar:</h4>
                <form>
                    <input type="text" id="search-input" placeholder="Buscar" ">
    <button id=" erase-button">
                    <i class="fa-solid fa-delete-left"></i>
                    </button>
                </form>
            </div>
            <div id="filter">
                <h4>Filtrar:</h4>
                <select i="filter-select">
                    <option value="all">Todos </option>
                    <option value="done">Feitos </option>
                    <option value="todo">A fazer</option>
                </select>
            </div>
        </div>
        <div id="todo-list">
            <div class="todo done">
                <div class="tarefa">
                    <h3>Estou fazendo alguma coisa..</h3>
                    <div class="controles">

                        <button class="finish-todo">
                            <i class="fa-solid fa-check"></i>
                        </button>
        
                        <button class="edit-todo">
                            <i class="fa-solid fa-pen"></i>
                        </button>
        
                        <button class="remove-toddo">
                            <i class="fa-solid fa-xmark"></i>
                        </button>
                    </div>

                </div>

                <div class="tarefa">

                    <h3>Estudar JavaScript..</h3>
    
                    <div class="controles">
                        <button class="finish-todo">
                            <i class="fa-solid fa-check"></i>
                        </button>
        
                        <button class="edit-todo">
                            <i class="fa-solid fa-pen"></i>
                        </button>
        
                        <button class="remove-todo">
                            <i class="fa-solid fa-xmark"></i>
                        </button>

                    </div>

                </div>
            </div>
            <!--a classe toda fecha aqui-->
        </div>
        <!--a ID todo-list fecha aqui-->
    </div>
    <!--a classe todo-container fecha aqui-->
    <script src="java/scripts2.js"defer></script>

</body>

</html>
                                  
                                  /* Geral */
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: Verdana;
  color: #333;
}

body {
  background-image: url("../img/img.jpg");
  background-position: center;
  background-size: cover;
}

button {
  background-color: #fdfdfd;
  color: #102f5e;
  border: 2px solid #102f5e;
  padding: 0.3rem 0.6rem;
  font-size: 1rem;
  cursor: pointer;
  display: flex;
  justify-content: center;
  align-items: center;
  transition: 0.4s;
}

button:hover {
  background-color: #102f5e;
  color: #fff;
}

button:hover > i {
  color: #fff;
}

button i {
  pointer-events: none;
  color: #102f5e;
  font-weight: bold;
}

input,
select {
  padding: 0.25rem 0.5rem;
}

.hide {
  display: none;
}
/* Todo Header */
.todo-container {
  max-width: 450px;
  margin: 3rem auto;
  background-color: #fdfdfd;
  padding: 1.5rem;
  border-radius: 15px;
}
.todo-container header {
  text-align: center;
  padding: 0 1rem 1rem;
  border-bottom: 1px solid #ccc;
}

/* Todo Form */
#todo-form,
#edit-form {
  padding: 1rem;
  border-bottom: 1px solid #ccc;
}

#todo-form p,
#edit-form p {
  margin-bottom: 0.5rem;
  font-weight: bold;
}

.form-control {
  display: flex;
}


.form-control input {
  margin-right: 0.3rem;
}

#cancel-edit-btn {
  margin-top: 1rem;
  color: #444;
}

/* Todo Toolbar */
#toolbar {
  padding: 1rem;
  border-bottom: 1px solid #ccc;
  display: flex;
}

#toolbar h4 {
  margin-bottom: 0.5rem;
}

#search {
  border-right: 1px solid #ddd;
  padding-right: 1rem;
  margin-right: 1rem;
  width: 65%;
  display: flex;
  flex-direction: column;
}

#search form {
  display: flex;
}

#search input {
  width: 100%;
  margin-right: 0.3rem;
}

#filter {
  width: 35%;
  display: flex;
  flex-direction: column;
}

#filter select {
  flex: 1;
}

/* Todo List */
.todo {
  display: flex;
  justify-content: space-around;
  flex-direction: column;
  padding: 1rem ;
  border-bottom: 1px solid #ddd;
  transition: 0.3s;
  gap: 10px;
}

.todo h3 {
  flex: 1;
  font-size: 0.9rem;
}

.todo button {
  margin-left: 0.4rem;
}

.done{
  background-color: #395169;
  
}

.done h3{
  color:#fff;
  text-decoration:line-through;
  font-style: italic;
}
.tarefa{
  display: flex;
  flex-direction: row;
}
.controles{
  display: flex;
  flex-direction: row;
}

                                        //Seleção de elementos
const todoform = document.querySelector("#todo-form");
const todoInput = document.querySelector("#todo-input");
const todolist = document.querySelector("#todo-list");
const editform = document.querySelector("#edit-form");
const editInput= document.querySelector("#edit-input");
const cancelEditBtn = document.querySelector("#cancel-edit-btn");

//funções
const savetodo = (text) =>{
    const todo = document.createElement ("div");
    todo.classList.add("todo") ;
    const todoTitle =document.createElement("h3") ;
    todoTitle.innerText = text;
    todo.appendChild(todoTitle);

    const doneBtn = document.createElement ("button");
    doneBtn.classList.add ("finish-todo");
    doneBtn.innerHTML ='<i class="fa-solid fa-check"></i>';
    todo.appendChild(doneBtn);
   
   const editBtn = document.createElement ("button");
    editBtn.classList.add ("edit-todo");
    editBtn.innerHTML ='<i class="fa-solid fa-pen"></i>';
    todo.appendChild(editBtn);

    const deleteBtn = document.createElement ("button");
    deleteBtn.classList.add ("remove-todo");
    deleteBtn.innerHTML ='<i class="fa-solid fa-xmar"></i>';
    todo.appendChild(deleteBtn)

    todolist.appendChild(todo);

    todoInput.value = "";
    todoInput.focus();
};

const toggleForms = () => {
    editform.classList.toggle ("hide")
    todoform.classList.toggle("hide")
    todolist.classList.toggle ("hide")
};

// Eventos
todoform.addEventListener("submit", (e) => {
    e.preventDefault();

    const inputValue = todoInput.value;

    if (inputValue) {
        savetodo(inputValue);
    }
});

document.addEventListener ("click",(e) => {
    const targetEl = e.target;
    const parentEl = targetEl.closest ("finish-todo")){
        parentEl.classList.toggle ("done");
    }

  if(targetEl.classList.contains("remove-todo")){
 parentEl.remove();
  }

  if(targetEl.classList.contains("edit-todo")){
    console.log("Editou");
     };
   
                                        
                                  
                                  
                                  
