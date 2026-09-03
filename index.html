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
            --bg-color: #f4f6f9;
        }
        * {
            box-sizing: border-box;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            margin: 0;
            padding: 10px;
            color: #333;
        }
        .container {
            max-width: 1000px;
            margin: 0 auto;
        }
        h1 {
            font-size: 1.5rem;
            text-align: center;
            color: var(--primary-color);
            margin-bottom: 15px;
        }
        h2 {
            font-size: 1.2rem;
            color: var(--primary-color);
            margin-top: 0;
        }
        .card {
            background: white;
            padding: 15px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            margin-bottom: 15px;
        }
        .form-grid {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }
        .form-group {
            display: flex;
            flex-direction: column;
        }
        label {
            font-weight: 600;
            margin-bottom: 4px;
            font-size: 13px;
        }
        input, select {
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 6px;
            font-size: 16px; /* Tamanho 16px evita zoom automático indesejado no iOS/Android */
            width: 100%;
        }
        button {
            background-color: var(--accent-color);
            color: white;
            border: none;
            padding: 14px;
            border-radius: 6px;
            font-size: 16px;
            cursor: pointer;
            font-weight: bold;
            width: 100%;
            margin-top: 5px;
            transition: background 0.2s;
        }
        button:active {
            background-color: #2980b9;
        }
        .search-box {
            margin-bottom: 12px;
        }
        .table-responsive {
            width: 100%;
            overflow-x: auto;
            -webkit-overflow-scrolling: touch;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 14px;
            min-width: 280px;
        }
        th, td {
            padding: 10px;
            text-align: left;
            border-bottom: 1px solid #eee;
        }
        th {
            background-color: var(--primary-color);
            color: white;
            font-size: 13px;
        }
        tr.clickable {
            cursor: pointer;
        }
        tr.clickable:hover {
            background-color: #f1f2f6;
        }
        .highlight {
            font-weight: bold;
            color: #e74c3c;
        }
        .grid-dashboard {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        /* Layout para Telas Maiores (PC/Tablet) */
        @media (min-width: 768px) {
            body { padding: 20px; }
            h1 { font-size: 2rem; }
            .form-grid {
                display: grid;
                grid-template-columns: repeat(2, 1fr);
                gap: 15px;
            }
            .form-group.full-width {
                grid-column: span 2;
            }
            button {
                grid-column: span 2;
            }
            .grid-dashboard {
                display: grid;
                grid-template-columns: 1fr 1fr;
                gap: 20px;
            }
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
                <div class="form-group full-width">
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
                    <label for="tamanho">Tamanho / Numeração:</label>
                    <input type="text" id="tamanho" required placeholder="Ex: 41, M, G">
                </div>
                <div class="form-group full-width">
                    <label for="item">Item Solicitado:</label>
                    <input type="text" id="item" required placeholder="Ex: Bota de Segurança, Luva, Camisa">
                </div>
                <div class="form-group full-width">
                    <label for="motivo">Motivo:</label>
                    <select id="motivo" required>
                        <option value="Primeira Entrega">Primeira Entrega</option>
                        <option value="Desgaste Natural">Desgaste Natural</option>
                        <option value="Perda / Extravio">Perda / Extravio</option>
                    </select>
                </div>
                <button type="submit">Registrar Retirada</button>
            </div>
        </form>
    </div>

    <div class="grid-dashboard">
        <div class="card">
            <h2>Ranking de Retiradas</h2>
            <div class="search-box">
                <input type="text" id="searchInput" placeholder="🔍 Buscar funcionário..." onkeyup="filtrarRanking()">
            </div>
            <p style="font-size: 12px; color: #666; margin-top: 0;">Toque em um nome para ver o histórico.</p>
            <div class="table-responsive">
                <table>
                    <thead>
                        <tr>
                            <th>Colaborador</th>
                            <th>Total</th>
                        </tr>
                    </thead>
                    <tbody id="rankingTableBody">
                        </tbody>
                </table>
            </div>
        </div>

        <div class="card">
            <h2>Detalhes do Colaborador</h2>
            <p id="detalheTitulo" class="highlight" style="font-size: 14px;">Selecione um colaborador ao lado</p>
            <div class="table-responsive">
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
                        <tr><td colspan="4" style="text-align: center; color: #888;">Nenhum selecionado.</td></tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
</div>

<script>
    let registros = JSON.parse(localStorage.getItem('registros_epi')) || [];
    let rankingCache = []; // Armazena os dados para a busca

    const epiForm = document.getElementById('epiForm');
    const rankingTableBody = document.getElementById('rankingTableBody');
    const detalheTableBody = document.getElementById('detalheTableBody');
    const detalheTitulo = document.getElementById('detalheTitulo');
    const searchInput = document.getElementById('searchInput');

    epiForm.addEventListener('submit', function(e) {
        e.preventDefault();

        const agora = new Date();
        const dataHoraFormatada = agora.toLocaleString('pt-BR', { dateStyle: 'short', timeStyle: 'short' });

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

    function atualizarDashboard() {
        rankingTableBody.innerHTML = '';

        if (registros.length === 0) {
            rankingTableBody.innerHTML = `<tr><td colspan="2" style="text-align: center; color: #888;">Nenhum registro.</td></tr>`;
            return;
        }

        const contagem = {};
        registros.forEach(reg => {
            contagem[reg.colaborador] = (contagem[reg.colaborador] || 0) + 1;
        });

        rankingCache = Object.entries(contagem).sort((a, b) => b[1] - a[1]);
        exibirTabelaRanking(rankingCache);
    }

    function exibirTabelaRanking(dados) {
        rankingTableBody.innerHTML = '';
        if (dados.length === 0) {
            rankingTableBody.innerHTML = `<tr><td colspan="2" style="text-align: center; color: #888;">Nenhum funcionário encontrado.</td></tr>`;
            return;
        }

        dados.forEach(([colaborador, total]) => {
            const tr = document.createElement('tr');
            tr.className = 'clickable';
            tr.innerHTML = `
                <td><strong>${colaborador}</strong></td>
                <td><span class="highlight">${total}</span> un</td>
            `;
            tr.addEventListener('click', () => mostrarDetalhes(colaborador));
            rankingTableBody.appendChild(tr);
        });
    }

    function filtrarRanking() {
        const termo = searchInput.value.toLowerCase();
        const filtrado = rankingCache.filter(([colaborador]) => 
            colaborador.toLowerCase().includes(termo)
        );
        exibirTabelaRanking(filtrado);
    }

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

    atualizarDashboard();
</script>

</body>
</html>
