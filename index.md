## Welcome to SwampStats

You can use the [editor on GitHub](https://github.com/bkurtz34/swampstats.github.io/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

title: "Team Talent Dashboard"
output:   flexdashboard::flex_dashboard:
    orientation: rows
    social: menu
    source_code: embed
---
### Team Talent Scores {data-width=650}
```{r team_talent}
team_talent %>% ungroup %>%filter(year==2020) %>%
  select(talent_rank,school,talent) %>%
  knitr::kable(team_talent,c("National Rank", "School", "Talent Score"))
```

###Conference Talent Rankings {data-width=350}
```{r conf_talent}
plot(conf_talent)
```

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/bkurtz34/swampstats.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
