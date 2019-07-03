
# Communication

Matériel pour la communication (logo, affiche, flyer…)

## Chartre graphique

``` r
df_couleurs <-
  tribble(~Nom, ~`Nom complet`, ~Hexadécimal, ~RGB, ~Aperçu,
          "Gris", "Very dark grayish blue", "#4B4B4D", "rgb(75, 75, 77)", "",
          "Bleu", "Very soft blue", "#92C6EB", "rgb(146, 198, 235)", "",
          "Rouge", "Moderate pink", "#CE3F6A", "rgb(206, 63, 106)", "",
          "Beige", "Light grayish yellow", "#F7F4D3", "rgb(247, 244, 211)", "")

couleurs <- pull(df_couleurs, Hexadécimal)


df_couleurs %>%
  datatable(options = list(pageLength = nrow(df_couleurs),
                           dom = "t", ordering = FALSE),
            rownames = FALSE) %>%
  formatStyle(columns = 1:4, backgroundColor = "white") %>%
  formatStyle(columns = "Aperçu", valueColumns = "Hexadécimal",
              backgroundColor = styleEqual(couleurs, couleurs))
```

    ## PhantomJS not found. You can install it with webshot::install_phantomjs(). If it is installed, please make sure the phantomjs executable can be found via the PATH variable.

<!--html_preserve-->

<div id="htmlwidget-8acd97175edf2b35c1ed" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-8acd97175edf2b35c1ed">{"x":{"filter":"none","data":[["Gris","Bleu","Rouge","Beige"],["Very dark grayish blue","Very soft blue","Moderate pink","Light grayish yellow"],["#4B4B4D","#92C6EB","#CE3F6A","#F7F4D3"],["rgb(75, 75, 77)","rgb(146, 198, 235)","rgb(206, 63, 106)","rgb(247, 244, 211)"],["","","",""]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th>Nom<\/th>\n      <th>Nom complet<\/th>\n      <th>Hexadécimal<\/th>\n      <th>RGB<\/th>\n      <th>Aperçu<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"pageLength":4,"dom":"t","ordering":false,"order":[],"autoWidth":false,"orderClasses":false,"lengthMenu":[4,10,25,50,100],"rowCallback":"function(row, data) {\nvar value=data[0]; $(this.api().cell(row, 0).node()).css({'background-color':'white'});\nvar value=data[1]; $(this.api().cell(row, 1).node()).css({'background-color':'white'});\nvar value=data[2]; $(this.api().cell(row, 2).node()).css({'background-color':'white'});\nvar value=data[3]; $(this.api().cell(row, 3).node()).css({'background-color':'white'});\nvar value=data[2]; $(this.api().cell(row, 4).node()).css({'background-color':value == '#4B4B4D' ? '#4B4B4D' : value == '#92C6EB' ? '#92C6EB' : value == '#CE3F6A' ? '#CE3F6A' : value == '#F7F4D3' ? '#F7F4D3' : ''});\n}"}},"evals":["options.rowCallback"],"jsHooks":[]}</script>

<!--/html_preserve-->

``` r
# df_couleurs %>%
#   mutate(Aperçu = cell_spec(Aperçu, background = couleurs)) %>% 
#   # kable_styling()
#   kable()
```

Couleurs:
