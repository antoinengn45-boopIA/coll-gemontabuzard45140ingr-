<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Collège Montabuzard</title>
<style>
  body { margin:0; font-family: Arial, sans-serif; background:#f9f9f9; }
  header {
    display:flex;
    justify-content:space-between;
    align-items:center;
    background:#edf4f9;
    padding:10px 20px;
    position:sticky;
    top:0;
    z-index:1000;
    border-bottom:2px solid #ccc;
  }
  #search-bar { width:50%; padding:5px; font-size:16px; }
  #header-right { display:flex; align-items:center; gap:10px; }
  #header-right img { width:30px; }
  #content { padding:20px; }
  h1, h2 { margin:0 0 10px 0; }
  section { margin-bottom:30px; }
  .postits-container { display:flex; flex-wrap:wrap; gap:10px; }
  .postit {
    background:#fff8c6;
    border:1px solid #ffd700;
    border-radius:8px;
    padding:15px;
    width:250px;
    box-shadow:2px 2px 6px rgba(0,0,0,0.2);
    cursor:pointer;
    transition:transform 0.2s;
  }
  .postit:hover { transform: scale(1.05); }
  a { color:#0645AD; text-decoration:none; }
  a:hover { text-decoration:underline; }
  select { padding:5px; font-size:14px; }
</style>
</head>
<body>

<header>
  <input type="text" id="search-bar" placeholder="Rechercher...">
  <div id="header-right">
    <img src="https://upload.wikimedia.org/wikipedia/en/c/c3/Flag_of_France.svg" alt="Drapeau français" id="flag">
    <span>by Antoine</span>
  </div>
</header>

<div id="content">

  <!-- CHORALE -->
  <section>
    <h2>Informations Chorale</h2>
    <p>Ce courrier pour rappeler aux parents et aux élèves plusieurs dates clés pour la chorale.</p>
    <p>Mais avant tout, comme précisé dans la présentation de la chorale en début d'année, signée par vos soins, la chorale est une option facultative, un enseignement, et donc, toute absence est notifiée et apparait dans le bulletin. Les élèves de 3es sont notés, les autres niveaux sont évalués sur la base de compétences propres au chant choral, et une appréciation figure sur le bulletin. Il n'est pas possible de se désinscrire de ce cours, même avec un courrier de votre part. Si les élèves s'absentent volontairement, ils seront punis par le professeur.</p>

    <p><strong>Horaires :</strong><br>
    Semaine A : 6es-5es-4es, le mardi de 12h15 à 13h<br>
    Semaine B : 3es, le mardi de 12h15 à 13h</p>

    <p><strong>Les deux sorties et le concert sont obligatoires :</strong><br>
    Vendredi 10 avril 2026 de 8h15 à 16h30 : répétition de bassin avec repas froid prévu par les familles<br>
    Mardi 2 juin 2026, de 8h15 à 16h30 : répétition générale avec repas froid prévu par les familles<br>
    Mardi 2 juin à partir de 20h15 : Concert jusqu'à 22h30</p>

    <p>Les réservations pour le concert se feront sur internet.<br>
    Rapporter au professeur la carte orange SCHORALIA, pour la vérification des signatures et des assurances.<br>
    N'hésitez pas à prendre contact avec le collège dans le cas où vous souhaitez des renseignements complémentaires.<br>
    A très bientôt pour un moment musical inoubliable !</p>
  </section>

  <!-- PADLET MUSICAL -->
  <section>
    <h2>Padlet Musical</h2>
    <p><a href="https://padlet.com/devilliers/ca-tourne-action-l70on11x6g86/wish/Ae2Ravk03OL4Qnz4" target="_blank">Voir le Padlet musical complet</a></p>
    <div class="postits-container">
      <div class="postit">Eyes of the tiger - SOPRANO ALTO: Risin' up, back on the street, did my time, took my chances...</div>
      <div class="postit">Medley FUN - Danse la Carioca: Sais-tu danser la Carioca ?...</div>
      <div class="postit">Just Because of You - I’m begging on you, you know it's for you, good morning my love...</div>
      <div class="postit">City of Stars - Est-ce que tu brilles pour moi ce soir ? J’ai encore tant de choses à voir...</div>
      <div class="postit">The shape of my heart - He deals the cards as a meditation, the sacred geometry of chance...</div>
      <div class="postit">Medley Action - Mission Impossible, Live and Let Die, Skyfall...</div>
      <div class="postit">This is Me - I am brave, I am bruised, I am who I'm meant to be...</div>
    </div>
  </section>

  <!-- SANTE / AUDITION -->
  <section>
    <h2>Santé / Audition</h2>
    <p><a href="https://0451068s.index-education.net/pronote/FichiersExternes/acf93f027e2ef97b7f3feed6f657ba73df7219e24f5ea1fc80f94c062ec6fd65711ecb27df6cf5bc2521ebb90056aba9e91f20593ef39bf684556ac8fa3bde8f3c44e4fb7b765cd09699d855da6db329/planning%20audition.pdf?Session=1679027" target="_blank">Voir le planning audition</a></p>
  </section>

  <!-- LANGUE -->
  <section>
    <h2>Choisir la langue</h2>
    <select id="lang-select">
      <option value="fr">Français</option>
      <option value="en">English</option>
      <option value="es">Español</option>
      <option value="de">Deutsch</option>
    </select>
  </section>

</div>

<script>
  // Filtre post-its par recherche
  const searchBar = document.getElementById('search-bar');
  const postits = document.querySelectorAll('.postit');
  searchBar.addEventListener('input', function() {
    const query = this.value.toLowerCase();
    postits.forEach(p => {
      p.style.display = p.textContent.toLowerCase().includes(query) ? 'block' : 'none';
    });
  });

  // Changement de langue simulé
  const langSelect = document.getElementById('lang-select');
  langSelect.addEventListener('change', function() {
    alert('Le site passerait en ' + this.value + ' (fonctionnalité à implémenter).');
  });
</script>

</body>
</html>
