
``` r
df_couleurs <- tibble(col = c("#4B4B1D", "#92CDEB", "#AE320A", "#B724D3"), 
                      viz = c(" ", "  ", "   ", "    "))
```

# DT

``` r
# df_couleurs %>%
#   datatable() %>%
#   formatStyle(columns = "viz", valueColumns = "col",
#               backgroundColor = styleEqual(df_couleurs$col, df_couleurs$col))
```

# Kable

``` r
# df_couleurs %>%
#   mutate(viz = cell_spec(viz, background = df_couleurs$col)) %>%
#   kable(format = "html", escape = TRUE)
# 
# df_couleurs %>%
#   mutate(viz = cell_spec(viz, background = df_couleurs$col)) %>%
#   kable()
```

``` r
library(gt)

df_couleurs <- tibble(col = c("#4B4B1D", "#92CDEB", "#AE320A", "#B724D3"), 
                      viz = c(" ", "  ", "   ", "    ")) 

# tibble(col = c("#4B4B1D", "#92CDEB", "#AE320A", "#B724D3"), 
#                       viz = c(" ", "  ", "   ", "    ")) %>% 
#   mutate(Viz = 1:n())

df_couleurs %>% 
  gt() %>% 
  data_color(columns = vars(viz), colors = df_couleurs$col)
```

<!--html_preserve-->

<style>html {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Helvetica Neue', 'Fira Sans', 'Droid Sans', Arial, sans-serif;
}

#mdpjtumnzs .gt_table {
  display: table;
  border-collapse: collapse;
  margin-left: auto;
  margin-right: auto;
  color: #000000;
  font-size: 16px;
  background-color: #FFFFFF;
  /* table.background.color */
  width: auto;
  /* table.width */
  border-top-style: solid;
  /* table.border.top.style */
  border-top-width: 2px;
  /* table.border.top.width */
  border-top-color: #A8A8A8;
  /* table.border.top.color */
}

#mdpjtumnzs .gt_heading {
  background-color: #FFFFFF;
  /* heading.background.color */
  border-bottom-color: #FFFFFF;
}

#mdpjtumnzs .gt_title {
  color: #000000;
  font-size: 125%;
  /* heading.title.font.size */
  padding-top: 4px;
  /* heading.top.padding */
  padding-bottom: 1px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#mdpjtumnzs .gt_subtitle {
  color: #000000;
  font-size: 85%;
  /* heading.subtitle.font.size */
  padding-top: 1px;
  padding-bottom: 4px;
  /* heading.bottom.padding */
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#mdpjtumnzs .gt_bottom_border {
  border-bottom-style: solid;
  /* heading.border.bottom.style */
  border-bottom-width: 2px;
  /* heading.border.bottom.width */
  border-bottom-color: #A8A8A8;
  /* heading.border.bottom.color */
}

#mdpjtumnzs .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  padding-top: 4px;
  padding-bottom: 4px;
}

#mdpjtumnzs .gt_col_heading {
  color: #000000;
  background-color: #FFFFFF;
  /* column_labels.background.color */
  font-size: 16px;
  /* column_labels.font.size */
  font-weight: initial;
  /* column_labels.font.weight */
  vertical-align: middle;
  padding: 10px;
  margin: 10px;
}

#mdpjtumnzs .gt_sep_right {
  border-right: 5px solid #FFFFFF;
}

#mdpjtumnzs .gt_group_heading {
  padding: 8px;
  color: #000000;
  background-color: #FFFFFF;
  /* row_group.background.color */
  font-size: 16px;
  /* row_group.font.size */
  font-weight: initial;
  /* row_group.font.weight */
  border-top-style: solid;
  /* row_group.border.top.style */
  border-top-width: 2px;
  /* row_group.border.top.width */
  border-top-color: #A8A8A8;
  /* row_group.border.top.color */
  border-bottom-style: solid;
  /* row_group.border.bottom.style */
  border-bottom-width: 2px;
  /* row_group.border.bottom.width */
  border-bottom-color: #A8A8A8;
  /* row_group.border.bottom.color */
  vertical-align: middle;
}

#mdpjtumnzs .gt_empty_group_heading {
  padding: 0.5px;
  color: #000000;
  background-color: #FFFFFF;
  /* row_group.background.color */
  font-size: 16px;
  /* row_group.font.size */
  font-weight: initial;
  /* row_group.font.weight */
  border-top-style: solid;
  /* row_group.border.top.style */
  border-top-width: 2px;
  /* row_group.border.top.width */
  border-top-color: #A8A8A8;
  /* row_group.border.top.color */
  border-bottom-style: solid;
  /* row_group.border.bottom.style */
  border-bottom-width: 2px;
  /* row_group.border.bottom.width */
  border-bottom-color: #A8A8A8;
  /* row_group.border.bottom.color */
  vertical-align: middle;
}

#mdpjtumnzs .gt_striped {
  background-color: #f2f2f2;
}

#mdpjtumnzs .gt_from_md > :first-child {
  margin-top: 0;
}

#mdpjtumnzs .gt_from_md > :last-child {
  margin-bottom: 0;
}

#mdpjtumnzs .gt_row {
  padding: 8px;
  /* row.padding */
  margin: 10px;
  vertical-align: middle;
}

#mdpjtumnzs .gt_stub {
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #A8A8A8;
  padding-left: 12px;
}

#mdpjtumnzs .gt_summary_row {
  color: #000000;
  background-color: #FFFFFF;
  /* summary_row.background.color */
  padding: 8px;
  /* summary_row.padding */
  text-transform: inherit;
  /* summary_row.text_transform */
}

#mdpjtumnzs .gt_grand_summary_row {
  color: #000000;
  background-color: #FFFFFF;
  /* grand_summary_row.background.color */
  padding: 8px;
  /* grand_summary_row.padding */
  text-transform: inherit;
  /* grand_summary_row.text_transform */
}

#mdpjtumnzs .gt_first_summary_row {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
}

#mdpjtumnzs .gt_first_grand_summary_row {
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #A8A8A8;
}

#mdpjtumnzs .gt_table_body {
  border-top-style: solid;
  /* table_body.border.top.style */
  border-top-width: 2px;
  /* table_body.border.top.width */
  border-top-color: #A8A8A8;
  /* table_body.border.top.color */
  border-bottom-style: solid;
  /* table_body.border.bottom.style */
  border-bottom-width: 2px;
  /* table_body.border.bottom.width */
  border-bottom-color: #A8A8A8;
  /* table_body.border.bottom.color */
}

#mdpjtumnzs .gt_footnote {
  font-size: 90%;
  /* footnote.font.size */
  padding: 4px;
  /* footnote.padding */
}

#mdpjtumnzs .gt_sourcenote {
  font-size: 90%;
  /* sourcenote.font.size */
  padding: 4px;
  /* sourcenote.padding */
}

#mdpjtumnzs .gt_center {
  text-align: center;
}

#mdpjtumnzs .gt_left {
  text-align: left;
}

#mdpjtumnzs .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#mdpjtumnzs .gt_font_normal {
  font-weight: normal;
}

#mdpjtumnzs .gt_font_bold {
  font-weight: bold;
}

#mdpjtumnzs .gt_font_italic {
  font-style: italic;
}

#mdpjtumnzs .gt_super {
  font-size: 65%;
}

#mdpjtumnzs .gt_footnote_glyph {
  font-style: italic;
  font-size: 65%;
}
</style>

<div id="mdpjtumnzs" style="overflow-x:auto;">

<!--gt table start-->

<table class="gt_table">

<tr>

<th class="gt_col_heading gt_left" rowspan="1" colspan="1">

col

</th>

<th class="gt_col_heading gt_left" rowspan="1" colspan="1">

viz

</th>

</tr>

<tbody class="gt_table_body">

<tr>

<td class="gt_row gt_left">

\#4B4B1D

</td>

<td class="gt_row gt_left" style="background-color:#4B4B1D;color:#FFFFFFFF;">

</td>

</tr>

<tr>

<td class="gt_row gt_left gt_striped">

\#92CDEB

</td>

<td class="gt_row gt_left gt_striped" style="background-color:#92CDEB;color:#000000FF;">

</td>

</tr>

<tr>

<td class="gt_row gt_left">

\#AE320A

</td>

<td class="gt_row gt_left" style="background-color:#AE320A;color:#FFFFFFFF;">

</td>

</tr>

<tr>

<td class="gt_row gt_left gt_striped">

\#B724D3

</td>

<td class="gt_row gt_left gt_striped" style="background-color:#B724D3;color:#FFFFFFFF;">

</td>

</tr>

</tbody>

</table>

<!--gt table end-->

</div>

<!--/html_preserve-->

<FONT face="DIN Altermate">DIN Altermate</FONT>

<font face="DIN Altermate">abcdefghijklmnopqrstuvwxyz</font> <br>
<font face="DIN Altermate">ABCDEFGHIJKLMNOPQRSTUVWXYZ</font>
<font face="DIN Altermate">0123456789-\_@&\#$€</font><br>
