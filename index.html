<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Tic Tac Toe</title>
<style>
* { box-sizing: border-box; margin: 0; padding: 0; }
:root {
  --bg: #ffffff; --bg2: #f1efe8; --bg3: #e8e6df;
  --text: #1a1a1a; --text2: #666660;
  --border: rgba(0,0,0,0.15); --border2: rgba(0,0,0,0.3);
  --cell-bg: #f1efe8; --cell-hover: #ffffff;
  --win-bg: #e6f1fb; --win-border: rgba(24,95,165,0.4);
  --x-color: #185FA5; --o-color: #993C1D;
}
.dark {
  --bg: #1a1a1a; --bg2: #242424; --bg3: #2e2e2e;
  --text: #f0ede6; --text2: #999890;
  --border: rgba(255,255,255,0.12); --border2: rgba(255,255,255,0.25);
  --cell-bg: #242424; --cell-hover: #2e2e2e;
  --win-bg: #0c447c33; --win-border: rgba(55,138,221,0.5);
  --x-color: #5ca8f0; --o-color: #e8825a;
}
body {
  font-family: system-ui, sans-serif;
  background: var(--bg);
  color: var(--text);
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background 0.2s, color 0.2s;
}
#app { padding: 1.5rem; max-width: 420px; width: 100%; margin: 0 auto; }
#top-bar { display: flex; align-items: center; justify-content: space-between; margin-bottom: 1.25rem; gap: 8px; }
h1 { font-size: 22px; font-weight: 500; color: var(--text); }
.top-right { display: flex; align-items: center; gap: 12px; }
.lang-select { font-size: 13px; padding: 4px 8px; border-radius: 8px; border: 0.5px solid var(--border2); background: var(--bg); color: var(--text); cursor: pointer; }
.toggle-wrap { display: flex; align-items: center; gap: 6px; }
.toggle-label { font-size: 13px; color: var(--text2); }
.toggle { position: relative; width: 40px; height: 22px; }
.toggle input { opacity: 0; width: 0; height: 0; }
.slider { position: absolute; inset: 0; background: var(--bg3); border-radius: 22px; cursor: pointer; border: 0.5px solid var(--border2); transition: background 0.2s; }
.slider:before { content: ''; position: absolute; width: 16px; height: 16px; left: 2px; top: 2px; background: var(--text2); border-radius: 50%; transition: transform 0.2s, background 0.2s; }
.toggle input:checked + .slider:before { transform: translateX(18px); background: var(--text); }
#subtitle { font-size: 14px; color: var(--text2); text-align: center; margin-bottom: 1.25rem; }
#diff-row { display: flex; gap: 8px; justify-content: center; margin-bottom: 1.25rem; }
.diff-btn { font-size: 13px; padding: 6px 16px; border-radius: 8px; border: 0.5px solid var(--border2); background: var(--bg); color: var(--text); cursor: pointer; transition: background 0.15s, color 0.15s, border-color 0.15s; }
.diff-btn:hover { background: var(--bg2); }
.diff-btn[data-d="easy"].active    { background: #C0DD97; border-color: #639922; color: #27500A; font-weight: 500; }
.diff-btn[data-d="medium"].active  { background: #FAC775; border-color: #BA7517; color: #633806; font-weight: 500; }
.diff-btn[data-d="hard"].active    { background: #F7C1C1; border-color: #A32D2D; color: #501313; font-weight: 500; }
.dark .diff-btn[data-d="easy"].active   { background: #27500A; border-color: #639922; color: #C0DD97; }
.dark .diff-btn[data-d="medium"].active { background: #633806; border-color: #BA7517; color: #FAC775; }
.dark .diff-btn[data-d="hard"].active   { background: #501313; border-color: #A32D2D; color: #F7C1C1; }
#score-row { display: flex; justify-content: center; gap: 12px; margin-bottom: 1.25rem; }
.score-card { background: var(--bg2); border-radius: 8px; padding: 10px 20px; text-align: center; min-width: 80px; }
.score-label { font-size: 12px; color: var(--text2); margin-bottom: 2px; }
.score-val { font-size: 22px; font-weight: 500; color: var(--text); }
#status { text-align: center; font-size: 15px; color: var(--text2); min-height: 24px; margin-bottom: 0.5rem; }
#who-starts { text-align: center; font-size: 13px; color: var(--text2); margin-bottom: 0.75rem; min-height: 20px; }
#board { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; margin-bottom: 1.25rem; }
.cell { aspect-ratio: 1; background: var(--cell-bg); border-radius: 8px; border: 0.5px solid var(--border); display: flex; align-items: center; justify-content: center; font-size: 36px; cursor: pointer; transition: background 0.12s; user-select: none; }
.cell:hover:not(.taken) { background: var(--cell-hover); border-color: var(--border2); }
.cell.taken { cursor: default; }
.cell.x { color: var(--x-color); }
.cell.o { color: var(--o-color); }
.cell.win { background: var(--win-bg); border-color: var(--win-border); }
.cell.pop { animation: pop 0.18s ease; }
@keyframes pop { 0%{transform:scale(0.7)} 60%{transform:scale(1.1)} 100%{transform:scale(1)} }
#btn-row { display: flex; justify-content: center; }
#restart-btn { font-size: 14px; padding: 8px 24px; border-radius: 8px; border: 0.5px solid var(--border2); background: var(--bg); color: var(--text); cursor: pointer; }
#restart-btn:hover { background: var(--bg2); }
</style>
</head>
<body>
<div id="app">
  <div id="top-bar">
    <h1>Tic Tac Toe</h1>
    <div class="top-right">
      <select class="lang-select" id="lang-select">
        <option value="en">🇬🇧 English</option>
        <option value="sk">🇸🇰 Slovenčina</option>
        <option value="de">🇩🇪 Deutsch</option>
        <option value="es">🇪🇸 Español</option>
      </select>
      <div class="toggle-wrap">
        <span class="toggle-label" id="lbl-dark">Dark</span>
        <label class="toggle">
          <input type="checkbox" id="dark-toggle">
          <span class="slider"></span>
        </label>
      </div>
    </div>
  </div>

  <p id="subtitle"></p>
  <div id="diff-row">
    <button class="diff-btn" data-d="easy"></button>
    <button class="diff-btn active" data-d="medium"></button>
    <button class="diff-btn" data-d="hard"></button>
  </div>
  <div id="score-row">
    <div class="score-card"><div class="score-label" id="lbl-you"></div><div class="score-val" id="s-player">0</div></div>
    <div class="score-card"><div class="score-label" id="lbl-draw"></div><div class="score-val" id="s-draw">0</div></div>
    <div class="score-card"><div class="score-label" id="lbl-bot"></div><div class="score-val" id="s-bot">0</div></div>
  </div>
  <div id="status"></div>
  <div id="who-starts"></div>
  <div id="board"></div>
  <div id="btn-row"><button id="restart-btn"></button></div>
</div>

<script>
const LANGS = {
  en: { subtitle:'You are X, bot is O', easy:'Easy', medium:'Medium', hard:'Unbeatable', you:'You (X)', draw:'Draw', bot:'Bot (O)', yourTurn:'Your turn', botThinking:'Bot is thinking...', youWin:'You won! 🎉', botWin:'Bot won! 🤖', drawMsg:'Draw!', roundYou:r=>`Round ${r} — you start`, roundBot:r=>`Round ${r} — bot starts`, restart:'New game', dark:'Dark' },
  sk: { subtitle:'Ty si X, bot je O', easy:'Ľahký', medium:'Stredný', hard:'Neporaziteľný', you:'Ty (X)', draw:'Remíza', bot:'Bot (O)', yourTurn:'Tvoj ťah', botThinking:'Bot premýšľa...', youWin:'Vyhral si! 🎉', botWin:'Bot vyhral! 🤖', drawMsg:'Remíza!', roundYou:r=>`Kolo ${r} — začínaš ty`, roundBot:r=>`Kolo ${r} — začína bot`, restart:'Nová hra', dark:'Tmavý' },
  de: { subtitle:'Du bist X, Bot ist O', easy:'Leicht', medium:'Mittel', hard:'Unschlagbar', you:'Du (X)', draw:'Unentsch.', bot:'Bot (O)', yourTurn:'Dein Zug', botThinking:'Bot denkt...', youWin:'Du hast gewonnen! 🎉', botWin:'Bot hat gewonnen! 🤖', drawMsg:'Unentschieden!', roundYou:r=>`Runde ${r} — du fängst an`, roundBot:r=>`Runde ${r} — Bot fängt an`, restart:'Neues Spiel', dark:'Dunkel' },
  es: { subtitle:'Tú eres X, el bot es O', easy:'Fácil', medium:'Medio', hard:'Invencible', you:'Tú (X)', draw:'Empate', bot:'Bot (O)', yourTurn:'Tu turno', botThinking:'Bot pensando...', youWin:'¡Ganaste! 🎉', botWin:'¡Ganó el bot! 🤖', drawMsg:'¡Empate!', roundYou:r=>`Ronda ${r} — empiezas tú`, roundBot:r=>`Ronda ${r} — empieza el bot`, restart:'Nuevo juego', dark:'Oscuro' }
};

let lang = 'en';
let board, gameOver, playerTurn, difficulty = 'medium';
let score = {player:0, draw:0, bot:0};
let botStarts = false, roundCount = 0;

const boardEl = document.getElementById('board');
const statusEl = document.getElementById('status');
const whoStartsEl = document.getElementById('who-starts');
const sPlayer = document.getElementById('s-player');
const sDraw = document.getElementById('s-draw');
const sBot = document.getElementById('s-bot');
const darkToggle = document.getElementById('dark-toggle');
const app = document.getElementById('app');
const langSelect = document.getElementById('lang-select');

function applyLang() {
  const t = LANGS[lang];
  document.getElementById('subtitle').textContent = t.subtitle;
  const btns = document.querySelectorAll('.diff-btn');
  btns[0].textContent = t.easy;
  btns[1].textContent = t.medium;
  btns[2].textContent = t.hard;
  document.getElementById('lbl-you').textContent = t.you;
  document.getElementById('lbl-draw').textContent = t.draw;
  document.getElementById('lbl-bot').textContent = t.bot;
  document.getElementById('restart-btn').textContent = t.restart;
  document.getElementById('lbl-dark').textContent = t.dark;
  if (!gameOver) statusEl.textContent = playerTurn ? t.yourTurn : t.botThinking;
}

langSelect.addEventListener('change', () => { lang = langSelect.value; applyLang(); });
darkToggle.addEventListener('change', () => {
  document.body.classList.toggle('dark', darkToggle.checked);
  app.classList.toggle('dark', darkToggle.checked);
});

document.querySelectorAll('.diff-btn').forEach(b => {
  b.addEventListener('click', () => {
    document.querySelectorAll('.diff-btn').forEach(x => x.classList.remove('active'));
    b.classList.add('active');
    difficulty = b.dataset.d;
    roundCount = 0; botStarts = false;
    init();
  });
});

document.getElementById('restart-btn').addEventListener('click', () => { roundCount = 0; botStarts = false; init(); });

const WINS = [[0,1,2],[3,4,5],[6,7,8],[0,3,6],[1,4,7],[2,5,8],[0,4,8],[2,4,6]];
function checkWin(b,sym){return WINS.some(([a,c,d])=>b[a]===sym&&b[c]===sym&&b[d]===sym);}
function winLine(b,sym){return WINS.find(([a,c,d])=>b[a]===sym&&b[c]===sym&&b[d]===sym);}
function isFull(b){return b.every(x=>x!=='');}

function minimax(b,isMax,alpha,beta){
  if(checkWin(b,'O'))return 10;
  if(checkWin(b,'X'))return -10;
  if(isFull(b))return 0;
  if(isMax){let best=-Infinity;for(let i=0;i<9;i++){if(!b[i]){b[i]='O';best=Math.max(best,minimax(b,false,alpha,beta));b[i]='';alpha=Math.max(alpha,best);if(beta<=alpha)break;}}return best;}
  else{let best=Infinity;for(let i=0;i<9;i++){if(!b[i]){b[i]='X';best=Math.min(best,minimax(b,true,alpha,beta));b[i]='';beta=Math.min(beta,best);if(beta<=alpha)break;}}return best;}
}

function botMove(){
  const empty=board.map((v,i)=>v?null:i).filter(v=>v!==null);
  if(!empty.length)return;
  let idx;
  if(difficulty==='easy'){
    idx=empty[Math.floor(Math.random()*empty.length)];
  } else if(difficulty==='medium'){
    for(const sym of['O','X']){for(const i of empty){board[i]=sym;if(checkWin(board,sym)){board[i]='';idx=i;break;}board[i]='';}if(idx!==undefined)break;}
    if(idx===undefined)idx=empty[Math.floor(Math.random()*empty.length)];
  } else {
    let best=-Infinity,bestIdx=empty[0];
    for(const i of empty){board[i]='O';const v=minimax(board,false,-Infinity,Infinity);board[i]='';if(v>best){best=v;bestIdx=i;}}
    idx=bestIdx;
  }
  board[idx]='O';
  renderBoard();
  if(checkWin(board,'O')){endGame('bot');return;}
  if(isFull(board)){endGame('draw');return;}
  playerTurn=true;
  statusEl.textContent=LANGS[lang].yourTurn;
}

function renderBoard(){
  boardEl.querySelectorAll('.cell').forEach((cell,i)=>{
    const prev=cell.textContent;
    const cur=board[i]==='X'?'✕':board[i]==='O'?'○':'';
    cell.textContent=cur;
    if(cur&&cur!==prev){cell.classList.add('pop');setTimeout(()=>cell.classList.remove('pop'),200);}
    cell.className='cell'+(board[i]?' taken':'')+(board[i]==='X'?' x':board[i]==='O'?' o':'');
  });
}

function endGame(result){
  gameOver=true;
  const t=LANGS[lang];
  const line=result==='draw'?null:winLine(board,result==='player'?'X':'O');
  if(line)line.forEach(i=>boardEl.children[i].classList.add('win'));
  if(result==='player'){score.player++;sPlayer.textContent=score.player;statusEl.textContent=t.youWin;}
  else if(result==='bot'){score.bot++;sBot.textContent=score.bot;statusEl.textContent=t.botWin;}
  else{score.draw++;sDraw.textContent=score.draw;statusEl.textContent=t.drawMsg;}
  botStarts=!botStarts;
  setTimeout(init,1600);
}

function init(){
  board=Array(9).fill('');
  gameOver=false;
  roundCount++;
  const t=LANGS[lang];
  boardEl.innerHTML='';
  for(let i=0;i<9;i++){
    const cell=document.createElement('div');
    cell.className='cell';
    cell.addEventListener('click',()=>{
      if(!playerTurn||gameOver||board[i])return;
      board[i]='X';playerTurn=false;
      renderBoard();
      if(checkWin(board,'X')){endGame('player');return;}
      if(isFull(board)){endGame('draw');return;}
      statusEl.textContent=t.botThinking;
      setTimeout(botMove,400);
    });
    boardEl.appendChild(cell);
  }
  if(botStarts){
    playerTurn=false;
    whoStartsEl.textContent=roundCount>1?t.roundBot(roundCount):'';
    statusEl.textContent=t.botThinking;
    setTimeout(botMove,600);
  } else {
    playerTurn=true;
    whoStartsEl.textContent=roundCount>1?t.roundYou(roundCount):'';
    statusEl.textContent=t.yourTurn;
  }
}

init();
applyLang();
</script>
</body>
</html>
