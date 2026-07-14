# Useful Links

- VM path : docker-projects/EQA-website/EQA-website/
- github repo : https://github.com/Center-for-Hybrid-Intelligence/EQA-website
- URL : https://staging.hybridintelligence.eu/eqa/contact.html
- Localhost URL : http://localhost:5010/home.html

# Localhost :

- First time : Clone the repo with "git clone https://github.com/Center-for-Hybrid-Intelligence/EQA-website"
- Open Docker
- Open a terminal in the CHI-Quantum-HR-Workflow-Assistant folder
- Run "docker compose up -d --build"
- Go to http://localhost:5010/home.html

# VM host / update :

- Connect to the staging VM
- Go to the right folder with "cd docker-projects/EQA-website/EQA-website/"
- "git pull" if you made changes
- Run "docker compose up -d --build"
- Go to https://staging.hybridintelligence.eu/eqa/contact.html


------

# Tips

To make a new page :
- Copy home.html
- Change the title of the tab (line 6)
- Add a new line to the header on every page and add the "active" class on the current html file
- Keep the current "main" structure : main > div "centeredContainer" > several sections (vertical segments) > content of each section

------

# Variables

Fonts used are Montserrat, Imperial for titles and ReenieBeanie if needed.


Colors used are:
- --primary #8f6deb and --secondary #fe8e21 for various colored content
- --dark #070a44 for basic text
- --light #e6e7ec for the header and footer
- --white #ffffff and --black #000000 for white and black

The other colors are unused now and were used in the V1 when the color palette was the one from the Quantum Flagship.

The background also comes from the Quantum Flagship and should be changed.

I made --header-size and --footer-size into variables because of how important their consistency is for the page structure..


-------

# Classes :

- img.logo : Used by the logo in the header
- a.active : Used by active links. Only used in the navigation menu in the header for now
#
- div.centeredContainer : The page's content zone in front of the background image, contains sections for vertical segmenting
- section.wideSection : Class applied to a section under the centered container to make it take all of the width ; can be used for a hero or a banner. Is not used at the moment.
- section.biSection : Used to have different content on the left and the right of the page (div.first and div.last), with 1/3 2/3 share and vertical centering. Is used in Contact.
- div.first and div.last : Designate the first and second element of a biSection.
#
- p.textParagraph : Basic text paragraph.
- p.justifText : Justified text, used in the bullet point list in the About page
- p.wpText : Justified text with increased margins, used in all the About page
- ul.textList : List containing text (li > p.justifText)

h1 titles are in Imperial, h5 are in ReenieBeanie, h2 to h4 and normal text use Montserrat
#
- ul.newsList : Used by the News list on the home page. Should be used with only 2 li inside
- img.newsImage : Image used in the newsList
- img.aboutPortrait : Used to make a portrait
- ul.resourceList : Same as news list but for more concise content. Can have up to four in a list
- img.resourceImage : Same as newsImage but for resources, has a lower max width
- ul.storiesList : List with horizontal short sentences. Contains up to 3 li > p