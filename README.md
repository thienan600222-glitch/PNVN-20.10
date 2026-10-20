<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<meta name="theme-color" content="#000000">
<title>Nụ & lời chúc 20/10</title>
<style>
:root{
  --pink:#ff9ec7; --rose:#ff6fa5; --lilac:#b79bff; --gold:#ffd98a; --ink:#1a0d33; --p:0;
  --font:'Be Vietnam Pro',system-ui,-apple-system,'Segoe UI',Roboto,sans-serif;
  --script:'Pacifico','Be Vietnam Pro',cursive;
}
*{box-sizing:border-box;margin:0;padding:0;-webkit-tap-highlight-color:transparent}
html,body{width:100%;height:100%;overflow:hidden;background:#0b0720;color:#fff;font-family:var(--font);user-select:none;-webkit-user-select:none}
button,input{font:inherit;color:inherit}

/* ---------- nền ---------- */
.bgl{position:fixed;inset:0;opacity:0;transition:opacity 1.6s ease}
.bgl.on{opacity:1}
.bgl:nth-child(1){background:radial-gradient(120% 90% at 50% 0%,#2a1458 0%,#140a35 45%,#0b0720 100%)}
.bgl:nth-child(2){background:radial-gradient(120% 90% at 50% 0%,#0e3a52 0%,#07202f 50%,#030d16 100%)}
.bgl:nth-child(3){background:radial-gradient(120% 90% at 50% 0%,#7a2d6a 0%,#3b1646 50%,#16082c 100%)}
.bgl:nth-child(4){background:linear-gradient(180deg,#2d1250 0%,#8c3a7c 45%,#ff8fa3 80%,#ffd6a5 100%)}
#fx{position:fixed;inset:0;width:100%;height:100%;pointer-events:none}

/* ---------- sân khấu ---------- */
#stage{position:fixed;inset:0;padding:env(safe-area-inset-top) env(safe-area-inset-right) env(safe-area-inset-bottom) env(safe-area-inset-left)}
.scene{position:absolute;left:4%;right:4%;top:26%;bottom:31%;display:flex;flex-direction:column;align-items:center;justify-content:center;opacity:0;pointer-events:none;transition:opacity .7s ease}
.scene.on{opacity:1}
.rv{opacity:0;transform:translateY(14px) scale(.96);transition:opacity .9s ease,transform .9s cubic-bezier(.2,.8,.2,1)}
.rv.on{opacity:1;transform:none}

/* ---------- Nụ ---------- */
#nu{position:absolute;width:min(62vw,36vh);aspect-ratio:240/300;left:50%;top:38%;transform:translate(-50%,-50%) scale(1);
  transition:left 1.1s cubic-bezier(.6,.05,.2,1),top 1.1s cubic-bezier(.6,.05,.2,1),transform 1.1s cubic-bezier(.6,.05,.2,1),opacity .8s;z-index:5}
.m-side #nu{left:21%;top:15%;transform:translate(-50%,-50%) scale(.52)}
.m-hide #nu{opacity:0}
.nu-glow{position:absolute;inset:-18%;border-radius:50%;background:radial-gradient(circle,rgba(255,170,215,.55) 0%,rgba(190,150,255,.22) 45%,transparent 70%);
  transform:scale(calc(.9 + var(--p)*.22));opacity:calc(.55 + var(--p)*.35)}
.nu-svg{position:relative;width:100%;height:100%;overflow:visible;animation:float 4.6s ease-in-out infinite;filter:drop-shadow(0 10px 22px rgba(255,120,190,.35))}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-9px)}}
.wing{animation:flap 2.6s ease-in-out infinite;opacity:.85}
.wing.wl{transform-origin:100px 182px}
.wing.wr{transform-origin:140px 182px;animation-delay:-.1s}
@keyframes flap{0%,100%{transform:rotate(0)}50%{transform:rotate(-7deg)}}
.wing.wr{animation-name:flapR}
@keyframes flapR{0%,100%{transform:rotate(0)}50%{transform:rotate(7deg)}}
.head{transform-origin:120px 156px;animation:sway 5.2s ease-in-out infinite}
@keyframes sway{0%,100%{transform:rotate(-1.6deg)}50%{transform:rotate(1.6deg)}}
.head-tilt{transform-origin:120px 156px;transition:transform .5s ease}
.eye{animation:blink 5.4s infinite}
.eyeR{animation-delay:.03s}
@keyframes blink{0%,91%,100%{transform:scaleY(1)}94.5%{transform:scaleY(.08)}}
.arcL,.arcR,.mouth-o,.wink-star{display:none}
.blush{opacity:.55;transition:opacity .5s}
.arm-r{transform-origin:143px 182px}
.wave .arm-r{animation:wave 1s ease-in-out infinite alternate}
@keyframes wave{from{transform:rotate(-26deg)}to{transform:rotate(10deg)}}
.shy .blush{opacity:1}
.shy .head-tilt{transform:rotate(4deg)}
.happy .eye{display:none}.happy .arcL,.happy .arcR{display:block}.happy .blush{opacity:.95}
.wink .eyeR{display:none}.wink .arcR{display:block}.wink .head-tilt{transform:rotate(-7deg)}
.wink .wink-star{display:block;animation:twk 1.1s ease-in-out infinite}
@keyframes twk{0%,100%{transform:scale(.6);opacity:.4}50%{transform:scale(1.15);opacity:1}}
.wink-star{transform-box:fill-box;transform-origin:center}
.talk .mouth-c{display:none}.talk .mouth-o{display:block;transform-origin:120px 139px;animation:mouth .3s ease-in-out infinite alternate}
@keyframes mouth{from{transform:scaleY(.35)}to{transform:scaleY(1)}}

/* ---------- lời thoại ---------- */
#bubble{position:absolute;left:6%;right:6%;bottom:calc(7% + env(safe-area-inset-bottom));display:flex;justify-content:center;z-index:6;pointer-events:none}
#bubble.empty{opacity:0}
#line{max-width:34em;text-align:center;font-size:clamp(19px,5.2vw,30px);line-height:1.42;font-weight:600;
  padding:.5em .9em;border-radius:1.2em;background:rgba(24,10,52,.38);backdrop-filter:blur(6px);-webkit-backdrop-filter:blur(6px);
  text-shadow:0 2px 14px rgba(0,0,0,.45)}
#line em{font-style:normal;font-family:var(--script);font-weight:400;color:var(--pink);text-shadow:0 0 16px rgba(255,130,190,.8)}
.w{display:inline-block;opacity:0;transform:translateY(8px);animation:wIn .55s cubic-bezier(.2,.8,.2,1) forwards;white-space:pre}
@keyframes wIn{to{opacity:1;transform:none}}

/* ---------- cảnh: ngày ---------- */
.bigdate{font-family:var(--script);font-size:clamp(74px,25vw,150px);line-height:1;display:flex;align-items:baseline;gap:.05em;
  background:linear-gradient(180deg,#fff 10%,#ffc2dd 55%,#ffd98a 100%);-webkit-background-clip:text;background-clip:text;color:transparent;
  filter:drop-shadow(0 0 22px rgba(255,130,190,.65));transform:scale(calc(1 + var(--p)*.06))}
.bigdate i{font-style:normal}
.date-sub{margin-top:.4em;letter-spacing:.35em;text-transform:uppercase;font-size:clamp(11px,3vw,16px);color:#ffd7ea;opacity:.9}

/* ---------- cảnh: lịch sử ---------- */
.hist{display:flex;flex-direction:column;align-items:center;gap:.7em;text-align:center}
.h-year{font-family:var(--script);font-size:clamp(54px,17vw,96px);color:var(--gold);text-shadow:0 0 24px rgba(255,200,120,.6);line-height:1}
.h-line{font-size:clamp(13px,3.6vw,19px);color:#ffe6f1;max-width:22em}
.h-track{display:flex;align-items:center;gap:10px;width:min(86%,420px);font-size:clamp(11px,3vw,14px);color:#ffd7ea}
.h-track .bar{flex:1;height:4px;border-radius:4px;background:rgba(255,255,255,.18);overflow:hidden}
.h-track .bar i{display:block;height:100%;width:0;background:linear-gradient(90deg,#ff9ec7,#ffd98a);border-radius:4px;transition:width 2.2s cubic-bezier(.3,.6,.2,1) .3s}
#h3.on .bar i{width:100%}
.h-yrs{font-size:clamp(15px,4.2vw,22px);color:#fff}
.h-yrs b{font-family:var(--script);font-weight:400;font-size:1.9em;color:var(--pink);text-shadow:0 0 18px rgba(255,130,190,.8)}

/* ---------- cảnh: chòm sao ---------- */
.heroes{width:min(100%,520px);height:100%}
.heroes svg{width:100%;height:100%;overflow:visible}
.node{opacity:0;transform-box:fill-box;transform-origin:center}
.node.on{opacity:1;animation:starPop .9s cubic-bezier(.2,.9,.3,1.4)}
@keyframes starPop{from{transform:scale(0)}to{transform:scale(1)}}
.edge{stroke:rgba(255,214,235,.55);stroke-width:1.2;stroke-dasharray:240;stroke-dashoffset:240;transition:stroke-dashoffset 1.2s ease}
.edge.on{stroke-dashoffset:0}
.hname{font-size:13.5px;fill:#fff;font-weight:600;paint-order:stroke;stroke:#150b30;stroke-width:4px;stroke-linejoin:round}
.hyear{font-size:11.5px;fill:#ffc8e0;paint-order:stroke;stroke:#150b30;stroke-width:3.5px;stroke-linejoin:round}
.hyou{font-size:17px;fill:#ffd98a;font-family:var(--script);paint-order:stroke;stroke:#150b30;stroke-width:4px}
.lbl{opacity:0;transition:opacity 1s ease .4s}
.lbl.on{opacity:1}

/* ---------- cảnh: thầm lặng ---------- */
.cards{display:flex;flex-direction:column;gap:.55em;width:min(100%,430px)}
.card{display:flex;gap:.8em;align-items:center;padding:.7em 1em;border-radius:1em;background:rgba(255,255,255,.09);border:1px solid rgba(255,200,225,.28);
  font-size:clamp(13px,3.7vw,17px);line-height:1.35;backdrop-filter:blur(5px);-webkit-backdrop-filter:blur(5px)}
.card span.ic{font-size:1.5em;color:var(--pink);text-shadow:0 0 14px rgba(255,130,190,.9);flex:none;width:1.3em;text-align:center}

/* ---------- cảnh: sức khỏe ---------- */
.health{position:relative;width:min(100%,420px);aspect-ratio:2/1.3;display:grid;place-items:start center}
.health svg.ecg{position:absolute;left:0;right:0;bottom:0;width:100%;height:32%;overflow:visible}
.ecg path{fill:none;stroke:#8ff3d3;stroke-width:3;stroke-linecap:round;stroke-linejoin:round;stroke-dasharray:100;stroke-dashoffset:100;animation:ecg 2.8s linear infinite;filter:drop-shadow(0 0 6px #5ff0c0)}
@keyframes ecg{0%{stroke-dashoffset:100}65%,88%{stroke-dashoffset:0;opacity:1}100%{stroke-dashoffset:0;opacity:0}}
.heart{position:relative;width:30%;margin-top:2%;transform:scale(calc(1 + var(--p)*.22));filter:drop-shadow(0 0 22px rgba(255,90,150,.85))}
.plus{position:absolute;color:#9ff7da;font-weight:600;animation:plus 3.4s ease-in-out infinite;opacity:0}
@keyframes plus{0%{opacity:0;transform:translateY(12px)}30%{opacity:.9}100%{opacity:0;transform:translateY(-30px)}}

/* ---------- cảnh: bình yên ---------- */
.pond{width:min(100%,420px)}
.pond svg{width:100%;overflow:visible}
.ring{fill:none;stroke:rgba(190,235,255,.6);stroke-width:1.4;transform-box:fill-box;transform-origin:center;animation:ripple 4.8s ease-out infinite}
@keyframes ripple{0%{transform:scale(.15);opacity:.9}100%{transform:scale(1.5);opacity:0}}
.lotus{transform-box:fill-box;transform-origin:50% 100%;animation:lotus 5s ease-in-out infinite}
@keyframes lotus{0%,100%{transform:translateY(0) rotate(-1.5deg)}50%{transform:translateY(-3px) rotate(1.5deg)}}

/* ---------- cảnh: tự do ---------- */
.sky{position:relative;width:min(100%,420px);height:100%}
.bfly{position:absolute;width:24%;animation:fly 9s ease-in-out infinite;filter:drop-shadow(0 0 10px rgba(190,160,255,.8))}
.bfly:nth-child(2){left:8%;top:60%;animation-delay:-3s;width:19%}
.bfly:nth-child(3){left:58%;top:22%;animation-delay:-6s;width:21%}
.bfly:nth-child(1){left:32%;top:46%}
@keyframes fly{0%{transform:translate(0,0) rotate(-8deg)}25%{transform:translate(40px,-34px) rotate(10deg)}50%{transform:translate(90px,-12px) rotate(-6deg)}75%{transform:translate(40px,-52px) rotate(12deg)}100%{transform:translate(0,0) rotate(-8deg)}}
.bw{transform-box:fill-box;animation:bw .28s ease-in-out infinite alternate}
.bw.r{transform-origin:left center}.bw.l{transform-origin:right center}
@keyframes bw{from{transform:scaleX(1)}to{transform:scaleX(.45)}}

/* ---------- cảnh: yêu thương ---------- */
.lovering{position:relative;width:min(70vw,300px);aspect-ratio:1}
.orbit{position:absolute;inset:0;animation:spin 22s linear infinite}
@keyframes spin{to{transform:rotate(360deg)}}
.orbit i{position:absolute;left:50%;top:50%;width:11%;height:11%;margin:-5.5%;display:grid;place-items:center;font-style:normal;color:var(--pink);text-align:center;font-size:clamp(16px,4vw,22px);line-height:1;text-shadow:0 0 12px rgba(255,120,180,.9)}
.bigheart{position:absolute;left:50%;top:50%;width:46%;transform:translate(-50%,-50%) scale(calc(1 + var(--p)*.2));filter:drop-shadow(0 0 24px rgba(255,100,160,.9))}

/* ---------- cảnh: hoa ---------- */
.bouquet{width:min(78vw,330px)}
.bouquet svg{width:100%;overflow:visible}
.fl{transform-box:fill-box;transform-origin:center;transform:scale(0)}
.scene.on .fl{animation:bloom 1.3s cubic-bezier(.2,.9,.3,1.25) forwards;animation-delay:var(--d)}
@keyframes bloom{from{transform:scale(0) rotate(-40deg)}to{transform:scale(1) rotate(0)}}
.stem{stroke-dasharray:260;stroke-dashoffset:260}
.scene.on .stem{animation:grow 1.1s ease-out forwards;animation-delay:var(--d)}
@keyframes grow{to{stroke-dashoffset:0}}
.bq-sway{transform-origin:50% 100%;animation:bqsway 4.5s ease-in-out infinite}
@keyframes bqsway{0%,100%{transform:rotate(-1.2deg)}50%{transform:rotate(1.2deg)}}

/* ---------- câu hỏi ---------- */
.qbtns{display:flex;gap:14px;flex-wrap:wrap;justify-content:center;pointer-events:auto}
.qbtns button{padding:.75em 1.4em;border:0;border-radius:2em;font-weight:600;font-size:clamp(15px,4vw,19px);cursor:pointer;color:#2b0f45;
  background:linear-gradient(135deg,#ffd0e6,#ffa6cf);box-shadow:0 8px 22px rgba(255,120,190,.45);transition:transform .2s}
.qbtns button:nth-child(2){background:linear-gradient(135deg,#e5dcff,#b7a3ff);box-shadow:0 8px 22px rgba(150,120,255,.45)}
.qbtns button:active{transform:scale(.95)}

#sc-question{top:61%;bottom:24%}
/* ---------- kết ---------- */
.final{pointer-events:auto;text-align:center;padding:1.2em 1.3em 1.1em;border-radius:1.6em;width:min(100%,430px);
  background:linear-gradient(160deg,rgba(255,255,255,.18),rgba(255,255,255,.06));border:1px solid rgba(255,220,235,.45);
  box-shadow:0 20px 60px rgba(60,10,70,.5),inset 0 0 30px rgba(255,200,230,.12);backdrop-filter:blur(8px);-webkit-backdrop-filter:blur(8px)}
.f-sub{font-size:clamp(12px,3.2vw,15px);letter-spacing:.3em;text-transform:uppercase;color:#ffd9ec}
.final h1{font-family:var(--script);font-weight:400;font-size:clamp(30px,9vw,50px);line-height:1.15;margin:.15em 0;color:#fff;text-shadow:0 0 22px rgba(255,130,190,.8)}
.f-date{font-family:var(--script);font-size:clamp(28px,8vw,44px);color:var(--gold);text-shadow:0 0 20px rgba(255,200,120,.6)}
.f-to{margin:.5em 0 .2em;font-size:clamp(14px,3.8vw,18px);color:#fff}
.f-msg{font-size:clamp(12.5px,3.4vw,15.5px);line-height:1.5;color:#ffe3f0;max-width:26em;margin:0 auto}
.f-act{display:flex;flex-wrap:wrap;gap:8px;justify-content:center;margin-top:.9em}
.f-act input{flex:1 1 100%;min-width:0;padding:.55em .9em;border-radius:2em;border:1px solid rgba(255,255,255,.35);background:rgba(255,255,255,.12);outline:none;font-size:14px;user-select:text;-webkit-user-select:text}
.f-act input::placeholder{color:rgba(255,255,255,.6)}
.f-act button{padding:.55em 1.1em;border-radius:2em;border:0;background:linear-gradient(135deg,#ffd0e6,#ffa6cf);color:#2b0f45;font-weight:600;font-size:14px;cursor:pointer}
.f-act button.alt{background:rgba(255,255,255,.18);color:#fff}

/* ---------- HUD, mở đầu ---------- */
#prog{position:fixed;left:0;top:0;height:3px;width:0;background:linear-gradient(90deg,#ff9ec7,#ffd98a);z-index:20;transition:width .8s ease;pointer-events:none}
#mute{position:fixed;right:max(12px,env(safe-area-inset-right));top:calc(12px + env(safe-area-inset-top));z-index:20;width:40px;height:40px;border-radius:50%;border:1px solid rgba(255,255,255,.3);background:rgba(255,255,255,.1);cursor:pointer;display:grid;place-items:center;backdrop-filter:blur(4px);-webkit-backdrop-filter:blur(4px)}
#mute svg{width:20px;height:20px;fill:none;stroke:#fff;stroke-width:2;stroke-linecap:round;stroke-linejoin:round}
#mute .off{display:none}#mute.muted .on{display:none}#mute.muted .off{display:block}
#hint{position:fixed;left:0;right:0;bottom:calc(2.2% + env(safe-area-inset-bottom));text-align:center;font-size:12px;letter-spacing:.2em;color:rgba(255,255,255,.55);opacity:0;transition:opacity .8s;z-index:6;pointer-events:none}
#hint.on{opacity:1;animation:hint 2.4s ease-in-out infinite}
@keyframes hint{50%{opacity:.25}}
#start{position:fixed;inset:0;z-index:30;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:1.2em;text-align:center;padding:24px;cursor:pointer;
  background:radial-gradient(120% 90% at 50% 20%,#4a1f6e 0%,#1a0b3c 55%,#0b0720 100%);transition:opacity 1s ease,visibility 1s}
#start.gone{opacity:0;visibility:hidden;pointer-events:none}
#start .bud{width:min(34vw,150px);animation:float 3.6s ease-in-out infinite;filter:drop-shadow(0 0 26px rgba(255,130,190,.8))}
#start h2{font-family:var(--script);font-weight:400;font-size:clamp(30px,8.5vw,52px);line-height:1.2;text-shadow:0 0 24px rgba(255,130,190,.7)}
#start p{font-size:clamp(13px,3.6vw,17px);color:#ffd9ec;letter-spacing:.14em;animation:hint 2.2s ease-in-out infinite}
#start small{position:absolute;bottom:calc(18px + env(safe-area-inset-bottom));font-size:12px;color:rgba(255,255,255,.5)}

/* ---------- ngang màn hình ---------- */
@media (orientation:landscape) and (max-height:620px){
  #nu{width:min(24vw,38vh);top:44%}
  .m-side #nu{left:17%;top:46%;transform:translate(-50%,-50%) scale(.85)}
  .scene{left:36%;right:3%;top:6%;bottom:27%}
  #bubble{left:12%;right:12%;bottom:5%}
  #sc-question{left:20%;right:20%;top:auto;bottom:24%;height:14%}
  #sc-final{top:3%;bottom:3%;left:36%;right:3%}
  .final{padding:.6em 1em .7em;border-radius:1.2em}
  .final h1{font-size:clamp(22px,7.5vh,36px);margin:.05em 0}
  .f-date{font-size:clamp(20px,6vh,30px)}
  .f-sub{font-size:11px}
  .f-to{margin:.2em 0;font-size:13px}
  .f-msg{font-size:11.5px;line-height:1.4}
  .f-act{margin-top:.45em;gap:6px}
  .f-act input{flex:1 1 55%;padding:.4em .8em}
  .f-act button{padding:.4em .9em}
  #line{font-size:clamp(15px,3.6vh,24px)}
}
@media (orientation:landscape) and (min-height:621px){
  #nu{width:min(26vw,40vh);top:42%}
  .m-side #nu{left:18%;top:46%;transform:translate(-50%,-50%) scale(.9)}
  .scene{left:38%;right:4%;top:8%;bottom:28%}
  #line{font-size:clamp(20px,2.4vw,32px)}
  #sc-question{left:20%;right:20%;top:auto;bottom:23%;height:12%}
}
@media (prefers-reduced-motion:reduce){.nu-svg,.head,.wing,.orbit{animation:none}}

/* ===== Neon đêm: nền đen, chữ mono phát sáng, nhân vật Nụ là nụ hoa neon ===== */
:root{--pink:#ff7ab8;--rose:#ff5fa2;--lilac:#a99bff;--gold:#ffd98a;--font:ui-monospace,'SF Mono',Menlo,Consolas,'Roboto Mono','DejaVu Sans Mono',monospace;--script:var(--font)}
html,body{background:#000}
.bgl:nth-child(1){background:radial-gradient(100% 55% at 50% 100%,#14082a 0%,#000 72%)}
.bgl:nth-child(2){background:radial-gradient(100% 55% at 50% 100%,#04202a 0%,#000 72%)}
.bgl:nth-child(3){background:radial-gradient(100% 55% at 50% 100%,#2a0a1e 0%,#000 72%)}
.bgl:nth-child(4){background:radial-gradient(100% 65% at 50% 100%,#33150c 0%,#000 74%)}
#start{background:radial-gradient(100% 55% at 50% 100%,#14082a 0%,#000 72%)}
#line{background:none;-webkit-backdrop-filter:none;backdrop-filter:none;font-weight:400;letter-spacing:.03em;font-size:clamp(16px,4.5vw,25px);text-shadow:0 0 8px rgba(255,255,255,.6),0 0 26px rgba(255,122,184,.4)}
#line em{color:var(--pink);text-shadow:0 0 12px var(--pink),0 0 30px var(--pink)}
.card{background:none;-webkit-backdrop-filter:none;backdrop-filter:none;border:1px solid rgba(255,122,184,.5);border-radius:.6em;box-shadow:0 0 14px rgba(255,122,184,.2),inset 0 0 12px rgba(255,122,184,.08)}
.final{background:rgba(0,0,0,.6);border:1px solid rgba(255,122,184,.55);border-radius:.8em;box-shadow:0 0 34px rgba(255,122,184,.28),inset 0 0 26px rgba(255,122,184,.08)}
.qbtns button,.f-act button{background:none;color:#ffe9f4;border:1px solid var(--pink);border-radius:.5em;box-shadow:0 0 14px rgba(255,122,184,.45),inset 0 0 10px rgba(255,122,184,.2)}
.qbtns button:nth-child(2){background:none;border-color:var(--lilac);box-shadow:0 0 14px rgba(169,155,255,.45),inset 0 0 10px rgba(169,155,255,.2)}
.f-act button.alt{background:none;border-color:rgba(255,255,255,.4);box-shadow:none}
.f-act input{border-radius:.5em;background:none}
.nu-glow{background:radial-gradient(circle,rgba(255,122,184,.3) 0%,transparent 62%);opacity:calc(.5 + var(--p)*.5)}
.nu-svg{filter:drop-shadow(0 0 10px rgba(255,150,200,.9)) drop-shadow(0 0 36px rgba(255,122,184,.45))}
.nbud{transform-box:fill-box;transform-origin:50% 100%;transform:scale(calc(1 + var(--p)*.06));transition:fill .9s,stroke .9s}
.bloom .nbud{fill:rgba(255,217,138,.16);stroke:#ffd98a}
.arm-r{transform-origin:170px 214px}
.talk .mouth-o{transform-origin:120px 199px}

/* ===================================================================
   PATCH: sửa nút khó ấn + hiệu ứng đẹp
   =================================================================== */
html,body{touch-action:manipulation;-webkit-touch-callout:none}
button{touch-action:manipulation;-webkit-appearance:none;appearance:none}

/* --- GỐC LỖI 1: Nụ (z-index:5) nằm đè lên nút, nuốt chạm --- */
#nu,#nu *{pointer-events:none}
/* --- GỐC LỖI 2: thẻ .final / .qbtns vô hình vẫn bắt chạm, chặn "chạm để qua" --- */
.scene.on{z-index:7}
.scene:not(.on) .final,
.scene:not(.on) .qbtns,
.qbtns:not(.on){pointer-events:none}
.scene.on .final{pointer-events:auto}
#sc-question.on .qbtns.on{pointer-events:auto}

/* --- nút câu hỏi: to, dễ ấn, có hiệu ứng --- */
.qbtns{gap:16px}
.qbtns button,.f-act button{
  position:relative;overflow:hidden;isolation:isolate;cursor:pointer;
  min-height:52px;min-width:132px;padding:.8em 1.6em;
  letter-spacing:.04em;
  transition:transform .18s cubic-bezier(.2,.9,.3,1.4),box-shadow .25s ease,background-color .25s ease,filter .25s ease;
  animation:btnBreath 2.8s ease-in-out infinite;
  will-change:transform
}
.qbtns button:nth-child(2){animation-delay:-1.4s}
.qbtns button::before,.f-act button::before{
  content:"";position:absolute;top:0;bottom:0;left:-60%;width:45%;z-index:-1;pointer-events:none;
  background:linear-gradient(100deg,transparent,rgba(255,255,255,.38),transparent);
  transform:skewX(-20deg);animation:btnShine 3.6s ease-in-out infinite
}
.qbtns button:nth-child(2)::before{animation-delay:-1.8s}
@keyframes btnBreath{
  0%,100%{box-shadow:0 0 14px rgba(255,122,184,.45),inset 0 0 10px rgba(255,122,184,.2)}
  50%{box-shadow:0 0 26px rgba(255,122,184,.8),0 0 50px rgba(255,122,184,.25),inset 0 0 16px rgba(255,122,184,.35)}
}
.qbtns button:nth-child(2){animation-name:btnBreath2}
@keyframes btnBreath2{
  0%,100%{box-shadow:0 0 14px rgba(169,155,255,.45),inset 0 0 10px rgba(169,155,255,.2)}
  50%{box-shadow:0 0 26px rgba(169,155,255,.85),0 0 50px rgba(169,155,255,.28),inset 0 0 16px rgba(169,155,255,.38)}
}
@keyframes btnShine{0%,55%{left:-60%}100%{left:130%}}
.qbtns button:active,.f-act button:active{transform:scale(.93);filter:brightness(1.25)}
.qbtns button:focus-visible,.f-act button:focus-visible,#mute:focus-visible{outline:2px solid var(--gold);outline-offset:3px}
@media (hover:hover){
  .qbtns button:hover,.f-act button:hover{transform:translateY(-3px) scale(1.05);filter:brightness(1.18)}
}
/* nút hiện ra kiểu nảy lên */
.qbtns.on button{animation:btnPop .7s cubic-bezier(.2,.9,.3,1.4) both,btnBreath 2.8s ease-in-out .7s infinite}
.qbtns.on button:nth-child(2){animation:btnPop .7s cubic-bezier(.2,.9,.3,1.4) .12s both,btnBreath2 2.8s ease-in-out .9s infinite}
@keyframes btnPop{from{opacity:0;transform:translateY(26px) scale(.6)}to{opacity:1;transform:none}}

/* nút ở thẻ kết */
.f-act{gap:10px}
.f-act button{min-height:46px;flex:1 1 40%;font-size:14px;animation:none}
.f-act button:not(.alt){animation:btnBreath 2.8s ease-in-out infinite}
.f-act button.alt:hover{border-color:var(--pink)}

/* nút âm thanh */
#mute{width:46px;height:46px;transition:transform .18s cubic-bezier(.2,.9,.3,1.4),box-shadow .3s,border-color .3s;
  border-color:rgba(255,122,184,.6);box-shadow:0 0 12px rgba(255,122,184,.35),inset 0 0 8px rgba(255,122,184,.15)}
#mute:active{transform:scale(.88)}
#mute:not(.muted){animation:muteRing 2.4s ease-out infinite}
@keyframes muteRing{0%{box-shadow:0 0 0 0 rgba(255,122,184,.55),0 0 12px rgba(255,122,184,.35)}100%{box-shadow:0 0 0 14px rgba(255,122,184,0),0 0 12px rgba(255,122,184,.35)}}
#mute svg{filter:drop-shadow(0 0 4px rgba(255,255,255,.7))}

/* ripple trong nút */
.rip{position:absolute;border-radius:50%;pointer-events:none;z-index:-1;
  background:radial-gradient(circle,rgba(255,255,255,.75),rgba(255,160,210,.35) 55%,transparent 70%);
  transform:translate(-50%,-50%) scale(0);animation:rip .65s ease-out forwards}
@keyframes rip{to{transform:translate(-50%,-50%) scale(1);opacity:0}}

/* hạt bay khi chạm */
.fxp{position:fixed;pointer-events:none;z-index:60;line-height:1;text-shadow:0 0 10px currentColor,0 0 22px currentColor;will-change:transform,opacity}
.tapring{position:fixed;pointer-events:none;z-index:59;width:14px;height:14px;margin:-7px 0 0 -7px;border-radius:50%;
  border:2px solid rgba(255,150,205,.9);box-shadow:0 0 14px rgba(255,122,184,.8),inset 0 0 8px rgba(255,122,184,.5);
  animation:tapring .7s ease-out forwards}
@keyframes tapring{to{transform:scale(7);opacity:0}}

/* màn hình mở quà */
#start{overflow:hidden}
#start::before,#start::after{content:"";position:absolute;border-radius:50%;pointer-events:none;filter:blur(50px);opacity:.55;animation:orb 9s ease-in-out infinite}
#start::before{width:60vmax;height:60vmax;left:-20vmax;top:-18vmax;background:radial-gradient(circle,rgba(255,122,184,.35),transparent 65%)}
#start::after{width:55vmax;height:55vmax;right:-22vmax;bottom:-20vmax;background:radial-gradient(circle,rgba(169,155,255,.35),transparent 65%);animation-delay:-4.5s}
@keyframes orb{0%,100%{transform:translate(0,0) scale(1)}50%{transform:translate(6vmax,4vmax) scale(1.15)}}
#start>*{position:relative;z-index:1}
#start small{position:absolute}
#start .bud{animation:float 3.6s ease-in-out infinite,budGlow 2.6s ease-in-out infinite}
@keyframes budGlow{0%,100%{filter:drop-shadow(0 0 16px rgba(255,130,190,.6))}50%{filter:drop-shadow(0 0 38px rgba(255,130,190,1))}}
#start p{padding:.9em 1.8em;border:1px solid var(--pink);border-radius:.5em;min-height:52px;display:flex;align-items:center;
  box-shadow:0 0 16px rgba(255,122,184,.5),inset 0 0 12px rgba(255,122,184,.2);animation:startBtn 2.2s ease-in-out infinite}
@keyframes startBtn{0%,100%{transform:scale(1);box-shadow:0 0 16px rgba(255,122,184,.5),inset 0 0 12px rgba(255,122,184,.2)}
  50%{transform:scale(1.06);box-shadow:0 0 34px rgba(255,122,184,.9),0 0 60px rgba(255,122,184,.3),inset 0 0 18px rgba(255,122,184,.35)}}
#start:active .bud{transform:scale(.92)}
#start.gone .bud{transform:scale(1.5);transition:transform 1s ease}

/* thẻ kết: xuất hiện hoành tráng + viền thở */
.scene.on .final{animation:finalIn 1s cubic-bezier(.2,.9,.3,1.15) both,finalGlow 3.4s ease-in-out 1s infinite}
@keyframes finalIn{from{opacity:0;transform:translateY(40px) scale(.86)}to{opacity:1;transform:none}}
@keyframes finalGlow{
  0%,100%{box-shadow:0 0 34px rgba(255,122,184,.28),inset 0 0 26px rgba(255,122,184,.08);border-color:rgba(255,122,184,.55)}
  50%{box-shadow:0 0 60px rgba(255,122,184,.55),0 0 110px rgba(169,155,255,.2),inset 0 0 36px rgba(255,122,184,.16);border-color:rgba(255,190,225,.9)}}
.final h1{animation:titleGlow 3s ease-in-out infinite}
@keyframes titleGlow{0%,100%{text-shadow:0 0 14px rgba(255,130,190,.7)}50%{text-shadow:0 0 30px rgba(255,130,190,1),0 0 60px rgba(255,130,190,.5)}}

/* thanh tiến trình sáng hơn */
#prog{box-shadow:0 0 10px rgba(255,150,200,.9),0 0 22px rgba(255,217,138,.5)}

/* lời thoại: thẻ card hiện lần lượt */
.card{transition:transform .25s ease,box-shadow .3s ease}
.card:hover{transform:translateX(4px);box-shadow:0 0 22px rgba(255,122,184,.4),inset 0 0 14px rgba(255,122,184,.12)}

@media (orientation:landscape) and (max-height:620px){
  .qbtns button{min-height:46px;padding:.55em 1.3em}
}
@media (prefers-reduced-motion:reduce){
  .qbtns button,.qbtns button::before,.f-act button,.f-act button::before,#mute,#start::before,#start::after,#start p,.final,.final h1{animation:none!important}
}

/* ===================================================================
   WOW PATCH 2: cực quang, 3D tilt, chữ nổ sáng, pháo hoa, trail
   =================================================================== */
:root{--tx:0;--ty:0}
#aurora{position:fixed;inset:0;z-index:0;pointer-events:none;overflow:hidden;mix-blend-mode:screen}
#aurora i{position:absolute;width:75vmax;height:75vmax;border-radius:50%;opacity:.42;animation:aur 18s ease-in-out infinite}
#aurora i:nth-child(1){left:-30vmax;top:-34vmax;background:radial-gradient(circle,#ff4fa0 0%,transparent 62%)}
#aurora i:nth-child(2){right:-34vmax;top:6vh;background:radial-gradient(circle,#6a5cff 0%,transparent 62%);animation-delay:-6s;animation-duration:22s}
#aurora i:nth-child(3){left:6vw;bottom:-50vmax;background:radial-gradient(circle,#14e0b6 0%,transparent 62%);animation-delay:-11s;opacity:.28;animation-duration:26s}
@keyframes aur{0%,100%{transform:translate(0,0) scale(1) rotate(0)}33%{transform:translate(9vmax,6vmax) scale(1.18) rotate(40deg)}66%{transform:translate(-6vmax,10vmax) scale(.92) rotate(-30deg)}}

#fx2{position:fixed;inset:0;width:100%;height:100%;pointer-events:none;z-index:55}
#flash{position:fixed;inset:0;z-index:58;pointer-events:none;opacity:0;mix-blend-mode:screen;
  background:radial-gradient(circle at 50% 45%,rgba(255,255,255,.95),rgba(255,140,200,.55) 40%,transparent 72%)}
#sweep{position:fixed;top:0;bottom:0;left:0;width:55%;z-index:57;pointer-events:none;opacity:0;mix-blend-mode:screen;
  background:linear-gradient(100deg,transparent,rgba(255,150,210,.25) 35%,rgba(255,255,255,.4) 50%,rgba(169,155,255,.25) 65%,transparent)}
#cglow{position:fixed;left:0;top:0;width:280px;height:280px;margin:-140px 0 0 -140px;border-radius:50%;pointer-events:none;z-index:50;
  background:radial-gradient(circle,rgba(255,122,184,.32),rgba(169,155,255,.14) 45%,transparent 70%);
  mix-blend-mode:screen;opacity:0;transition:opacity .45s ease;will-change:transform}

/* 3D tilt theo tay / con trỏ / nghiêng máy */
.scene{transform:perspective(1000px) rotateX(calc(var(--tx)*1deg)) rotateY(calc(var(--ty)*1deg))}
.nu-glow{translate:calc(var(--ty)*-2px) calc(var(--tx)*2px)}

/* chữ hiện: mờ nhoè -> bừng sáng -> sắc nét */
.w{animation:wIn2 .8s cubic-bezier(.2,.8,.2,1) forwards}
@keyframes wIn2{
  0%{opacity:0;transform:translateY(18px) scale(.6) rotateX(70deg);filter:blur(12px);text-shadow:0 0 34px #fff}
  55%{opacity:1;filter:blur(0);text-shadow:0 0 14px #fff,0 0 42px #ff7ab8,0 0 80px #ff7ab8}
  100%{opacity:1;transform:none;filter:none}
}
#line{perspective:600px}

.bigdate{animation:dateGlow 3.2s ease-in-out infinite}
@keyframes dateGlow{
  0%,100%{filter:drop-shadow(0 0 18px rgba(255,130,190,.6))}
  50%{filter:drop-shadow(0 0 38px rgba(255,150,200,1)) drop-shadow(0 0 90px rgba(255,217,138,.55))}}

/* màn mở quà */
#start h2{animation:neonFlick 6s linear infinite}
@keyframes neonFlick{0%,18%,22%,62%,64%,100%{opacity:1}19%,21%{opacity:.5}63%{opacity:.7}}
.budwrap{position:relative;display:grid;place-items:center;width:min(34vw,150px)}
.budwrap .bud{width:100%}
.sring{position:absolute;left:50%;top:50%;width:100%;aspect-ratio:1;margin:-50% 0 0 -50%;border-radius:50%;pointer-events:none;
  border:1.5px solid rgba(255,122,184,.7);box-shadow:0 0 16px rgba(255,122,184,.5),inset 0 0 14px rgba(255,122,184,.3);
  animation:sring 3.3s ease-out infinite;opacity:0}
.sring:nth-child(2){animation-delay:1.1s;border-color:rgba(169,155,255,.7)}
.sring:nth-child(3){animation-delay:2.2s;border-color:rgba(255,217,138,.7)}
@keyframes sring{0%{transform:scale(.7);opacity:.9}100%{transform:scale(3.4);opacity:0}}
#start.gone{transform:scale(1.25)}
#start{transition:opacity 1s ease,visibility 1s,transform 1.2s ease}

@media (prefers-reduced-motion:reduce){
  .w{animation:wInR .4s forwards}@keyframes wInR{to{opacity:1;transform:none}}
  #aurora i,.sring,.bigdate,#start h2{animation:none!important}
  .scene{transform:none}
}
</style>
</head>
<body class="m-hero">

<div id="bgs"><div class="bgl on"></div><div class="bgl"></div><div class="bgl"></div><div class="bgl"></div></div>
<canvas id="fx"></canvas>
<div id="prog"></div>
<button id="mute" class="ui" aria-label="Bật/tắt nhạc">
  <svg viewBox="0 0 24 24"><g class="on"><path d="M4 9v6h4l5 4V5L8 9H4z"/><path d="M16.5 8.5a5 5 0 010 7M19 6a8.5 8.5 0 010 12"/></g><g class="off"><path d="M4 9v6h4l5 4V5L8 9H4z"/><path d="M17 9l5 6M22 9l-5 6"/></g></svg>
</button>

<div id="stage">

  <!-- ===== các cảnh ===== -->
  <section class="scene" id="sc-date"><div class="bigdate"><span>20</span><i>/</i><span>10</span></div><div class="date-sub">ngày phụ nữ việt nam</div></section>

  <section class="scene" id="sc-history"><div class="hist">
    <div class="h-year rv" id="h1">1930</div>
    <div class="h-line rv" id="h2">20 tháng 10 · Hội Phụ nữ phản đế Việt Nam ra đời, tiền thân của Hội Liên hiệp Phụ nữ Việt Nam</div>
    <div class="h-track rv" id="h3"><span>1930</span><span class="bar"><i></i></span><span>nay</span></div>
    <div class="h-yrs rv" id="h4"><b id="yrs">0</b> năm nói lời cảm ơn</div>
  </div></section>

  <section class="scene" id="sc-heroes"><div class="heroes">
    <svg viewBox="0 -10 360 310" preserveAspectRatio="xMidYMid meet">
      <g fill="none">
        <line class="edge" id="e12" x1="60" y1="75" x2="180" y2="100"/>
        <line class="edge" id="e23" x1="180" y1="100" x2="290" y2="72"/>
        <line class="edge" id="e24" x1="180" y1="100" x2="110" y2="178"/>
        <line class="edge" id="e35" x1="290" y1="72" x2="236" y2="178"/>
        <line class="edge" id="e45" x1="110" y1="178" x2="236" y2="178"/>
        <line class="edge" id="e46" x1="110" y1="178" x2="180" y2="252"/>
        <line class="edge" id="e56" x1="236" y1="178" x2="180" y2="252"/>
      </g>
      <g class="node" id="n1"><circle cx="60" cy="75" r="9" fill="rgba(255,190,225,.28)"/><circle cx="60" cy="75" r="4.5" fill="#fff"/></g>
      <g class="lbl" id="l1"><text class="hname" x="60" y="48" text-anchor="middle">Hai Bà Trưng</text><text class="hyear" x="60" y="62" text-anchor="middle">năm 40</text></g>
      <g class="node" id="n2"><circle cx="180" cy="100" r="9" fill="rgba(255,190,225,.28)"/><circle cx="180" cy="100" r="4.5" fill="#fff"/></g>
      <g class="lbl" id="l2"><text class="hname" x="180" y="73" text-anchor="middle">Bà Triệu</text><text class="hyear" x="180" y="87" text-anchor="middle">năm 248</text></g>
      <g class="node" id="n3"><circle cx="290" cy="72" r="9" fill="rgba(255,190,225,.28)"/><circle cx="290" cy="72" r="4.5" fill="#fff"/></g>
      <g class="lbl" id="l3"><text class="hname" x="290" y="26" text-anchor="middle">Nguyễn Thị</text><text class="hname" x="290" y="41" text-anchor="middle">Minh Khai</text><text class="hyear" x="290" y="55" text-anchor="middle">1910–1941</text></g>
      <g class="node" id="n4"><circle cx="110" cy="178" r="9" fill="rgba(255,190,225,.28)"/><circle cx="110" cy="178" r="4.5" fill="#fff"/></g>
      <g class="lbl" id="l4"><text class="hname" x="97" y="176" text-anchor="end">Võ Thị Sáu</text><text class="hyear" x="97" y="190" text-anchor="end">1933–1952</text></g>
      <g class="node" id="n5"><circle cx="236" cy="178" r="9" fill="rgba(255,190,225,.28)"/><circle cx="236" cy="178" r="4.5" fill="#fff"/></g>
      <g class="lbl" id="l5"><text class="hname" x="249" y="176">Nguyễn Thị Định</text><text class="hyear" x="249" y="190">1920–1992</text></g>
      <g class="node" id="n6"><circle cx="180" cy="252" r="16" fill="rgba(255,217,138,.22)"/><circle cx="180" cy="252" r="7" fill="#ffd98a"/><path d="M180 232v40M160 252h40" stroke="#ffd98a" stroke-width="1.2" opacity=".7"/></g>
      <g class="lbl" id="l6"><text class="hyou" x="180" y="286" text-anchor="middle">và cậu nữa</text></g>
    </svg>
  </div></section>

  <section class="scene" id="sc-unseen"><div class="cards">
    <div class="card rv" id="c1"><span class="ic">☀</span><span>Mang lại năng lượng tích cực và sự ấm áp cho mọi người mỗi ngày</span></div>
    <div class="card rv" id="c2"><span class="ic">✿</span><span>Luôn dịu dàng, chu đáo và biết ơn trong từng việc nhỏ ở gia đình lẫn Hội Thánh</span></div>
    <div class="card rv" id="c3"><span class="ic">☾</span><span>Giữ vững lòng tin yêu và sự khiêm nhường ngay cả khi đối diện với những thử thách trong cuộc sống</span></div>
    <div class="card rv" id="c4"><span class="ic">✦</span><span>Âm thầm cầu thay, chia sẻ và nâng đỡ những người xung quanh</span></div>
  </div></section>

  <section class="scene" id="sc-health"><div class="health">
    <svg class="ecg" viewBox="0 0 420 100" preserveAspectRatio="none"><path pathLength="100" d="M0 52 H120 L138 44 156 52 H176 L190 18 206 88 222 6 240 52 H270 L286 45 304 52 H420"/></svg>
    <svg class="heart" viewBox="0 0 100 92"><defs><linearGradient id="hg" x1="0" y1="0" x2="0" y2="1"><stop offset="0" stop-color="#ffb3d1"/><stop offset="1" stop-color="#ff4f8b"/></linearGradient></defs><path d="M50 88C36 76 4 56 4 30 4 10 28 2 40 14c5 5 8 9 10 14 2-5 5-9 10-14C72 2 96 10 96 30c0 26-32 46-46 58z" fill="url(#hg)" stroke="#fff" stroke-opacity=".7" stroke-width="1.5"/><path d="M20 24c3-8 12-11 18-7" fill="none" stroke="#fff" stroke-opacity=".7" stroke-width="3" stroke-linecap="round"/></svg>
    <span class="plus" style="left:8%;top:62%;font-size:22px">+</span>
    <span class="plus" style="left:86%;top:30%;font-size:28px;animation-delay:-1.2s">+</span>
    <span class="plus" style="left:70%;top:76%;font-size:18px;animation-delay:-2.2s">+</span>
    <span class="plus" style="left:22%;top:20%;font-size:20px;animation-delay:-.6s">+</span>
  </div></section>

  <section class="scene" id="sc-peace"><div class="pond">
    <svg viewBox="0 0 300 210">
      <defs>
        <linearGradient id="boxG" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#ffd0e6"/><stop offset="1" stop-color="#ff6fa5"/></linearGradient>
      </defs>
      <ellipse class="ring" cx="150" cy="135" rx="65" ry="22" style="animation-delay:0s"/>
      <ellipse class="ring" cx="150" cy="135" rx="65" ry="22" style="animation-delay:2s"/>
      <g class="lotus" style="transform-origin: 150px 115px;">
        <!-- Thân hộp quà -->
        <rect x="110" y="90" width="80" height="50" rx="6" fill="url(#boxG)" stroke="#fff" stroke-opacity=".8" stroke-width="1.5"/>
        <path d="M110 115 H190" stroke="#ffd98a" stroke-width="4"/>
        <rect x="105" y="76" width="90" height="18" rx="4" fill="#ff8fbd" stroke="#fff" stroke-opacity=".8" stroke-width="1.5"/>
        <!-- Dải ruy băng nơ trên hộp -->
        <path d="M150 76 V52 C140 42 125 48 135 62 C142 70 150 76 150 76 Z" fill="#ffd98a" stroke="#fff" stroke-opacity=".7" stroke-width="1"/>
        <path d="M150 76 V52 C160 42 175 48 165 62 C158 70 150 76 150 76 Z" fill="#ffd98a" stroke="#fff" stroke-opacity=".7" stroke-width="1"/>
        <circle cx="150" cy="74" r="5" fill="#fff"/>
      </g>
    </svg>
  </div></section>

  <section class="scene" id="sc-free"><div class="sky">
    <svg class="bfly" viewBox="0 0 80 50"><g><ellipse class="bw r" cx="57" cy="19" rx="17" ry="14" fill="#c9b3ff"/><ellipse class="bw l" cx="23" cy="19" rx="17" ry="14" fill="#ffb5da"/><ellipse class="bw r" cx="52" cy="35" rx="11" ry="9" fill="#b49cff"/><ellipse class="bw l" cx="28" cy="35" rx="11" ry="9" fill="#ff9ccb"/><rect x="39" y="10" width="2.2" height="30" rx="1.1" fill="#fff"/></g></svg>
    <svg class="bfly" viewBox="0 0 80 50"><g><ellipse class="bw r" cx="57" cy="19" rx="17" ry="14" fill="#ffe0a6"/><ellipse class="bw l" cx="23" cy="19" rx="17" ry="14" fill="#ffc2dd"/><ellipse class="bw r" cx="52" cy="35" rx="11" ry="9" fill="#ffd085"/><ellipse class="bw l" cx="28" cy="35" rx="11" ry="9" fill="#ffaad0"/><rect x="39" y="10" width="2.2" height="30" rx="1.1" fill="#fff"/></g></svg>
    <svg class="bfly" viewBox="0 0 80 50"><g><ellipse class="bw r" cx="57" cy="19" rx="17" ry="14" fill="#a8e6ff"/><ellipse class="bw l" cx="23" cy="19" rx="17" ry="14" fill="#d9c4ff"/><ellipse class="bw r" cx="52" cy="35" rx="11" ry="9" fill="#8fd6f5"/><ellipse class="bw l" cx="28" cy="35" rx="11" ry="9" fill="#c8afff"/><rect x="39" y="10" width="2.2" height="30" rx="1.1" fill="#fff"/></g></svg>
  </div></section>

  <section class="scene" id="sc-love"><div class="lovering">
    <div class="orbit"><i style="transform:rotate(0deg) translateY(-400%)">♥</i><i style="transform:rotate(45deg) translateY(-400%)">✿</i><i style="transform:rotate(90deg) translateY(-400%)">♥</i><i style="transform:rotate(135deg) translateY(-400%)">✿</i><i style="transform:rotate(180deg) translateY(-400%)">♥</i><i style="transform:rotate(225deg) translateY(-400%)">✿</i><i style="transform:rotate(270deg) translateY(-400%)">♥</i><i style="transform:rotate(315deg) translateY(-400%)">✿</i></div>
    <svg class="bigheart" viewBox="0 0 100 92"><defs><linearGradient id="hg2" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#ffc2dd"/><stop offset="1" stop-color="#ff5f9a"/></linearGradient></defs><path d="M50 88C36 76 4 56 4 30 4 10 28 2 40 14c5 5 8 9 10 14 2-5 5-9 10-14C72 2 96 10 96 30c0 26-32 46-46 58z" fill="url(#hg2)" stroke="#fff" stroke-opacity=".7" stroke-width="1.5"/><path d="M20 24c3-8 12-11 18-7" fill="none" stroke="#fff" stroke-opacity=".75" stroke-width="3" stroke-linecap="round"/></svg>
  </div></section>

  <section class="scene" id="sc-gift"><div class="bouquet"><div class="bq-sway">
    <svg viewBox="0 0 300 340">
      <defs>
        <linearGradient id="wrapG" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#ffd0e6"/><stop offset="1" stop-color="#ff8fbd"/></linearGradient>
        <radialGradient id="pet1" cx=".5" cy=".8"><stop offset="0" stop-color="#ff7fb0"/><stop offset="1" stop-color="#ffe3ef"/></radialGradient>
        <radialGradient id="pet2" cx=".5" cy=".8"><stop offset="0" stop-color="#b79bff"/><stop offset="1" stop-color="#f1eaff"/></radialGradient>
        <radialGradient id="pet3" cx=".5" cy=".8"><stop offset="0" stop-color="#ffc66b"/><stop offset="1" stop-color="#fff4d6"/></radialGradient>
        <g id="flw"><g><ellipse cx="0" cy="-17" rx="8" ry="17"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(45)"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(90)"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(135)"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(180)"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(225)"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(270)"/><ellipse cx="0" cy="-17" rx="8" ry="17" transform="rotate(315)"/></g></g>
      </defs>
      <g fill="none" stroke="#4fc79b" stroke-width="3" stroke-linecap="round">
        <path class="stem" style="--d:.1s" d="M150 300 C150 240 120 190 84 120"/>
        <path class="stem" style="--d:.25s" d="M150 300 C150 230 140 170 150 84"/>
        <path class="stem" style="--d:.4s" d="M150 300 C150 240 180 190 216 118"/>
        <path class="stem" style="--d:.55s" d="M150 300 C145 250 100 220 54 178"/>
        <path class="stem" style="--d:.7s" d="M150 300 C155 250 200 220 246 176"/>
      </g>
      <g stroke="#2e9f78" stroke-width="1.5" fill="#6fe0b4" opacity=".9"><path d="M118 230 q-26 -6 -30 -28 q24 2 30 28z"/><path d="M182 228 q26 -6 30 -28 q-24 2 -30 28z"/><path d="M140 200 q-14 -20 -4 -38 q14 16 4 38z"/></g>
      <g transform="translate(54 168) scale(.8)" fill="url(#pet2)" stroke="#fff" stroke-opacity=".7" stroke-width="1"><use class="fl" style="--d:.9s" href="#flw"/></g>
      <g transform="translate(246 166) scale(.8)" fill="url(#pet3)" stroke="#fff" stroke-opacity=".7" stroke-width="1"><use class="fl" style="--d:1.1s" href="#flw"/></g>
      <g transform="translate(84 110)" fill="url(#pet1)" stroke="#fff" stroke-opacity=".7" stroke-width="1"><use class="fl" style="--d:.7s" href="#flw"/></g><g transform="translate(216 108)" fill="url(#pet1)" stroke="#fff" stroke-opacity=".7" stroke-width="1"><use class="fl" style="--d:.85s" href="#flw"/></g>
      <g transform="translate(150 74) scale(1.25)" fill="url(#pet1)" stroke="#fff" stroke-opacity=".8" stroke-width="1"><use class="fl" style="--d:.5s" href="#flw"/></g>
      <g transform="translate(150 74)"><circle class="fl" style="--d:.6s" r="9" fill="#ffe28a"/></g>
      <path d="M72 224 L228 224 L166 324 Q150 336 134 324Z" fill="url(#wrapG)" stroke="#fff" stroke-opacity=".7" stroke-width="1.5"/>
      <path d="M72 224 Q150 250 228 224" fill="none" stroke="#fff" stroke-opacity=".65" stroke-width="2"/>
      <path d="M110 236 L142 326 M190 236 L158 326" stroke="#fff" stroke-opacity=".35" stroke-width="1.5" fill="none"/>
      <path d="M150 258 q-30 -26 -40 -4 q10 20 40 4 q30 16 40 -4 q-10 -22 -40 4z" fill="#fff" opacity=".95"/><circle cx="150" cy="258" r="6" fill="#ffc2dd"/>
      <path d="M146 262 q-10 26 -22 40 M154 262 q10 26 22 40" stroke="#fff" stroke-width="3.5" stroke-linecap="round" fill="none" opacity=".9"/>
      </svg>
  </div></div></section>

  <section class="scene" id="sc-question"><div class="qbtns rv" id="q1">
    <button data-a="yes">rồi nè ✿</button><button data-a="no">chưa nữa…</button>
  </div></section>

  <section class="scene" id="sc-final"><div class="final">
    <div class="f-sub">chúc mừng ngày</div>
    <h1>Phụ nữ Việt Nam</h1>
    <div class="f-date">20 · 10</div>
    <p class="f-to" id="f-to">gửi người phụ nữ tuyệt vời</p>
    <p class="f-msg">mong mỗi ngày của cậu đều có hoa, có nắng, có tiếng cười — và có người nhớ đến cậu thật nhiều.</p>
    <div style="margin-top: 10px; padding: 8px 12px; background: rgba(255,122,184,0.08); border-left: 2px solid var(--pink); border-radius: 4px; text-align: left;">
      <p style="font-size: clamp(11px, 3vw, 13.5px); line-height: 1.4; color: #ffd9ec; font-style: italic;">“Hãy trang điểm con người bề trong thầm kín bằng vẻ đẹp không phai tàn của tinh thần dịu dàng, yên lặng; đó là điều quý giá trước mặt Đức Chúa Trời.”</p>
      <p style="font-size: clamp(10px, 2.5vw, 12px); color: var(--gold); text-align: right; margin-top: 4px;">— 1 Phi-e-rơ 3:4 —</p>
    </div>

    <div class="f-act">
      <button id="b-link" class="alt" hidden>chép link</button>
      <button id="b-replay" class="alt">xem lại</button>
    </div>
  </div></section>

  <!-- ===== Nụ — nhân vật gốc ===== -->
  <div id="nu" class="wave" aria-hidden="true">
    <div class="nu-glow"></div>
    <svg class="nu-svg" viewBox="0 0 240 300"><defs><radialGradient id="eyeG" cx=".5" cy=".35" r=".75"><stop offset="0" stop-color="#fff"/><stop offset=".5" stop-color="#ffd3e8"/><stop offset="1" stop-color="#ff7ab8"/></radialGradient></defs>
<g class="head"><g class="head-tilt">
<path class="nbud" d="M120 44C62 92 54 152 68 204c10 34 94 34 104 0 14-52 6-112-52-160z" fill="rgba(255,122,184,.07)" stroke="#ff7ab8" stroke-width="3" stroke-linejoin="round"/>
<path d="M120 44C119 30 114 20 106 12M120 44c2-14 10-22 20-26" fill="none" stroke="#7dffd0" stroke-width="3" stroke-linecap="round"/>
<g class="arm-l"><path d="M70 214C50 218 38 206 36 190c18-2 32 6 34 24z" fill="rgba(125,255,208,.2)" stroke="#7dffd0" stroke-width="2.5" stroke-linejoin="round"/></g>
<g class="arm-r"><path d="M170 214c20 4 32-8 34-24-18-2-32 6-34 24z" fill="rgba(125,255,208,.2)" stroke="#7dffd0" stroke-width="2.5" stroke-linejoin="round"/></g>
<ellipse class="blush" cx="78" cy="186" rx="11" ry="5.5" fill="#ff7ab8"/><ellipse class="blush" cx="162" cy="186" rx="11" ry="5.5" fill="#ff7ab8"/>
<g class="eye eyeL" style="transform-origin:96px 152px"><rect x="82" y="128" width="28" height="48" rx="14" fill="url(#eyeG)"/><ellipse cx="91" cy="142" rx="4" ry="6" fill="#fff"/></g>
<g class="eye eyeR" style="transform-origin:144px 152px"><rect x="130" y="128" width="28" height="48" rx="14" fill="url(#eyeG)"/><ellipse cx="139" cy="142" rx="4" ry="6" fill="#fff"/></g>
<path class="arcL" d="M80 162Q96 138 112 162" stroke="#ffd3e8" stroke-width="6" fill="none" stroke-linecap="round"/><path class="arcR" d="M128 162Q144 138 160 162" stroke="#ffd3e8" stroke-width="6" fill="none" stroke-linecap="round"/>
<path class="mouth-c" d="M110 196Q120 206 130 196" stroke="#ffd3e8" stroke-width="3.5" fill="none" stroke-linecap="round"/><ellipse class="mouth-o" cx="120" cy="199" rx="7" ry="7" fill="#ffd3e8"/>
<g class="wink-star" fill="#ffd98a"><path transform="translate(10 52)" d="M170 100l2.5 6 6 2.5-6 2.5-2.5 6-2.5-6-6-2.5 6-2.5z"/></g>
</g></g></svg>
  </div>

  <div id="bubble" class="empty"><div id="line"></div></div>
  <div id="hint">chạm để qua</div>
</div>

<div id="start">
  <svg class="bud" viewBox="0 0 120 150"><defs><linearGradient id="bg1" x1="0" y1="1" x2="0" y2="0"><stop offset="0" stop-color="#ff8fbd"/><stop offset="1" stop-color="#fff0f7"/></linearGradient></defs>
    <path d="M60 140 C60 110 58 96 60 80" stroke="#6fe0b4" stroke-width="4" fill="none" stroke-linecap="round"/><path d="M60 118 q-26 -4 -30 -26 q26 2 30 26z" fill="#6fe0b4" opacity=".9"/>
    <path d="M60 86 C34 78 28 44 60 14 C92 44 86 78 60 86Z" fill="url(#bg1)" stroke="#fff" stroke-opacity=".8"/><path d="M60 86 C42 80 40 52 60 30 C80 52 78 80 60 86Z" fill="#ffc2dd" opacity=".7"/></svg>
  <h2>Có một món quà nhỏ<br>cho ngày 20/10</h2>
  <p>chạm để mở quà</p>
  <small>bật âm thanh để nghe trọn vẹn nhé</small>
</div>
<script>
(()=>{
'use strict';
const $=(s,r=document)=>r.querySelector(s), $$=(s,r=document)=>[...r.querySelectorAll(s)];
const BAR=1950;                       // thời lượng đọc gốc (ms) của 1 "bar" kịch bản
const BPM=76.5, BEAT=60000/BPM, OFF=450;   // Từng Ngày Yêu Em: nhịp & độ lệch pha (ms)
function snap(ms){ const U=BEAT*2; let d=Math.max(1,Math.round(ms/U))*U;
  if(!bgm.paused){ const t=bgm.currentTime*1000-OFF; d=Math.max(U*.75,Math.round((t+d)/U)*U-t); }
  return d; }
const YRS=new Date().getFullYear()-1930;
const qp=new URLSearchParams(location.search);
const TO=(qp.get('to')||'').trim().slice(0,40), FROM=(qp.get('from')||'').trim().slice(0,40);
const esc=s=>s.replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));

/* ================= KỊCH BẢN ================= */
const S=[
 {say:TO?'này <em>'+esc(TO)+'</em> ơi!':'này cậu ơi!', bars:1.1, mood:'wave', mode:'hero', bg:0, fx:{meteor:1}},
 {say:'tớ là <em>Nụ</em> — nàng tiên nhỏ của vườn hoa', bars:1.7, mood:'talk'},
 {say:'hôm nay tớ được giao một nhiệm vụ đặc biệt lắm đó…', bars:1.7, mood:'shy'},
 {say:'vì hôm nay là…', bars:1, mood:'talk'},
 {scene:'date', mode:'side', say:'<em>20/10</em> rồi!', bars:1.7, mood:'happy', bg:2, fx:{petals:.7,meteor:1}},

 {scene:'history', say:'ngày 20/10/1930, Hội Phụ nữ phản đế Việt Nam ra đời', bars:2, mood:'talk', reveal:['h1','h2']},
 {say:'đã <em>'+YRS+'</em> năm trôi qua, và 20/10 thành ngày cả nước dành để tri ân phụ nữ', bars:2.3, mood:'talk', reveal:['h3','h4'], on(){countTo($('#yrs'),YRS,2200)}},

 {scene:'heroes', say:'trong câu chuyện đất nước, có biết bao người phụ nữ phi thường…', bars:2, mood:'talk', bg:0, fx:{meteor:1.6}, reveal:['n1','l1','n2','l2','e12']},
 {say:'từ Hai Bà Trưng, Bà Triệu thuở dựng nước, đến những người con gái kiên cường của thế kỷ XX', bars:2.4, mood:'talk', reveal:['n3','l3','e23','n4','l4','e24','n5','l5','e35','e45']},
 {say:'và còn những người không có tên trong sách: bà, mẹ, chị, cô giáo… và cả <em>cậu</em> nữa', bars:2.4, mood:'happy', reveal:['n6','l6','e46','e56'], fx:{meteor:2.2,petals:.3}},

 {scene:'unseen', say:'có những điều mà <em>cậu</em> vẫn lặng lẽ làm mỗi ngày…', bars:2, mood:'talk', bg:2, fx:{petals:.2}},
 {say:'', bars:1.15, reveal:['c1']},
 {say:'', bars:1.15, reveal:['c2']},
 {say:'', bars:1.15, reveal:['c3']},
 {say:'', bars:1.4, reveal:['c4']},
 {say:'mà hiếm khi có ai nói lời cảm ơn', bars:1.8, mood:'shy'},
 {scene:'none', mode:'hero', say:'nên hôm nay, đến lượt <em>cậu</em> được quan tâm', bars:2, mood:'happy', fx:{petals:1.1}},

 {say:'tớ xin gửi cậu bốn lời chúc nhé', bars:1.5, mood:'wave', bg:2},
 {scene:'health', mode:'side', say:'chúc cậu thật nhiều <em>sức khỏe</em> — để có thể đi hết những nơi cậu muốn đến', bars:2.4, mood:'talk', bg:1, fx:{meteor:.6}},
 {scene:'peace', say:'chúc cậu <em>luôn ngập tràn ơn phước </em>và <em>niềm vui</em> trên mỗi bước đường đi cùng Ngài ', bars:2.2, mood:'talk', bg:1},
 {scene:'free', say:'chúc cậu đủ <em>tự do</em> để làm điều mình thích, và đủ dũng cảm để theo đuổi nó', bars:2.5, mood:'talk', bg:0, fx:{lantern:1,meteor:.8}},
 {scene:'love', say:'chúc cậu luôn được <em>yêu thương</em> — đúng cách, đúng người, và cả bởi chính cậu', bars:2.5, mood:'happy', bg:2, fx:{hearts:1,petals:.3}},

 {scene:'none', mode:'hero', say:'cậu không cần phải hoàn hảo đâu', bars:1.6, mood:'talk', fx:{petals:.8}},
 {say:'cậu đẹp ở cách cậu cố gắng, cách cậu cười, và cách cậu thương người khác', bars:2.4, mood:'shy'},

 {scene:'gift', mode:'side', say:'tớ tặng cậu bó hoa này nè', bars:1.8, mood:'happy', bg:3, fx:{petals:1,meadow:1.1}},
 {say:'một loài hoa không bao giờ héo — vì mỗi cánh là một lời yêu thương', bars:2.4, mood:'talk'},

 {scene:'question', mode:'hero', say:'cho tớ hỏi một câu thôi nhé…<br>hôm nay cậu đã <em>khen bản thân</em> chưa?', bars:2, mood:'wink', bg:2, fx:{petals:.3,meteor:1}, wait:true, reveal:['q1']},
 {scene:'final', mode:'side', say:'', mood:'happy', bg:3, fx:{fire:1,petals:.9,meadow:1.5}, wait:true, final:true}
];

/* ================= TRẠNG THÁI ================= */
const nu=$('#nu'), bgls=$$('.bgl'), line=$('#line'), bubble=$('#bubble'), hint=$('#hint'), prog=$('#prog');
let idx=-1, timer=null, started=false, curScene=null, waiting=false, lock=0, talkT=null;
let fxS={petals:0,hearts:0,lantern:0,fire:0,meteor:1,meadow:.6};

function mood(m){ nu.className=(m||''); }
function talk(on){ clearTimeout(talkT); nu.classList.toggle('talk',on); if(on) talkT=setTimeout(()=>nu.classList.remove('talk'),1500); }

function say(html){
  bubble.classList.toggle('empty',!html);
  line.innerHTML=html||'';
  let k=0;
  (function walk(n){
    [...n.childNodes].forEach(c=>{
      if(c.nodeType===3){
        const f=document.createDocumentFragment();
        c.textContent.split(/(\s+)/).forEach(p=>{
          if(!p) return;
          if(!p.trim()){ f.append(p); return; }
          const s=document.createElement('span'); s.className='w'; s.textContent=p; s.style.animationDelay=(k++*65)+'ms'; f.append(s);
        });
        c.replaceWith(f);
      } else if(c.nodeType===1 && c.tagName!=='BR') walk(c);
    });
  })(line);
}

function showScene(name){
  if(name===undefined) return;
  const next = name==='none' ? null : $('#sc-'+name);
  if(next===curScene) return;
  if(curScene){ curScene.classList.remove('on'); }
  const old=curScene; curScene=next;
  if(old) setTimeout(()=>{ if(old!==curScene) $$('.rv.on,.node.on,.edge.on,.lbl.on',old).forEach(e=>e.classList.remove('on')); },800);
  if(next) setTimeout(()=>{ if(curScene===next) next.classList.add('on'); }, old?420:60);
}

function countTo(el,to,ms){
  const t0=performance.now();
  (function f(t){ const k=Math.min(1,(t-t0)/ms); el.textContent=Math.round(to*(1-Math.pow(1-k,3))); if(k<1) requestAnimationFrame(f); })(t0);
}

function go(n){
  clearTimeout(timer);
  if(n>=S.length) return;
  idx=n; const st=S[n]; document.body.classList.toggle('bloom',!!st.final);
  if(st.mode){ document.body.classList.toggle('m-side',st.mode==='side'); document.body.classList.toggle('m-hero',st.mode==='hero'); }
  if(st.bg!==undefined) bgls.forEach((e,k)=>e.classList.toggle('on',k===st.bg));
  if(st.fx){ fxS=Object.assign({petals:0,hearts:0,lantern:0,fire:0,meteor:1,meadow:.6},st.fx); parts.forEach(p=>{ if((p.t==='lantern'&&!fxS.lantern)||(p.t==='heart'&&!fxS.hearts)) p.kill=true; }); }
  showScene(st.scene);
  if(st.mood!==undefined){ const talking=nu.classList.contains('talk'); mood(st.mood); if(talking) nu.classList.add('talk'); }
  say(st.say);
  talk(!!st.say);
  if(st.reveal) st.reveal.forEach((id,j)=>setTimeout(()=>{const e=document.getElementById(id); if(e) e.classList.add('on');}, (st.scene?650:0)+j*260));
  if(st.on) st.on();
  prog.style.width=((n+1)/S.length*100)+'%';
  hint.classList.toggle('on', n>=1 && n<=4);
  waiting=!!st.wait;
  if(!st.wait && !qp.has('hold')) timer=setTimeout(()=>go(n+1),snap((st.bars||1.5)*BAR));
  if(st.final) setupFinal();
}

function next(){ const now=Date.now(); if(now-lock<220) return; lock=now; if(!waiting && idx<S.length-1) go(idx+1); }

/* ================= TƯƠNG TÁC ================= */
document.addEventListener('click',e=>{
  if(!started) return;
  if(e.target.closest('.ui,button,input,a,.final')) return;
  next();
});
document.addEventListener('keydown',e=>{ if(started&&(e.key===' '||e.key==='ArrowRight')&&e.target.tagName!=='INPUT'){e.preventDefault();next();} });

$('#q1').addEventListener('click',e=>{
  const b=e.target.closest('button'); if(!b||!waiting) return;
  waiting=false; $('#q1').classList.remove('on');
  mood('happy'); talk(true);
  if(b.dataset.a==='yes'){
    say('giỏi quá! cứ khen thật nhiều vào nhé — cậu xứng đáng mà');
  } else {
    say('vậy để tớ khen giúp: cậu <em>mạnh mẽ</em> hơn cậu nghĩ, <em>dịu dàng</em> hơn cậu tưởng, và quan trọng hơn cậu vẫn nghĩ rất nhiều');
  }
  clearTimeout(timer); timer=setTimeout(()=>go(idx+1), snap(4.4*BAR));
});

function setupFinal(){
  const to=TO||'';
  $('#f-to').textContent = to ? 'gửi '+to+(FROM?' · từ '+FROM:'') : 'gửi người phụ nữ tuyệt vời'+(FROM?' · từ '+FROM:'');
  if(location.protocol.startsWith('http')) $('#b-link').hidden=false;
}
$('#b-link').addEventListener('click',()=>{
  const v=TO;
  const u=new URL(location.href); u.search=''; if(v) u.searchParams.set('to',v);
  (navigator.clipboard?navigator.clipboard.writeText(u.toString()):Promise.reject()).then(()=>{$('#b-link').textContent='đã chép ✓';setTimeout(()=>$('#b-link').textContent='chép link',1800);}).catch(()=>prompt('Sao chép liên kết:',u.toString()));
});
$('#b-replay').addEventListener('click',()=>{
  $$('.rv.on,.node.on,.edge.on,.lbl.on').forEach(e=>e.classList.remove('on'));
  if(curScene){curScene.classList.remove('on'); curScene=null;}
  setTimeout(()=>go(0),300);
});

/* ================= ÂM THANH ================= */
const bgm=$('#bgm'); let actx=null, an=null, fd=null, avg=0, dpeak=.02;
function setupAudio(){
  try{
    const AC=window.AudioContext||window.webkitAudioContext; actx=new AC();
    const src=actx.createMediaElementSource(bgm); an=actx.createAnalyser(); an.fftSize=256; an.smoothingTimeConstant=.55;
    src.connect(an); an.connect(actx.destination); fd=new Uint8Array(an.frequencyBinCount);
    if(actx.state==='suspended') actx.resume();
  }catch(err){ an=null; }
}
$('#mute').addEventListener('click',()=>{ bgm.muted=!bgm.muted; $('#mute').classList.toggle('muted',bgm.muted); });

$('#start').addEventListener('click',()=>{
  if(started) return; started=true;
  $('#start').classList.add('gone');
  setupAudio(); bgm.volume=.9; const pr=bgm.play(); if(pr&&pr.catch) pr.catch(()=>{});
  setTimeout(()=>go(0),500);
});

/* ================= HIỆU ỨNG NỀN (canvas) ================= */
const cv=$('#fx'), ctx=cv.getContext('2d');
let W=0,H=0,DPR=1, stars=[], parts=[], pulse=0, lastP=-1, acc={p:0,h:0,l:0,f:0,m:0};

function spr(w,h,fn){ const c=document.createElement('canvas'); c.width=w; c.height=h; fn(c.getContext('2d'),w,h); return c; }
function petalSpr(c1,c2){ return spr(40,56,(g,w,h)=>{ const gr=g.createLinearGradient(0,h,0,0); gr.addColorStop(0,c1); gr.addColorStop(1,c2);
  g.fillStyle=gr; g.beginPath(); g.moveTo(w/2,h*.96); g.bezierCurveTo(-w*.25,h*.62,w*.08,h*.02,w/2,0); g.bezierCurveTo(w*.92,h*.02,w*1.25,h*.62,w/2,h*.96); g.fill(); }); }
const SP={ petal:[petalSpr('#ff7ab8','#ffe3f0'),petalSpr('#ffb347','#fff0c4'),petalSpr('#9b6bff','#eadfff')],
  heart:spr(48,44,(g,w,h)=>{ const gr=g.createLinearGradient(0,0,0,h); gr.addColorStop(0,'#ffc2dd'); gr.addColorStop(1,'#ff5f9a'); g.fillStyle=gr;
    g.beginPath(); g.moveTo(w/2,h*.95); g.bezierCurveTo(-w*.2,h*.55,w*.12,-h*.1,w/2,h*.28); g.bezierCurveTo(w*.88,-h*.1,w*1.2,h*.55,w/2,h*.95); g.fill(); }),
  lantern:spr(64,84,(g,w,h)=>{ const r=g.createRadialGradient(w/2,h*.5,2,w/2,h*.5,w/2); r.addColorStop(0,'rgba(255,200,120,.7)'); r.addColorStop(1,'rgba(255,160,90,0)'); g.fillStyle=r; g.fillRect(0,0,w,h);
    const gr=g.createLinearGradient(0,h*.25,0,h*.75); gr.addColorStop(0,'#fff0b8'); gr.addColorStop(1,'#ff9a58'); g.fillStyle=gr;
    g.beginPath(); g.moveTo(w*.34,h*.24); g.quadraticCurveTo(w*.14,h*.5,w*.3,h*.74); g.lineTo(w*.7,h*.74); g.quadraticCurveTo(w*.86,h*.5,w*.66,h*.24); g.closePath(); g.fill();
    g.fillStyle='#ffd9a0'; g.fillRect(w*.32,h*.2,w*.36,h*.05); g.fillStyle='#e07a3c'; g.fillRect(w*.32,h*.74,w*.36,h*.04);
    g.strokeStyle='rgba(180,70,20,.35)'; g.lineWidth=1; g.beginPath(); g.moveTo(w*.5,h*.25); g.lineTo(w*.5,h*.74); g.stroke(); }) };

function resize(){
  DPR=Math.min(devicePixelRatio||1,1.5); W=innerWidth; H=innerHeight;
  cv.width=W*DPR; cv.height=H*DPR; ctx.setTransform(DPR,0,0,DPR,0,0);
  const n=Math.min(230,Math.round(W*H/6500)); stars=[];
  for(let i=0;i<n;i++) stars.push({x:Math.random()*W,y:Math.random()*H,r:Math.random()*1.5+.4,t:Math.random()*6.28,s:.6+Math.random()*1.6,h:Math.random()<.2?330:Math.random()<.4?210:45});
}
addEventListener('resize',resize); resize();
let mdw=.6; const BL=[];
function blades(){ BL.length=0; const n=Math.round(W/5);
  for(let i=0;i<n;i++) BL.push({x:i/n*W+Math.random()*4, h:(.04+Math.random()*.08)*H*(.55+.9*Math.pow(Math.sin(i/n*9+1),2)), ph:Math.random()*6.28, w:1+Math.random()*1.2, hue:[160,175,190,95,55,320][(Math.random()*6)|0]}); }
blades(); addEventListener('resize',blades);

function spawn(type){
  const R=Math.random;
  if(type==='petal') parts.push({t:'petal',x:R()*W,y:-30,vx:-10+R()*30,vy:40+R()*55,r:R()*6.28,vr:(R()-.5)*3,s:.35+R()*.45,ph:R()*6.28,sp:SP.petal[(R()*3)|0],a:1});
  else if(type==='heart') parts.push({t:'heart',x:R()*W,y:H+20,vx:(R()-.5)*30,vy:-(50+R()*60),r:0,vr:0,s:.25+R()*.45,ph:R()*6.28,sp:SP.heart,a:.9});
  else if(type==='lantern') parts.push({t:'lantern',x:R()*W,y:H+50,vx:(R()-.5)*14,vy:-(24+R()*28),r:0,vr:0,s:.5+R()*.7,ph:R()*6.28,sp:SP.lantern,a:.95});
  else if(type==='meteor'){ const x=W*(.3+R()*.7), y=R()*H*.35; parts.push({t:'meteor',x,y,vx:-(380+R()*220),vy:150+R()*100,life:1}); }
  else if(type==='fire'){ const cx=W*(.15+R()*.7), cy=H*(.12+R()*.4), hue=[330,45,280,200][(R()*4)|0], n=34;
    for(let i=0;i<n;i++){ const a=i/n*6.283+R()*.2, v=90+R()*120; parts.push({t:'spark',x:cx,y:cy,vx:Math.cos(a)*v,vy:Math.sin(a)*v,life:1,hue}); } }
}

let lastT=performance.now();
function frame(now){
  const dt=Math.min(.05,(now-lastT)/1000); lastT=now;
  /* nhịp bass → pulse */
  let target=0;
  if(an&&fd&&!bgm.paused){ an.getByteFrequencyData(fd); const lvl=(fd[0]+fd[1]+fd[2]+fd[3])/(4*255); avg+=(lvl-avg)*Math.min(1,dt*3.2); const d=lvl-avg; dpeak=Math.max(dpeak*Math.pow(.6,dt),d,.02); target=Math.min(1,Math.max(0,d/dpeak)); target*=target; }
  else if(started){ { const bp=BEAT/1000; target=Math.max(0,1-(((now/1000)%bp)/bp)*3); } }
  if(!bgm.paused){ const ph=(((bgm.currentTime*1000-OFF)%BEAT)+BEAT)%BEAT/BEAT; target=Math.max(target,Math.pow(Math.max(0,1-ph*2.4),2)*.65); }
  pulse=Math.max(pulse*Math.pow(.02,dt),target); if(pulse>1) pulse=1;
  if(Math.abs(pulse-lastP)>.03){ lastP=pulse; document.documentElement.style.setProperty('--p',pulse.toFixed(2)); }

  ctx.clearRect(0,0,W,H);
  /* sao */
  for(const s of stars){ s.t+=dt*s.s; const a=.35+.45*Math.abs(Math.sin(s.t))+pulse*.25; ctx.globalAlpha=Math.min(1,a); ctx.fillStyle='hsl('+s.h+',90%,88%)'; ctx.beginPath(); ctx.arc(s.x,s.y,s.r*(1+pulse*.35),0,6.283); ctx.fill(); }
  ctx.globalAlpha=1;
  /* đồng cỏ neon */
  mdw+=(fxS.meadow-mdw)*Math.min(1,dt*1.6);
  ctx.globalCompositeOperation='lighter'; ctx.lineCap='round'; const tm=now/1000;
  for(const b of BL){ const sw=Math.sin(tm*1.2+b.ph+b.x*.004)*(5+b.h*.12)+Math.sin(tm*.5+b.x*.01)*4, h=b.h*mdw;
    ctx.strokeStyle='hsla('+b.hue+',95%,60%,'+(.5+pulse*.35)+')'; ctx.lineWidth=b.w;
    ctx.beginPath(); ctx.moveTo(b.x,H); ctx.quadraticCurveTo(b.x+sw*.3,H-h*.6,b.x+sw,H-h); ctx.stroke(); }
  ctx.globalCompositeOperation='source-over';
  /* sinh hạt */
  acc.p+=dt*fxS.petals*7; while(acc.p>=1){acc.p--; spawn('petal');}
  acc.h+=dt*fxS.hearts*4; while(acc.h>=1){acc.h--; spawn('heart');}
  acc.l+=dt*fxS.lantern*1.5; while(acc.l>=1){acc.l--; spawn('lantern');}
  acc.f+=dt*fxS.fire*1.1; while(acc.f>=1){acc.f--; spawn('fire');}
  acc.m+=dt*fxS.meteor*.22; while(acc.m>=1){acc.m--; spawn('meteor');}
  if(parts.length>420) parts.splice(0,parts.length-420);
  /* vẽ hạt */
  for(let i=parts.length-1;i>=0;i--){
    const p=parts[i];
    if(p.t==='meteor'){ p.x+=p.vx*dt; p.y+=p.vy*dt; p.life-=dt*1.1; if(p.life<=0){parts.splice(i,1);continue;}
      const g=ctx.createLinearGradient(p.x,p.y,p.x-p.vx*.16,p.y-p.vy*.16); g.addColorStop(0,'rgba(255,255,255,'+p.life+')'); g.addColorStop(1,'rgba(255,255,255,0)');
      ctx.strokeStyle=g; ctx.lineWidth=2; ctx.beginPath(); ctx.moveTo(p.x,p.y); ctx.lineTo(p.x-p.vx*.16,p.y-p.vy*.16); ctx.stroke(); continue; }
    if(p.t==='spark'){ p.vy+=90*dt; p.x+=p.vx*dt; p.y+=p.vy*dt; p.vx*=.985; p.life-=dt*.75; if(p.life<=0){parts.splice(i,1);continue;}
      ctx.globalCompositeOperation='lighter'; ctx.globalAlpha=Math.max(0,p.life); ctx.fillStyle='hsl('+p.hue+',100%,70%)'; ctx.beginPath(); ctx.arc(p.x,p.y,2.2,0,6.283); ctx.fill(); ctx.globalCompositeOperation='source-over'; ctx.globalAlpha=1; continue; }
    if(p.kill){ p.a-=dt*.9; if(p.a<=0){parts.splice(i,1);continue;} }
    p.ph+=dt*2; p.x+=(p.vx+Math.sin(p.ph)*22)*dt; p.y+=p.vy*dt; p.r+=p.vr*dt;
    if(p.y>H+60||p.y<-90){parts.splice(i,1);continue;}
    const sc=p.s*(1+(p.t==='heart'?pulse*.12:0)), w=p.sp.width*sc, h=p.sp.height*sc;
    ctx.save(); ctx.globalAlpha=p.a; ctx.translate(p.x,p.y); ctx.rotate(p.r);
    if(p.t==='petal') ctx.scale(Math.abs(Math.cos(p.ph))*.7+.3,1);
    ctx.drawImage(p.sp,-w/2,-h/2,w,h); ctx.restore();
  }
  requestAnimationFrame(frame);
}
requestAnimationFrame(frame);

if(qp.has('debug')) window.__go=go;
document.addEventListener('visibilitychange',()=>{ if(started&&!document.hidden&&bgm.paused&&!bgm.muted) bgm.play().catch(()=>{}); });
})();
</script>
<script>
/* ===== PATCH: hiệu ứng chạm + nút dễ ấn ===== */
(function(){
  const reduce=matchMedia('(prefers-reduced-motion:reduce)').matches;
  const G=['✿','♡','✦','❀','✧','♥','✺'], C=['#ff7ab8','#ffd98a','#a99bff','#7dffd0','#ffffff','#ff9ec7'];
  const rnd=(a,b)=>a+Math.random()*(b-a), pick=a=>a[(Math.random()*a.length)|0];

  function burst(x,y,n,spread){
    if(reduce) return;
    for(let i=0;i<n;i++){
      const s=document.createElement('span'); s.className='fxp'; s.textContent=pick(G);
      s.style.left=x+'px'; s.style.top=y+'px'; s.style.color=pick(C); s.style.fontSize=rnd(11,26)+'px';
      document.body.appendChild(s);
      const a=rnd(0,Math.PI*2), d=rnd(spread*.35,spread), dx=Math.cos(a)*d, dy=Math.sin(a)*d-rnd(10,40), rot=rnd(-200,200);
      const an=s.animate([
        {transform:'translate(-50%,-50%) scale(.2) rotate(0deg)',opacity:1},
        {transform:`translate(calc(-50% + ${dx}px),calc(-50% + ${dy}px)) scale(1) rotate(${rot*.6}deg)`,opacity:1,offset:.55},
        {transform:`translate(calc(-50% + ${dx*1.1}px),calc(-50% + ${dy+60}px)) scale(.3) rotate(${rot}deg)`,opacity:0}
      ],{duration:rnd(800,1400),easing:'cubic-bezier(.2,.8,.3,1)'});
      an.onfinish=()=>s.remove();
    }
  }
  function ring(x,y){
    if(reduce) return;
    const r=document.createElement('div'); r.className='tapring'; r.style.left=x+'px'; r.style.top=y+'px';
    document.body.appendChild(r); setTimeout(()=>r.remove(),750);
  }
  function ripple(btn,e){
    const b=btn.getBoundingClientRect(), s=Math.max(b.width,b.height)*2.4;
    const r=document.createElement('span'); r.className='rip';
    r.style.cssText=`left:${e.clientX-b.left}px;top:${e.clientY-b.top}px;width:${s}px;height:${s}px`;
    btn.appendChild(r); setTimeout(()=>r.remove(),700);
  }
  function vibrate(ms){ try{ navigator.vibrate&&navigator.vibrate(ms); }catch(_){} }

  const startEl=document.getElementById('start');
  const isStarted=()=>startEl.classList.contains('gone');

  /* pointerdown: phản hồi NGAY khi chạm (không chờ nhả tay) */
  document.addEventListener('pointerdown',e=>{
    const btn=e.target.closest&&e.target.closest('button');
    if(btn){
      ripple(btn,e);
      const b=btn.getBoundingClientRect();
      burst(b.left+b.width/2,b.top+b.height/2,btn.closest('.qbtns')?22:12,btn.closest('.qbtns')?130:80);
      ring(e.clientX,e.clientY); vibrate(14);
      return;
    }
    if(e.target.closest&&e.target.closest('input')) return;
    if(!isStarted()){ burst(e.clientX,e.clientY,26,170); ring(e.clientX,e.clientY); vibrate(20); return; }
    burst(e.clientX,e.clientY,6,60); ring(e.clientX,e.clientY);
  },{passive:true});

  /* Space/Enter trên nút phải bấm được nút, không bị nhảy cảnh */
  document.addEventListener('keydown',e=>{
    if(e.target&&e.target.tagName==='BUTTON'&&(e.key===' '||e.key==='Enter')) e.stopPropagation();
  },true);

  /* nút "yes/no": nổ pháo hoa nhỏ ở giữa màn khi chọn xong */
  const q1=document.getElementById('q1');
  if(q1) q1.addEventListener('click',e=>{
    if(!e.target.closest('button')) return;
    const w=innerWidth,h=innerHeight;
    setTimeout(()=>burst(w/2,h*.4,34,Math.min(w,h)*.45),120);
    vibrate([18,40,18]);
  });

  /* thẻ kết: mưa tim nhẹ khi hiện ra */
  const fin=document.getElementById('sc-final');
  if(fin) new MutationObserver(()=>{
    if(fin.classList.contains('on')){
      let k=0; const t=setInterval(()=>{ burst(rnd(innerWidth*.15,innerWidth*.85),rnd(innerHeight*.15,innerHeight*.45),5,90); if(++k>6) clearInterval(t); },320);
    }
  }).observe(fin,{attributes:true,attributeFilter:['class']});
})();
</script>
<script>
/* ===== WOW PATCH 2: canvas fx (pháo hoa tim, trail, shockwave, confetti) ===== */
(function(){
  const reduce=matchMedia('(prefers-reduced-motion:reduce)').matches;
  const $=s=>document.querySelector(s);
  const rnd=(a,b)=>a+Math.random()*(b-a), pick=a=>a[(Math.random()*a.length)|0];
  const HUES=[335,345,45,265,160,320];

  /* --- cực quang + vòng sóng ở màn mở quà (CSS thuần, chạy cả khi reduce) --- */
  const au=document.createElement('div'); au.id='aurora'; au.innerHTML='<i></i><i></i><i></i>';
  const bgs=$('#bgs'); bgs.parentNode.insertBefore(au,bgs.nextSibling);
  const start=$('#start'), bud=start.querySelector('.bud');
  if(bud){
    const wrap=document.createElement('div'); wrap.className='budwrap';
    bud.replaceWith(wrap);
    wrap.innerHTML='<span class="sring"></span><span class="sring"></span><span class="sring"></span>';
    wrap.appendChild(bud);
  }
  if(reduce) return;

  /* --- phần tử overlay --- */
  const mk=(tag,id)=>{const e=document.createElement(tag); e.id=id; document.body.appendChild(e); return e;};
  const cv=mk('canvas','fx2'), flashEl=mk('div','flash'), sweepEl=mk('div','sweep'), cglow=mk('div','cglow');
  const g=cv.getContext('2d');
  let W=0,H=0,D=1;
  function rs(){ D=Math.min(devicePixelRatio||1,2); W=innerWidth; H=innerHeight; cv.width=W*D; cv.height=H*D; g.setTransform(D,0,0,D,0,0); }
  rs(); addEventListener('resize',rs);

  const P=[], R=[], RING=[], CF=[];
  const MAXP=1600;

  function spark(x,y,vx,vy,h,life,s,grav,drag,tw){
    if(P.length>MAXP) return;
    P.push({x,y,px:x,py:y,vx,vy,h,l:life,m:life,s,g:grav,d:drag,tw:!!tw});
  }
  function ring(x,y,h,max){ RING.push({x,y,r:6,max:max||Math.min(W,H)*.55,h:h==null?335:h,a:1}); }
  function confetti(x,y,n,rain){
    for(let i=0;i<n;i++){
      CF.push({x:rain?rnd(0,W):x+rnd(-20,20), y:rain?rnd(-H*.3,-10):y,
        vx:rain?rnd(-1,1):rnd(-7,7), vy:rain?rnd(1.5,4):-rnd(6,15),
        r:rnd(0,6.28), vr:rnd(-.25,.25), w:rnd(5,10), h:rnd(8,16), c:`hsl(${pick(HUES)+rnd(-10,10)},100%,${rnd(60,80)}%)`, ph:rnd(0,6.28), l:rnd(260,420)});
    }
  }
  function flash(a){ flashEl.animate([{opacity:a},{opacity:0}],{duration:900,easing:'ease-out'}); }
  function sweep(){ sweepEl.style.opacity=1; sweepEl.animate([{transform:'translateX(-110%)',opacity:1},{transform:'translateX(260%)',opacity:1}],{duration:950,easing:'cubic-bezier(.4,0,.2,1)'}).onfinish=()=>{sweepEl.style.opacity=0;}; }

  /* --- nổ pháo hoa: tim hoặc tròn --- */
  function explode(x,y,h,shape){
    const m=Math.min(W,H);
    ring(x,y,h,m*.28);
    if(shape==='heart'){
      const k=m*.00085*rnd(.9,1.15);
      [[1,86],[.55,48]].forEach(([sc,n])=>{
        for(let i=0;i<n;i++){
          const t=i/n*6.2832, hx=16*Math.pow(Math.sin(t),3),
                hy=-(13*Math.cos(t)-5*Math.cos(2*t)-2*Math.cos(3*t)-Math.cos(4*t));
          spark(x,y,hx*k*sc,hy*k*sc,h+rnd(-10,10),rnd(60,85),2.4,.018,.94,1);
        }
      });
      for(let i=0;i<46;i++){ const a=rnd(0,6.28), s=rnd(.4,3.2)*m*.0016; spark(x,y,Math.cos(a)*s*3,Math.sin(a)*s*3,45+rnd(-10,10),rnd(30,60),1.4,.03,.93,1); }
    } else {
      const sp=m*.0105;
      for(let i=0;i<110;i++){ const a=rnd(0,6.28), s=sp*rnd(.55,1); spark(x,y,Math.cos(a)*s,Math.sin(a)*s,h+(i%2?rnd(20,50):0),rnd(55,85),2.1,.035,.94,1); }
      for(let i=0;i<30;i++){ const a=i/30*6.28, s=sp*.5; spark(x,y,Math.cos(a)*s,Math.sin(a)*s,50,rnd(45,60),1.6,.03,.95,1); }
    }
  }
  function launch(tx,ty,shape,h,delay){
    setTimeout(()=>{ R.push({x:tx+rnd(-60,60),y:H+10,tx,ty,h:h==null?pick(HUES):h,shape:shape||(Math.random()<.5?'heart':'ring')}); },delay||0);
  }

  /* --- vòng lặp vẽ --- */
  let last=performance.now(), dirty=false;
  function loop(t){
    const f=Math.min(3,(t-last)/16.667); last=t;
    if(P.length||R.length||RING.length||CF.length){
      dirty=true;
      g.globalCompositeOperation='source-over'; g.clearRect(0,0,W,H);
      /* confetti */
      for(let i=CF.length-1;i>=0;i--){
        const c=CF[i]; c.ph+=.08*f; c.vy=Math.min(5,c.vy+.14*f); c.vx*=Math.pow(.985,f);
        c.x+=(c.vx+Math.sin(c.ph)*1.2)*f; c.y+=c.vy*f; c.r+=c.vr*f; c.l-=f;
        if(c.l<=0||c.y>H+30){ CF[i]=CF[CF.length-1]; CF.pop(); continue; }
        g.save(); g.translate(c.x,c.y); g.rotate(c.r); g.scale(1,Math.abs(Math.cos(c.ph)));
        g.globalAlpha=Math.min(1,c.l/40); g.fillStyle=c.c; g.fillRect(-c.w/2,-c.h/2,c.w,c.h); g.restore();
      }
      g.globalAlpha=1; g.globalCompositeOperation='lighter';
      /* sóng xung kích */
      for(let i=RING.length-1;i>=0;i--){
        const r=RING[i]; r.r+=(r.max-r.r)*.07*f+2*f; r.a=Math.max(0,1-r.r/r.max);
        if(r.a<=.02){ RING[i]=RING[RING.length-1]; RING.pop(); continue; }
        g.lineWidth=1+r.a*5; g.strokeStyle=`hsla(${r.h},100%,70%,${r.a*.8})`;
        g.shadowColor=`hsl(${r.h},100%,60%)`; g.shadowBlur=18;
        g.beginPath(); g.arc(r.x,r.y,r.r,0,6.2832); g.stroke();
      }
      g.shadowBlur=0;
      /* tên lửa */
      for(let i=R.length-1;i>=0;i--){
        const r=R[i], dx=r.tx-r.x, dy=r.ty-r.y, d=Math.hypot(dx,dy);
        if(d<14){ explode(r.tx,r.ty,r.h,r.shape); flash(.1); R[i]=R[R.length-1]; R.pop(); continue; }
        const s=Math.min(d,(8+d*.035)*f); r.x+=dx/d*s; r.y+=dy/d*s;
        spark(r.x,r.y,rnd(-.4,.4),rnd(.5,1.4),rnd(35,55),rnd(14,24),1.8,.02,.95);
        g.fillStyle='rgba(255,240,220,.95)'; g.beginPath(); g.arc(r.x,r.y,2.4,0,6.2832); g.fill();
      }
      /* tia lửa */
      g.lineCap='round';
      for(let i=P.length-1;i>=0;i--){
        const p=P[i]; p.px=p.x; p.py=p.y;
        const dr=Math.pow(p.d,f); p.vx*=dr; p.vy=p.vy*dr+p.g*f; p.x+=p.vx*f; p.y+=p.vy*f; p.l-=f;
        if(p.l<=0){ P[i]=P[P.length-1]; P.pop(); continue; }
        let a=Math.min(1,p.l/p.m*1.7); if(p.tw&&p.l<p.m*.5&&Math.random()<.3) a*=.35;
        g.strokeStyle=`hsla(${p.h},100%,${62+a*18}%,${a})`; g.lineWidth=p.s;
        g.beginPath(); g.moveTo(p.px,p.py); g.lineTo(p.x,p.y); g.stroke();
        if(p.s>1.9){ g.fillStyle=`hsla(${p.h},100%,78%,${a*.45})`; g.beginPath(); g.arc(p.x,p.y,p.s*1.9,0,6.2832); g.fill(); }
      }
    } else if(dirty){ g.clearRect(0,0,W,H); dirty=false; }

    /* tilt mượt */
    tcx+=(ttx-tcx)*.08*f; tcy+=(tty-tcy)*.08*f;
    if(Math.abs(tcx-lx)>.01||Math.abs(tcy-ly)>.01){ lx=tcx; ly=tcy; const s=document.documentElement.style; s.setProperty('--tx',tcx.toFixed(2)); s.setProperty('--ty',tcy.toFixed(2)); }
    requestAnimationFrame(loop);
  }
  let ttx=0,tty=0,tcx=0,tcy=0,lx=0,ly=0;
  requestAnimationFrame(loop);

  /* --- trail bám theo tay + quầng sáng --- */
  let glowT=null, th=0, lastX=-1, lastY=-1;
  function trail(x,y){
    th=(th+6)%360;
    const hue=[335,345,45,265][(th/90)|0]+rnd(-8,8);
    const dx=lastX<0?0:x-lastX, dy=lastY<0?0:y-lastY;
    const n=Math.min(4,1+Math.hypot(dx,dy)/18|0);
    for(let i=0;i<n;i++) spark(x-dx*i/n+rnd(-3,3),y-dy*i/n+rnd(-3,3),rnd(-.7,.7)-dx*.02,rnd(-.7,.7)+.35,hue,rnd(26,48),rnd(1.4,3),.03,.95,1);
    lastX=x; lastY=y;
  }
  function moveGlow(x,y){
    cglow.style.transform=`translate3d(${x}px,${y}px,0)`; cglow.style.opacity=1;
    clearTimeout(glowT); glowT=setTimeout(()=>{cglow.style.opacity=0;lastX=lastY=-1;},900);
  }
  addEventListener('pointermove',e=>{
    trail(e.clientX,e.clientY); moveGlow(e.clientX,e.clientY);
    tty=(e.clientX/W-.5)*12; ttx=-(e.clientY/H-.5)*9;
  },{passive:true});
  addEventListener('pointerup',e=>{ if(e.pointerType!=='mouse'){ clearTimeout(glowT); glowT=setTimeout(()=>{cglow.style.opacity=0;lastX=lastY=-1;},350);} },{passive:true});
  addEventListener('deviceorientation',e=>{
    if(e.gamma==null||e.pointerType) return;
    tty=Math.max(-25,Math.min(25,e.gamma))*.4;
    ttx=-Math.max(-25,Math.min(25,(e.beta||45)-45))*.3;
  },{passive:true});

  /* --- sự kiện chạm: nút / nền --- */
  const fin=$('#sc-final');
  const finalOn=()=>fin&&fin.classList.contains('on');
  addEventListener('pointerdown',e=>{
    moveGlow(e.clientX,e.clientY);
    for(let i=0;i<16;i++){ const a=rnd(0,6.28), s=rnd(1,5); spark(e.clientX,e.clientY,Math.cos(a)*s,Math.sin(a)*s,pick(HUES),rnd(22,42),rnd(1.5,2.8),.05,.93,1); }
    ring(e.clientX,e.clientY,pick(HUES),90);
    if(finalOn() && !(e.target.closest&&e.target.closest('button,input'))){
      R.push({x:e.clientX,y:H+10,tx:e.clientX,ty:Math.max(H*.12,Math.min(e.clientY,H*.55)),h:pick(HUES),shape:Math.random()<.65?'heart':'ring'});
    }
  },{passive:true});

  /* --- mở quà: bùng nổ --- */
  let opened=false;
  start.addEventListener('click',()=>{
    if(opened) return; opened=true;
    flash(.95); sweep();
    const cx=W/2, cy=H*.4;
    [335,45,265].forEach((h,i)=>setTimeout(()=>ring(cx,cy,h,Math.max(W,H)*.8),i*140));
    confetti(cx,H*.55,150);
    launch(W*.25,H*.28,'heart',335,200); launch(W*.75,H*.26,'heart',265,500);
    launch(W*.5,H*.18,'heart',45,850);
  });

  /* --- mỗi lần đổi cảnh: quét sáng + sóng + pháo nhỏ --- */
  document.querySelectorAll('.scene').forEach(sc=>{
    new MutationObserver(ms=>{
      ms.forEach(m=>{
        const was=(m.oldValue||'').split(/\s+/).includes('on'), now=sc.classList.contains('on');
        if(now&&!was&&opened){
          if(sc.id==='sc-final') return;
          ring(W/2,H*.4,pick(HUES),Math.max(W,H)*.6); sweep(); flash(.12);
          if(Math.random()<.6) launch(rnd(W*.2,W*.8),rnd(H*.12,H*.3),'ring');
        }
      });
    }).observe(sc,{attributes:true,attributeFilter:['class'],attributeOldValue:true});
  });

  /* --- trả lời câu hỏi: pháo trái tim giữa màn --- */
  const q1=$('#q1');
  if(q1) q1.addEventListener('click',e=>{
    if(!e.target.closest('button')) return;
    flash(.35); confetti(W/2,H*.62,90);
    launch(W*.5,H*.3,'heart',335,0); launch(W*.25,H*.36,'ring',265,280); launch(W*.75,H*.36,'ring',45,420);
  });

  /* --- thẻ kết: đại tiệc --- */
  let finT=null;
  if(fin) new MutationObserver(ms=>{
    const on=finalOn();
    if(on&&!finT){
      flash(.7); sweep(); ring(W/2,H*.4,335,Math.max(W,H)*.9); confetti(0,0,170,true);
      launch(W*.3,H*.25,'heart',335,150); launch(W*.7,H*.22,'heart',265,450); launch(W*.5,H*.14,'heart',45,800);
      finT=setInterval(()=>{
        if(document.hidden) return;
        launch(rnd(W*.12,W*.88),rnd(H*.1,H*.42),Math.random()<.55?'heart':'ring');
        if(Math.random()<.25) confetti(0,0,26,true);
      },1100);
    } else if(!on&&finT){ clearInterval(finT); finT=null; }
  }).observe(fin,{attributes:true,attributeFilter:['class']});
})();
</script>


</body>
</html>
