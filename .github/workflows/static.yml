<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Meu Site — Título da Página</title>
  <meta name="description" content="Descrição breve do site." />

  <!-- Metadados sociais básicos -->
  <meta property="og:title" content="Meu Site" />
  <meta property="og:description" content="Descrição breve do site." />
  <meta property="og:type" content="website" />
  <meta property="og:image" content="/assets/og-image.png" />
  <link rel="icon" href="/favicon.ico" />

  <style>
    /* ===== Reset e Variáveis ===== */
    *, *::before, *::after { box-sizing: border-box; }
    html, body { height: 100%; }
    body { margin: 0; font-family: system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, sans-serif; line-height: 1.5; }

    :root {
      --bg: #0f172a;      /* slate-900 */
      --card: #111827;    /* gray-900 */
      --text: #e5e7eb;    /* gray-200 */
      --muted: #94a3b8;   /* slate-400 */
      --brand: #6366f1;   /* indigo-500 */
      --brand-contrast: #e0e7ff; /* indigo-100 */
      --border: #1f2937;  /* gray-800 */
      --radius: 16px;
      --shadow: 0 10px 20px rgba(0,0,0,.25);
      --maxw: 1100px;
    }

    @media (prefers-color-scheme: light) {
      :root {
        --bg: #ffffff;
        --card: #f8fafc;   /* slate-50 */
        --text: #0f172a;   /* slate-900 */
        --muted: #475569;  /* slate-600 */
        --brand: #4f46e5;  /* indigo-600 */
        --brand-contrast: #eef2ff;
        --border: #e5e7eb; /* gray-200 */
      }
    }

    /* ===== Layout ===== */
    body { background: var(--bg); color: var(--text); display: flex; flex-direction: column; }
    .container { width: 100%; max-width: var(--maxw); margin: 0 auto; padding: 0 1rem; }

    /* ===== Acessibilidade ===== */
    .skip-link { position: absolute; left: -999px; top: -999px; background: var(--brand); color: var(--brand-contrast); padding: .5rem .75rem; border-radius: .5rem; }
    .skip-link:focus { left: 1rem; top: 1rem; z-index: 1000; }

    /* ===== Header/Navegação ===== */
    header { position: sticky; top: 0; backdrop-filter: saturate(1.2) blur(6px); background: color-mix(in oklab, var(--bg) 85%, transparent); border-bottom: 1px solid var(--border); }
    .nav { display: flex; align-items: center; justify-content: space-between; gap: 1rem; padding: .75rem 0; }
    .brand { display: inline-flex; align-items: center; gap: .5rem; font-weight: 700; }
    .brand__logo { width: 32px; height: 32px; border-radius: 50%; background: var(--brand); box-shadow: var(--shadow); }

    .menu { display: flex; align-items: center; gap: .75rem; }
    .menu a { text-decoration: none; color: var(--text); padding: .5rem .75rem; border-radius: .75rem; }
    .menu a:hover { background: var(--brand-contrast); color: #111827; }

    .btn { appearance: none; border: 1px solid var(--border); background: var(--card); color: var(--text); padding: .5rem .9rem; border-radius: .75rem; cursor: pointer; }
    .btn--primary { background: var(--brand); color: var(--brand-contrast); border-color: transparent; }

    .hamburger { display: none; background: transparent; border: 1px solid var(--border); border-radius: .75rem; padding: .35rem .5rem; }

    @media (max-width: 768px) {
      .menu { display: none; position: absolute; right: 1rem; top: 60px; flex-direction: column; background: var(--card); padding: .5rem; border: 1px solid var(--border); border-radius: .75rem; box-shadow: var(--shadow); }
      .menu.open { display: flex; }
      .hamburger { display: inline-flex; }
    }

    /* ===== Hero ===== */
    .hero { padding: 4rem 0 2rem; }
    .hero__grid { display: grid; grid-template-columns: 1.2fr 1fr; gap: 2rem; align-items: center; }
    .hero h1 { font-size: clamp(1.8rem, 2.5vw + 1rem, 3rem); margin: 0 0 .5rem; }
    .hero p { color: var(--muted); margin: 0 0 1.25rem; }
    .hero__card { background: var(--card); border: 1px solid var(--border); border-radius: var(--radius); padding: 1rem; box-shadow: var(--shadow); min-height: 200px; display: grid; place-items: center; }

    @media (max-width: 900px) {
      .hero__grid { grid-template-columns: 1fr; }
    }

    /* ===== Seções ===== */
    section { padding: 3rem 0; border-top: 1px solid var(--border); }
    .section__title { font-size: 1.5rem; margin: 0 0 .5rem; }
    .section__desc { color: var(--muted); margin: 0 0 1.5rem; }
    .grid { display: grid; gap: 1rem; }
    .grid--3 { grid-template-columns: repeat(3, 1fr); }
    @media (max-width: 900px) { .grid--3 { grid-template-columns: 1fr; } }

    .card { background: var(--card); border: 1px solid var(--border); border-radius: var(--radius); padding: 1rem; box-shadow: var(--shadow); }
    .card h3 { margin-top: 0; }

    /* ===== Rodapé ===== */
    footer { border-top: 1px solid var(--border); margin-top: auto; }
    .footer__inner { padding: 2rem 0; display: flex; flex-wrap: wrap; gap: 1rem; align-items: center; justify-content: space-between; }
    .fineprint { color: var(--muted); font-size: .9rem; }

    /* ===== Utilidades ===== */
    .sr-only { position: absolute; width: 1px; height: 1px; padding: 0; margin: -1px; overflow: hidden; clip: rect(0, 0, 0, 0); white-space: nowrap; border: 0; }
  </style>
</head>
<body>
  <a href="#conteudo" class="skip-link">Pular para o conteúdo</a>

  <!-- ===== Cabeçalho / Navegação ===== -->
  <header>
    <div class="container nav" role="navigation" aria-label="principal">
      <a class="brand" href="#" aria-label="Página inicial">
        <span class="brand__logo" aria-hidden="true"></span>
        <span>MinhaMarca</span>
      </a>

      <button class="hamburger" aria-label="Abrir menu" aria-expanded="false" aria-controls="menu">
        <span>☰</span>
      </button>

      <nav id="menu" class="menu" aria-label="Menu principal">
        <a href="#servicos">Serviços</a>
        <a href="#sobre">Sobre</a>
        <a href="#contato">Contato</a>
        <a class="btn btn--primary" href="#cta">Começar</a>
      </nav>
    </div>
  </header>

  <!-- ===== Hero ===== -->
  <main id="conteudo">
    <section class="hero">
      <div class="container hero__grid">
        <div>
          <h1>Base moderna para seu site HTML</h1>
          <p>Estrutura inicial pronta para personalizar: semântica, responsiva, acessível e com estilos elegantes.</p>
          <div style="display:flex; gap:.5rem; flex-wrap: wrap;">
            <a class="btn btn--primary" href="#servicos" id="cta">Ver recursos</a>
            <a class="btn" href="#sobre">Saiba mais</a>
          </div>
        </div>
        <div class="hero__card" aria-hidden="true">Prévia/Imagem/Ilustração</div>
      </div>
    </section>

    <!-- ===== Seção de recursos/serviços ===== -->
    <section id="servicos">
      <div class="container">
        <h2 class="section__title">Recursos</h2>
        <p class="section__desc">Alguns blocos prontos para você editar e adaptar.</p>
        <div class="grid grid--3">
          <article class="card">
            <h3>Estrutura Semântica</h3>
            <p>Uso de <code>&lt;header&gt;</code>, <code>&lt;main&gt;</code>, <code>&lt;section&gt;</code>, <code>&lt;article&gt;</code> e <code>&lt;footer&gt;</code> para SEO e acessibilidade.</p>
          </article>
          <article class="card">
            <h3>Responsividade</h3>
            <p>Grid fluido, tipografia adaptável e menu mobile com hambúrguer.</p>
          </article>
          <article class="card">
            <h3>Design Limpo</h3>
            <p>Paleta baseada em variáveis CSS, sombras suaves e cantos arredondados.</p>
          </article>
        </div>
      </div>
    </section>

    <!-- ===== Seção Sobre ===== -->
    <section id="sobre">
      <div class="container">
        <h2 class="section__title">Sobre</h2>
        <p class="section__desc">Escreva aqui a missão do seu projeto, valores e diferenciais. Mantenha claro e objetivo.</p>
        <div class="card">
          <p>Este boilerplate foi pensado para acelerar seu início. Substitua textos, ajuste cores em <code>:root</code> e adicione suas imagens na pasta <code>/assets</code>.</p>
        </div>
      </div>
    </section>

    <!-- ===== Seção Contato ===== -->
    <section id="contato">
      <div class="container">
        <h2 class="section__title">Contato</h2>
        <p class="section__desc">Formulário de contato simples (não envia ainda; adicione backend ou serviço de formulário).</p>
        <form class="card" action="#" method="post" onsubmit="event.preventDefault(); alert('Exemplo: conecte um backend para enviar.');">
          <label>
            <span class="sr-only">Nome</span>
            <input type="text" name="nome" placeholder="Seu nome" required style="width:100%; padding:.75rem; border-radius:.5rem; border:1px solid var(--border); background:transparent; color:var(--text); margin-bottom:.75rem;" />
          </label>
          <label>
            <span class="sr-only">Email</span>
            <input type="email" name="email" placeholder="Seu email" required style="width:100%; padding:.75rem; border-radius:.5rem; border:1px solid var(--border); background:transparent; color:var(--text); margin-bottom:.75rem;" />
          </label>
          <label>
            <span class="sr-only">Mensagem</span>
            <textarea name="mensagem" rows="4" placeholder="Sua mensagem" required style="width:100%; padding:.75rem; border-radius:.5rem; border:1px solid var(--border); background:transparent; color:var(--text); margin-bottom:.75rem;"></textarea>
          </label>
          <button class="btn btn--primary" type="submit">Enviar</button>
        </form>
      </div>
    </section>
  </main>

  <!-- ===== Rodapé ===== -->
  <footer>
    <div class="container footer__inner">
      <small class="fineprint">© <span id="year"></span> MinhaMarca. Todos os direitos reservados.</small>
      <nav aria-label="links de rodapé" class="fineprint" style="display:flex; gap: .75rem; flex-wrap: wrap;">
        <a href="#">Termos</a>
        <a href="#">Privacidade</a>
        <a href="#">Acessibilidade</a>
      </nav>
    </div>
  </footer>

  <script>
    // Ano automático no rodapé
    document.getElementById('year').textContent = new Date().getFullYear();

    // Menu mobile acessível
    const btn = document.querySelector('.hamburger');
    const menu = document.getElementById('menu');
    btn?.addEventListener('click', () => {
      const open = menu.classList.toggle('open');
      btn.setAttribute('aria-expanded', String(open));
    });
  </script>
</body>
</html>
