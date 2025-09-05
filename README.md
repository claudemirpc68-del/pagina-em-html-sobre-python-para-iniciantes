# pagina-em-html-sobre-python-para-iniciantes
PYTHON PARA INICIANTES ELABORADO POR CLAUDEMIR PEDROSO CUBAS COM AUXILIO DA IA DEEPSEEK
(https://github.com/user-attachments/files/22163839/deepseek_html_20250904_0365e2.html)
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Python para Iniciantes - por Claudemir</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .header {
            background: linear-gradient(135deg, #306998 0%, #4B8BBE 100%);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0,0,0,0.2);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #FFD43B;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }
        
        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s ease;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        .nav-links a:hover {
            color: #FFD43B;
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .hero {
            text-align: center;
            padding: 4rem 0;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="%23306998" fill-opacity="0.1" d="M0,128L48,117.3C96,107,192,85,288,112C384,139,480,213,576,218.7C672,224,768,160,864,138.7C960,117,1056,139,1152,149.3C1248,160,1344,160,1392,160L1440,160L1440,0L1392,0C1344,0,1248,0,1152,0C1056,0,960,0,864,0C768,0,672,0,576,0C480,0,384,0,288,0C192,0,96,0,48,0L0,0Z"></path></svg>') no-repeat bottom;
            background-size: cover;
        }
        
        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: #306998;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
        }
        
        .hero .author {
            font-size: 1.5rem;
            color: #4B8BBE;
            margin-bottom: 1.5rem;
            font-weight: 600;
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto;
            color: #444;
            margin-bottom: 2rem;
        }
        
        .cta-button {
            display: inline-block;
            background-color: #FFD43B;
            color: #306998;
            padding: 15px 35px;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            margin-top: 1rem;
            transition: transform 0.3s ease, background-color 0.3s ease;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
        }
        
        .cta-button:hover {
            transform: translateY(-3px);
            background-color: #FFE873;
        }
        
        .content {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: #306998;
            font-size: 2.5rem;
        }
        
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin-bottom: 4rem;
        }
        
        .card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
            display: flex;
            flex-direction: column;
        }
        
        .card:hover {
            transform: translateY(-5px);
        }
        
        .card-content {
            padding: 1.5rem;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
        }
        
        .card h3 {
            color: #306998;
            margin-bottom: 1rem;
            font-size: 1.5rem;
        }
        
        .card p {
            margin-bottom: 1.5rem;
            flex-grow: 1;
        }
        
        .card-icon {
            font-size: 3rem;
            text-align: center;
            padding: 1rem;
            background-color: #4B8BBE;
            color: white;
        }
        
        .doc-link {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background-color: #306998;
            color: white;
            padding: 10px 15px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: 500;
            transition: background-color 0.3s ease;
            margin-top: auto;
        }
        
        .doc-link:hover {
            background-color: #3b7cad;
        }
        
        .code-section {
            background-color: #2d2d2d;
            color: #f8f8f2;
            border-radius: 8px;
            padding: 1.5rem;
            margin: 2rem 0;
            overflow-x: auto;
            font-family: 'Consolas', 'Monaco', monospace;
        }
        
        .code-section pre {
            margin: 0;
        }
        
        .code-keyword {
            color: #f92672;
        }
        
        .code-function {
            color: #66d9ef;
        }
        
        .code-string {
            color: #a6e22e;
        }
        
        .code-number {
            color: #ae81ff;
        }
        
        .code-comment {
            color: #75715e;
        }
        
        .example-title {
            color: #306998;
            margin: 2rem 0 1rem;
            font-size: 1.5rem;
            border-bottom: 2px solid #FFD43B;
            padding-bottom: 0.5rem;
        }
        
        .footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 2rem 0;
            margin-top: 4rem;
        }
        
        .footer a {
            color: #FFD43B;
            text-decoration: none;
        }
        
        @media (max-width: 768px) {
            .nav {
                flex-direction: column;
                gap: 1rem;
            }
            
            .nav-links {
                gap: 1rem;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .hero .author {
                font-size: 1.2rem;
            }
            
            .hero p {
                font-size: 1.1rem;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="container">
            <nav class="nav">
                <a href="#" class="logo">
                    <span>🐍</span> Python para Iniciantes
                </a>
                <ul class="nav-links">
                    <li><a href="#inicio">Início</a></li>
                    <li><a href="#conteudo">Conteúdo</a></li>
                    <li><a href="#exemplos">Exemplos</a></li>
                    <li><a href="#sobre">Sobre</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <section class="hero" id="inicio">
        <div class="container">
            <h1>Aprenda Python do Zero</h1>
            <div class="author">por Claudemir</div>
            <p>Domine os fundamentos da programação Python de forma prática e divertida. Perfeito para iniciantes!</p>
            <a href="#exemplos" class="cta-button">Ver Exemplos de Código</a>
        </div>
    </section>

    <section class="content container" id="conteudo">
        <h2 class="section-title">O que você vai aprender</h2>
        
        <div class="cards">
            <div class="card">
                <div class="card-icon">📘</div>
                <div class="card-content">
                    <h3>Fundamentos</h3>
                    <p>Variáveis, tipos de dados, operadores e estruturas básicas da linguagem Python.</p>
                    <a href="https://docs.python.org/3/" target="_blank" class="doc-link">
                        <i class="fas fa-external-link-alt"></i> Documentação Oficial
                    </a>
                </div>
            </div>
            
            <div class="card">
                <div class="card-icon">🔧</div>
                <div class="card-content">
                    <h3>Estruturas de Controle</h3>
                    <p>Condicionais (if, else), loops (for, while) e controle de fluxo de programas.</p>
                    <a href="#exemplos" class="doc-link">
                        <i class="fas fa-code"></i> Ver Exemplos
                    </a>
                </div>
            </div>
            
            <div class="card">
                <div class="card-icon">📊</div>
                <div class="card-content">
                    <h3>Estruturas de Dados</h3>
                    <p>Listas, tuplas, dicionários, sets e como utilizá-las eficientemente.</p>
                    <a href="#exemplos" class="doc-link">
                        <i class="fas fa-code"></i> Ver Exemplos
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section class="content container" id="exemplos">
        <h2 class="section-title">Exemplos de Código Python</h2>
        
        <h3 class="example-title">Variáveis e Tipos de Dados</h3>
        <div class="code-section">
            <pre><code><span class="code-comment"># Variáveis básicas</span>
<span class="code-keyword">nome</span> = <span class="code-string">"João"</span>          <span class="code-comment"># String (texto)</span>
<span class="code-keyword">idade</span> = <span class="code-number">25</span>            <span class="code-comment"># Inteiro</span>
<span class="code-keyword">altura</span> = <span class="code-number">1.75</span>         <span class="code-comment"># Float (decimal)</span>
<span class="code-keyword">estudante</span> = <span class="code-keyword">True</span>      <span class="code-comment"># Boolean (True ou False)</span>

<span class="code-comment"># Saída de dados</span>
<span class="code-function">print</span>(<span class="code-string">"Nome:"</span>, nome)
<span class="code-function">print</span>(<span class="code-string">"Idade:"</span>, idade)
<span class="code-function">print</span>(<span class="code-string">"Altura:"</span>, altura)
<span class="code-function">print</span>(<span class="code-string">"É estudante?"</span>, estudante)</code></pre>
        </div>

        <h3 class="example-title">Operadores</h3>
        <div class="code-section">
            <pre><code><span class="code-comment"># Operadores Aritméticos</span>
<span class="code-keyword">a</span> = <span class="code-number">10</span>
<span class="code-keyword">b</span> = <span class="code-number">3</span>

<span class="code-function">print</span>(<span class="code-string">"Soma:"</span>, a + b)        <span class="code-comment"># 13</span>
<span class="code-function">print</span>(<span class="code-string">"Subtração:"</span>, a - b)   <span class="code-comment"># 7</span>
<span class="code-function">print</span>(<span class="code-string">"Multiplicação:"</span>, a * b) <span class="code-comment"># 30</span>
<span class="code-function">print</span>(<span class="code-string">"Divisão:"</span>, a / b)     <span class="code-comment"># 3.333...</span>
<span class="code-function">print</span>(<span class="code-string">"Resto da divisão:"</span>, a % b) <span class="code-comment"># 1</span>
<span class="code-function">print</span>(<span class="code-string">"Exponenciação:"</span>, a ** b) <span class="code-comment"># 1000</span>

<span class="code-comment"># Operadores de Comparação</span>
<span class="code-function">print</span>(<span class="code-string">"a é igual a b?"</span>, a == b)  <span class="code-comment"># False</span>
<span class="code-function">print</span>(<span class="code-string">"a é diferente de b?"</span>, a != b) <span class="code-comment"># True</span>
<span class="code-function">print</span>(<span class="code-string">"a é maior que b?"</span>, a > b)   <span class="code-comment"># True</span></code></pre>
        </div>

        <h3 class="example-title">Estruturas Básicas</h3>
        <div class="code-section">
            <pre><code><span class="code-comment"># Estrutura Condicional (if, elif, else)</span>
<span class="code-keyword">nota</span> = <span class="code-number">85</span>

<span class="code-keyword">if</span> nota >= <span class="code-number">90</span>:
    <span class="code-function">print</span>(<span class="code-string">"Conceito A"</span>)
<span class="code-keyword">elif</span> nota >= <span class="code-number">80</span>:
    <span class="code-function">print</span>(<span class="code-string">"Conceito B"</span>)  <span class="code-comment"># Isso será executado</span>
<span class="code-keyword">elif</span> nota >= <span class="code-number">70</span>:
    <span class="code-function">print</span>(<span class="code-string">"Conceito C"</span>)
<span class="code-keyword">else</span>:
    <span class="code-function">print</span>(<span class="code-string">"Conceito D"</span>)

<span class="code-comment"># Loop For</span>
<span class="code-keyword">for</span> i <span class="code-keyword">in</span> <span class="code-function">range</span>(<span class="code-number">5</span>):
    <span class="code-function">print</span>(<span class="code-string">"Número:"</span>, i)  <span class="code-comment"># Imprime 0, 1, 2, 3, 4</span>

<span class="code-comment"># Loop While</span>
<span class="code-keyword">contador</span> = <span class="code-number">0</span>
<span class="code-keyword">while</span> contador < <span class="code-number">3</span>:
    <span class="code-function">print</span>(<span class="code-string">"Contador:"</span>, contador)
    contador += <span class="code-number">1</span>  <span class="code-comment"># Incrementa o contador</span></code></pre>
        </div>

        <h3 class="example-title">Estruturas de Dados</h3>
        <div class="code-section">
            <pre><code><span class="code-comment"># Listas (mutáveis)</span>
<span class="code-keyword">frutas</span> = [<span class="code-string">"maçã"</span>, <span class="code-string">"banana"</span>, <span class="code-string">"laranja"</span>]
<span class="code-function">print</span>(<span class="code-string">"Primeira fruta:"</span>, frutas[<span class="code-number">0</span>])  <span class="code-comment"># maçã</span>
frutas.append(<span class="code-string">"uva"</span>)  <span class="code-comment"># Adiciona item</span>
<span class="code-function">print</span>(<span class="code-string">"Todas as frutas:"</span>, frutas)

<span class="code-comment"># Tuplas (imutáveis)</span>
<span class="code-keyword">coordenadas</span> = (<span class="code-number">10.5</span>, <span class="code-number">20.3</span>)
<span class="code-function">print</span>(<span class="code-string">"Coordenada X:"</span>, coordenadas[<span class="code-number">0</span>])

<span class="code-comment"># Dicionários (pares chave-valor)</span>
<span class="code-keyword">pessoa</span> = {
    <span class="code-string">"nome"</span>: <span class="code-string">"Maria"</span>,
    <span class="code-string">"idade"</span>: <span class="code-number">30</span>,
    <span class="code-string">"cidade"</span>: <span class="code-string">"São Paulo"</span>
}
<span class="code-function">print</span>(<span class="code-string">"Nome da pessoa:"</span>, pessoa[<span class="code-string">"nome"</span>])</code></pre>
        </div>
    </section>

    <section class="content container" id="sobre">
        <h2 class="section-title">Sobre</h2>
        <div style="background-color: white; padding: 2rem; border-radius: 10px; box-shadow: 0 5px 15px rgba(0,0,0,0.1);">
            <p style="font-size: 1.2rem; margin-bottom: 1.5rem;">Este material foi desenvolvido por <strong>Claudemir</strong> para auxiliar iniciantes na jornada de aprendizado da linguagem Python.</p>
            <p style="margin-bottom: 1rem;">Python é uma linguagem de programação poderosa e fácil de aprender, com estruturas de dados de alto nível e uma abordagem simples mas eficaz à programação orientada a objetos.</p>
            <p>Com este guia, você aprenderá os conceitos fundamentais da linguagem e estará preparado para explorar tópicos mais avançados.</p>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <p>🐍 Python para Iniciantes - por Claudemir - Todos os direitos reservados &copy; 2023</p>
            <p>Email para contato: <a href="mailto:claudemirpc68@gmail.com">claudemirpc68@gmail.com</a></p>
        </div>
    </footer>
</body>
</html>
