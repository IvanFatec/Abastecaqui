# Abastecaqui



O que é o Abasteçaqui:
O Abasteçaqui foi desenvolvido com o objetivo de trazer mais informações referente a postos de combustíveis no que diz respeito a loclização e preços.
O Abasteçaqui é uma aplicação Mobile, que visa facilitar a vida dos motoristas, trazendo informações referente a preços de combustíveis.
O que nos Motivou a desenvolver o StravaClone:
A Dificuldade que eu tenho em saber qual posto está mais em conta, tanto com preços quanto localização, me motivou a criar essa plataforma.

## 🚧 Status do Projeto *Status:* Em Processo de Desenvolvimento

## ⚙ Funcionalidades e Demonstração da Aplicação
Funcionalidades Principais
[Funcionalidade 1]: Cadastro e autenticação de novos usuários.(Donos de Postos e Motoristas)
[Funcionalidade 2]: Cadastro de preços e promoções
[Funcionalidade 3]: Interface responsiva para acesso via dispositivos móveis.

VISUALIZAÇÃO DA PÁGINA HOME:
Interface Mobile:

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mockup Sistema Abasteça - Motorista</title>
    <style>
        /* Estilos base para simular a tela de um smartphone */
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            background-color: #f0f0f0;
            font-family: Arial, sans-serif;
            margin: 0;
        }

        .app-screen {
            width: 375px; /* Largura padrão de smartphone */
            height: 667px; /* Altura padrão de smartphone */
            background-color: #fff;
            border: 8px solid #333;
            border-radius: 20px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            overflow: hidden;
            display: flex;
            flex-direction: column;
            position: relative;
        }

        /* Área do Mapa */
        .map-area {
            flex-grow: 1;
            background-color: #b3e5fc; /* Cor para simular o mapa */
            display: flex;
            justify-content: center;
            align-items: center;
            color: #000;
            font-weight: bold;
            font-size: 14px;
            position: relative;
        }

        /* Barra de Pesquisa e Filtros */
        .header-search {
            position: absolute;
            top: 20px;
            width: 90%;
            padding: 10px;
            background-color: #fff;
            border-radius: 25px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
            text-align: center;
        }

        /* Lista de Resultados Deslizante (Simulação) */
        .results-list {
            height: 40%; 
            background-color: #fff;
            padding: 10px;
            box-shadow: 0 -4px 8px rgba(0, 0, 0, 0.1);
            overflow-y: scroll;
            border-top-left-radius: 15px;
            border-top-right-radius: 15px;
            position: absolute;
            bottom: 0;
            width: 100%;
            box-sizing: border-box;
        }
        
        .results-list h4 {
            margin-top: 0;
            text-align: center;
            color: #333;
            font-size: 16px;
        }

        /* Filtros Rápidos (Mais Barato / Mais Próximo) */
        .quick-filters {
            display: flex;
            justify-content: space-around;
            margin-bottom: 10px;
        }

        .filter-btn {
            background-color: #4CAF50;
            color: white;
            padding: 5px 10px;
            border: none;
            border-radius: 15px;
            cursor: pointer;
            font-size: 12px;
        }

        .filter-btn:hover {
            background-color: #45a049;
        }

        /* Cartão de Posto */
        .posto-card {
            border: 1px solid #ddd;
            padding: 10px;
            margin-bottom: 8px;
            border-radius: 8px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .posto-info h5 {
            margin: 0 0 5px 0;
            font-size: 14px;
            color: #00796b;
        }

        .posto-info p {
            margin: 0;
            font-size: 12px;
            color: #666;
        }

        .posto-price {
            font-size: 18px;
            font-weight: bold;
            color: #e53935;
        }
        
        .promotion {
            color: #4CAF50;
            font-size: 10px;
            font-weight: bold;
            margin-left: 5px;
        }
    </style>
</head>
<body>

<div class="app-screen">
    
    <div class="map-area">
        Localização Atual (GPS)
        
        <div class="header-search">
            🔍 Buscar endereço ou posto...
        </div>
        
        <div style="position: absolute; top: 50%; left: 30%; color: red; font-size: 20px;">📍 R$ 5,29</div>
        <div style="position: absolute; top: 65%; left: 60%; color: red; font-size: 20px;">📍 R$ 5,19</div>
        <div style="position: absolute; top: 40%; left: 70%; color: red; font-size: 20px;">📍 R$ 5,35</div>
        <div style="position: absolute; top: 55%; left: 15%; color: red; font-size: 20px;">📍 R$ 5,25</div>
    </div>

    <div class="results-list">
        <div style="width: 40px; height: 4px; background-color: #ccc; margin: 0 auto 10px; border-radius: 2px;"></div>
        
        <h4>⛽️ Preços de Gasolina na Região</h4>

        <div class="quick-filters">
            <button class="filter-btn" style="background-color: #00796b;">💰 Mais Barato</button>
            <button class="filter-btn">🗺️ Mais Próximo</button>
        </div>

        <div class="posto-card">
            <div class="posto-info">
                <h5>Posto Économico</h5>
                <p>1.8 km - Gasolina</p>
            </div>
            <div class="posto-price">
                R$ 5,19 <span class="promotion">🔥 PROMO!</span>
            </div>
        </div>

        <div class="posto-card">
            <div class="posto-info">
                <h5>Posto BR Central</h5>
                <p>0.9 km - Gasolina</p>
            </div>
            <div class="posto-price">
                R$ 5,25
            </div>
        </div>

        <div class="posto-card">
            <div class="posto-info">
                <h5>Posto Premium Shell</h5>
                <p>3.5 km - Gasolina</p>
            </div>
            <div class="posto-price">
                R$ 5,35
            </div>
        </div>
        
        <div class="posto-card">
            <div class="posto-info">
                <h5>Posto da Cidade</h5>
                <p>1.5 km - Gasolina</p>
            </div>
            <div class="posto-price">
                R$ 5,40
            </div>
        </div>
        
        </div>

</div>

</body>
</html>
