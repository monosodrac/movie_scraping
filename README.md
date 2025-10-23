[PYTHON_BADGE]:https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54
[BS4_BADGE]:https://img.shields.io/badge/BeautifulSoup-4B8BBE?style=for-the-badge&logo=python&logoColor=white
[REQUESTS_BADGE]:https://img.shields.io/badge/requests-20232A?style=for-the-badge&logo=python&logoColor=white
[PRS_BADGE]:https://img.shields.io/badge/PRs-welcome-green?style=for-the-badge

<h1 align="center" style="font-weight: bold;">IMDb Movie Scraper 🎬</h1>

![python][PYTHON_BADGE]
![bs4][BS4_BADGE]
![requests][REQUESTS_BADGE]
![prs][PRS_BADGE]

<details open="open">
<summary>Table of Contents</summary>

- [🚀 Getting Started](#started)
  - [Prerequisites](#prerequisites)
  - [Cloning](#cloning)
  - [Environment Setup](#environment)
  - [Running the Scraper](#running)
- [📍 How It Works](#how-it-works)
- [📄 CSV Output](#csv)
- [🧰 Files Overview](#files)
- [⚙️ Technologies Used](#tech)
- [🤝 How to Reach Me](#reach)
- [📫 Contribute](#contribute)
- [📌 Notes](#notes)

</details>

<p align="center">
  <b>A multithreaded Python web scraping that collects movie data from IMDb’s Popular Movies page, including title, release date, rating, and plot summary.</b>
</p>

---

<h2 id="started">🚀 Getting Started</h2>

<h3 id="prerequisites">Prerequisites</h3>

- [Python 3.10+](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/installation/)
- [BeautifulSoup4](https://beautiful-soup-4.readthedocs.io/en/latest/)

<h3 id="cloning">Cloning</h3>

```bash
git clone https://github.com/monosodrac/movie_scraping.git
```

<h3 id="environment">Environment Setup</h3>

Install dependencies:

```
pip install requests beautifulsoup4
```

<h3 id="running">Running the Scraper</h3>

Execute the script:

```
python main.py
```

The script will start scraping the [IMDb Most Popular Movies](https://www.imdb.com/chart/moviemeter/?ref_=nv_mv_mpm) page and save the results into a file called movies.csv.

<h2 id="how-it-works">📍 How It Works</h2>

1. Sends a request to IMDb’s Most Popular Movies chart.
2. Extracts all movie links from the list.
3. Uses multithreading (up to 20 threads) to scrape multiple movie pages simultaneously.
4. For each movie page, it extracts:
    - 🎬 Title
    - 📅 Release Date
    - ⭐ IMDb Rating
    - 📝 Plot Summary
5. Saves the data into a CSV file (movies.csv).

<h2 id="csv">📄 CSV Output</h2>

The generated movies.csv file contains the following columns:

| title       | release_date | rating | plot                                                                                                      |
| ----------- | ------------ | ------ | --------------------------------------------------------------------------------------------------------- |
| Oppenheimer | 2023         | 8.9    | The story of American scientist J. Robert Oppenheimer and his role in the development of the atomic bomb. |
| Barbie      | 2023         | 7.3    | Barbie suffers a crisis that leads her to question her world and her existence.                           |

Each row corresponds to one movie scraped from IMDb.

<h2 id="files">🧰 Files Overview</h2>

| File              | Description                                                                |
| ----------------- | -------------------------------------------------------------------------- |
| `main.py`         | Main script responsible for scraping IMDb movie data using multithreading. |
| `movies.csv`      | Generated file containing the scraped movie data.                          |

<h2 id="tech">⚙️ Technologies Used</h2>

- 🐍 Python 3.10+
- 🧠 BeautifulSoup 4 – for parsing HTML and extracting movie details
- 🌐 Requests – for handling HTTP requests
- ⚡ concurrent.futures – for running multiple scraping threads simultaneously
- 📑 CSV module – for saving data to a structured file

<h2 id="reach">🤝 How to reach me</h2>

<table>
  <tr>
    <td align="center">
      <a href="https://linktr.ee/monosodrac">
        <img src="https://avatars.githubusercontent.com/u/141099551?v=4" width="100px;" alt="Mono Cardoso Profile Picture"/><br>
        <sub>
          <b>Mono</b>
        </sub>
      </a>
    </td>
  </tr>
</table>

<h2 id="contribute">📫 Contribute</h2>

Contributions are welcome! 🧩
If you’d like to improve this scraper or add new features, follow these steps:

1. Clone the repository
```
git clone https://github.com/monosodrac/movie_scraping.git
```
2. Create a new branch for your feature or fix
```
git checkout -b feature/your-feature-name
```
3. Follow good commit practices
4. After implementing your changes, open a Pull Request including:
    - Description of what was improved or added
    - How to test the update
    - (Optional) example of output or screenshots
Once submitted, your PR will be reviewed and merged if approved 🚀

<h2 id="notes">📌 Notes</h2>

- The scraper is designed for educational purposes only.
- Avoid sending too many requests too quickly — IMDb may temporarily block automated traffic.
- You can adjust the delay or thread count (MAX_THREADS) in the code for safer performance.
