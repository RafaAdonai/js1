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
