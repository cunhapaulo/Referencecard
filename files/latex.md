## Ampliando o LaTeX

### Escrever novos comandos
  ```latex
  \newcommand{\NAME}[NUMBER] { COMMANDS }
```

### Definições
  ```latex
  \def \askesis {\textit{áskesis}\xspace}
  ```

## Escrever em mais de um idioma (`Multilingual text`)
```latex
% No cabeçalho:
\usepackage[english, german, greek, main=brazilian]{babel}
\babelprovide[import]{greek}

% Uso no corpo do texto:
\foreignlanguage{greek}{αλέθεια}

% macros criadas para simplificar:
\newcommand{\grego}[2] {\foreignlanguage{greek}{#1}, \textit{#2}\xspace }
\def \aleteia     {\grego{αλέθεια}{alétheia}}
```
## Duas figuras em uma mesma linha
```latex
\begin{figure}[h]
\begin{subfigure}[b]{0.385\textwidth}
      \centering
      \includegraphics[width=5cm]{./img/tetraktys.jpg}
      $1+2+3+4=10$
      \caption{Exemplo de tetraktys.} \label{fig:1a}
\end{subfigure}
\begin{subfigure}[b]{0.615\textwidth}
      \centering
      \includegraphics[width=8cm]{./img/tetraktys_geometria.png}
      \caption{Geração a partir da unidade.} \label{fig:1b}
\end{subfigure}
\caption{Representações pitagoricas geometrico-numericas das quantidades.}
\label{fig:1}
\end{figure}
```
Resultado:

