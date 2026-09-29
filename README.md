# Atividade-Pr-tica-M-dulo-1-Introdu-o-ao-HTML
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Evoluções Tecnológicas do Dia a Dia</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Segoe UI', system-ui, -apple-system, sans-serif;
            background: #0f172a;
            color: #e2e8f0;
            line-height: 1.7;
        }

        /* ===== MENU DE NAVEGAÇÃO ===== */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            background: rgba(15, 23, 42, 0.95);
            backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(148, 163, 184, 0.15);
            z-index: 1000;
            padding: 0 20px;
        }

        nav {
            max-width: 1100px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }

        .logo {
            font-size: 1.3rem;
            font-weight: 700;
            background: linear-gradient(90deg, #38bdf8, #818cf8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .menu {
            display: flex;
            gap: 8px;
            list-style: none;
        }

        .menu a {
            color: #cbd5e1;
            text-decoration: none;
            padding: 8px 16px;
            border-radius: 8px;
            font-size: 0.95rem;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .menu a:hover {
            background: rgba(56, 189, 248, 0.15);
            color: #38bdf8;
        }

        /* Botão menu mobile */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: #e2e8f0;
            font-size: 1.8rem;
            cursor: pointer;
        }

        /* ===== CONTEÚDO ===== */
        main {
            max-width: 900px;
            margin: 0 auto;
            padding: 100px 20px 60px;
        }

        section {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 40px;
            border: 1px solid rgba(148, 163, 184, 0.1);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        h1 {
            font-size: 2.6rem;
            background: linear-gradient(90deg, #38bdf8, #818cf8);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 20px;
            text-align: center;
        }

        h2 {
            font-size: 1.6rem;
            color: #38bdf8;
            margin-bottom: 20px;
            border-left: 4px solid #818cf8;
            padding-left: 15px;
        }

        p {
            margin-bottom: 16px;
            color: #cbd5e1;
            font-size: 1.05rem;
        }

        ul {
            list-style: none;
            margin: 20px 0;
        }

        ul li {
            background: rgba(56, 189, 248, 0.08);
            margin-bottom: 12px;
            padding: 14px 18px;
            border-radius: 10px;
            border-left: 4px solid #38bdf8;
            transition: all 0.3s ease;
        }

        ul li:hover {
            background: rgba(56, 189, 248, 0.15);
            transform: translateX(8px);
        }

        .img-container {
            text-align: center;
            margin: 30px 0;
        }

        img {
            max-width: 100%;
            border-radius: 16px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
            transition: transform 0.4s ease;
        }

        img:hover {
            transform: scale(1.02);
        }

        a {
            color: #38bdf8;
            text-decoration: none;
            font-weight: 600;
            border-bottom: 2px solid transparent;
            transition: border-color 0.3s;
        }

        a:hover {
            border-bottom-color: #38bdf8;
        }

        .btn {
            display: inline-block;
            margin-top: 20px;
            background: linear-gradient(90deg, #3b82f6, #8b5cf6);
            color: white;
            padding: 14px 28px;
            border-radius: 50px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(59, 130, 246, 0.3);
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(59, 130, 246, 0.4);
        }

        /* Cards de benefícios */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
            margin-top: 25px;
        }

        .card {
            background: rgba(56, 189, 248, 0.08);
            border-radius: 14px;
            padding: 25px;
            border: 1px solid rgba(56, 189, 248, 0.15);
            transition: all 0.3s ease;
        }

        .card:hover {
            transform: translateY(-6px);
            background: rgba(56, 189, 248, 0.12);
        }

        .card h3 {
            color: #38bdf8;
            margin-bottom: 10px;
            font-size: 1.15rem;
        }

        .card p {
            font-size: 0.95rem;
            margin: 0;
        }

        footer {
            text-align: center;
            padding: 30px 20px;
            color: #94a3b8;
            font-size: 0.9rem;
            border-top: 1px solid rgba(148, 163, 184, 0.1);
        }

        /* ===== RESPONSIVO ===== */
        @media (max-width: 768px) {
            .menu {
                display: none;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: #0f172a;
                flex-direction: column;
                padding: 20px;
                border-bottom: 1px solid rgba(148, 163, 184, 0.15);
            }

            .menu.active {
                display: flex;
            }

            .menu-toggle {
                display: block;
            }

            h1 {
                font-size: 2rem;
            }

            section {
                padding: 30px 20px;
            }
        }
    </style>
</head>
<body>

    <!-- MENU DE NAVEGAÇÃO -->
    <header>
        <nav>
            <div class="logo">TechEvolução</div>
            <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            <ul class="menu" id="menu">
                <li><a href="#inicio">Início</a></li>
                <li><a href="#exemplos">Exemplos</a></li>
                <li><a href="#beneficios">Benefícios</a></li>
                <li><a href="#desafios">Desafios</a></li>
                <li><a href="#futuro">Futuro</a></li>
                <li><a href="#cotidiano">Cotidiano</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- SEÇÃO INÍCIO -->
        <section id="inicio">
            <h1>Evoluções Tecnológicas do Dia a Dia</h1>
            <p>
                A tecnologia está presente em diversas atividades do nosso cotidiano.
                Ao longo dos anos, dispositivos e sistemas tecnológicos evoluíram para
                facilitar a comunicação, o trabalho, os estudos e o entretenimento.
            </p>
            <p>
                Atualmente, smartphones, computadores, aplicativos e dispositivos
                inteligentes fazem parte da rotina de muitas pessoas. Essas tecnologias
                permitem realizar tarefas com mais rapidez e praticidade, além de
                possibilitar o acesso a informações de qualquer lugar.
            </p>
        </section>

        <!-- SEÇÃO EXEMPLOS -->
        <section id="exemplos">
            <h2>Exemplos de evoluções tecnológicas</h2>
            <ul>
                <li>Smartphones cada vez mais avançados</li>
                <li>Inteligência Artificial</li>
                <li>Computação em nuvem</li>
                <li>Casas e dispositivos inteligentes</li>
                <li>Internet das Coisas (IoT)</li>
            </ul>
        </section>

        <!-- SEÇÃO BENEFÍCIOS -->
        <section id="beneficios">
            <h2>Principais benefícios no dia a dia</h2>
            <div class="cards">
                <div class="card">
                    <h3>Comunicação</h3>
                    <p>Conectamos pessoas instantaneamente por mensagens, vídeo e redes sociais.</p>
                </div>
                <div class="card">
                    <h3>Produtividade</h3>
                    <p>Ferramentas digitais aceleram o trabalho e organizam tarefas.</p>
                </div>
                <div class="card">
                    <h3>Acesso à informação</h3>
                    <p>Conhecimento disponível a qualquer hora e em qualquer lugar.</p>
                </div>
                <div class="card">
                    <h3>Conveniência</h3>
                    <p>Compras, pagamentos e serviços feitos pelo celular.</p>
                </div>
            </div>
        </section>

        <!-- SEÇÃO DESAFIOS -->
        <section id="desafios">
            <h2>Desafios e cuidados</h2>
            <p>
                Apesar dos avanços, a tecnologia também traz desafios importantes:
            </p>
            <ul>
                <li>Dependência excessiva de dispositivos</li>
                <li>Privacidade e segurança de dados</li>
                <li>Desinformação e fake news</li>
                <li>Impacto na saúde mental (uso excessivo de telas)</li>
                <li>Exclusão digital de quem não tem acesso</li>
            </ul>
        </section>

        <!-- SEÇÃO FUTURO -->
        <section id="futuro">
            <h2>O que vem pela frente</h2>
            <p>
                As próximas décadas prometem transformações ainda maiores:
            </p>
            <ul>
                <li>Inteligência Artificial generativa em quase tudo</li>
                <li>Realidade aumentada e virtual no cotidiano</li>
                <li>Carros autônomos e mobilidade inteligente</li>
                <li>Computação quântica</li>
                <li>Interfaces cérebro-máquina</li>
            </ul>
            <div style="text-align: center;">
                <button class="btn" onclick="mostrarCuriosidade()">
                    Ver uma curiosidade tecnológica
                </button>
            </div>
            <p id="mensagem" style="text-align: center; margin-top: 20px; color: #a5b4fc; font-weight: 500;"></p>
        </section>

        <!-- SEÇÃO COTIDIANO -->
        <section id="cotidiano">
            <h2>Tecnologia no cotidiano</h2>
            <div class="img-container">
                <img 
                    src="https://images.unsplash.com/photo-1518770660439-4636190af475"
                    alt="Equipamentos e componentes utilizados na tecnologia"
                    width="500"
                >
            </div>
            <p>
                Para conhecer mais sobre tecnologia e suas aplicações, acesse o site
                da <a href="https://www.techtudo.com.br/" target="_blank">TechTudo</a>.
            </p>
        </section>
    </main>

    <footer>
        Página criada com HTML, CSS e JavaScript • Evoluções Tecnológicas do Dia a Dia
    </footer>

    <script>
        // Menu mobile
        function toggleMenu() {
            document.getElementById('menu').classList.toggle('active');
        }

        // Fecha o menu ao clicar em um link (mobile)
        document.querySelectorAll('.menu a').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('menu').classList.remove('active');
            });
        });

        // Curiosidades aleatórias
        function mostrarCuriosidade() {
            const curiosidades = [
                "A Inteligência Artificial já está presente em assistentes virtuais, recomendações e até na medicina!",
                "A Internet das Coisas conecta geladeiras, relógios e carros à internet.",
                "A computação em nuvem permite guardar arquivos e trabalhar de qualquer lugar.",
                "Smartphones de hoje têm mais poder de processamento que computadores de 20 anos atrás.",
                "Em 2025, estima-se que existirão mais de 75 bilhões de dispositivos conectados à IoT."
            ];
            const aleatoria = curiosidades[Math.floor(Math.random() * curiosidades.length)];
            document.getElementById('mensagem').textContent = aleatoria;
        }
    </script>

</body>
</html>
