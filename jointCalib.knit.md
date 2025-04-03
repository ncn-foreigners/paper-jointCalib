---
title: "jointCalib: A Joint Calibration of Totals and Quantiles"
date: "2025-04-03"
abstract: >
  An abstract of less than 150 words.
draft: true
editor: source
author:  
  - name: Maciej Beręsewicz
    affiliation: 
      Poznań University of Economics and Business
      Statistical Office in Poznań
    address:
    - Department of Statistics, Al. Niepodległości 10, 61-875 Poznań, Poland
    - Centre for the Methodology of Population Studies, Wojska Polskiego 27/29, 60-624 Poznań Poland
    url: https://www.britannica.com/animal/quokka
    orcid: 0000-0002-8281-4301
    email:  maciej.beresewicz@ue.poznan.pl
  - name: Marcin Szymkowiak
    affiliation:
      Poznań University of Economics and Business
      Statistical Office in Poznań
    address:
    - Department of Statistics, Al. Niepodległości 10, 61-875 Poznań, Poland
    - Wojska Polskiego 27/29, 60-624 Poznań Poland
    url: https://www.britannica.com/animal/bilby
    email: marcin.szymkowiak@ue.poznan.pl
    orcid: 0000-0003-3432-4364
type: package
output: 
  rjtools::rjournal_article:
    self_contained: yes
    toc: no
bibliography: RJreferences.bib
---



# Introduction

Interactive data graphics provides plots that allow users to interact
them. One of the most basic types of interaction is through tooltips,
where users are provided additional information about elements in the
plot by moving the cursor over the plot.

This paper will first review some R packages on interactive graphics and
their tooltip implementations. A new package \CRANpkg{ToOoOlTiPs} that
provides customized tooltips for plot, is introduced. Some example plots
will then be given to showcase how these tooltips help users to better
read the graphics.

# Background

Some packages on interactive graphics include \CRANpkg{plotly} [@plotly]
that interfaces with Javascript for web-based interactive graphics,
\CRANpkg{crosstalk} [@crosstalk] that specializes cross-linking elements
across individual graphics. The recent R Journal paper
\CRANpkg{tsibbletalk} [@RJ-2021-050] provides a good example of
including interactive graphics into an article for the journal. It has
both a set of linked plots, and also an animated gif example,
illustrating linking between time series plots and feature summaries.

# Customizing tooltip design with \pkg{ToOoOlTiPs}

\pkg{ToOoOlTiPs} is a packages for customizing tooltips in interactive
graphics, it features these possibilities.

# A gallery of tooltips examples

The \CRANpkg{palmerpenguins} data [@palmerpenguins] features three
penguin species which has a lovely illustration by Alison Horst in
Figure \@ref(fig:penguins-alison).

\begin{figure}
\includegraphics[width=1\linewidth,height=0.3\textheight,alt={A picture of three different penguins with their species: Chinstrap, Gentoo, and Adelie. }]{figures/penguins} \caption{Artwork by \@allison\_horst}(\#fig:penguins-alison)
\end{figure}

Table
\@ref(tab:penguins-tab-static)
prints at the first few rows of the `penguins` data:



\begin{table}
\centering
\caption{(\#tab:penguins-tab-static)A basic table}
\centering
\fontsize{7}{9}\selectfont
\begin{tabular}[t]{l|l|r|r|r|r|l|r}
\hline
species & island & bill\_length\_mm & bill\_depth\_mm & flipper\_length\_mm & body\_mass\_g & sex & year\\
\hline
Adelie & Torgersen & 39.1 & 18.7 & 181 & 3750 & male & 2007\\
\hline
Adelie & Torgersen & 39.5 & 17.4 & 186 & 3800 & female & 2007\\
\hline
Adelie & Torgersen & 40.3 & 18.0 & 195 & 3250 & female & 2007\\
\hline
Adelie & Torgersen & NA & NA & NA & NA & NA & 2007\\
\hline
Adelie & Torgersen & 36.7 & 19.3 & 193 & 3450 & female & 2007\\
\hline
Adelie & Torgersen & 39.3 & 20.6 & 190 & 3650 & male & 2007\\
\hline
\end{tabular}
\end{table}

Figure
\@ref(fig:penguins-ggplot)
shows an  plot of
the penguins data, made using the
\CRANpkg{ggplot2}
package.




``` r
penguins %>% 
  ggplot(aes(x = bill_depth_mm, y = bill_length_mm, 
             color = species)) + 
  geom_point()
```

\begin{figure}
\includegraphics[width=1\linewidth]{jointCalib_files/figure-latex/penguins-ggplot-1} \caption{A basic non-interactive plot made with the ggplot2 package on palmer penguin data. Three species of penguins are plotted with bill depth on the x-axis and bill length on the y-axis. Visit the online article to access the interactive version made with the plotly package.}(\#fig:penguins-ggplot)
\end{figure}

# Summary

We have displayed various tooltips that are available in the package
\pkg{ToOoOlTiPs}.

# References

