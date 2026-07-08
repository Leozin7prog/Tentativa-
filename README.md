<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DR Atacadista | Produtos Naturais</title>
    
    <!-- Bootstrap 5 -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

    <style>
        /* ============================================= */
        /* ESTILOS - TEMA PRODUTOS NATURAIS (VERDE)       */
        /* ============================================= */
        
        /* Definição das cores do tema */
        :root {
            --green-dark: #1b5e20;     /* Verde escuro da natureza */
            --green-main: #2e7d32;     /* Verde principal */
            --green-light: #8bc34a;    /* Verde claro (folhas novas) */
            --green-pale: #f1f8e9;     /* Fundo clarinho suave */
            --brown-soft: #6d4c41;     /* Tom terra */
            --beige-bg: #fafbf7;       /* Fundo do site levemente amarelado/natural */
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            background: var(--beige-bg); /* Fundo claro e natural */
            color: #333; 
            line-height: 1.6;
        }

        /* MENU - Estilo mais orgânico */
        .navbar {
            background: linear-gradient(135deg, var(--green-dark), var(--green-main)) !important;
            box-shadow: 0 4px 15px rgba(27, 94, 32, 0.3);
            border-bottom: 3px solid var(--green-light);
        }
        .navbar-brand { font-size: 1.4rem; font-weight: 700; letter-spacing: 1px; }
        .navbar-brand img { filter: drop-shadow(0 2px 4px rgba(0,0,0,0.2)); }
        .nav-link { font-weight: 500; margin-left: 15px; transition: .3s; position: relative; }
        .nav-link:hover { color: var(--green-light) !important; transform: translateY(-2px); }
        .nav-link i { margin-right: 5px; }

        /* HERO - Banner com visual de natureza */
        .hero {
            padding: 80px 0;
            background: linear-gradient(120deg, var(--green-main) 0%, var(--green-light) 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }
        /* Detalhe de fundo simulando folhas */
        .hero::before {
            content: "🌿";
            position: absolute;
            right: 5%;
            top: 20%;
            font-size: 15rem;
            opacity: 0.1;
            transform: rotate(20deg);
        }
        .hero h1 { 
            font-size: 3.2rem; 
            margin-bottom: 20px; 
            font-weight: 800; 
            text-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .hero p { font-size: 1.3rem; margin-bottom: 30px; font-weight: 300; }
        .hero .btn-light { 
            background: white; 
            color: var(--green-dark); 
            font-weight: 700; 
            border-radius: 50px;
            padding: 12px 30px;
            border: 2px solid transparent;
        }
        .hero .btn-light:hover {
            background: transparent;
            color: white;
            border-color: white;
        }

        /* PESQUISA */
        .input-group { box-shadow: 0 8px 25px rgba(46, 125, 50, 0.1); border-radius: 50px; overflow: hidden; }
        .input-group-text { background: var(--green-main); color: white; border: none; padding: 0 20px; }
        .form-control { border: none; padding: 15px 20px; }
        .form-control:focus { box-shadow: none; border-color: var(--green-light); }

        /* CATEGORIAS */
        #categorias { margin-top: 60px; }
        .categoria {
            border-radius: 50px;
            padding: 8px 28px;
            font-weight: 600;
            transition: .3s;
            border: 2px solid var(--green-main);
            color: var(--green-dark);
        }
        .categoria:hover {
            transform: translateY(-4px);
            box-shadow: 0 5px 15px rgba(46, 125, 50, 0.2);
        }
        .categoria.active, .categoria.btn-success {
            background: var(--green-dark) !important;
            border-color: var(--green-dark) !important;
        }

        /* PRODUTOS - Cards mais naturais */
        #produtos { margin-top: 50px; }
        .card-produto {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            transition: .4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            box-shadow: 0 5px 20px rgba(0,0,0,0.05);
            height: 100%;
            display: flex;
            flex-direction: column;
            border: 1px solid rgba(46, 125, 50, 0.1);
        }
        .card-produto:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(46, 125, 50, 0.15);
            border-color: var(--green-light);
        }
        .card-produto img {
            width: 100%;
            height: 260px;
            object-fit: contain;
            padding: 25px;
            background: #fff;
            transition: .3s;
        }
        .card-produto:hover img { transform: scale(1.05); }
        
        .card-body { padding: 20px 25px 25px; display: flex; flex-direction: column; flex: 1; }
        .card-title { 
            font-size: 1.2rem; 
            font-weight: 700; 
            color: var(--green-dark); 
            margin-bottom: 8px; 
            line-height: 1.4;
        }
        .card-text { flex: 1; color: #555; font-size: .95rem; line-height: 1.5; }
        
        .preco { 
            font-size: 2rem; 
            font-weight: 800; 
            color: var(--green-main); 
            margin: 15px 0; 
        }
        .preco small { font-size: 1rem; font-weight: 400; color: #888; }

        .badge-top {
            position: absolute;
            top: 15px;
            left: 15px;
            background: var(--green-light);
            color: var(--green-dark);
            padding: 5px 15px;
            border-radius: 30px;
            font-size: .8rem;
            font-weight: 700;
            z-index: 2;
        }
        
        .btn-natural {
            background: var(--green-main);
            color: white;
            font-weight: 700;
            border: none;
            width: 100%;
            padding: 12px;
            border-radius: 50px;
            transition: .3s;
            letter-spacing: 0.5px;
        }
        .btn-natural:hover {
            background: var(--green-dark);
            color: white;
            transform: scale(1.02);
            box-shadow: 0 5px 15px rgba(46, 125, 50, 0.3);
        }
        .btn-natural i { margin-right: 8px; }

        /* CTA e FOOTER */
        section.bg-success { 
            background: linear-gradient(135deg, var(--green-dark), var(--green-main)) !important; 
            margin-top: 80px; 
            border-radius: 0; 
        }
        footer {
            margin-top: 80px;
            background: #1a2e1a !important; /* Um verde bem escuro, quase preto */
            border-top: 5px solid var(--green-light);
        }
        footer h5 { margin-bottom: 20px; font-weight: 700; color: var(--green-light); }
        footer a { transition: .3s; }
        footer a:hover { color: var(--green-light) !important; transform: translateX(5px); }

        /* BOTÃO TOPO */
        #topo {
            position: fixed;
            bottom: 25px;
            right: 25px;
            width: 55px;
            height: 55px;
            border: none;
            border-radius: 50%;
            background: var(--green-main);
            color: white;
            font-size: 22px;
            cursor: pointer;
            display: none;
            box-shadow: 0 8px 20px rgba(0,0,0,0.2);
            transition: .3s;
            z-index: 999;
        }
        #topo:hover { transform: scale(1.1) translateY(-5px); background: var(--green-dark); }

        /* RESPONSIVIDADE */
        @media(max-width: 992px) {
            .hero { text-align: center; padding: 60px 20px; }
            .hero h1 { font-size: 2.5rem; }
            .hero::before { font-size: 10rem; top: 10%; }
        }
        @media(max-width: 768px) {
            .card-produto img { height: 200px; }
            .hero h1 { font-size: 2rem; }
            .preco { font-size: 1.6rem; }
        }
        @media(max-width: 576px) {
            .hero { padding: 40px 15px; }
            .hero p { font-size: 1rem; }
            .categoria { margin-bottom: 10px; width: 100%; }
            #topo { width: 48px; height: 48px; }
        }
    </style>
</head>
<body>

    <!-- ========================= -->
    <!-- MENU - TEMÁTICA NATURAL -->
    <!-- ========================= -->
    <nav class="navbar navbar-expand-lg navbar-dark shadow sticky-top">
        <div class="container">
            <a class="navbar-brand fw-bold" href="#">
                <!-- Substitua pelo caminho da sua Logo Verde -->
                <i class="fas fa-leaf me-2"></i> DR Atacadista
            </a>
            <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#menu">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="menu">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#"><i class="fas fa-home"></i> Início</a></li>
                    <li class="nav-item"><a class="nav-link" href="#produtos"><i class="fas fa-bottle-water"></i> Produtos</a></li>
                    <li class="nav-item"><a class="nav-link" href="#categorias"><i class="fas fa-tags"></i> Categorias</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contato"><i class="fas fa-envelope"></i> Contato</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- ========================= -->
    <!-- BANNER -->
    <!-- ========================= -->
    <section class="hero">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-7">
                    <h1 class="display-4 fw-bold">Sua saúde <br>vem da natureza.</h1>
                    <p class="lead">Vitaminas, suplementos e produtos naturais com qualidade e preço de atacado.</p>
                    <a href="#produtos" class="btn btn-light btn-lg">Explorar Catálogo</a>
                </div>
                <div class="col-lg-5 text-center">
                    <img src="https://placehold.co/550x450/ffffff/2e7d32?text=Natureza+%2B+Sa%C3%BAde" class="img-fluid rounded shadow-lg" style="border-radius: 50px 50px 50px 0 !important;">
                </div>
            </div>
        </div>
    </section>

    <!-- ========================= -->
    <!-- PESQUISA -->
    <!-- ========================= -->
    <section class="container mt-5">
        <div class="row">
            <div class="col-lg-8 mx-auto">
                <div class="input-group shadow-sm">
                    <span class="input-group-text"><i class="fas fa-search"></i></span>
                    <input type="text" id="pesquisa" class="form-control" placeholder="Pesquisar produtos naturais...">
                </div>
            </div>
        </div>
    </section>

    <!-- ========================= -->
    <!-- CATEGORIAS -->
    <!-- ========================= -->
    <section id="categorias" class="container mt-5">
        <h2 class="text-center mb-4" style="color: var(--green-dark); font-weight: 700;">Nossas Categorias</h2>
        <div class="d-flex flex-wrap justify-content-center gap-3">
            <button class="btn btn-success categoria active" data-cat="todos">🌿 Todos</button>
            <button class="btn btn-outline-success categoria" data-cat="vitaminas">Vitaminas</button>
            <button class="btn btn-outline-success categoria" data-cat="aminoacidos">Aminoácidos</button>
            <button class="btn btn-outline-success categoria" data-cat="beleza">Beleza Natural</button>
            <button class="btn btn-outline-success categoria" data-cat="omega">Ômega</button>
            <button class="btn btn-outline-success categoria" data-cat="colageno">Colágeno</button>
        </div>
    </section>

    <!-- ========================= -->
    <!-- PRODUTOS -->
    <!-- ========================= -->
    <section id="produtos" class="container mt-5">
        <div class="row" id="listaProdutos">
            <!-- Os cards serão carregados dinamicamente -->
        </div>
    </section>

    <!-- ========================= -->
    <!-- CTA -->
    <!-- ========================= -->
    <section class="text-white py-5 mt-5" style="background: linear-gradient(135deg, var(--green-dark), var(--green-main)); border-radius: 0;">
        <div class="container text-center">
            <h2 class="fw-bold"><i class="fas fa-seedling me-2"></i> Não encontrou o produto ideal?</h2>
            <p class="mt-2 opacity-75">Nossa equipe está pronta para te ajudar a encontrar o melhor para a sua saúde.</p>
            <a href="https://wa.me/5500000000000" target="_blank" class="btn btn-light btn-lg mt-3" style="border-radius: 50px; padding: 12px 35px;">
                <i class="fab fa-whatsapp text-success me-2" style="font-size: 1.3rem;"></i> Atendimento via WhatsApp
            </a>
        </div>
    </section>

    <!-- ========================= -->
    <!-- RODAPÉ -->
    <!-- ========================= -->
    <footer id="contato" class="text-white mt-5">
        <div class="container py-5">
            <div class="row g-4">
                <div class="col-md-4">
                    <h5><i class="fas fa-leaf me-2"></i> DR Atacadista</h5>
                    <p class="text-white-50">Suplementos e vitaminas de alta qualidade, cultivados com a pureza que a natureza oferece.</p>
                </div>
                <div class="col-md-4">
                    <h5><i class="fas fa-headset me-2"></i> Contato</h5>
                    <p class="text-white-50"><i class="fas fa-phone me-2"></i> (00) 0000-0000</p>
                    <p class="text-white-50"><i class="fab fa-whatsapp me-2"></i> (00) 90000-0000</p>
                    <p class="text-white-50"><i class="fas fa-envelope me-2"></i> contato@dratacadista.com.br</p>
                </div>
                <div class="col-md-4">
                    <h5><i class="fas fa-share-alt me-2"></i> Siga-nos</h5>
                    <div class="mt-3">
                        <a href="#" class="text-white me-3 fs-4"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="text-white me-3 fs-4"><i class="fab fa-facebook"></i></a>
                        <a href="#" class="text-white fs-4"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
            </div>
            <hr class="mt-4" style="border-color: rgba(255,255,255,0.1);">
            <div class="text-center text-white-50 small">
                © 2026 DR Atacadista - Produtos Naturais. Todos os direitos reservados.
            </div>
        </div>
    </footer>

    <button id="topo"><i class="fas fa-arrow-up"></i></button>

    <!-- ========================= -->
    <!-- SCRIPTS (Já integrados)  -->
    <!-- ========================= -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>

    <script>
        // ---- BANCO DE DADOS DOS PRODUTOS ----
        const produtos = [
            {
                id: 1,
                nome: "6 Magnésios",
                categoria: "vitaminas",
                imagem: "https://placehold.co/300x300/ffffff/2e7d32?text=6+Magn%C3%A9sios", 
                preco: 35.90,
                peso: "1000mg",
                quantidade: "60 Comprimidos",
                descricao: "Combinação de seis tipos de magnésio para melhor absorção. Essencial para a função cardiovascular e energia."
            },
            {
                id: 2,
                nome: "Arginina e Alanina",
                categoria: "aminoacidos",
                imagem: "https://placehold.co/300x300/1b5e20/ffffff?text=Arginina+Alanina", 
                preco: 44.90,
                peso: "1000mg",
                quantidade: "120 Comprimidos",
                descricao: "Aminoácidos que atuam na circulação sanguínea e desempenho físico. Melhora vascular e recuperação muscular."
            },
            {
                id: 3,
                nome: "Barba e Cabelos",
                categoria: "beleza",
                imagem: "https://placehold.co/300x300/8bc34a/ffffff?text=Barba+Cabelos", 
                preco: 29.90,
                peso: "500mg",
                quantidade: "60 Cápsulas",
                descricao: "Fórmula com vitaminas e minerais. Estimula o crescimento, fortalece os fios e previne a queda."
            },
            {
                id: 4,
                nome: "Coenzima Q10",
                categoria: "vitaminas",
                imagem: "https://placehold.co/300x300/2e7d32/ffffff?text=Coenzima+Q10", 
                preco: 39.90,
                peso: "1000mg",
                quantidade: "60 Comprimidos",
                descricao: "Potente antioxidante que auxilia na produção de energia celular. Fortalece o coração e combate o envelhecimento."
            },
            {
                id: 5,
                nome: "Colágeno Hidrolisado (C/ Ácido Hialurônico)",
                categoria: "colageno",
                imagem: "https://placehold.co/300x300/6d4c41/ffffff?text=Col%C3%A1geno", 
                preco: 34.90,
                peso: "1000mg",
                quantidade: "90 Comprimidos Mastigáveis",
                descricao: "Auxilia na firmeza da pele, hidratação, fortalecimento de unhas e cabelos. Ajuda a proteger as articulações."
            },
            {
                id: 6,
                nome: "Ômega 3 (Óleo de Peixe)",
                categoria: "omega",
                imagem: "img/Omega_3.png", 
                preco: 49.90,
                peso: "1400mg",
                quantidade: "120 Cápsulas",
                descricao: "Fonte concentrada de ácidos graxos (EPA e DHA). Promove a saúde cardiovascular, cerebral e articular."
            }
        ];

        // Função para formatar moeda (BRL)
        function formatarPreco(valor) {
            return valor.toLocaleString("pt-BR", { style: "currency", currency: "BRL" });
        }

        // ---- LÓGICA DA APLICAÇÃO ----
        function carregarProdutos(lista) {
            const container = document.getElementById("listaProdutos");
            container.innerHTML = "";

            if(lista.length === 0) {
                container.innerHTML = `<div class="col-12 text-center mt-4"><h4 class="text-muted">Nenhum produto natural encontrado.</h4></div>`;
                return;
            }

            lista.forEach(produto => {
                const col = document.createElement("div");
                col.className = "col-md-6 col-lg-4 mb-4";

                col.innerHTML = `
                    <div class="card-produto">
                        <div class="position-relative">
                            <img src="${produto.imagem}" alt="${produto.nome}" loading="lazy">
                        </div>
                        <div class="card-body">
                            <h5 class="card-title">${produto.nome}</h5>
                            <p class="card-text">
                                <small class="text-muted">${produto.quantidade} | ${produto.peso}</small><br>
                                ${produto.descricao.substring(0, 85)}...
                            </p>
                            <div class="preco">${formatarPreco(produto.preco)}</div>
                            <div class="d-grid gap-2 mt-auto">
                                <a href="https://wa.me/5500000000000?text=Olá! Tenho interesse no produto: ${encodeURIComponent(produto.nome)}" 
                                   target="_blank" 
                                   class="btn-natural">
                                    <i class="fab fa-whatsapp"></i> Comprar Agora
                                </a>
                            </div>
                        </div>
                    </div>
                `;
                container.appendChild(col);
            });
        }

        function filtrarProdutos() {
            const termo = document.getElementById("pesquisa").value.toLowerCase();
            const categoriaSelecionada = document.querySelector(".categoria.active") ? 
                                         document.querySelector(".categoria.active").getAttribute("data-cat") : "todos";

            let listaFiltrada = produtos;

            if (termo) {
                listaFiltrada = listaFiltrada.filter(p => 
                    p.nome.toLowerCase().includes(termo) || 
                    p.descricao.toLowerCase().includes(termo)
                );
            }

            if (categoriaSelecionada !== "todos") {
                listaFiltrada = listaFiltrada.filter(p => p.categoria === categoriaSelecionada);
            }

            carregarProdutos(listaFiltrada);
        }

        // ---- INICIALIZAÇÃO E EVENTOS ----
        document.addEventListener("DOMContentLoaded", function() {
            carregarProdutos(produtos);

            document.getElementById("pesquisa").addEventListener("input", filtrarProdutos);

            document.querySelectorAll(".categoria").forEach(btn => {
                btn.addEventListener("click", function() {
                    document.querySelectorAll(".categoria").forEach(b => {
                        b.classList.remove("active", "btn-success");
                        b.classList.add("btn-outline-success");
                    });
                    
                    this.classList.remove("btn-outline-success");
                    this.classList.add("active", "btn-success");
                    
                    filtrarProdutos();
                });
            });

            const botaoTopo = document.getElementById("topo");
            window.addEventListener("scroll", () => {
                if (window.scrollY > 300) {
                    botaoTopo.style.display = "block";
                } else {
                    botaoTopo.style.display = "none";
                }
            });
            botaoTopo.addEventListener("click", () => {
                window.scrollTo({ top: 0, behavior: "smooth" });
            });
        });
    </script>
</body>
</html>
