# GhostMc.Webstore 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>GhostMC Store</title>
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Press Start 2P', cursive;
      background-image: url('https://images.unsplash.com/photo-1622061608508-2f62cb063e0f?auto=format&fit=crop&w=1950&q=80');
      background-size: cover;
      background-position: center;
      color: white;
    }

    nav {
      background-color: rgba(0, 0, 0, 0.7);
      padding: 1rem;
      display: flex;
      justify-content: center;
      gap: 2rem;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-size: 1rem;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #00ffcc;
    }

    .page {
      display: none;
      padding: 2rem;
      text-align: center;
    }

    .page.active {
      display: block;
    }

    .rank {
      background-color: rgba(0, 0, 0, 0.6);
      margin: 1rem auto;
      padding: 1rem;
      width: 300px;
      border: 2px solid #00ffcc;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <nav>
    <a href="#" onclick="showPage('home')">Home</a>
    <a href="#" onclick="showPage('ranks')">Ranks</a>
    <a href="#" onclick="showPage('coins')">Coins</a>
    <a href="#" onclick="showPage('shop')">Shop</a>
    <a href="#" onclick="showPage('crates')">Crate Keys</a>
  </nav>

  <div id="home" class="page active">
    <h1>Welcome to GhostMC Store</h1>
    <p>Choose from ranks, crate keys, coins, and more!</p>
  </div>

  <div id="ranks" class="page">
    <h1>Ranks</h1>
    <div class="rank">
      <h2>VIP</h2>
      <p>Basic rank with perks</p>
    </div>
    <div class="rank">
      <h2>MVP</h2>
      <p>Advanced rank with extra features</p>
    </div>
  </div>

  <div id="coins" class="page">
    <h1>Coins - Coming Soon</h1>
  </div>

  <div id="shop" class="page">
    <h1>Shop - Coming Soon</h1>
  </div>

  <div id="crates" class="page">
    <h1>Crate Keys - Coming Soon</h1>
  </div>

  <script>
    function showPage(id) {
      document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
      document.getElementById(id).classList.add('active');
    }
  </script>
</body>
</html>
