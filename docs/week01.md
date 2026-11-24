# Principles and Practices, Project Management

The first week of lectures focused on Project Management and how to effectively organize our workflow throughout the program.

Having some previous experience with GitLab, GitHub, and terminal commands gave me a good head start in setting up my workspace.

## Website

To start initializing my documentation page, I created a new repository on GitHub to host the website. After setting up the repository, I signed into GitHub directly through Visual Studio Code to connect the two, cloned the repository locally, and began working on it.

Using the integrated VS Code terminal, I created a Python virtual environment to isolate and install the required libraries. Specifically, I ran the following commands:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install zensical
zensical new .
```
After creating your page, you can start your page with 
```
zensical new
```
You can view the page on localhost:8000

### Tips for Markdown
* zensical.toml is the baseline file the holds the sctructure
* You can add the headpages and build the structure in the navigation bar by adding your pages in "nav".
```
nav = [
  { "Home" = "index.md" },
```
* To add maths in latex form you need to add the following in zensical.toml file:
```
extra_javascript = [
  "javascripts/mathjax.js",
  "https://unpkg.com/mathjax@3/es5/tex-mml-chtml.js"
]
```