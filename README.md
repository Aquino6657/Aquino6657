<div align="center">
  <h1>✨ Welcome to My Coding Space ✨</h1>
  <p>Code • Anime • Games • Cute Things</p>
  <img src="https://readme-typing-svg.herokuapp.com?font=JetBrains+Mono&weight=500&size=20&pause=1000&color=ff8fab&width=550&lines=Kawaii+Code+Lover;Anime+Fan;Wordle+Gamer+🌸;Always+Learning+New+Things">
</div>

---

<div align="center">
  <h1>🌸 Kawaii Wordle ゲーム</h1>
  <p><b>6 次机会猜出 5 个字母单词 ✏️</b></p>
  <p>🟩 正解の文字・位置<br>🟨 文字は正しいが位置が違う<br>⬜ この文字は含まれていない</p>

<details>
<summary>💖 クリックしてゲームスタート</summary>

<div style="background:#fff0f5; padding:20px; border-radius:16px; max-width:320px; margin:10px auto; border:3px solid #ffc0d0;">
  <div id="game" style="font-family: 'Segoe UI', sans-serif; text-align:center;">
    <div id="board" style="display: grid; grid-template-columns: repeat(5, 50px); gap:6px; justify-content:center; margin:10px 0;"></div>
    <input id="input" maxlength="5" placeholder="5文字 入力" style="width:160px; padding:8px; border-radius:8px; border:2px solid #ffc0cb; text-align:center; margin-top:10px;">
    <button onclick="guess()" style="background:#ff8fab; color:white; border:none; padding:8px 16px; border-radius:8px; margin-left:6px; cursor:pointer;">決定</button>
  </div>

  <script>
    const words = ["apple","bread","cream","dream","fruit","grape","honey","lemon","mango","peach","pine","sugar","sweet","water","sunny","cloud","smile","happy","dream","angel"];
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
      if(w==answer) alert("🎉 おめでとう！正解です～！");
      else if(row>=6) alert("💧 残念… 正解は "+answer+" でした！");
    }
    renderBoard();
  </script>
</div>

</details>
</div>
---

### 🛠 好きな技術
![HTML5](https://img.shields.io/badge/-HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/-CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat-square&logo=react&logoColor=black)
![Vue](https://img.shields.io/badge/-Vue-4FC08D?style=flat-square&logo=vue.js&logoColor=white)
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat-square&logo=node.js&logoColor=white)
![Git](https://img.shields.io/badge/-Git-F05032?style=flat-square&logo=git&logoColor=white)

---

### 📊 GitHub Stats
<div align="center">
<img height="170" src="https://github-readme-stats.vercel.app/api?username=Aquino6657&show_icons=true&theme=dracula&hide_border=true">
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Aquino6657&layout=compact&theme=dracula&hide_border=true">
</div>

<div align="center" style="margin-top:20px; color:#ff8fab;">
⭐ 遊んでくれてありがとう ⭐
</div>
