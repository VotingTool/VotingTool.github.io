## Welcome to the Online Voting Tool

The Online Voting Tool presented by the Computational Social Choice research group at Technical University of Munich (TUM) offers an easy-to-use tool to compute [maximal lotteries](http://fishburn.ml/) and other voting rules.
You can test it under [voting.ml](https://voting.ml) and learn more about social choice [here](http://dss.in.tum.de/14-research/research-projects/56-algorithmic-game-theory-and-computational-social-choice.html).

---
## Main Features
<table>
<tbody>
<tr>
  <td>
  <ul>
  <li><p><b>Pairwise Social Choice Functions</b>: Borda, Nanson, Baldwin, Black, MaxiMin, Tideman, Copeland, Uncovered Set, Essetinal Set, and Bipartisan Set</p></li>
  <li><p><b>Rank-Based Social Choice Functions</b>: Plurality, Plurality with Runoff, Instant Runoff, Anti-Plurality, Bucklin, and Coombs</p></li>
  <li><p><b>Social Decision Schemes</b>: Maximal Lottery, Random Dictatorship, and Proportional Borda</p></li>
  <li><p><b>Social Welfare Functions</b>: Kemeny, Schulze, and Ranked Pairs</p></li>
  <li><p><b>Random voting instances</b>: Generation of random preference profiles with or without Condorcet winners, and of random majority matrices with bounded weights</p></li>
  <li><p><b>Minimal profiles</b>: Generation of preference profiles with minimal number of voters for a given majority matrix</p></li>
  <li><p><b>Profile import and export</b> via URL query string</p></li>
  <li><p><b>Examination</b> for (weak) Condorcet winner(s), Pareto-dominated alternatives, and components in the weighted majority graph</p></li>
  </ul>
  </td>
</tr></tbody></table>

### Maintenance
* System status and uptime statistics can be checked at: [status.voting.ml](https://status.voting.ml/)
* Press ? on your keyboard for an overview of keyboard shortcuts.
* For questions or feedback, please contact us at <feedback@voting.ml>.

## Theoretical Details

### Majority Margins
The majority margin \\(M\_{x,y}\\) between a pair of alternatives \\(x\\) and \\(y\\) is the the number of voters in \\(N\\) who strictly prefer \\(x\\) to \\(y\\) minus the number of voters who strictly prefer \\(y\\) to \\(x\\):

\\[ M\_{x,y} = \vert\\{i \in N: x \succ\_i y\\}\vert - \vert\\{i \in N: y \succ\_i x\\}\vert.  \\]

The majority margins between all pairs of alternatives for a given preference profile \\(R\\) are represented by a skew-symmetric matrix \\(M^R\\) whose rows and columns are indexed by alternatives. Voting rules which only depend on \\(M^R\\) are called *pairwise* or, following a proposal by Fishburn, *C2 rules*.

<img src="assets/img/computer.png" width="20"> You can directly manipulate the majorty margin matrix \\(M^R\\) by clicking on `Edit` or any entry in the matrix. After you `Save` the matrix again, a corresponding preference profile is computed. For easy instances, Integer Linear Programming is used and returns a preference profile with a minimal number of voters. A green notification indicates the minimality. Otherwise, a heuristics computes a good approximation with few voters.

### Maximal Lotteries
Maximal lottery schemes return an optimal mixed strategy of the symmetric zero-sum game induced by the (\\(\tau\\)-scaled) majority margins. Formally, the set of maximal lotteries in the preference profile \\(R\\) with respect to \\(\tau\\) among the set of all lotteries \\(\Delta(A)\\) over the alternatives \\(A\\) is as follows:
\\[ \mathit{ML}^{\tau} (R) = \\{p\in\Delta(A)\colon\ p^t{\tau(M^R)}\ge 0\\}, \\]
where \\( {\tau}\colon\mathbb Z\rightarrow \mathbb R \\), \\({\tau(1)} = 1 \\) is *odd* and *monotone*.

<img src="assets/img/computer.png" width="20"> The default option for \\(\tau\\) is the identity function. However, you can choose another \\(\tau\\) in the form of \\(\tau(x)=x^k\\) by modifying the *majority margin exponent* \\(k\\) in the settings.

Further references:

* [Fishburn.ml](http://fishburn.ml/)
* [English Wikipedia](https://en.wikipedia.org/wiki/Maximal_lotteries)
* [French Wikipedia](https://fr.wikipedia.org/wiki/Scrutin_de_Condorcet_randomisé)


<!---
### Other voting rules
* Borda
* Nanson
* Baldwin
* Black
* MaxiMin
* Tideman
* Plurality
* Plurality with Runoff
* Instant-Runoff
* Anti-Plurality
* Bucklin
* Coombs
* Copeland
* Uncovered Set
* Essential Set
* Bipartisan Set
* Kemeny
* Schulze
* Ranked Pairs
* Condorcet
* Pareto

### Software and tools used in the project
* Angular
* Node
* jsLPSolver
* WinWheel
* Cloudflare

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

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

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/VotingTool/VotingTool.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
-->
