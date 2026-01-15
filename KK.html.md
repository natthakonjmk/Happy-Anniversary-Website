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

section {
  padding: 50px 20px;
  max-width: 900px;
  margin: auto;
}

/* HERO */
.hero {
  text-align: center;
  padding-top: 70px;
}
.hero h1 {
  font-weight: 500;
  font-size: 2.3rem;
}
.hero p {
  color: #777;
}

/* TIMELINE */
.timeline div {
  border-left: 3px solid #e6a9b4;
  padding-left: 15px;
  margin: 15px 0;
}

/* GALLERY */
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
  gap: 12px;
}
.gallery img {
  width: 100%;
  border-radius: 14px;
  box-shadow: 0 6px 15px rgba(0,0,0,0.08);
}

/* LETTER */
.letter {
  background: white;
  border-radius: 20px;
  padding: 28px;
  line-height: 1.9;
  box-shadow: 0 6px 20px rgba(0,0,0,0.06);
}

/* SONGS */
.song-block {
  margin-bottom: 24px;
}
.song-text {
  font-size: 0.9rem;
  color: #777;
  margin-bottom: 6px;
}

/* COUPONS */
.coupons {
  text-align: center;
}
.coupon {
  background: white;
  border: 2px dashed #e6a9b4;
  border-radius: 22px;
  padding: 22px;
  margin: 16px auto;
  max-width: 320px;
  transition: 0.3s;
  cursor: pointer;
  box-shadow: 0 6px 18px rgba(0,0,0,0.05);
}
.coupon:hover {
  transform: translateY(-3px);
}
.coupon.used {
  opacity: 0.45;
}
.coupon h3 {
  margin: 0;
  font-weight: 500;
}
.coupon p {
  font-size: 0.9rem;
  color: #666;
}
.btn {
  margin-top: 10px;
  display: inline-block;
  background: #e6a9b4;
  color: white;
  padding: 7px 18px;
  border-radius: 999px;
  font-size: 0.85rem;
}

/* FOOTER */
footer {
  text-align: center;
  color: #aaa;
  padding-bottom: 50px;
}
</style>
</head>

<body>

<section class="hero">
  <h1>🐈 ครบรอบ 2 เดือนแล้วนะน้องข้าว 🐈</h1>
  <p>ไปด้วยกันนาน ๆ จะได้ไปเที่ยวกันหลาย ๆ ที่เลย 🤍</p>
</section>

<section class="timeline">
  <h2>Our Story</h2>
  <div>💫 วันที่เราเริ่มคุยกัน</div>
  <div>☕ เดทแรกของเรา</div>
  <div>📸 ความทรงจำที่ไม่เคยลืม</div>
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
  <h2>Our Songs</h2>

  <div class="song-block">
    <p class="song-text">🎵 เพลงที่น้องข้าวให้ครั้งแรก</p>
    <iframe style="border-radius:12px"
      src="https://open.spotify.com/embed/track/SONG_ID_1"
      width="100%" height="80" frameborder="0" allow="encrypted-media">
    </iframe>
  </div>

  <div class="song-block">
    <p class="song-text">💌 เพลงที่พี่ดรีมขอน้องข้าวเป็นแฟน</p>
    <iframe style="border-radius:12px"
      src="https://open.spotify.com/embed/track/SONG_ID_2"
      width="100%" height="80" frameborder="0" allow="encrypted-media">
    </iframe>
  </div>

</section>

<section class="coupons">
  <h2>🎟 Love Coupons</h2>

  <div class="coupon" onclick="useCoupon(this)">
    <h3>🤍 คูปองโอ๋</h3>
    <p>โอ๋ได้ทันที ไม่จำกัดเวลา</p>
    <span class="btn">ใช้คูปอง</span>
  </div>

  <div class="coupon" onclick="useCoupon(this)">
    <h3>🍜 คูปองเลี้ยงข้าว</h3>
    <p>มื้อไหนก็ได้ ที่เธอเลือก</p>
    <span class="btn">ใช้คูปอง</span>
  </div>

  <div class="coupon" onclick="useCoupon(this)">
    <h3>🎬 คูปองดูหนัง</h3>
    <p>แนวไหนก็ได้ ตามใจเธอ</p>
    <span class="btn">ใช้คูปอง</span>
  </div>

  <div class="coupon" onclick="useCoupon(this)">
    <h3>🫂 คูปองกอด</h3>
    <p>กอดยาว 5 นาที</p>
    <span class="btn">ใช้คูปอง</span>
  </div>

  <div class="coupon" onclick="useCoupon(this)">
    <h3>😴 คูปองง้อ</h3>
    <p>ใช้ได้เมื่อเรางอนกัน</p>
    <span class="btn">ใช้คูปอง</span>
  </div>

  <div class="coupon" onclick="useCoupon(this)">
    <h3>✈️ คูปองทริปเล็ก ๆ</h3>
    <p>ไปด้วยกันที่ไหนก็ได้</p>
    <span class="btn">ใช้คูปอง</span>
  </div>
</section>

<footer>
  Always us 🤍
</footer>

<script>
function useCoupon(el){
  if(el.classList.contains("used")){
    el.classList.remove("used");
    el.querySelector(".btn").innerText = "ใช้คูปอง";
  } else {
    el.classList.add("used");
    el.querySelector(".btn").innerText = "ใช้แล้ว 🤍";
  }
}
</script>

</body>
</html>