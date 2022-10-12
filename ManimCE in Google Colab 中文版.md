# 如何在 Google Colab 中使用 ManimCE
Manim 也可以在 Google Colaboratory 環境中安裝，但是必須要注意，每次在 Google Colab 中開啟新筆記本時都需要重新安裝資源包。

## 安裝 Manim 和 LaTex 包
建立 Google Colab 新筆記本後，將下列指令貼在新建立的儲存格並執行
```python
!sudo apt update
!sudo apt install libcairo2-dev ffmpeg \
    texlive texlive-latex-extra texlive-fonts-extra \
    texlive-latex-recommended texlive-science \
    tipa libpango1.0-dev
!pip install manim
!pip install IPython --upgrade
```
對於我個人習慣，為了可以讓 LaTeX 可以順利顯示繁體中文，還會新增以下指令列
```python
!sudo apt install texlive-full
```
>注意：使用此指令列後會大幅增加載入時間

您應該開始看到 Colab 安裝了這些指令列中指定的所有項目。在運行完所有項目後，會出現警告訊息並要求重新啟動運行。此時請按下位於輸出格中的"restart runtime"按鈕，完成後即完成安裝動作。

---
## 開始使用 Manim 在 Google Colab 內
確認所有運行項目順利完成後，我們需要先載入 Manim 方便之後運行(可透過新儲存格運行一次即可)
```python
from manim import *
```
其次，在所有需要運行顯示的儲存格中，皆需要遵守以下的格式要求
```python
%%manim -qm -v WARNING 檔案名

class 檔案名(Scene):
   def construct(self):
      # Manim 指令區
```
你可以任意修改*檔案名*

# 資料來源
觀看詳細介紹 [Jupyter Notebooks - Manim Commiunity v0.16.0.posy()](https://docs.manim.community/en/stable/installation/jupyter.html#)
