<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Controle de EPIs e Uniformes</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --accent-color: #3498db;
            --bg-color: #f8f9fa;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 20px;
            color: #333;
        }
        .container {
            max-width: 1100px;
            margin: 0 auto;
        }
        h1, h2 {
            color: var(--primary-color);
        }
        .card {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
            margin-bottom: 20px;
        }
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
        }
        .form-group {
            display: flex;
            flex-direction: column;
        }
        label {
            font-weight: 600;
            margin-bottom: 5px;
            font-size: 14px;
        }
        input, select {
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
        }
        button {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 12px;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
            font-weight: bold;
            margin-top: 15px;
            transition: background 0.2s;
        }
        button:hover {
            background-color: #2980b9;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        th {
            background-color: var(--primary-color);
            color: white;
        }
        tr.clickable {
            cursor: pointer;
        }
        tr.clickable:hover {
            background-color: #f1f2f6;
        }
        .grid-dashboard {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
        }
        @media (max-width: 768px) {
            .grid-dashboard {
                grid-template-columns: 1fr;
            }
        }
        .highlight {
            font-weight: bold;
            color: #e74c3c;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Controle de EPIs e Uniformes</h1>

    <div class="card">
        <h2>Novo Registro de Retirada</h2>
        <form id="epiForm">
            <div class="form-grid">
                <div class="form-group">
                    <label for="colaborador">Nome Completo:</label>
                    <input type="text" id="colaborador" required placeholder="Ex: João da Silva">
                </div>
                <div class="form-group">
                    <label for="tipo">Tipo:</label>
                    <select id="tipo" required>
                        <option value="EPI">EPI</option>
                        <option value="Uniforme">Uniforme</option>
                    </select>
                </div>
                <div class="form-group">
                    <label for="item">Item Solicitado:</label>
                    <input type="text" id="item" required placeholder="Ex: Bota de Segurança, Luva">
                </div>
                <div class="form-group">
                    <label for="tamanho">Tamanho / Numeração:</label>
                    <input type="text" id="tamanho" required placeholder="Ex: 41, M, G">
                </div>
                <div class="form-group">
                    <label for="motivo">Motivo:</label>
                    <select id="motivo" required>
                        <option value="Primeira Entrega">Primeira Entrega</option>
                        <option value="Desgaste Natural">Desgaste Natural</option>
                        <option value="Perda / Extravio">Perda / Extravio</option>
                    </select>
                </div>
            </div>
            <button type="submit">Registrar Retirada</button>
        </form>
    </div>

    <div class="grid-dashboard">
        <div class="card">
            <h2>Ranking de Retiradas</h2>
            <p style="font-size: 13px; color: #666;">Clique em um colaborador para ver o histórico detalhado.</p>
            <table>
                <thead>
                    <tr>
                        <th>Colaborador</th>
                        <th>Total Retiradas</th>
                    </tr>
                 dulces
                    <th style="display:none"></th>
                </thead>
                <tbody id="rankingTableBody">
                    </tbody>
            </table>
        </div>

        <div class="card">
            <h2>Detalhes do Colaborador</h2>
            <p id="detalheTitulo" class="highlight">Selecione um colaborador ao lado</p>
            <table>
                <thead>
                    <tr>
                        <th>Data/Hora</th>
                        <th>Item</th>
                        <th>Tam.</th>
                        <th>Motivo</th>
                    </tr>
                </thead>
                <tbody id="detalheTableBody">
                    <tr><td colspan="4" style="text-align: center; color: #888;">Nenhum colaborador selecionado.</td></tr>
                </tbody>
            </table>
        </div>
    </div>
</div>

<script>
    // Carrega registros salvos no navegador ou inicia array vazio
    let registros = JSON.parse(localStorage.getItem('registros_epi')) || [];

    const epiForm = document.getElementById('epiForm');
    const rankingTableBody = document.getElementById('rankingTableBody');
    const detalheTableBody = document.getElementById('detalheTableBody');
    const detalheTitulo = document.getElementById('detalheTitulo');

    // Manipula o envio do formulário
    epiForm.addEventListener('submit', function(e) {
        e.preventDefault();

        const agora = new Date();
        const dataHoraFormatada = agora.toLocaleString('pt-BR');

        const novoRegistro = {
            id: Date.now(),
            dataHora: dataHoraFormatada,
            colaborador: document.getElementById('colaborador').value.trim(),
            tipo: document.getElementById('tipo').value,
            item: document.getElementById('item').value.trim(),
            tamanho: document.getElementById('tamanho').value.trim(),
            motivo: document.getElementById('motivo').value.trim()
        };

        registros.push(novoRegistro);
        localStorage.setItem('registros_epi', JSON.stringify(registros));

        epiForm.reset();
        atualizarDashboard();
        alert('Registro salvo com sucesso!');
    });

    // Atualiza as tabelas do painel gerencial
    function atualizarDashboard() {
        rankingTableBody.innerHTML = '';

        if (registros.length === 0) {
            rankingTableBody.innerHTML = `<tr><td colspan="2" style="text-align: center; color: #888;">Nenhum registro encontrado.</td></tr>`;
            return;
        }

        // Agrupa contagem por colaborador
        const contagem = {};
        registros.forEach(reg => {
            contagem[reg.colaborador] = (contagem[reg.colaborador] || 0) + 1;
        });

        // Ordena do que mais retirou para o que menos retirou
        const rankingOrdenado = Object.entries(contagem).sort((a, b) => b[1] - a[1]);

        rankingOrdenado.forEach(([colaborador, total]) => {
            const tr = document.createElement('tr');
            tr.className = 'clickable';
            tr.innerHTML = `
                <td><strong>${colaborador}</strong></td>
                <td><span class="highlight">${total}</span> item(ns)</td>
            `;
            // Evento de clique para filtrar o histórico do colaborador
            tr.addEventListener('click', () => mostrarDetalhes(colaborador));
            rankingTableBody.appendChild(tr);
        });
    }

    // Mostra o histórico específico do colaborador clicado
    function mostrarDetalhes(colaboradorNome) {
        detalheTitulo.textContent = `Histórico de: ${colaboradorNome}`;
        detalheTableBody.innerHTML = '';

        const itensColaborador = registros.filter(reg => reg.colaborador === colaboradorNome);

        if (itensColaborador.length === 0) {
            detalheTableBody.innerHTML = `<tr><td colspan="4" style="text-align: center;">Nenhum item encontrado.</td></tr>`;
            return;
        }

        itensColaborador.forEach(reg => {
            const tr = document.createElement('tr');
            tr.innerHTML = `
                <td>${reg.dataHora}</td>
                <td>${reg.item} (${reg.tipo})</td>
                <td>${reg.tamanho}</td>
                <td>${reg.motivo}</td>
            `;
            detalheTableBody.appendChild(tr);
        });
    }

    // Inicializa a tela ao carregar a página
    atualizarDashboard();
</script>

</body>
</html>
