<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vitrina de Coleccionables - Autos a Escala</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --primary: #e63946;
            --secondary: #1d3557;
            --accent: #ffb703;
            --dark: #212529;
            --light: #f8f9fa;
            --gray: #6c757d;
        }
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Poppins', sans-serif;
        }
        body {
            background-color: #f0f2f5;
            color: var(--dark);
            line-height: 1.6;
        }
        header {
            background: linear-gradient(135deg, var(--secondary), var(--dark));
            color: white;
            padding: 2.5rem 1rem;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }
        header h1 {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
            color: var(--accent);
        }
        header p {
            font-size: 1.1rem;
            font-weight: 300;
            opacity: 0.9;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem 1rem;
        }
        .filters {
            display: flex;
            justify-content: center;
            gap: 0.5rem;
            flex-wrap: wrap;
            margin-bottom: 2.5rem;
        }
        .filter-btn {
            background: white;
            border: 2px solid var(--secondary);
            color: var(--secondary);
            padding: 0.5rem 1.25rem;
            border-radius: 30px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s ease;
        }
        .filter-btn:hover, .filter-btn.active {
            background: var(--secondary);
            color: white;
            transform: translateY(-2px);
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
        }
        .card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 6px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 25px rgba(0,0,0,0.15);
        }
        .card-img-container {
            width: 100%;
            height: 220px;
            background: #e9ecef;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
            position: relative;
        }
        .card-img-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .badge {
            position: absolute;
            top: 10px;
            right: 10px;
            background: var(--primary);
            color: white;
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 700;
            text-transform: uppercase;
        }
        .card-content {
            padding: 1.5rem;
            display: flex;
            flex-direction: column;
            flex-grow: 1;
        }
        .card-title {
            font-size: 1.25rem;
            font-weight: 700;
            color: var(--secondary);
            margin-bottom: 0.5rem;
        }
        .card-specs {
            font-size: 0.85rem;
            color: var(--gray);
            margin-bottom: 1rem;
            flex-grow: 1;
        }
        .card-specs p {
            margin-bottom: 0.2rem;
        }
        .card-specs i {
            width: 18px;
            color: var(--secondary);
            margin-right: 5px;
        }
        .card-footer {
            display: flex;
            align-items: center;
            justify-content: space-between;
            margin-top: 1rem;
            padding-top: 1rem;
            border-top: 1px solid #eee;
        }
        .price {
            font-size: 1.3rem;
            font-weight: 700;
            color: var(--primary);
        }
        .whatsapp-btn {
            background-color: #25d366;
            color: white;
            border: none;
            padding: 0.6rem 1rem;
            border-radius: 8px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            display: inline-flex;
            align-items: center;
            gap: 6px;
            font-size: 0.9rem;
            transition: background 0.3s ease;
        }
        .whatsapp-btn:hover {
            background-color: #1ebe5d;
        }
        footer {
            text-align: center;
            padding: 2.5rem;
            color: var(--gray);
            font-size: 0.9rem;
            background: white;
            margin-top: 3rem;
            border-top: 1px solid #dee2e6;
        }
    </style>
