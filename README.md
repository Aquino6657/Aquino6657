<div align="center">
  <h1>Welcome to My Space ✨</h1>
  <p>Code • Anime • Games • Fun</p>
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=20&pause=1000&color=ffacc8&width=550&lines=Kawaii+Code+Lover;Anime+Fan;Wordle+Gamer+🌸;Always+learning+new+things">
</div>

---

# 🌸 Kawaii Wordle — 可愛い単語ゲーム
<p align="center">
  <b>6 次机会猜出 5 个字母的单词</b><br>
  🟩 正解の文字・位置<br>
  🟨 文字は正しいが位置が違う<br>
  ⬜ この文字は含まれていない<br>
</p>

<div align="center">
<details>
<summary>💖 クリックしてゲームをスタート</summary>

```html
<!-- 二次元 Wordle 纯本地运行 -->
<div style="background:#fff0f5; padding:20px; border-radius:16px; max-width:320px; margin:10px auto; border:3px solid #ffc0d0;">
  <div id="game" style="font-family: 'Segoe UI', sans-serif; text-align:center;">
    <div id="board" style="display: grid; grid-template-columns: repeat(5, 50px); gap:6px; justify-content:center; margin:10px 0;"></div>
    <input id="input" maxlength="5" placeholder="5文字 入力" style="width:160px; padding:8px; border-radius:8px; border:2px solid #ffc0cb; text-align:center; margin-top:10px;">
    <button onclick="guess()" style="background:#ffacc8; color:white; border:none; padding:8px 16px; border-radius:8px; margin-left:6px;">決定</button>
  </div>

  <script>
    const words = ["apple","bread","cream","dream","fruit","grape","honey","lemon","mango","peach","pine","sugar","sweet","water"];
    let answer = words[Math.floor(Math.random()*words.length)];
    let row = 0;
    const board = document.getElementById("board");
    const input = document.getElementById("input");

    function renderBoard(){
      board.innerHTML = "";
      for(let i=0;i<6;i++){
        for(let j=0;j<5;j++){
          const cell = document.createElement("div");
          cell.style.width = "50px";
          cell.style.height = "50px";
          cell.style.border = "2px solid #ffc0d0";
          cell.style.borderRadius = "10px";
          cell.style.display = "flex";
          cell.style.alignItems = "center";
          cell.style.justifyContent = "center";
          cell.style.fontSize = "22px";
          cell.style.fontWeight = "bold";
          cell.id = `c${i}-${j}`;
          board.appendChild(cell);
        }
      }
    }

    function guess(){
      let w = input.value.toLowerCase().trim();
      if(w.length!=5) return;
      for(let i=0;i<5;i++){
        const c = document.getElementById(`c${row}-${i}`);
        c.innerText = w[i];
        if(w[i]==answer[i]) c.style.background="#b2f2bb";
        else if(answer.includes(w[i])) c.style.background="#fff3bf";
        else c.style.background="#e9ecef";
        c.style.color="#222";
        c.style.border="none";
      }
      row++;
      input.value="";
      if(w==answer) alert("🎉 おめでとう！正解です！");
      else if(row>=6) alert("💧 残念… 正解は "+answer+" でした");
    }
    renderBoard();
  </script>
</div>
