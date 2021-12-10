# CLIP Mol

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/whitead/clipmol/blob/master/CLIPMol.ipynb)

Make molecules that look like a given text prompt. This was built using [SELFIES](https://github.com/aspuru-guzik-group/selfies) to generate the molecules, [rdkit](https://www.rdkit.org/) to draw the molecules, [CLIP](https://github.com/openai/CLIP) to compare the images to the text prompt, and [pymoo](https://pymoo.org) to optimize the molecules' agreement with CLIP.

Here are some examples:

### Bird
![Molecule that looks like a bird](https://raw.githubusercontent.com/whitead/clipmol/main/examples/bird.png)

### Cat
![Molecule that looks like a cat](https://raw.githubusercontent.com/whitead/clipmol/main/examples/cat.png)


### Fir Tree Animation
<details>
<summary>Click to show</summary>

![Time lapse of molecule turning into a fir tree](https://raw.githubusercontent.com/whitead/clipmol/main/examples/christmas.gif)

</details>


## FAQ

### Why does it suck?
It's true. CLIPMol works pretty poorly. I usually have to mess with the prompt and parameters a lot to get something nice. CLIP is maybe not suited for "line art" that we get from molecule structures. I'm actively looking for ideas to improve -- please open a [PR or Issue with ideas](https://github.com/whitead/clipmol).

### How does it work?
This uses pymoo to do multi-objective optimization with genetic algorithms. The objectives are (1) make a molecule of a minimum size (2) maximize similarity with text prompt and (3) maximize difference from the current best molecule (to encourage diversity).

### Why did you make this?
This is an example of finding a molecule that optimizes multiple objectives without a differentiable function -- which is quite similar to doing an experiment. So it is an interesting problem. On the other hand, this is kind of just for fun.

### Will you publish this?
When I have time, yes. If you find a way to make it better, you're welcome to be a co-author.

### How can I support this important work?

Follow me on Twitter [@andrewwhite01](https://twitter.com/andrewwhite01) or donate $500M to my university to fund an instute on computational emoji studies.
