
# CS50 Wiki

<div style="display:flex;flex-direction:row; justify-content; space-between;width:100%"> 
 <h3><b>Wiki</b> - Wikipedia-like online encyclopedia</h3>
  <h3>:rocket: <a  target="_blank" href="https://cbedroid-wiki.herokuapp.com"> Run Wiki Live </a></h3>  
</div>

Welcome to my [**Harvard University CS50 Wiki Project**](https://online-learning.harvard.edu/course/cs50s-web-programming-python-and-javascript?delta=0). I invite you to explore this repository and check out some of the cool features. In our project, our class was instructed to created a similar clone website to **Wikipedia** called **Wiki** using **Python's Django framework**.

For details on the `Specification` for this project, Please take a look at the [**Specification**](#specification) section below.


##

# Introduction

 ## So..what is this Wiki thing you keep babbling about :thinking: ?

This Wiki thing.. is an online encyclopedia much like [**Wikipedia**](https://www.wikipedia.org/). It contains numerous interesting articles about different topics. It's open-sourced so anyone can create and edit its entries. It's the 15th most popular website in the world. Oh yeah, did I mention it's **FREE**.

 In this project, our class was asked to design a similar website like Wikipedia and implement many of its original features. One of the most prominent features of this assignment was the use of [**`WikiText`**](https://en.wikipedia.org/wiki/Help:Wikitext), the markup language used to create entries on Wikipedia. In addition to building this website using `HTML`, `CSS`, and `JavaScript`, we had to make our own *`WikiText`* syntax using [**`Github's Markdown`**](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax)  along with creating Wiki entries for your website.

*For full detail description of CS50 Wiki, visit:* [**CS50 Wiki Full Description**](https://cs50.harvard.edu/web/2020/projects/1/wiki/#:~:text=web50/projects/2020/x/wiki)


---
# TechStack
Here are some of the tools used in this project.
- Python
- Django
- HTML
- CSS
- Javascript
- Bootstrap 4
---

# Prerequisites
- [**Python**](https://www.python.org) >= 3.6
- [**Django**](https://www.djangoproject.com/download/) >= 3.1.2

# Setup

- **Clone this Repo (Wiki branch)**
  ``` bash
   git clone https://github.com/cbedroid/CS50-Wiki.git
  
   # Change directory into repository folder
   cd CS50-Wiki 
  ```

- **Setup up virtual environment**
 ``` bash
   
   # If virtualenv is already installed on your system, skip this step here 
   apt-get install virtualenv 

   # Setup virtual env
   virtualenv venv
  
   # Activate virtual environment
   source venv/bin/activate
  ```

- **Install python requirements from `requirements.txt`**
  ``` bash
    pip install -r requirements.txt
  ```

- **Start Django server**
  ``` bash
  # First makemigrations and migrate to create database for the Django server
  python manage.py makemigrations

  python manage.py migrate

  # run server
  python manage.py runserver

  # Finally open your internet browser to localhost port: 8000

  localhost:8000 # copy this into your browser

  ```



# Specification

*For full detail description of CS50 Wiki, visit:* [**CS50 Wiki Full Specification**](https://cs50.harvard.edu/web/2020/projects/1/wiki/#:~:text=web50/projects/2020/x/wiki)

Complete the implementation of your Wiki encyclopedia. You must fulfill the following requirements:


- **Entry Page**: Visiting `/wiki/TITLE`, where `TITLE` is the title of an encyclopedia entry, should render a page that displays the contents of that encyclopedia entry.
  -  The view should get the content of the encyclopedia entry by calling the appropriate `util` function.

  - If an entry is requested that does not exist, the user should be presented with an error page indicating that their requested page was not found.

  - If the entry does exist, the user should be presented with a page that displays the content of the entry. The title of the page should include the name of the entry.

- **Index Page**: Update ***index.html*** such that, instead of merely listing the names of all pages in the encyclopedia, user can click on any entry name to be taken directly to that entry page.

- **Search**: Allow the user to type a query into the search box in the sidebar to search for an encyclopedia entry.
  - If the query matches the name of an encyclopedia entry, the user should be redirected to that entry’s page.

  - If the query does not match the name of an encyclopedia entry, the user should instead be taken to a search results page that displays a list of all encyclopedia entries that have the query as a substring. For example, if the search query were `Py`, then `Python` should appear in the search results.

  - Clicking on any of the entry names on the search results page should take the user to that entry’s page.

- **New Page**: Clicking ``“Create New Page”`` in the sidebar should take the user to a page where they can create a new encyclopedia entry.
Users should be able to enter a title for the page and, in a `textarea`, should be able to enter the Markdown content for the page.
  - Users should be able to click a button to save their new page.
  -  When the page is saved, if an encyclopedia entry already exists with the provided title, the user should be presented with an error message.
  - Otherwise, the encyclopedia entry should be saved to disk, and the user should be taken to the new entry’s page.

 - **Edit Page**: On each entry page, the user should be able to click a link to be taken to a page where the user can edit that entry’s Markdown content in a `textarea`.
   - The `textarea` should be pre-populated with the existing Markdown content of the page. (i.e., the existing content should be the initial `value` of the `textarea`).

   - The user should be able to click a button to save the changes made to the entry.

   - Once the entry is saved, the user should be redirected back to that entry’s page.
Random Page: Clicking “Random Page” in the sidebar should take user to a random encyclopedia entry.

- **Markdown to HTML Conversion**: On each entry’s page, any Markdown content in the entry file should be converted to HTML before being displayed to the user. You may use the python-markdown2 package to perform this conversion, installable via ***pip3 install markdown2***.
  - Challenge for those more comfortable: If you’re feeling more comfortable, try implementing the Markdown to HTML conversion without using any external libraries, supporting headings, boldface text, unordered lists, links, and paragraphs. You may find using **_regular expressions_** in Python helpful.

--- 

- Created with :heart: by [Cbedroid](https://github.com/cbedroid)

- For more projects - [Github](https://github.com/cbedroid)

- Follow me on Twitter - [Follow me](https://twitter.com/cbedroid)
