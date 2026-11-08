

# tikeffectthtml = r'''<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TIKEFFECT | Painel Live</title>
<style>
:root{--bg:#0b0d14;--panel:#141824;--panel2:#1b2130;--line:#293143;--muted:#929bad;--text:#f5f7fb;--pink:#ff315d;--cyan:#31d7e8;--green:#35d49a}
*{box-sizing:border-box}body{margin:0;background:radial-gradient(circle at 80% 0%,#202039 0,transparent 34%),var(--bg);color:var(--text);font:15px Inter,system-ui,Arial}
.app{display:flex;min-height:100vh}.sidebar{width:245px;background:#10131d;border-right:1px solid var(--line);padding:25px 17px;display:flex;flex-direction:column}.brand{display:flex;align-items:center;gap:11px;font-size:22px;font-weight:900;letter-spacing:1px;margin:0 8px 38px}.logo{width:39px;height:39px;border-radius:12px;background:linear-gradient(135deg,var(--pink),#8d3cff);display:grid;place-items:center;font-size:22px}.navlabel{font-size:10px;color:#6f788a;letter-spacing:1.5px;margin:18px 10px 9px}.nav a{display:flex;gap:12px;padding:12px 13px;border-radius:10px;color:#aab2c2;text-decoration:none;margin:3px 0}.nav a.active,.nav a:hover{background:#252033;color:white}.nav a.active{box-shadow:inset 3px 0 var(--pink)}.sidebottom{margin-top:auto;color:#778195;font-size:12px;padding:12px}
main{padding:32px 38px;max-width:1500px;width:100%;margin:auto}.top{display:flex;align-items:center;justify-content:space-between;gap:20px;margin-bottom:32px}.eyebrow{color:var(--cyan);font-size:11px;letter-spacing:2px;font-weight:800}.top h1{font-size:29px;margin:7px 0 5px}.sub{color:var(--muted);margin:0}.profile{display:flex;align-items:center;gap:10px;background:var(--panel);border:1px solid var(--line);padding:9px 13px;border-radius:12px}.avatar{width:32px;height:32px;border-radius:50%;background:#583c79;display:grid;place-items:center;font-weight:800}
button{border:0;border-radius:10px;padding:11px 15px;font-weight:750;cursor:pointer;color:white;background:linear-gradient(100deg,var(--pink),#b72cff)}button.secondary{background:#252d3d;border:1px solid #354056}button:active{transform:scale(.98)}
.cards{display:grid;grid-template-columns:repeat(4,1fr);gap:15px;margin-bottom:20px}.card,.panel{background:linear-gradient(145deg,var(--panel),#121722);border:1px solid var(--line);border-radius:16px;padding:19px}.metric{display:flex;justify-content:space-between;align-items:center;color:var(--muted);font-size:13px}.ico{width:38px;height:38px;border-radius:11px;display:grid;place-items:center;font-size:18px;background:#28213a}.value{font-size:28px;font-weight:850;margin-top:13px}.hint{font-size:11px;color:#778195;margin-top:4px}
.content{display:grid;grid-template-columns:1.35fr .85fr;gap:18px}.panel h2{font-size:16px;margin:0 0 5px}.panelhead{display:flex;justify-content:space-between;align-items:center;margin-bottom:17px}.muted{color:var(--muted);font-size:12px}.connect{background:linear-gradient(110deg,#21172d,#172538);border:1px solid #46304f;border-radius:13px;padding:18px;display:flex;align-items:center;justify-content:space-between;gap:14px;margin-bottom:20px}.connect strong{display:block;margin-bottom:5px}.status{font-size:11px;color:#ffb5c2;background:#492331;padding:6px 9px;border-radius:30px;white-space:nowrap}
.effect{display:flex;align-items:center;gap:12px;padding:13px 0;border-bottom:1px solid #252c3a}.effect:last-child{border:0}.effecticon{width:39px;height:39px;border-radius:11px;background:#242c3d;display:grid;place-items:center;font-size:18px}.effectname{font-weight:700}.effectdesc{font-size:11px;color:var(--muted);margin-top:4px}.toggle{margin-left:auto;width:36px;height:20px;border-radius:20px;background:#2b3545;position:relative}.toggle:after{content:"";position:absolute;width:14px;height:14px;top:3px;left:3px;border-radius:50%;background:#8d98aa}.toggle.on{background:#176d58}.toggle.on:after{left:19px;background:#65f0bd}
.preview{height:235px;border:1px dashed #3a4559;border-radius:13px;background:linear-gradient(135deg,#151b29,#10141e);display:grid;place-items:center;text-align:center;padding:20px}.preview .screen{font-size:36px}.preview p{color:var(--muted);font-size:12px;max-width:260px;line-height:1.6}
.bottom{display:flex;gap:10px;flex-wrap:wrap;margin-top:18px}.pill{font-size:11px;padding:7px 10px;border-radius:30px;background:#202a37;color:#b8c3d3}
@media(max-width:900px){.sidebar{width:70px;padding:20px 9px}.brand span,.nav a span,.navlabel,.sidebottom{display:none}.brand{margin:0 5px 35px}.nav a{justify-content:center;font-size:18px}.cards{grid-template-columns:repeat(2,1fr)}.content{grid-template-columns:1fr}main{padding:24px 18px}}
@media(max-width:520px){.top{align-items:flex-start;flex-direction:column}.cards{gap:9px}.card{padding:14px}.value{font-size:23px}.connect{align-items:flex-start;flex-direction:column}}
</style>
</head>
<body>
<div class="app">
<aside class="sidebar">
  <div class="brand"><div class="logo">ϟ</div><span>TIKEFFECT</span></div>
  <div class="navlabel">MENU PRINCIPAL</div>
  <nav class="nav">
    <a class="active" href="#"><span>▦</span><span>Visão geral</span></a>
    <a href="#conexao"><span>◉</span><span>Conectar TikTok</span></a>
    <a href="#efeitos"><span>✦</span><span>Meus efeitos</span></a>
    <a href="#overlay"><span>▣</span><span>Overlay OBS</span></a>
    <a href="#eventos"><span>⌁</span><span>Eventos da live</span></a>
  </nav>
  <div class="navlabel">SISTEMA</div>
  <nav class="nav"><a href="#"><span>⚙</span><span>Configurações</span></a><a href="#"><span>♙</span><span>Minha conta</span></a></nav>
  <div class="sidebottom">TIKEFFECT • PRÉVIA 0.1</div>
</aside>
<main>
  <header class="top">
    <div><div class="eyebrow">CENTRAL DE CONTROLE</div><h1>Visão geral</h1><p class="sub">Gerencie sua live e seus efeitos em um só lugar.</p></div>
    <div class="profile"><div class="avatar">L</div><div><b>Administrador</b><div class="muted">Acesso privado</div></div></div>
  </header>
  <section class="cards">
    <div class="card"><div class="metric">Status da conexão <span class="ico">◉</span></div><div class="value" style="color:#ff7892">Offline</div><div class="hint">TikTok Live não conectado</div></div>
    <div class="card"><div class="metric">Efeitos cadastrados <span class="ico">✦</span></div><div class="value">08</div><div class="hint">Prontos para configurar</div></div>
    <div class="card"><div class="metric">Presentes recebidos <span class="ico">🎁</span></div><div class="value">0</div><div class="hint">Nesta sessão demonstrativa</div></div>
    <div class="card"><div class="metric">Comentários <span class="ico">▤</span></div><div class="value">0</div><div class="hint">Nesta sessão demonstrativa</div></div>
  </section>
  <section class="content">
    <div>
      <div class="panel" id="conexao">
        <div class="panelhead"><div><h2>Conectar TikTok Live</h2><div class="muted">Vincule sua transmissão para receber eventos.</div></div><span class="status">● DESCONECTADO</span></div>
        <div class="connect"><div><strong>Pronto para conectar sua live?</strong><div class="muted">A conexão real será ativada na próxima etapa do projeto.</div></div><button onclick="alert('Esta é uma prévia. A conexão real com o TikTok ainda será configurada.')">Conectar conta</button></div>
        <h2 id="efeitos">Seus efeitos</h2><div class="muted">Ative, desative e organize os efeitos da transmissão.</div>
        <div class="effect"><div class="effecticon">🎁</div><div><div class="effectname">Presente recebido</div><div class="effectdesc">Dispara ao receber um presente</div></div><div class="toggle on"></div></div>
        <div class="effect"><div class="effecticon">💰</div><div><div class="effectname">Chuva de moedas</div><div class="effectdesc">Animação de moedas na tela</div></div><div class="toggle on"></div></div>
        <div class="effect"><div class="effecticon">🔥</div><div><div class="effectname">Explosão de curtidas</div><div class="effectdesc">Dispara por meta de likes</div></div><div class="toggle on"></div></div>
        <div class="effect"><div class="effecticon">💬</div><div><div class="effectname">Alerta de comentário</div><div class="effectdesc">Mostra mensagem na tela</div></div><div class="toggle"></div></div>
        <div class="bottom"><button onclick="alert('O editor de efeitos será desenvolvido na próxima etapa.')">＋ Adicionar efeito</button><button class="secondary" onclick="alert('Editor demonstrativo.')">Editar efeitos</button></div>
      </div>
    </div>
    <div>
      <div class="panel" id="overlay">
        <div class="panelhead"><div><h2>Prévia do Overlay</h2><div class="muted">Como os efeitos poderão aparecer na live.</div></div><span class="pill">OBS / Live Studio</span></div>
        <div class="preview"><div><div class="screen">✨ 🎁 ✨</div><b>Seu efeito aparecerá aqui</b><p>Esta área será a fonte de navegador que você adicionará ao OBS ou TikTok Live Studio.</p></div></div>
        <div class="bottom"><button class="secondary" onclick="alert('O link do overlay será gerado quando o sistema estiver hospedado.')">Copiar link do overlay</button></div>
      </div>
      <div class="panel" id="eventos" style="margin-top:18px">
        <div class="panelhead"><div><h2>Últimos eventos</h2><div class="muted">Atividade recente da transmissão.</div></div><span class="pill">AO VIVO</span></div>
        <div style="text-align:center;padding:22px 5px;color:#8994a8"><div style="font-size:25px;margin-bottom:9px">⌁</div><b style="color:#dce2ed">Nenhum evento ainda</b><div class="muted" style="margin-top:6px">Conecte sua live para começar a receber eventos.</div></div>
      </div>
    </div>
  </section>
  <div class="muted" style="text-align:center;margin:25px 0 5px">TIKEFFECT • Prévia visual demonstrativa — ainda não conectado ao TikTok.</div>
</main>
</div>
</body>
</html>'''
path = Path("/mnt/data/tikeffect-preview.html")
path.write_text(html, encoding="utf-8")
print(path)



