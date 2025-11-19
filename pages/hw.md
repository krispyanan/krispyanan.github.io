---
layout: default
title: "Homework: Jekyll Webpage"
permalink: /homework/hw5/
---

# Homework 5: Jekyll Webpage
---

## Plot 1 – Top 10 License Types

**What this shows**

For this plot, I used the FA2022 professional licenses dataset and counted how many records there were for each “License Type.” I then took the top 10 most common ones. The bar chart makes it easy to see which license types show up the most. For example, teh variables DETECTIVE BOARD and COSMO have way more licenses than the other ones

**Design choices**

I used a horizontal bar chart because the license names are long and this makes them easier to read. The x axis is the number of licenses and the y axis is the license type. I also sorted the bars so the most common ones are at the top upfront so they're already neat and organized for whoever's looking at it. I kept the color simple and added tooltips so you can hover over and see the exact counts for each license.

<div id="hw5-vis1"></div>

---

## Plot 2 – License Status Breakdown for Top 5 Types

**What this shows**

For the second plot, I took the five most common license types from Plot 1 and looked at how each license status within are distributed. Each bar represents a license type, and each colored part of the bar represents a status like ACTIVE, NOT RENEWED, INACTIVE, and so on. Since the bars are normalized to 100%, you can compare the proportions instead of the raw counts. It's really interesting because you can see some license types favor and have a more common status than others. For example, Funeral licences have noticibally higher cancellations.

**Design choices & interactivity**

The x-axis is the license type and the y-axis shows the proportion of each status using a stacked bar. I used color to show the different license statuses. I added interactivity by making each status in the legend clickable. So when you click a status in the legend, that status becomes highlighted while the others fade. This makes it easier to focus on one status at a time and compare across license types.

<div id="hw5-vis2"></div>

---

## Data and Analysis Links

- **The Data:**  
  [licenses_fall2022.csv](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/licenses_fall2022.csv)

- **The Analysis Notebook:**  
  [Workbook (5).ipynb](https://github.com/krispyanan/krispyanan.github.io/blob/main/python_notebooks/Workbook%20(5).ipynb)

<!-- vega pls work -->
<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>

<script type="text/javascript">
  var spec1 = "{{ '/assets/json/hw5_plot1.json' | relative_url }}";
  vegaEmbed('#hw5-vis1', spec1).catch(console.error);

  var spec2 = "{{ '/assets/json/hw5_plot2.json' | relative_url }}";
  vegaEmbed('#hw5-vis2', spec2).catch(console.error);
</script>
