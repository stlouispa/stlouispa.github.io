# St Louis Parents Association website

This is the website for the St Louis Primary Schools Parents Association, live at
**[stlouispa.org](https://stlouispa.org)**.

You do **not** need to install anything or use any special software to update it.
Everything can be edited right here on the GitHub website. When you save a change,
the live site updates itself automatically within about a minute.

---

## Signing in (first time)

The website is managed through a **shared Parents Association GitHub account** —
you do not need your own personal account.

- **Username:** `stlouispa-web`
- **Email:** `pa.stlouisschools@gmail.com`

1. Get the **password** for this account from the previous website coordinator
   (it is kept in the PA handover document — it is not stored here).
2. Go to **[github.com/login](https://github.com/login)** and sign in as
   `stlouispa-web` with that password.
3. Open the website's files at
   **[github.com/stlouispa/stlouispa.github.io](https://github.com/stlouispa/stlouispa.github.io)**.
4. You're ready — follow "How to make a change" below.

> 🔑 Keep the login details safe and pass them on to the next coordinator at
> handover time. If you ever can't sign in, contact the PA committee.

---

## How to make a change

1. Go to the file you want to edit (see the guide below for which file).
2. Click the **pencil icon** (✏️ "Edit this file") in the top-right of the file.
3. Make your changes in the text box.
4. Scroll to the bottom, leave the default message, and click the green
   **Commit changes** button.
5. Wait about a minute, then refresh **[stlouispa.org](https://stlouispa.org)** to see it live.

> Tip: If something looks wrong after an edit, don't panic. Every change is saved
> in history and can be undone — see "If you make a mistake" at the bottom of the page.

---

## Where everything lives

The website pages are the files inside the **`_pages`** folder. Each page is a simple
text file ending in `.md`:

| Page on the website | File to edit              |
|---------------------|---------------------------|
| Home                | `_pages/home.md`          |
| About Us            | `_pages/about.md`         |
| Contact Us          | `_pages/contact.md`       |
| News                | `_pages/news.md`          |
| Events              | `_pages/events.md`        |
| After School        | `_pages/after_school.md`  |
| Photos              | `_pages/photos.md`        |
| Competitions        | `_pages/competitions.md`  |
| FAQ                 | `_pages/faq.md`           |

---

## Writing text on a page

Pages are written in **Markdown** — plain text with a few simple symbols for
formatting. The most common ones:

```
## A big heading
### A smaller heading

Normal text just goes on its own line.

**This makes text bold.**

[This is a clickable link](https://example.com)
```

Leave a **blank line** between paragraphs.

⚠️ At the very top of every page there is a block fenced by `---` lines (the
"front matter"). It controls the page title and menu. **Don't change anything
between those `---` lines** unless you mean to — just edit the text below it.

---

## Common tasks

### Add a link to a new newsletter (News page)
Edit `_pages/news.md` and copy one of the existing newsletter lines, then change
the date and the link:

```
[January 2026](https://link-to-the-newsletter)
```

### Add a photo to a page
1. First upload the image: open the **`assets/images`** folder, click
   **Add file → Upload files**, drag your photo in, and Commit.
2. Then, on the page where you want it to appear, add a line like this
   (use the exact file name you uploaded):

```
![Description of the photo](/assets/images/your-photo-name.jpg)
```

### Change a link in the top menu
Edit **`_data/navigation.yml`**. Follow the pattern of the existing entries —
each one has a `title` (what people see) and a `url` (where it goes). Keep the
spacing/indentation exactly as the other entries.

---

## If you make a mistake

Nothing is ever truly lost. To undo a change:

1. Click the **Commits** link (the clock/history icon) near the top of the page.
2. Find your change in the list, open it, and you can see exactly what changed.
3. If you need help reverting, contact whoever set this site up — they can roll
   it back in seconds.

---

## For developers (optional)

This is a [Jekyll](https://jekyllrb.com/) site using the
[minimal-mistakes](https://mmistakes.github.io/minimal-mistakes/) theme, hosted on
GitHub Pages. To run it locally:

```
bundle install
bundle exec jekyll serve
# then open http://localhost:4000/
```

- Site settings: `_config.yml`
- Custom domain: `CNAME` (points to stlouispa.org)
- Deployment is automatic — GitHub Pages rebuilds `main` on every push.
