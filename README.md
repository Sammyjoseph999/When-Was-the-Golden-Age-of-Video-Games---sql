# When was the golden age of video games? (SQL)

A SQL analysis of the 400 best-selling video games released between 1977 and 2020, combining sales with critic and user review scores to find the years in which games were both well reviewed and commercially successful.

## Data

A PostgreSQL database named `games` with two tables:

- `game_sales`: game, platform, publisher, developer, units sold (millions) and release year
- `reviews`: game, critic score and user score

The data comes from the DataCamp project of the same name and is not included in this repository.

## Queries

1. The ten best-selling games
2. How many games have no review scores
3. Years with the highest average critic score
4. The same, restricted to years with more than four reviewed games
5. Years that drop out once that restriction is applied (`EXCEPT`)
6. Years with the highest average user score
7. Years that appear on both the critic and user lists (`INTERSECT`)
8. Total sales in those years (subquery)

## Running the notebook

The notebook uses the `%%sql` magic from `ipython-sql` against a local PostgreSQL database:

```bash
pip install ipython-sql psycopg2-binary notebook
jupyter notebook notebook.ipynb
```

The saved notebook has no query outputs, because the database is not available outside the original environment.
