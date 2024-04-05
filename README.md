# Desafio SOP

## Resolução Desafio 1

<img src="https://i.pinimg.com/736x/c3/81/59/c38159773f7568f9af92d2546a0974c3.jpg" style="width:500px">

### Parte de HTML 
```
<!DOCTYPE html>
<html>

<head>
    <title> Auxiliar</title>
    <meta charset="UTF-8">
</head>

<body style="background-color: #ffffff; display: flex; flex-direction: column;align-items: center;">

    <header style="background-color: rgb(0, 0, 0);display: flex; flex-direction: column;align-items:row;">
        <h1 style="color:#ffffff; font-size: 50px; padding: 30px; text-align: center;">Guia para novos empreendedores
    </Header>
    </h1>
    <fieldset>
        <legend> Conte sobre sua empresa</legend>
        <div>

            <h2>Calculadora de Despesas</h2>

            <form id="despesasForm">
                <label for="aluguel">Aluguel:</label>
                <input type="number" id="aluguel" name="aluguel">

                <label for="agua">Água:</label>
                <input type="number" id="agua" name="agua">

                <label for="energia">Energia Elétrica:</label>
                <input type="number" id="energia" name="energia">

                <label for="folhaPagamento">Folha de Pagamento:</label>
                <input type="number" id="folhaPagamento" name="folhaPagamento">

                <label for="impostos">Impostos:</label>
                <input type="number" id="impostos" name="impostos">

                <button type="button" onclick="calcularDespesas()">Calcular Despesas</button>
            </form>

        </div>
    </fieldset>

 
    <main>
        <h1 style="color:rgb(19, 38, 55); font-size: 20px;" id="totalGastos">Total de gastos: </h1>
        <h1 style="color:rgb(19, 38, 55); font-size: 20px;" id="mediaGastos">Media de gastos: </h1>
        <h1 style="color:rgb(19, 38, 55); font-size: 20px;" id="estimativaAnual">Estimativa Anual: </h1>
    </main>


    <footer style="background-color:#000000; color:hsl(0, 0%, 100%); font-size: 10;"> By:João Lucas, Laila,Leonardo,
        Lucas G., Lucas H., Milena </footer>
''

<script src="script.js"></script>
</body>

</html>
``` 

### Parte de JS
```
function calcularDespesas() {
            var aluguel = parseFloat(document.getElementById('aluguel').value);
            var agua = parseFloat(document.getElementById('agua').value);
            var energia = parseFloat(document.getElementById('energia').value);
            var folhaPagamento = parseFloat(document.getElementById('folhaPagamento').value);
            var impostos = parseFloat(document.getElementById('impostos').value);

            const totalGastos = document.querySelector("h1#totalGastos");
            const mediaGastos = document.querySelector("h1#mediaGastos");
            const estimativaAnual = document.querySelector("h1#estimativaAnual");


            totalGastos.innerHTML = `<p>Total de gastos: R$ ${aluguel + agua + energia + folhaPagamento + impostos}</p>`;
            mediaGastos.innerHTML = `<p>Media de gastos: R$ ${(aluguel + agua + energia + folhaPagamento + impostos)/5}</p>`;
            estimativaAnual.innerHTML = `<p>Estimativa Anual: R$ ${(aluguel + agua + energia + folhaPagamento + impostos) * 12}</p>`;

            // resultadoHTML += "<h3>Média de Gastos:</h3>";
            // resultadoHTML += "<p>R$ " + mediaGastos.toFixed(2) + "</p>";
            // resultadoHTML += "<h3>Estimativa Anual de Gastos:</h3>";
            // resultadoHTML += "<p>R$ " + estimativaAnual.toFixed(2) + "</p>";

            // document.getElementById('resultado').innerHTML = resultadoHTML;
            console.log(totalGastos);
            console.log(mediaGastos);
            console.log(estimativaAnual);
        }
```



