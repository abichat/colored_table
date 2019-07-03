
``` r
df_couleurs <- tibble(col = c("#4B4B1D", "#92CDEB", "#AE320A", "#B724D3"), viz = "")
```

# DT

``` r
df_couleurs %>% 
  datatable() %>%
  formatStyle(columns = "viz", valueColumns = "col",
              backgroundColor = styleEqual(df_couleurs$col, df_couleurs$col))
```

    ## PhantomJS not found. You can install it with webshot::install_phantomjs(). If it is installed, please make sure the phantomjs executable can be found via the PATH variable.

<!--html_preserve-->

<div id="htmlwidget-6e0202616cfaf004f70f" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-6e0202616cfaf004f70f">{"x":{"filter":"none","data":[["1","2","3","4"],["#4B4B1D","#92CDEB","#AE320A","#B724D3"],["","","",""]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> <\/th>\n      <th>col<\/th>\n      <th>viz<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"order":[],"autoWidth":false,"orderClasses":false,"columnDefs":[{"orderable":false,"targets":0}],"rowCallback":"function(row, data) {\nvar value=data[1]; $(this.api().cell(row, 2).node()).css({'background-color':value == '#4B4B1D' ? '#4B4B1D' : value == '#92CDEB' ? '#92CDEB' : value == '#AE320A' ? '#AE320A' : value == '#B724D3' ? '#B724D3' : ''});\n}"}},"evals":["options.rowCallback"],"jsHooks":[]}</script>

<!--/html_preserve-->

# Kable

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
