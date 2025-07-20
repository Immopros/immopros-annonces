# immopros-annonces
site d'annoces d' immobillier d'entreprises et commerces 
Flask
web: python app.py
<!DOCTYPE html>
<html>
<head>
    <title>IMMOPROS - Annonces</title>
    <link rel="stylesheet" href="/static/style.css">
</head>
<body>
    <h1>IMMOPROS</h1>
    <a href="/poster">➕ Poster une annonce</a>
    <hr>
    {% for annonce in annonces %}
        <div class="annonce">
            <h2>{{ annonce.titre }}</h2>
            <p><strong>Catégorie :</strong> {{ annonce.categorie }}</p>
            <p>{{ annonce.description }}</p>
        </div>
    {% else %}
        <p>Aucune annonce pour l’instant.</p>
    {% endfor %}
</body>
</html>
<!DOCTYPE html>
<html>
<head>
    <title>Poster une annonce</title>
    <link rel="stylesheet" href="/static/style.css">
</head>
<body>
    <h1>Nouvelle annonce</h1>
    <form method="post">
        <label>Titre</label><br>
        <input type="text" name="titre"><br><br>

        <label>Description</label><br>
        <textarea name="description"></textarea><br><br>

        <label>Catégorie</label><br>
        <input type="text" name="categorie"><br><br>

        <button type="submit">Publier</button>
    </form>
</body>
</html>
body {
    font-family: Arial;
    padding: 20px;
    background-color: #f9f9f9;
}

h1 {
    color: #444;
}

.annonce {
    background: #fff;
    padding: 10px;
    border: 1px solid #ddd;
    margin-bottom: 20px;
}
cd ~/Bureau/IMMOPROS
git init
git remote add origin https://github.com/immopros/immopros.git
git add .
git commit -m "Premier envoi du site IMMOPROS"
git push -u origin main
