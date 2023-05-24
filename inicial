<!DOCTYPE html>
<html>
<head>
    <title>Previsão de Empréstimo</title>
</head>
<body>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>
        $(document).ready(function() {
            // Função para enviar os dados e obter a previsão
            function fazerPrevisao() {
                var txt_uf = $("#txt_uf").val();
                var txt_origem_contrato = $("#txt_origem_contrato").val();
                var txt_modalidade_programa = $("#txt_modalidade_programa").val();
                var txt_faixa_grupo_renda = $("#txt_faixa_grupo_renda").val();

                // Enviar os dados para o servidor
                $.ajax({
                    type: "POST",
                    url: "previsao_empreendimento.py",
                    data: {
                        txt_uf: txt_uf,
                        txt_origem_contrato: txt_origem_contrato,
                        txt_modalidade_programa: txt_modalidade_programa,
                        txt_faixa_grupo_renda: txt_faixa_grupo_renda
                    },
                    success: function(result) {
                        // Exibir o resultado
                        $("#resultado").text(result);
                    }
                });
            }

            // Associar o evento de clique ao botão de previsão
            $("#btn_prever").click(function() {
                fazerPrevisao();
            });
        });
    </script>

    <h1>Previsão de Empréstimo</h1>

    <label for="txt_uf">Estado:</label>
    <input type="text" id="txt_uf"><br>

    <label for="txt_origem_contrato">Origem do Contrato (PF/PJ):</label>
    <input type="text" id="txt_origem_contrato"><br>

    <label for="txt_modalidade_programa">Modalidade do Programa:</label>
    <input type="text" id="txt_modalidade_programa"><br>

    <label for="txt_faixa_grupo_renda">Faixa de Renda:</label>
    <input type="text" id="txt_faixa_grupo_renda"><br>

    <button id="btn_prever">Prever</button>

    <h2>Resultado da Previsão:</h2>
    <pre id="resultado"></pre>
</body>
</html>
