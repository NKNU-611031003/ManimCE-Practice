# ManimCE-Practice
This page is only written to practice ManimCE related content, This page is only written for the practice of ManimCE related content, and some English are translated by Google, please forgive me if there is any inconsistency.

## How to use ManimCE with Google Colab
It is also possible to install Manim in a Google Colaboratory environment, but you will have to take care of that every time you start a new notebook in Google Colab.

### Install Manim and LaTex package
After creating a new notebook, paste the following code block in a cell, then execute it.
```python
!sudo apt update
!sudo apt install libcairo2-dev ffmpeg \
    texlive texlive-latex-extra texlive-fonts-extra \
    texlive-latex-recommended texlive-science \
    tipa libpango1.0-dev
!pip install manim
!pip install IPython --upgrade
```
For my personal habits, in order to ensure that LaTeX Traditional Chinese is displayed correctly, the following instructions are usually added
```python
!sudo apt install texlive-full
```
>Warning: using directives will increase load time

You should start to see Colab installing all the dependencies specified in these commands. After the execution has completed, you will be prompted to restart the runtime. Click the “restart runtime” button at the bottom of the cell output.

---
### Ready to use Manim in Colab
To check that everything works as expected, first import Manim by running
```python
from manim import *
```
Next, in all new code cell, ou must follow the format below to start running
```python
%%manim -qm -v WARNING Filename

class Filename(Scene):
   def construct(self):
      # manim command
```
You can change the name of *Filename*

### Source
See more in [Jupyter Notebooks - Manim Commiunity v0.16.0.posy()](https://docs.manim.community/en/stable/installation/jupyter.html#)

---
# Various types of math problems
Solve various types of math problems, make ManimCE animations, and save related code
