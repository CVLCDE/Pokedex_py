# Pokedex_py
A Python Pokedex made with BeautifulSoup4 web scrapping and PyQt5. 

The program works by scrapping https://pokemondb.net/pokedex/all and grabs all rows related to each pokemon. The stats of each Pokemon are then placed into a nested dictionary, where the data will then be used to populate the various fields of the PyQt GUI. 

The name, number, typing, and pokemon's statistics are text values from the scrapped rows, however, the pokemon's image are grabbed using the request library. a GET request is made to https://img.pokemondb.net/artwork/ (with "pokemon_name".jpg appended to the end), where its contents are then loaded into a QPixmap object. The QPixmap object is then set to a QLabel in order for it to be drawn on to the screen. 

The PyQt5 was made using PyQt desisgner. I originally wrote the code manually, but it didn't come out the way I wanted it to and I figured it would be easier to just make everything in the designer. 

The file to run in your terminal or text editor is pokedex_py.py. I tried creating an executable for the file (found under the "dist" folder), but its not working so ¯\\_(ツ)_/¯.

It might take a little while for everything to load, since it has to scrap a lot of fields, but it shouldn't take more than 3 seconds to load. 

Everything within the main should scale proeprly as well. 

The only issue I have with this is that certain pokemon images will not load due to the formatting of the image_url. Any Mega, alolan, or special variant (like "Hero of Many Battles" Zamazenta) will not appear on the UI.

I plan to rewrite this in NodeJS and React but for now, I am pretty happy with this (barring its issues). 
