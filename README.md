# anniversary-web
 <!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Happy Anniversary 🤍</title>

<style>
body {
  margin: 0;
  font-family: -apple-system, BlinkMacSystemFont, "Helvetica Neue", sans-serif;
  background: linear-gradient(180deg, #fff6f8, #f9f9f9);
  color: #333;
}

/* 🔐 LOCK */
#lockScreen{
  position:fixed; inset:0;
  background:linear-gradient(135deg,#fff0f4,#fafafa);
  display:flex;align-items:center;justify-content:center;z-index:9999;
}
.lockBox{
  background:#fff;padding:30px;border-radius:22px;text-align:center;
  box-shadow:0 12px 35px rgba(230,169,180,.25);
  max-width:320px;width:100%;
}
.lockBox h2{color:#e6a9b4;}
.passInputs{display:flex;justify-content:space-between;margin:15px 0;}
.passInputs input{
  width:55px;height:55px;font-size:2rem;text-align:center;
  border-radius:14px;border:1px solid #f0c5cf;
  background:#fff6f8;color:transparent;
  text-shadow:0 0 0 #e6a9b4;caret-color:transparent;
}
.lockBox button{
  background:#e6a9b4;color:#fff;border:none;
  padding:8px 22px;border-radius:20px;cursor:pointer;
}
.shake{animation:shake .35s;}
@keyframes shake{
  0%{transform:translateX(0)}
  25%{transform:translateX(-6px)}
  50%{transform:translateX(6px)}
  75%{transform:translateX(-6px)}
  100%{transform:translateX(0)}
}
#hearts span{
  position:absolute;font-size:1.4rem;
  animation:floatUp 1.2s ease forwards;
}
@keyframes floatUp{
  from{transform:translateY(0) scale(.8);opacity:1}
  to{transform:translateY(-80px) scale(1.2);opacity:0}
}

/* ===== MAIN ===== */
section{padding:50px 20px;max-width:900px;margin:auto;}
.hero{text-align:center;padding-top:70px;}
.hero h1{font-weight:500;font-size:2.3rem;}
.hero p{color:#777;}

/* 🎥 VIDEO */
.video-grid{
  display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:22px;
}
.video-card{
  background:#fff;border-radius:20px;padding:12px;
  box-shadow:0 8px 24px rgba(0,0,0,.08);
  opacity:0;transform:translateY(30px);transition:1s;
}
.video-card.show{opacity:1;transform:translateY(0);}
.video-card video{width:100%;border-radius:14px;}
.video-caption{margin-top:10px;font-size:.95rem;color:#777;}

.timeline div{border-left:3px solid #e6a9b4;padding-left:15px;margin:15px 0;}
.gallery{display:grid;grid-template-columns:repeat(auto-fit,minmax(130px,1fr));gap:12px;}
.gallery img{width:100%;border-radius:14px;box-shadow:0 6px 15px rgba(0,0,0,.08);}
.letter{background:#fff;border-radius:20px;padding:28px;line-height:1.9;box-shadow:0 6px 20px rgba(0,0,0,.06);}
.song-block{margin-bottom:24px;}
.song-text{font-size:.9rem;color:#777;margin-bottom:6px;}

.coupons{text-align:center;}
.coupon{
  position:relative;
  background:#fff;border:2px dashed #e6a9b4;border-radius:22px;
  padding:22px;margin:16px auto;max-width:320px;cursor:pointer;
  box-shadow:0 6px 18px rgba(0,0,0,.05);
}
.coupon.used{opacity:.45;}
.btn{margin-top:10px;display:inline-block;background:#e6a9b4;color:#fff;padding:7px 18px;border-radius:999px;font-size:.85rem;}

.coupon.pop{animation:pop .35s ease;}
@keyframes pop{
  0%{transform:scale(1)}
  50%{transform:scale(1.08)}
  100%{transform:scale(1)}
}
.heart-fx{
  position:absolute;font-size:1.3rem;
  color:#e6a9b4;
  animation:heartUp .9s ease forwards;
}
@keyframes heartUp{
  from{transform:translateY(0) scale(.8);opacity:1}
  to{transform:translateY(-50px) scale(1.2);opacity:0}
}

footer{text-align:center;color:#aaa;padding-bottom:50px;}
</style>
</head>

<body>

<div id="lockScreen">
  <div class="lockBox" id="lockBox">
    <h2>🤍 ใส่รหัสวันครบรอบ</h2>
    <p>ของพี่ดรีม & น้องข้าว</p>
    <div class="passInputs">
      <input type="password" maxlength="1">
      <input type="password" maxlength="1">
      <input type="password" maxlength="1">
      <input type="password" maxlength="1">
    </div>
    <button onclick="checkPass()">เข้าเว็บ 🤍</button>
    <div id="hearts"></div>
  </div>
</div>

<audio id="successSound">
  <source src="https://cdn.pixabay.com/download/audio/2022/03/15/audio_3c8e32c2bb.mp3">
</audio>

<section class="hero">
  <h1>🐈 ครบรอบของพี่ดรีม & น้องข้าว 🐈</h1>
  <p>ไปด้วยกันนาน ๆ นะ 🤍</p>
</section>

<section>
<h2>🎬 Our Moments</h2>
<div class="video-grid">
  <div class="video-card">
    <video controls><source src="videos/1.mp4"></video>
    <div class="video-caption">💫 คลิปแรกของเราด้วยกัน</div>
  </div>
  <div class="video-card">
    <video controls><source src="videos/2.mp4"></video>
    <div class="video-caption">☕ เดทเล็ก ๆ แต่ความทรงจำใหญ่</div>
  </div>
</div>
</section>

<section class="timeline">
<h2>Our Story</h2>
<div>💫 วันที่เราเริ่มคุยกัน</div>
<div>☕ เดทแรก</div>
<div>📸 ความทรงจำ</div>
<div>🤍 วันนี้ – Anniversary</div>
</section>

<section>
  <h2>Memories</h2>
  <div class="gallery">
    <img src="images/1.jpg">
    <img src="images/2.jpg">
    <img src="images/3.jpg">
    <img src="images/4.jpg">
  </div>
</section>

<section>
  <h2>Letter</h2>
  <div class="letter">
    ขอบคุณที่อยู่ด้วยกันในทุกวันธรรมดา<br>
    ขอบคุณที่ทำให้เรื่องเล็ก ๆ มีความหมาย<br>
    และหวังว่าเราจะยังเลือกกันแบบนี้ต่อไป 🤍
  </div>
</section>

<section>
  <h2>Our Songs 🎶</h2>

  <div class="song-block">
    <p class="song-text">🎵 เพลงที่น้องข้าวให้ครั้งแรก</p>
    <iframe style="border-radius:12px"
      src="https://open.spotify.com/embed/track/6pQp49ThiAsKwCl8OWcO4V"
      width="100%" height="80" frameborder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>
  </div>

  <div class="song-block">
    <p class="song-text">💌 เพลงที่พี่ดรีมขอน้องข้าวเป็นแฟน</p>
    <iframe style="border-radius:12px"
      src="https://open.spotify.com/embed/track/79qhHPvit6BeOVu2wNnLgJ"
      width="100%" height="80" frameborder="0"
      allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture">
    </iframe>
  </div>

</section>

<section class="coupons">
<h2>🎟 Love Coupons</h2>

<div class="coupon"><h3>🤍 คูปองโอ๋</h3><p>โอ๋ได้ทันที</p><span class="btn">ใช้คูปอง</span></div>
<div class="coupon"><h3>🍜 คูปองเลี้ยงข้าว</h3><p>มื้อไหนก็ได้</p><span class="btn">ใช้คูปอง</span></div>
<div class="coupon"><h3>🎬 คูปองดูหนัง</h3><p>ตามใจเธอ</p><span class="btn">ใช้คูปอง</span></div>
<div class="coupon"><h3>🫂 คูปองกอด</h3><p>กอดยาว 5 นาที</p><span class="btn">ใช้คูปอง</span></div>
<div class="coupon"><h3>😴 คูปองง้อ</h3><p>ใช้ตอนงอน</p><span class="btn">ใช้คูปอง</span></div>
<div class="coupon"><h3>✈️ คูปองทริปเล็ก ๆ</h3><p>ไปด้วยกัน</p><span class="btn">ใช้คูปอง</span></div>

</section>

<footer>Always us 🤍</footer>

<script>
document.querySelectorAll(".coupon").forEach((coupon,i)=>{
  const saved=localStorage.getItem("coupon_"+i);
  if(saved==="used"){coupon.classList.add("used");coupon.querySelector(".btn").innerText="ใช้แล้ว 🤍";}
  coupon.addEventListener("click",()=>{
    if(!coupon.classList.contains("used")){
      coupon.classList.add("used");
      coupon.querySelector(".btn").innerText="ใช้แล้ว 🤍";
      localStorage.setItem("coupon_"+i,"used");

      coupon.classList.add("pop");
      setTimeout(()=>coupon.classList.remove("pop"),350);

      for(let j=0;j<4;j++){
        const h=document.createElement("span");
        h.className="heart-fx";
        h.textContent="❤";
        h.style.left=(20+Math.random()*60)+"%";
        h.style.bottom="20px";
        coupon.appendChild(h);
        setTimeout(()=>h.remove(),900);
      }
    }
  });
});

const correctPass="0312";
const inputs=document.querySelectorAll(".passInputs input");
inputs.forEach((input,i)=>{
  input.addEventListener("input",()=>{if(input.value&&i<3)inputs[i+1].focus();});
  input.addEventListener("keydown",e=>{
    if(e.key==="Backspace"&&!input.value&&i>0)inputs[i-1].focus();
    if(e.key==="Enter")checkPass();
  });
});
function checkPass(){
  let val="";inputs.forEach(i=>val+=i.value);
  if(val===correctPass){
    document.getElementById("successSound").play();
    showHearts();
    setTimeout(()=>lockScreen.style.display="none",600);
  }else{
    lockBox.classList.add("shake");
    setTimeout(()=>lockBox.classList.remove("shake"),400);
    inputs.forEach(i=>i.value="");inputs[0].focus();
  }
}
function showHearts(){
  for(let i=0;i<8;i++){
    const s=document.createElement("span");
    s.innerText="💗";
    s.style.left=Math.random()*200+"px";
    s.style.top="140px";
    hearts.appendChild(s);
    setTimeout(()=>s.remove(),1200);
  }
}

const cards=document.querySelectorAll(".video-card");
const obs=new IntersectionObserver(e=>e.forEach(x=>x.isIntersecting&&x.target.classList.add("show")),{threshold:.3});
cards.forEach(c=>obs.observe(c));
</script>

</body>
</html>
