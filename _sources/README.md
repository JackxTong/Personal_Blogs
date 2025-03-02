Refer to

[Jupyter book](https://jupyterbook.org/en/stable/start/publish.html)

## Make Edits
To create a new .md or .ipynb file, need to add it to the `_toc.yml` file. 
Otherwise just make changes to the `.ipynb` notebooks or `.md` files directly, and run
```bash
jupyter-book build .
```
So that these changes appear in `_build/html/_sources`. 

Note i don't need to git push, instead just run
```bash
ghp-import -n -p -f _build/html
```
and the changes will show on the gh-pages branch on github remote.


## Github Actions
Under github settings/pages, can change `deploy from a branch` to `Github Actions`

Then need to build a `.github/workflows/deploy.yml` under main branch

It is responsible for auto-building, when you push to origin/main, 
it should automate the jupyter-book build process

The webpage is available [here](https://jackxtong.github.io/Personal_Blogs/)

