# docs
import nbformat as nbf

# Read the markdown content
with open("README.md", "r", encoding="utf-8") as f:
    md_content = f.read()

# Create a new Jupyter notebook
nb = nbf.v4.new_notebook()

# Add a single markdown cell with the README content
nb.cells.append(nbf.v4.new_markdown_cell(md_content))

# Save the notebook
with open("README.ipynb", "w", encoding="utf-8") as f:
    nbf.write(nb, f)

print("README.md has been converted to README.ipynb")
