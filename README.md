# Creating a zip file to store the website files

import zipfile



# Define the file path for the zip archive

zip_file_path = "/mnt/data/black_mystery_website.zip"



# Create a zip archive

with zipfile.ZipFile(zip_file_path, "w") as zipf:

    # Creating the basic HTML structure

    html_content = """<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Black Mystery</title>

    <link rel="stylesheet" href="style.css">

</head>

<body>

    <header>

        <h1>Welcome to Black Mystery</h1>

        <p>Unraveling the Secrets of Black Holes</p>

    </header>

    <nav>

        <ul>

            <li><a href="index.html">Home</a></li>

            <li><a href="about.html">About</a></li>

            <li><a href="mystery.html">Mystery Zone</a></li>

            <li><a href="gallery.html">Gallery</a></li>

            <li><a href="contact.html">Contact</a></li>

        </ul>

    </nav>

    <main>

        <section>

            <h2>Exploring the Unknown</h2>

            <p>Delve into the enigmatic world of black holes and uncover the mysteries of the universe.</p>

        </section>

    </main>

    <footer>

        <p>&copy; 2025 Black Mystery. All rights reserved.</p>

    </footer>

</body>

</html>

"""

    # Creating the CSS file

    css_content = """body {

    margin: 0;

    font-family: Arial, sans-serif;

    background-color: black;

    color: white;

    text-align: center;

}

header {

    background: radial-gradient(circle, rgba(0,0,0,1) 30%, rgba(32,32,32,1) 100%);

    padding: 20px;

}

nav ul {

    list-style: none;

    padding: 0;

}

nav ul li {

    display: inline;

    margin: 10px;

}

nav ul li a {

    color: cyan;

    text-decoration: none;

    font-weight: bold;

}

main {

    padding: 20px;

}

footer {

    margin-top: 20px;

    padding: 10px;

    background: rgba(50,50,50,0.8);

}"""



    # Creating additional HTML pages

    about_content = "<h1>About Black Mystery</h1><p>Dedicated to uncovering black hole mysteries.</p>"

    mystery_content = "<h1>Mystery Zone</h1><p>Latest research and discoveries.</p>"

    gallery_content = "<h1>Gallery</h1><p>Cosmic images and black hole visuals.</p>"

    contact_content = "<h1>Contact</h1><p>Reach out to us for collaboration.</p>"



    # Writing files into the zip archive

    zipf.writestr("index.html", html_content)

    zipf.writestr("style.css", css_content)

    zipf.writestr("about.html", about_content)

    zipf.writestr("mystery.html", mystery_content)

    zipf.writestr("gallery.html", gallery_content)

    zipf.writestr("contact.html", contact_content)



# Provide the file for user download

zip_file_path
