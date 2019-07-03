
``` r
df_couleurs <- tibble(col = c("#4B4B1D", "#92CDEB", "#AE320A", "#B724D3"), viz = "")
```

<!-- # DT -->

<!-- ```{r} -->

<!-- df_couleurs %>%  -->

<!--   datatable() %>% -->

<!--   formatStyle(columns = "viz", valueColumns = "col", -->

<!--               backgroundColor = styleEqual(df_couleurs$col, df_couleurs$col)) -->

<!-- ``` -->

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
