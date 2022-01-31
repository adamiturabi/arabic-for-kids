# arabic-for-kids

An instructor's course-book for teaching Arabic to non-native speaking children. Work-in-progress.

Incomplete work published here: https://adamiturabi.github.io/arabic-for-kids/

# Install software prerequisites

(For Ubuntu and derivatives)

1. Tex
   ```
   sudo apt install texlive-base
   sudo apt install texlive-xetex
   sudo apt install texlive-lang-arabic
   
   ```
2. Fonts
   + Scheherazade New: https://software.sil.org/scheherazade/download/
   + Microsoft Core Fonts:
   ```
   sudo add-apt-repository multiverse
   sudo apt update && sudo apt install ttf-mscorefonts-installer
   sudo fc-cache -f -v
   ```

3. Pandoc
   ```
   sudo apt install pandoc
   ```
   
4. R
   ```
   sudo apt install r-base
   sudo apt install libcurl4-openssl-dev libfontconfig1-dev libssl-dev libxml2-dev
   ```

5. Rmarkdown and Bookdown
   1. Open R in a terminal
      ```
      sudo R
      ```
   2. In R:
      ```
      install.packages("rmarkdown", dependencies = TRUE)
      install.packages("bookdown", dependencies = TRUE)
      install.packages("kableExtra", dependencies = TRUE)
      install.packages("tidyverse", dependencies = TRUE)
      install.packages("pander", dependencies = TRUE)
      q()
      ```

# Building the book from source files

In a Linux terminal:

```
cd path-to-your-preferred-dir
git clone https://github.com/adamiturabi/arabic-for-kids.git
cd arabic-for-kids
./buildscript
```

The created files will be under the `_book` directory. Open `docs/index.html` in a browser and `_book/_main.pdf` in a PDF viewer.

To delete created files in order to do a clean build:

```
./cleanbuild
```