</head>
<body>

    <header>
        <h1><i class="fas fa-car-side"></i> Coleccionables de Autos a Escala</h1>
        <p>Modelos selectos Hot Wheels, Matchbox y Maisto listos para coleccionistas</p>
    </header>

    <div class="container">
        <!-- Filtros -->
        <div class="filters">
            <button class="filter-btn active" onclick="filterSelection('all')">Todos</button>
            <button class="filter-btn" onclick="filterSelection('hotwheels')">Hot Wheels</button>
            <button class="filter-btn" onclick="filterSelection('matchbox')">Matchbox</button>
            <button class="filter-btn" onclick="filterSelection('maisto')">Maisto</button>
        </div>

        <!-- Cuadrícula de Autos -->
        <div class="grid">
            
            <!-- Item 1 -->
            <div class="card" data-category="hotwheels">
                <div class="card-img-container">
                    <span class="badge">Hot Wheels</span>
                    <img src="https://images.unsplash.com/photo-1581235720704-06d3acfcb36f?auto=format&fit=crop&w=600&q=80" alt="Bone Shaker">
                </div>
                <div class="card-content">
                    <h3 class="card-title">Bone Shaker</h3>
                    <div class="card-specs">
                        <p><i class="fas fa-calendar-alt"></i> <strong>Año:</strong> 2020 (Mainline)</p>
                        <p><i class="fas fa-globe"></i> <strong>Origen:</strong> Malasia</p>
                        <p><i class="fas fa-puzzle-piece"></i> <strong>Material:</strong> Metal / Base Plástica</p>
                        <p><i class="fas fa-star"></i> <strong>Rareza:</strong> Común / Alta demanda</p>
                    </div>
                    <div class="card-footer">
                        <span class="price">$3.500 CLP</span>
                        <a href="https://wa.me/?text=Hola,%20me%20interesa%20el%20modelo%20Bone%20Shaker%20de%20tu%20vitrina." target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Consultar
                        </a>
                    </div>
                </div>
            </div>

            <!-- Item 2 -->
            <div class="card" data-category="matchbox">
                <div class="card-img-container">
                    <span class="badge" style="background:#0077b6;">Matchbox</span>
                    <img src="https://images.unsplash.com/photo-1617814076367-b759c7d7e738?auto=format&fit=crop&w=600&q=80" alt="Ford Mustang GT">
                </div>
                <div class="card-content">
                    <h3 class="card-title">1968 Ford Mustang GT</h3>
                    <div class="card-specs">
                        <p><i class="fas fa-calendar-alt"></i> <strong>Año:</strong> 2018</p>
                        <p><i class="fas fa-globe"></i> <strong>Origen:</strong> Tailandia</p>
                        <p><i class="fas fa-puzzle-piece"></i> <strong>Material:</strong> Die-cast Premium</p>
                        <p><i class="fas fa-star"></i> <strong>Rareza:</strong> Semi-Raro</p>
                    </div>
                    <div class="card-footer">
                        <span class="price">$4.800 CLP</span>
                        <a href="https://wa.me/?text=Hola,%20me%20interesa%20el%20modelo%201968%20Ford%20Mustang%20GT%20de%20tu%20vitrina." target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Consultar
                        </a>
                    </div>
                </div>
            </div>

            <!-- Item 3 -->
            <div class="card" data-category="maisto">
                <div class="card-img-container">
                    <span class="badge" style="background:#52b788;">Maisto</span>
                    <img src="https://images.unsplash.com/photo-1542282088-72c9c27ed0cd?auto=format&fit=crop&w=600&q=80" alt="Porsche 911 GT3">
                </div>
                <div class="card-content">
                    <h3 class="card-title">Porsche 911 GT3 RS</h3>
                    <div class="card-specs">
                        <p><i class="fas fa-calendar-alt"></i> <strong>Año:</strong> 2021 (Special Edition)</p>
                        <p><i class="fas fa-globe"></i> <strong>Origen:</strong> China</p>
                        <p><i class="fas fa-puzzle-piece"></i> <strong>Material:</strong> Metal con aperturas</p>
                        <p><i class="fas fa-star"></i> <strong>Rareza:</strong> Colección Escala 1:24</p>
                    </div>
                    <div class="card-footer">
                        <span class="price">$12.000 CLP</span>
                        <a href="https://wa.me/?text=Hola,%20me%20interesa%20el%20modelo%20Porsche%20911%20GT3%20RS%20de%20tu%20vitrina." target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Consultar
                        </a>
                    </div>
                </div>
            </div>

            <!-- Item 4 -->
            <div class="card" data-category="hotwheels">
                <div class="card-img-container">
                    <span class="badge">Hot Wheels</span>
                    <img src="https://images.unsplash.com/photo-1552519507-da3b142c6e3d?auto=format&fit=crop&w=600&q=80" alt="Lamborghini Huracán">
                </div>
                <div class="card-content">
                    <h3 class="card-title">Lamborghini Huracán</h3>
                    <div class="card-specs">
                        <p><i class="fas fa-calendar-alt"></i> <strong>Año:</strong> 2022</p>
                        <p><i class="fas fa-globe"></i> <strong>Origen:</strong> Malasia</p>
                        <p><i class="fas fa-puzzle-piece"></i> <strong>Material:</strong> Metal / Base Plástica</p>
                        <p><i class="fas fa-star"></i> <strong>Rareza:</strong> Edición Especial</p>
                    </div>
                    <div class="card-footer">
                        <span class="price">$4.000 CLP</span>
                        <a href="https://wa.me/?text=Hola,%20me%20interesa%20el%20modelo%20Lamborghini%20Huracán%20de%20tu%20vitrina." target="_blank" class="whatsapp-btn">
                            <i class="fab fa-whatsapp"></i> Consultar
                        </a>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <footer>
        <p>&copy; 2026 Vitrina de Coleccionables | Todos los derechos reservados.</p>
    </footer>

    <script>
        function filterSelection(category) {
            let cards = document.getElementsByClassName('card');
            if (category == 'all') category = '';
            for (let i = 0; i < cards.length; i++) {
                cards[i].style.display = "none";
                if (cards[i].getAttribute('data-category').indexOf(category) > -1) {
                    cards[i].style.display = "flex";
                }
            }
            let btns = document.getElementsByClassName('filter-btn');
            for (let i = 0; i < btns.length; i++) {
                btns[i].classList.remove("active");
            }
            event.currentTarget.classList.add("active");
        }
    </script>
</body>
</html>
