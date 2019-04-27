# LaTex handler
<h1>Transforming LaTeX accents to UTF8</h1>

A simple Python script providing a self-contained functionality for transforming accented characters of LaTex into their equivalent UTF8.

<h2>A sample usage</h2>

 ```python
    import LaTexAccents as TeX
    
    T_encode = TeX.LaTexAccents_to_UTF8() # initialize the accent transformer class instance

     s = 'This t\\"{e}xt cont\\.ains Lat\\`ex ac\\^{c}ents'  #some string containig (or not) Tex accents
     # the result of print(s) (to see the actual string without espace characters)
     # This t\"{e}xt cont\.ains Lat\`ex ac\^{c}ents
    
     s1 = T_encode.decode_Tex_Accents(s) # replacing accents by UTF8
     # the result of print(s1)
     # This tëxt contȧins Latèx acĉents
  ```
    

<h4>Motivation</h4>

A variant of this script is intended to be used in <a href="https://www.scilag.net">SciLag</a> a community project dedicated to open problems in mathematics. We thought to share it here, as this might be potentially useful in some routine tasks with Latex format.

<h4>Version</h4>

This is version 0.1 and might be subject to change. The list of current accents might not be complete, however, one may easily add more a translation rules from accents to UTF8 adding new rules
inside function `create_Translation_Rules`.
