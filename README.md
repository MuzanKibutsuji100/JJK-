# JJK-
 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Jujutsu Legends: Character Creator</title>
  <style>
    body {
      background: #0b0b0b;
      color: #f2f2f2;
      font-family: 'Segoe UI', sans-serif;
      padding: 2em;
    }
    h1 { color: #ff3c3c; }
    label { display: block; margin: 1em 0 0.3em; }
    select, input {
      width: 100%;
      padding: 0.5em;
      background: #1c1c1c;
      border: 1px solid #333;
      color: #fff;
    }
    #preview {
      margin-top: 2em;
      background: #111;
      padding: 1em;
      border-radius: 10px;
    }
    .highlight {
      color: #ffcc00;
    }
  </style>
</head>
<body>

  <h1>Jujutsu Legends: Character Creation</h1>

  <label for="charName">Character Name</label>
  <input type="text" id="charName" placeholder="Enter your Jujutsu name">

  <label for="clan">Select Clan</label>
  <select id="clan">
    <option value="Gojo">Gojo Clan</option>
    <option value="Zenin">Zenin Clan</option>
    <option value="Kamo">Kamo Clan</option>
    <option value="Original">Original Clan</option>
  </select>

  <label for="technique">Cursed Technique</label>
  <select id="technique">
    <option value="Infinity Warp">Infinity Warp</option>
    <option value="Blood Thorn">Blood Thorn</option>
    <option value="Shadow Mirage">Shadow Mirage</option>
    <option value="Time Rend">Time Rend</option>
  </select>

  <label for="weapon">Weapon</label>
  <select id="weapon">
    <option value="Cursed Katana">Cursed Katana</option>
    <option value="Shadow Gauntlet">Shadow Gauntlet</option>
    <option value="Spirit Chains">Spirit Chains</option>
    <option value="None">None (Fist Fighter)</option>
  </select>

  <div id="preview">
    <h2>Character Preview</h2>
    <p><strong>Name:</strong> <span class="highlight" id="previewName">-</span></p>
    <p><strong>Clan:</strong> <span class="highlight" id="previewClan">-</span></p>
    <p><strong>Technique:</strong> <span class="highlight" id="previewTechnique">-</span></p>
    <p><strong>Weapon:</strong> <span class="highlight" id="previewWeapon">-</span></p>
  </div>

  <script>
    const updatePreview = () => {
      document.getElementById('previewName').innerText = document.getElementById('charName').value || '-';
      document.getElementById('previewClan').innerText = document.getElementById('clan').value;
      document.getElementById('previewTechnique').innerText = document.getElementById('technique').value;
      document.getElementById('previewWeapon').innerText = document.getElementById('weapon').value;
    };

    document.querySelectorAll('input, select').forEach(el => {
      el.addEventListener('input', updatePreview);
    });

    updatePreview(); // Initial preview
  </script>

</body>
</html>
