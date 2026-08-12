<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>For Aisy</title>
  <style>
    :root{
      --paper:#f7f0e7;
      --ink:#342a27;
      --muted:#806d64;
      --rose:#a96f6b;
      --line:#d9c9bb;
      --bg:#e8dcd0;
      --shadow:0 0 60px #49352a22;
    }
    *{box-sizing:border-box}
    html{scroll-behavior:smooth}
    body{
      margin:0;
      background:var(--bg);
      color:var(--ink);
      font-family: Arial, sans-serif;
    }
    .book{
      max-width:980px;
      min-height:100vh;
      margin:auto;
      background:var(--paper);
      box-shadow:var(--shadow);
    }
    .page{
      min-height:100vh;
      padding:clamp(38px,8vw,90px) clamp(26px,9vw,110px);
      display:flex;
      flex-direction:column;
      justify-content:center;
      position:relative;
    }
    .cover{
      background:radial-gradient(circle at 85% 18%,#c4877620,transparent 25%),var(--paper);
    }
    .eyebrow{
      color:var(--rose);
      font-size:.68rem;
      font-weight:bold;
      letter-spacing:.2em;
      text-transform:uppercase;
    }
    h1{
      font:italic clamp(3rem,8vw,6.4rem)/.93 Georgia,serif;
      margin:20px 0;
      letter-spacing:-.02em;
    }
    .cover p,
    .intro,
    .reading p{
      max-width:680px;
      font:1.2rem/1.85 Georgia,serif;
      color:var(--muted);
      white-space:pre-wrap;
    }
    .button{
      margin-top:22px;
      width:max-content;
      padding:15px 22px;
      background:transparent;
      border:1px solid var(--ink);
      color:var(--ink);
      font-size:.68rem;
      font-weight:bold;
      letter-spacing:.15em;
      text-transform:uppercase;
      cursor:pointer;
      text-decoration:none;
      display:inline-block;
    }
    .button:hover{
      background:var(--ink);
      color:var(--paper);
    }
    .hidden{display:none !important;}
    .rule{
      width:92px;
      border:0;
      border-top:1px solid var(--rose);
      margin:23px 0;
    }
    .menu{
      justify-content:flex-start;
      padding-top:clamp(40px,8vw,82px);
    }
    .menu h1{
      font-size:clamp(2.8rem,7vw,5.4rem);
    }
    .intro{
      margin:0 0 42px;
      color:var(--ink);
    }
    .entries{
      border-top:1px solid var(--line);
      max-width:760px;
    }
    .entry{
      display:flex;
      align-items:baseline;
      gap:16px;
      padding:21px 0;
      border-bottom:1px solid var(--line);
      text-decoration:none;
      color:var(--ink);
      transition:padding .25s ease,color .25s ease;
    }
    .entry:hover{
      padding-left:10px;
      color:var(--rose);
    }
    .entry span{
      color:var(--rose);
      font-size:.72rem;
      letter-spacing:.12em;
    }
    .entry strong{
      font:italic 1.3rem Georgia,serif;
      font-weight:normal;
    }
    .entry em{
      margin-left:auto;
      color:var(--muted);
      font-size:.76rem;
      font-style:normal;
    }
    .reading{
      justify-content:flex-start;
      padding-top:clamp(45px,8vw,90px);
    }
    .reading h1{
      font-size:clamp(2.6rem,6vw,5rem);
      max-width:800px;
    }
    .reading p{
      color:var(--ink);
      max-width:690px;
    }
    .back{
      margin-top:30px;
    }
    .footer{
      margin-top:auto;
      padding-top:45px;
      color:var(--muted);
      font-size:.68rem;
      letter-spacing:.12em;
    }
    @media(max-width:600px){
      .entry em{display:none}
      .entry strong{font-size:1.12rem}
      .page{padding:34px 22px}
    }
    @media(prefers-reduced-motion:reduce){
      html{scroll-behavior:auto}
      *{transition:none !important}
    }
  </style>
</head>
<body>
  <main class="book">
    <section id="cover" class="page cover">
      <div class="eyebrow">A small book, made for you</div>
      <h1>For Aisy,<br>with love</h1>
      <hr class="rule" />
      <p>“The writing is still; to you, with you, about you, because of you and for you.”</p>
      <button class="button" onclick="show('menu')">Open the book</button>
      <div class="footer">VOL. I · WITH LOVE</div>
    </section>

    <section id="menu" class="page menu hidden">
      <div class="eyebrow">Contents</div>
      <h1>For you, slowly.</h1>
      <p class="intro">Dear Aisy, it's in my faith that these series of words would make you feel loved. And whenever you feel alone, and I'm not near to comfort you, I hope these words will give you warmth and hope in love.</p>
      <div class="entries">
        <a class="entry" href="#p1"><span>01</span><strong>Roses are red, Violets are blue</strong><em>poem</em></a>
        <a class="entry" href="#p2"><span>02</span><strong>summer rain</strong><em>poem</em></a>
        <a class="entry" href="#p3"><span>03</span><strong>the fabric of the night</strong><em>poem</em></a>
        <a class="entry" href="#p4"><span>04</span><strong>A letter to Aisy</strong><em>letter</em></a>
      </div>
      <button class="button" onclick="show('cover')">Back to cover</button>
      <div class="footer">A BOOK OF WORDS · CONTENTS</div>
    </section>

    <section id="p1" class="page reading hidden">
      <div class="eyebrow">Poem 01</div>
      <h1>Roses are red, Violets are blue</h1>
      <p>Roses are red, violets are blue,
Time is a measure both fleeting and small,
Yet every brief cadence spent talking with you
Holds a gentle quietude lasting through all.
Though our story is young and our days are but few,
I cherish each conversation we share,
An elegant cosmos discovered anew
In every soft sentence suspended in air.
Though distance keeps eyes from beholding your face,
And miles stretch wide where our steps ought to meet,
Love is not governed by measure or space,
Nor bound by the ground underneath our feet.
So trust in this warmth that remains undismayed,
A truth that endures though the distance is wide;
For brief as our start was, the bridge has been made,
And you are the light that I carry inside.</p>
      <button class="button back" onclick="show('menu')">Back to contents</button>
    </section>

    <section id="p2" class="page reading hidden">
      <div class="eyebrow">Poem 02</div>
      <h1>summer rain</h1>
      <p>If you were the rain, I'd never open an umbrella. Instead, I'd lie on the cold street and enjoy every drop that falls on my skin. I'd be there, even if it meant drowning in you</p>
      <button class="button back" onclick="show('menu')">Back to contents</button>
    </section>

    <section id="p3" class="page reading hidden">
      <div class="eyebrow">Poem 03</div>
      <h1>the fabric of the night</h1>
      <p>If I could fold the horizon like a thread,
And gather up the miles into my palm,
I’d draw the distant sky where shadows tread
To bring your quiet morning to my calm.
For every ocean pales before the light
Of all you mean to me within this space;
I’d bend the very fabric of the night,
If only it would bring me to your face.</p>
      <button class="button back" onclick="show('menu')">Back to contents</button>
    </section>

    <section id="p4" class="page reading hidden">
      <div class="eyebrow">Final letter</div>
      <h1>A letter to Aisy</h1>
      <p>Dear Aisy, I hope these quiet words reach you as a sanctuary of warmth and comfort, wrapping around you like a gentle light across the distance. Were time not an unyielding boundary, I would devote every hour to writing you endless letters, lingering poems, and entire books just to articulate the quiet gravity of what you mean to me. But even in the brevity of this single page, know that you are my most cherished thought—a profound, constant truth that brightens everything it touches.</p>
      <button class="button back" onclick="show('menu')">Back to contents</button>
    </section>
  </main>

  <script>
    const ids = ['cover','menu','p1','p2','p3','p4'];
    function show(id){
      ids.forEach(x => document.getElementById(x).classList.toggle('hidden', x !== id));
      if(location.hash.slice(1) !== id) history.pushState(null, '', '#' + id);
      window.scrollTo(0,0);
    }
    function route(){
      const id = location.hash.slice(1);
      show(ids.includes(id) ? id : 'cover');
    }
    window.addEventListener('hashchange', route);
    window.addEventListener('popstate', route);
    route();
  </script>
</body>
</html># aisy