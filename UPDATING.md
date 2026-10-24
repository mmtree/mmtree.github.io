# Updating the website

Most updates mean editing one file in `_data/`. Push to `main` (or edit the file on github.com
and commit) and the site rebuilds in about a minute.

| To change...              | Edit                                   |
|---------------------------|----------------------------------------|
| News on the home page     | `_data/news.yml` (newest at the top)   |
| Papers (Research page)    | `_data/publications.yml`               |
| Upcoming talks and events | `_data/talks.yml`                      |
| Courses                   | `_data/teaching.yml`                   |
| Students                  | `_data/students.yml`                   |
| Bio                       | `index.md`                             |
| Research descriptions     | `research.md`                          |
| Resources                 | `resources.md`                         |
| Links, email, menu        | `_config.yml`                          |

## Common tasks

**New paper.** Copy an entry in `_data/publications.yml`, put it at the top, and fill in the
fields, including `theme`, which sets the Research page section it appears in. Put a figure (about 800px wide) in `assets/img/pubs/` and give its filename as `image`.
When a submitted paper is accepted, change `status: submitted` to `status: published` and add `doi`.

**New CV.** Replace `assets/files/Morrison_CV.pdf` with the new PDF (keep the same filename so
links don't break).

**New talk or event.** Add an entry at the top of `_data/talks.yml` with `date: YYYY-MM-DD`
(or `YYYY-MM` if you don't know the day yet). It appears under "Upcoming talks and events" on the
home page until the date has passed; the site rebuilds daily so this stays current. For an event that isn't a talk (a workshop you're organizing,
for example), use `type: event` and put the event's name in `title`.
If a talk dated by month only has already happened, add `done: true` to take it off the home page.

## Preview on your computer

```sh
export PATH=/opt/homebrew/opt/ruby/bin:$PATH
bundle install          # first time only
bundle exec jekyll serve
```

Then open http://localhost:4000.
