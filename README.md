:root{
  --primary:#0a58ca; /* ganti sesuai warna sekolah */
  --dark:#153243;
  --muted:#666;
  --bg:#f6f8fb;
  --container:1100px;
  --radius:8px;
  font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
}

*{box-sizing:border-box}
html,body{height:100%;margin:0;background:var(--bg);color:#222}
.container{max-width:var(--container);margin:0 auto;padding:0 20px}

/* Header */
.site-header{background:#fff;box-shadow:0 2px 6px rgba(10,10,10,0.04);position:sticky;top:0;z-index:30}
.header-inner{display:flex;align-items:center;justify-content:space-between;height:68px}
.brand{font-weight:700;color:var(--primary);text-decoration:none;font-size:1.1rem}
.nav-toggle{display:none;background:none;border:0;font-size:1.4rem}
.main-nav ul{display:flex;gap:18px;list-style:none;margin:0;padding:0}
.main-nav a{text-decoration:none;color:var(--dark);padding:8px 6px;border-radius:6px}
.main-nav a:hover{background:rgba(10,88,202,0.08);color:var(--primary)}

/* Hero */
.hero{padding:48px 0;background:linear-gradient(180deg, rgba(10,88,202,0.06), transparent)}
.hero-inner{display:flex;align-items:center;gap:30px}
.hero-text{flex:1}
.hero-text h1{margin:0 0 12px;font-size:2rem;color:var(--dark)}
.hero-text p{color:var(--muted);margin:0 0 16px}
.btn{display:inline-block;background:var(--primary);color:#fff;padding:10px 16px;border-radius:8px;text-decoration:none}
.hero-image{width:420px;max-width:40%}
.hero-image img{width:100%;border-radius:10px;display:block}

/* Sections */
.section{padding:40px 0;background:transparent}
.section h2{margin-top:0;color:var(--dark)}
.cards{display:flex;gap:16px;margin-top:16px}
.card{background:#fff;padding:18px;border-radius:8px;flex:1;box-shadow:0 6px 20px rgba(10,10,10,0.04)}
.program-grid{display:flex;gap:16px;flex-wrap:wrap;margin-top:16px}
.program{background:#fff;border-radius:8px;padding:12px;width:calc(33.333% - 10.666px);box-shadow:0 6px 18px rgba(10,10,10,0.04)}
.program img{width:100%;height:140px;object-fit:cover;border-radius:6px}

/* News */
.news-list{display:grid;gap:14px}
.news-item{background:#fff;padding:14px;border-radius:8px;box-shadow:0 6px 18px rgba(10,10,10,0.03)}
.news-item h3{margin:0 0 6px;font-size:1.05rem}

/* Gallery */
.gallery-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:8px}
.gallery-grid img{width:100%;height:110px;object-fit:cover;border-radius:6px}

/* Footer */
.site-footer{padding:18px 0;background:#fff;margin-top:30px;box-shadow:0 -1px 6px rgba(10,10,10,0.03)}
.footer-inner{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap}
.small{opacity:0.7;font-size:0.9rem}

/* Responsive */
@media(max-width:900px){
  .hero-inner{flex-direction:column}
  .hero-image{max-width:100%;width:100%}
  .program{width:calc(50% - 8px)}
  .gallery-grid{grid-template-columns:repeat(2,1fr)}
}
@media(max-width:700px){
  .nav-toggle{display:block}
  .main-nav{position:absolute;right:20px;top:68px;background:#fff;padding:18px;border-radius:8px;box-shadow:0 12px 40px rgba(10,10,10,0.08);display:none}
  .main-nav.open{display:block}
  .main-nav ul{flex-direction:column;gap:8px}
  .program{width:100%}
}
