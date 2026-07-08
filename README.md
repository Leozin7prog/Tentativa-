<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Catálogo Natural</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: #f4f7f4;
      padding: 30px 20px;
      color: #2d3e2d;
    }

    h1 {
      text-align: center;
      font-weight: 300;
      letter-spacing: 2px;
      margin-bottom: 30px;
      color: #3a5a3a;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      max-width: 1100px;
      margin: 0 auto;
    }

    .card {
      background: white;
      border-radius: 16px;
      padding: 20px 16px;
      box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
      transition: transform 0.2s, box-shadow 0.2s;
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
      border: 1px solid #e6ece6;
    }

    .card:hover {
      transform: translateY(-4px);
      box-shadow: 0 8px 20px rgba(0, 40, 0, 0.08);
    }

    .card img {
      width: 100%;
      max-width: 140px;
      height: 140px;
      object-fit: contain;
      background: #f9fbf9;
      border-radius: 12px;
      padding: 8px;
      margin-bottom: 12px;
    }

    .card h3 {
      font-size: 1.1rem;
      font-weight: 600;
      margin-bottom: 4px;
      color: #1e3a1e;
    }

    .card .tag {
      font-size: 0.75rem;
      background: #e2efe2;
      color: #2b5e2b;
      padding: 4px 12px;
      border-radius: 20px;
      display: inline-block;
      margin: 6px 0 8px;
      font-weight: 500;
    }

    .card p {
      font-size: 0.9rem;
      color: #4d6b4d;
      margin-bottom: 8px;
    }

    .card .price {
      font-size: 1.2rem;
      font-weight: 700;
      color: #1f4a1f;
      margin-top: auto;
      padding-top: 8px;
      border-top: 1px solid #eef3ee;
      width: 100%;
    }

    /* Responsivo */
    @media (max-width: 768px) {
      .grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    @media (max-width: 480px) {
      .grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <h1>🌿 Catálogo Natural</h1>

  <div class="grid">
    <!-- Produto 1 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Óleo+Coco" alt="Óleo de Coco">
      <h3>Óleo de Coco Extra Virgem</h3>
      <span class="tag">Orgânico</span>
      <p>Prensado a frio, 500ml</p>
      <div class="price">R$ 32,90</div>
    </div>

    <!-- Produto 2 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Chá+Camomila" alt="Chá de Camomila">
      <h3>Chá de Camomila</h3>
      <span class="tag">Floral</span>
      <p>Flores secas, pacote 100g</p>
      <div class="price">R$ 18,50</div>
    </div>

    <!-- Produto 3 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Mel+Silvestre" alt="Mel Silvestre">
      <h3>Mel Silvestre</h3>
      <span class="tag">Puro</span>
      <p>Colheita orgânica, 300g</p>
      <div class="price">R$ 24,90</div>
    </div>

    <!-- Produto 4 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Farinha+Amêndoas" alt="Farinha de Amêndoas">
      <h3>Farinha de Amêndoas</h3>
      <span class="tag">Sem glúten</span>
      <p>400g</p>
      <div class="price">R$ 29,90</div>
    </div>

    <!-- Produto 5 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Sabonete+Argila" alt="Sabonete de Argila">
      <h3>Sabonete de Argila</h3>
      <span class="tag">Vegano</span>
      <p>Com lavanda, 100g</p>
      <div class="price">R$ 12,90</div>
    </div>

    <!-- Produto 6 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Chia" alt="Semente de Chia">
      <h3>Semente de Chia</h3>
      <span class="tag">Orgânica</span>
      <p>Pote 250g</p>
      <div class="price">R$ 15,90</div>
    </div>

    <!-- Produto 7 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Vinagre+Maçã" alt="Vinagre de Maçã">
      <h3>Vinagre de Maçã</h3>
      <span class="tag">Não filtrado</span>
      <p>500ml</p>
      <div class="price">R$ 19,90</div>
    </div>

    <!-- Produto 8 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Escova+Bambu" alt="Escova de Bambu">
      <h3>Escova de Bambu</h3>
      <span class="tag">Biodegradável</span>
      <p>Cerdas naturais</p>
      <div class="price">R$ 9,90</div>
    </div>

    <!-- Produto 9 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Tempero+Ervas" alt="Tempero de Ervas">
      <h3>Tempero de Ervas</h3>
      <span class="tag">Mix</span>
      <p>Para churrasco e saladas, 80g</p>
      <div class="price">R$ 11,90</div>
    </div>

    <!-- Produto 10 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Óleo+Hortelã" alt="Óleo Essencial de Hortelã">
      <h3>Óleo Essencial de Hortelã</h3>
      <span class="tag">Aromático</span>
      <p>10ml</p>
      <div class="price">R$ 35,00</div>
    </div>

    <!-- Produto 11 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Granola" alt="Granola Artesanal">
      <h3>Granola Artesanal</h3>
      <span class="tag">Com castanhas</span>
      <p>Frutas secas, 300g</p>
      <div class="price">R$ 22,90</div>
    </div>

    <!-- Produto 12 -->
    <div class="card">
      <img src="https://via.placeholder.com/140x140/edf5ed/3a5a3a?text=Karité" alt="Creme de Karité">
      <h3>Creme de Manteiga de Karité</h3>
      <span class="tag">Hidratante</span>
      <p>Natural, 120g</p>
      <div class="price">R$ 28,50</div>
    </div>
  </div>

</body>
</html>