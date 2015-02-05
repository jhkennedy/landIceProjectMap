DOE Land Ice Models relation map
================================

Below is a preview of the map:

![DOE Land Ice Models reference map][map]

This map was created with the tikz package for LaTeX.

Get your copy:
--------------

You can download a `.pdf` by clicking [here][pdf] or a `.png` by clicking [here][mapRaw].
The `.png` version was created with ImageMagik using the comand:
```bash
convert main.pdf main.png
```
ImageMagik can convert to a number of different image 
[formats](http://www.imagemagick.org/script/formats.php).

If you would like to use this map in your LaTeX document, you can fork this repo 
into your own branch, or clone it with this command:
```
git clone git@github.com:jhkennedy/landIceProjectMap.git
```
Alternatively, you can download a `.zip` by clicking download link on the right.


How to insert this map into your LaTeX document:
------------------------------------------------

Once you have a copy of the source, you will need to link (or copy) `mapStyle.tex` 
and `mapCommands.tex` into your LaTeX document directory. Then place these lines 
in your document preamble (after your `\usepackage` declarations):
```latex
\usepackage{tikz}
\usetikzlibrary{shapes, arrows, calc, fit}
\input{mapStyle.tex}
```
To insert the map, place these lines wherever you want the map figure to be:
```latex
\begin{figure}[h!]
    \centering
    \begin{tikzpicture}[scale=2]
        \input{mapCommands.tex}
    \end{tikzpicture}
\end{figure}
```
You can adjust the size by changing the scale value. For a minimal example, see
`main.tex`.

Thats all folks!

[map]: https://github.com/jhkennedy/landIceProjectMap/blob/master/main.png
[mapRaw]: https://github.com/jhkennedy/landIceProjectMap/blob/master/main.png?raw=true
[pdf]: https://github.com/jhkennedy/landIceProjectMap/blob/master/main.pdf?raw=true
