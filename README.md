# Whittington Parish Timeline

A searchable timeline of Whittington parish, Chesterfield, from Domesday to today. It has over 260 local events taken from [whittingtonhistory.org](https://whittingtonhistory.org), set beside 46 events from Derbyshire, Britain and the wider world.

Live page: https://phil-morris17.github.io/whittington-timeline/

## Files

| File | What it is |
|---|---|
| `index.html` | The timeline page |
| `data/timeline-data.js` | All the events, national context and picture credits. Edit this to add or correct an event. |
| `img/` | Pictures for the "Meanwhile" panels, from Wikimedia Commons (credits are shown on the page) |
| `whittington_full_interactive_timeline_with_biographies.html` | "When They Lived Together": the lifespans timeline, linked from the main page |
| `whittington_timeline_csv_autoload.html`, `whittington_timeline_autoload_dataset.csv` | The earlier CSV-driven version, kept for reference |

## Opening at a period

Add one of these to the end of the address to open the timeline at that period. They are useful for exhibition QR codes and for links from articles.

| Period | Link ending |
|---|---|
| 1086 – 1599 Domesday to the Tudors | `#medieval` |
| 1600 – 1749 Freeholders, Quakers and the Revolution | `#stuart` |
| 1750 – 1849 Pegge's parish and the Dixon glasshouse | `#georgian` |
| 1850 – 1913 Coal, iron and a new village | `#victorian` |
| 1914 – today Wars and the modern parish | `#modern` |

## Putting it on the WordPress site

Add a **Custom HTML** block to the Whittington Timeline page and paste this:

```html
<iframe src="https://phil-morris17.github.io/whittington-timeline/"
        title="Whittington Parish Timeline"
        style="width:100%;height:85vh;min-height:640px;border:0"
        loading="lazy"></iframe>
<p><a href="https://phil-morris17.github.io/whittington-timeline/" target="_blank" rel="noopener">Open the timeline full screen</a></p>
```

To link from an article to a period, add a line at the foot of the article, for example:

```html
<p><a href="https://phil-morris17.github.io/whittington-timeline/#victorian" target="_blank" rel="noopener">See this on the Whittington timeline</a></p>
```

## Adding an event

Open `data/timeline-data.js`, copy an existing line in `EVENTS`, change it, and keep the lines in year order. Each line has:

- `y`: the year, used for sorting and for deciding the period
- `d`: the date as shown, for example `"c.1830"` or `"29 Jan 1895"`
- `c`: the theme, one of `manor`, `revolution`, `church`, `people`, `industry`, `newwhitt`, `buildings`, `civic`, `social`, `war`, `national`, `whhg`
- `t`: a short title
- `x`: a one-sentence summary
- `s`: the article's address after `whittingtonhistory.org/`, for example `"the-fire-of-1895"`

Whittington History & Heritage Group
