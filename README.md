
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

<div id="htmlwidget-c4ed59c524f526173c20" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-c4ed59c524f526173c20">{"x":{"filter":"none","data":[["Gris","Bleu","Rouge","Beige"],["Very dark grayish blue","Very soft blue","Moderate pink","Light grayish yellow"],["#4B4B4D","#92C6EB","#CE3F6A","#F7F4D3"],["rgb(75, 75, 77)","rgb(146, 198, 235)","rgb(206, 63, 106)","rgb(247, 244, 211)"],["","","",""]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th>Nom<\/th>\n      <th>Nom complet<\/th>\n      <th>Hexadécimal<\/th>\n      <th>RGB<\/th>\n      <th>Aperçu<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"pageLength":4,"dom":"t","ordering":false,"order":[],"autoWidth":false,"orderClasses":false,"lengthMenu":[4,10,25,50,100],"rowCallback":"function(row, data) {\nvar value=data[0]; $(this.api().cell(row, 0).node()).css({'background-color':'white'});\nvar value=data[1]; $(this.api().cell(row, 1).node()).css({'background-color':'white'});\nvar value=data[2]; $(this.api().cell(row, 2).node()).css({'background-color':'white'});\nvar value=data[3]; $(this.api().cell(row, 3).node()).css({'background-color':'white'});\nvar value=data[2]; $(this.api().cell(row, 4).node()).css({'background-color':value == '#4B4B4D' ? '#4B4B4D' : value == '#92C6EB' ? '#92C6EB' : value == '#CE3F6A' ? '#CE3F6A' : value == '#F7F4D3' ? '#F7F4D3' : ''});\n}"}},"evals":["options.rowCallback"],"jsHooks":[]}</script>

<!--/html_preserve-->

``` r
# df_couleurs %>%
#   mutate(Aperçu = cell_spec(Aperçu, background = couleurs)) %>% 
#   # kable_styling()
#   kable()
```

``` r
df_couleurs <- tibble(col = c("#4B4B1D", "#92CDEB", "#AE320A", "#B724D3"), viz = "")

df_couleurs %>% 
  datatable() %>%
  formatStyle(columns = "viz", valueColumns = "col",
              backgroundColor = styleEqual(df_couleurs$col, df_couleurs$col))
```

<!--html_preserve-->

<div id="htmlwidget-21881ff157f0619accc2" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-21881ff157f0619accc2">{"x":{"filter":"none","data":[["1","2","3","4"],["#4B4B1D","#92CDEB","#AE320A","#B724D3"],["","","",""]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> <\/th>\n      <th>col<\/th>\n      <th>viz<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"order":[],"autoWidth":false,"orderClasses":false,"columnDefs":[{"orderable":false,"targets":0}],"rowCallback":"function(row, data) {\nvar value=data[1]; $(this.api().cell(row, 2).node()).css({'background-color':value == '#4B4B1D' ? '#4B4B1D' : value == '#92CDEB' ? '#92CDEB' : value == '#AE320A' ? '#AE320A' : value == '#B724D3' ? '#B724D3' : ''});\n}"}},"evals":["options.rowCallback"],"jsHooks":[]}</script>

<!--/html_preserve-->

``` r
df_couleurs %>%
  mutate(viz = cell_spec(viz, background = df_couleurs$col)) %>%
  kable()
```

<table>

<thead>

<tr>

<th style="text-align:left;">

col

</th>

<th style="text-align:left;">

viz

</th>

</tr>

</thead>

<tbody>

<tr>

<td style="text-align:left;">

\#4B4B1D

</td>

<td style="text-align:left;">

\<span style=" border-radius: 4px; padding-right: 4px; padding-left:
4px; background-color: \#4B4B1D \!important;" \>\</span\>

</td>

</tr>

<tr>

<td style="text-align:left;">

\#92CDEB

</td>

<td style="text-align:left;">

\<span style=" border-radius: 4px; padding-right: 4px; padding-left:
4px; background-color: \#92CDEB \!important;" \>\</span\>

</td>

</tr>

<tr>

<td style="text-align:left;">

\#AE320A

</td>

<td style="text-align:left;">

\<span style=" border-radius: 4px; padding-right: 4px; padding-left:
4px; background-color: \#AE320A \!important;" \>\</span\>

</td>

</tr>

<tr>

<td style="text-align:left;">

\#B724D3

</td>

<td style="text-align:left;">

\<span style=" border-radius: 4px; padding-right: 4px; padding-left:
4px; background-color: \#B724D3 \!important;" \>\</span\>

</td>

</tr>

</tbody>

</table>

Couleurs:
