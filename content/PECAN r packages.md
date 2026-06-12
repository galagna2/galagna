> **How to Visualize PECAN Networks With R**. There are several possibilities to create network graphics with R. One useful R package for PECAN is the visNetwork package (Almende & Thieurmel, 2022) as it allows to create and edit networks. This feature is especially useful in clinical settings when patients want to add nodes or edges while viewing their network. The network graphics in this article were created by the PECAN2 package (Reichert & Vogel, 2024). The PECAN2 package is a wrapper around the visNetwork package with the purpose of simplifying the workflow of PECAN. It allows users to aggregate networks, calculate centrality measures, and use specific coloring and simplification. For visualization, the PECAN2 package can either be used to prepare data for the visNetwork package or to directly visualize them via visNetwork. The latter comes with a predefined setup of PECAN-specific defaults and enables simplification and coloring in one function. Example code on how to use the PECAN2 package can be found at https://github.com/JR-psych/PECAN2.

Here is a first try only using visNetwork: ![[PECAN-ACT_alpha.r]]
Here are some commands for [[PECAN2]]
Here is the Script for PECAN-ACT with [[PECAN2]]: ![[PECAN2.r]]
With this script you can print a centrality table like this:
```
## CENTRALITY MEASURES (out-degree, in-degree and feedback loops)
centrality_table <- pecanCen(
edges_df, 
nodes_df, 
centrality_by = "strength",   
sev_weighted = NULL, 
nodes_label = NULL, 
absV = FALSE
)

print(centrality_table)

# A tibble: 4 × 10
  id                degree_type out_degree out_connect per_degree per_out_connect in_degree in_connect per_indegree
  <chr>             <chr>            <dbl>       <int>      <dbl>           <dbl>     <dbl>      <int>        <dbl>
1 Awareness         Expected I…          5           3      0.192               1         9          3        0.346
2 Engagement        Expected I…          6           3      0.231               1         7          3        0.269
3 Life Satisfaction Expected I…          6           3      0.231               1         5          3        0.192
4 Openness          Expected I…          9           3      0.346               1         5          3        0.192
# ℹ 1 more variable: per_in_connect <dbl>
```

| Node              | Out-degree | In-Degree | Rel. Out-Impact | Rel. Vulnerability |
| :---------------- | ---------: | --------: | --------------: | -----------------: |
| Awareness         |          5 |         9 |           0.192 |              0.346 |
| Engagement        |          6 |         7 |           0.231 |              0.269 |
| Life Satisfaction |          6 |         5 |           0.231 |              0.192 |
| Openness          |          9 |         5 |           0.346 |              0.192 |
Out-degree: how much a node drives the networkd
In-degree: how much a node is driven by the network
out-connect: how many arrows go out
in-connect: how many arrows go in
per_degree (Rel. Out-Impact): How much a node (Openness) accounts for the total energy of the network (34.6%)
per_indegree (Rel. Vulnerability): How much a node (Awareness) absorbs the energy of the network