![image](https://user-images.githubusercontent.com/28146759/174351910-3f46df1d-f96e-40e5-86cb-cfe672d395c0.png)


## Comandos importantes
- `\xspace` acrescenta, de forma inteligente, espaços ao final de um texto definido através de um `\def`.
- `\def \name {definition}`

## Argumentos no Cabeçalho YAML

- `aspectratio=169:` muda a razão de proporção.
- `header-includes: |` usado para inserir pacotes.

## Diagrama
```latex
\begin{figure}[h]
	$$
		\text{Filosofia}
		\begin{cases}
			{\text{Teoria da Ciência}}
			\begin{cases}
				{\text{Formal: \textit{Lógica}}} \\ \\
				{\text{Material: \textbf{\color{blue} \textit{Teoria do Conhecimento}}}}
				\begin{cases}
					{\text{\textit{Geral}}}    \\
					{\text{\textit{Especial}}} \\
				\end{cases}        \\
			\end{cases} \\ \\

			{\text{Teoria dos Valores}}
			\begin{cases}
				{\text{Éticos}: \textit{Ética}}                     \\
				{\text{Estéticos}: \textit{Estética}}               \\
				{\text{Religiosos}: \textit{Filosofia da Religião}} \\
			\end{cases} \\ \\

			{\text{Concepção do Universo}}
			\begin{cases}
				{\text{Metafísica}}
				\begin{cases}
					{\text{\textit{Metafísica da Natureza}}} \\
					{\text{\textit{Metafísica do Espírito}}} \\
				\end{cases} \\ \\
				{\text{\textit{Teoria} do Universo}}
				\begin{cases}
					{Deus}         \\
					{Liberdade}    \\
					{Imortalidade} \\
				\end{cases} \\
			\end{cases} \\
		\end{cases}
	$$
	\\
	\caption{Divisão da Filosofia segundo \citeonline{Hessen1980}.}
	\label{fig::filosofia}
\end{figure}
```
Resultado:

![image](https://user-images.githubusercontent.com/28146759/174417375-264886ac-718d-4818-bcc8-1b10f6d61117.png)



## CÓDIGO LATEX NO TEXTO MARKDOWN:

1. Inserir no cabeçalho YAML a sessão para incluir no cabeçalho **header-includes**:

    ``` latex
    ---
    # YAML Header
    #
    header-includes: |
        \usepackage{tikz,pgfplots}
    ---
    ```
2. Inserir o **código LaTeX** no texto **Markdown**:

   ```latex
   \begin{center}
       \begin{tikzpicture}[->,>=stealth',shorten >=1pt,auto,node distance=3.5cm,
       thick,main node/.style={circle,fill=blue!20,draw,font=\sffamily\Large\bfseries}]

       \node[main node] (1) {1};
       \node[main node] (2) [below left of=1] {2};

       (8) edge node [left] {0.2} (7)
           edge [loop right] node {0.6} (8)
           edge [bend right] node[right] {0.2} (5);

   \end{tikzpicture}
   \end{center}
   ```

.
## FONTES IMPORTANTES PARA O LATEX

- **XeLaTeX command to use fonts**:
  ```latex
  \setmainfont[Ligatures=TeX]{Linux Libertine O}
  ```
- **Localização**: 
  - `C:\Program Files (x86)\TeXmacs\fonts\truetype`
  - `C:\Users\paulo.cunha.TJ.PA.GOV.BR\AppData\Local\Microsoft\Windows\Fonts`
  - `C:\Users\paulo.cunha.TJ.PA.GOV.BR\AppData\Roaming\MiKTeX\fonts\opentype`
  - `C:\Users\paulo.cunha.TJ.PA.GOV.BR\OneDrive\_LaTeX\_TYPEFACES\`
.
- **Antiqua**
.
- **Palatino**
.
- **Charter**
  ``` latex
  \usefonttheme{serif} % change font to allow \textbf{}
  \usepackage{charter} % Nicer fonts
  ```
.
- **Fira** 
  > Uso: (`Metropolis`)
  > - Fonte utilizada no estilo [METROPOLIS](https://github.com/matze/mtheme). Está disponível na forma de um um _package_ do LaTeX, sob o nome `Fira` em `\Fonts\Outline fonts`no MiKTeX.

.
- **Flama** 
  > Uso: (`HSRM`) 
  > - Fonte utilizada pelo estilo [HSRM`(Hochschule RheinMain)` ](https://github.com/benjamin-weiss/hsrmbeamertheme) para slides `Beamer`, criado por _Benjamin Weiss_.
  > - Download: [Font Geek](https://fontsgeek.com/flama-font?ref=readme).

.
- **Biolinum** e **Libertine** 
  > Uso: (`ACM`)
  > - Fonte utilizada nos modelos de artigos da `ACM`.
  > - Download: [Font Squirrel - Biolinum](https://www.fontsquirrel.com/fonts/linux-biolinum)  e [DaFont - Libertine](https://www.dafont.com/pt/linux-libertine.font?text=Haskell+is+a+Functional+Programming+Language)
  > - [Site da ACM](https://www.acm.org/publications/taps/accepted-latex-packages)

.
- **Linux Libertine O**
  ``` latex
  \setmainfont[Ligatures=TeX]{Linux Libertine O}
  ```
.
## ESTILOS E THEMAS IMPORTANTES
- **EISVOGEL**
    Template para documentos
    Site: https://github.com/Wandmalfarbe/pandoc-latex-template
- **Metropolis** 
    Site: [https://github.com/matze/mtheme](https://github.com/matze/mtheme)
- **HSRM** 
Site da universidade: [https://www.hs-rm.de](https://www.hs-rm.de/de/hochschule/personen/hofmann-karl-heinrich/service-latex/beamer-latex)
    Site: [Hochschule RheinMain Beamer Thema](https://github.com/benjamin-weiss/hsrmbeamertheme)

.
## CONTRIBUIÇÕES INTERESSANTES

- Impressão na forma de _handout_
  ``` latex
    $if(handout)$
    \usepackage{pgfpages}
    %\pgfpagesuselayout{2 on 1}[a4paper,border shrink=3mm]
    \pgfpagesuselayout{4 on 1}[a4paper,border shrink=4mm,landscape]
    $endif$
  ```
- Estilos de Fontes para o LaTeX
  > \usepackage[tt=false]{**antiqua**}
  > \usepackage[tt=false]{**palatino}**
  > \usepackage[tt=false]{**libertine**}

- Penn State University

    ```latex
    \definecolor{mpigreen}{HTML}{007977}
    \setbeamercolor{frametitle}{bg=mpigreen}
    ```

- Código **LaTeX** para diferenciar números menores que 10:
  ``` latex  
  \def\artnum#1{\ifnum#1<10 #1º\else #1\fi}

  \artnum{12}

  \newcommand{\arti}[2][]{(art.~\bold{\artnum{#2}}#1)}
  \newcommand{\artii}[3][]{(art.~\bold{\artnum{#2}},~\bold{#3}#1)}
  \newcommand{\artiii}[4][]{(art.~\bold{\artnum{#2}},~\bold{#3}~``\bold{#4}''#1)}
  ```

- Numeração diferente nos Anexos (Appendix) em LaTeX
  ```latex
  <!-- 
  ******************************** A P E N D I C E S ******************************** 
  \renewcommand{\thesection}{\arabic{section}}
  -->

  \appendix

  \newcounter{iSECTION}
  \newcounter{iSUBSECTION}
  \newcounter{iSUBSUBSECTION}

  \def \beginNewChapter{\beginNewSection}
  \def \beginNewSection{\setcounter{iSECTION}{0}}
  \def \beginNewSubsection{\setcounter{iSUBSECTION}{0}}
  \def \beginNewSubsubsection{\setcounter{iSUBSUBSECTION}{0}}


  \renewcommand{\thechapter}{\Alph{chapter}}

  \renewcommand{\section}[1]{
          \refstepcounter{iSECTION}
          \beginNewSubsection
          \vspace{.75cm}
          \textbf{\Large{\theiSECTION \hspace{.1cm} #1}}
          \vspace{.4cm}}

  \renewcommand{\subsection}[1]{
          \refstepcounter{iSUBSECTION}
          \beginNewSubsubsection
          \textbf{\theiSECTION.\theiSUBSECTION} \hspace{.1cm} #1}

  \renewcommand{\subsubsection}[1]{
          \refstepcounter{iSUBSUBSECTION}
          \begin{quote}
          \textbf{\theiSECTION.\theiSUBSECTION.\theiSUBSUBSECTION} \hspace{.1cm} #1
          \end{quote}
  }

  ```


- Resolving the problem with {.standout} slides corrupting the following ones **(Metropolis)**:
  ```markdown
  header-includes: 
      - \usepackage[portuges]{babel}
      # - \usepackage[tt=false]{antiqua}
      # - \usepackage[tt=false]{palatino}
      # - \usepackage[tt=false]{libertine}
      # - \usepackage{multicol}
      # - \usepackage{tabularx}
      # - \usepackage{array}
      # - \usepackage{longtable}
      - '\usetheme{metropolis}'
      - '\makeatletter'
      - '\beamer@ignorenonframefalse'
      - '\makeatother'
  
  ```

-  Usar fontes do modelo **ACM**
   ```latex
      \usepackage{tikz,pgfplots}
      \usepackage[T1]{fontenc} 
      \usepackage[tt=false]{libertine} 
      \setmonofont{inconsolata} 
      \usepackage[varqu]{zi4} 
      \usepackage[libertine]{newtxmath}
    ```
  
  - Modificações feitas por Paulo Cunha:
  
    ``` latex
    %---- begin(paulo.cunha)------------------------------------------------

    %---------------------------------------------------------------------
    % Colors
    %---------------------------------------------------------------------
    \definecolor{red}{rgb}{0.75,0.10,0.20}
    \definecolor{red2}{RGB}{150,0,0}
    \definecolor{blue}{rgb}{0.00,0.25,0.71}
    \definecolor{blue2}{RGB}{36, 25, 200}
    \definecolor{orange}{RGB}{255, 69, 0}
    \definecolor{orange2}{RGB}{255, 94, 14}
    \definecolor{black}{RGB}{100, 100, 100}

    \newcommand{\laranja}[1]{\textcolor{orange}{#1}}
    \newcommand{\azul}[1]{\textcolor{blue2}{#1}}
    \newcommand{\vermelho}[1]{\textcolor{red2}{#1}}
    \newcommand{\negro}[1]{\textcolor{black}{#1}}

    %---------------------------------------------------------------------
    % Markers \sout and \emph
    %---------------------------------------------------------------------
    %\setbeamerfont{negrito}{family=\Medium}
    %\renewcommand{\textbf}[1]{{\usebeamerfont{negrito}\negro{#1}}}
    \renewcommand{\textbf}[1]{{\Medium \negro{#1}}}
    \renewcommand{\emph}[1]{\laranja{#1}}

    \newcommand{\sout}[1]{\azul{#1}}
    \newcommand{\tightlist}{}

    \setbeamercolor{progress bar}{fg=orange,bg=orange2}

    $if(handout)$
    \usepackage{pgfpages}
    %\pgfpagesuselayout{2 on 1}[a4paper,border shrink=3mm]
    \pgfpagesuselayout{4 on 1}[a4paper,border shrink=4mm,landscape]
    $endif$

    %---- end(paulo.cunha)------------------------------------------------

    ```