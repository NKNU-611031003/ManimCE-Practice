# Vedio
[](https://user-images.githubusercontent.com/105583349/195397090-560dbe8f-4945-4b6c-a486-03e8959676ac.mp4)

# Code
```python
from manim import *
```
###### Main Code
```python
class OP_Animate(Scene):
  def construct(self):
    # logo
    banner = ManimBanner(dark_theme=False)
    circle_banner = Circle(color="#ece6e2", fill_opacity=1).surround(banner).scale(2)
    # logo Text
    logo_Text = Text("Manim Community", font_size=48).shift(RIGHT)
    logo_MadeBy = Text("Made by", font_size=24).next_to(logo_Text, UP).shift(LEFT*2.5)
    logo_Web = Text("https://docs.manim.community/en/stable/index.html", font_size=16).next_to(logo_Text, DOWN)
    # Group
    banner_Group = VGroup(circle_banner, banner)
    logo_Text_Group = Group(logo_MadeBy, logo_Web)

    self.play(FadeIn(circle_banner), banner.create())
    self.play(banner.animate.scale(0.2), circle_banner.animate.scale(0.1))
    self.play(banner_Group.animate.next_to(logo_Text_Group, LEFT))
    self.play(FadeIn(logo_Text_Group), Write(logo_Text), run_time=2.5)
    self.wait(3)
    self.play(FadeOut(banner_Group), FadeOut(logo_Text_Group), FadeOut(logo_Text))
    self.wait()
```
