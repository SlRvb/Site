---
alias: MediaDB
title: "MediaDB"
---

# MediaDB Vault Setup
> My media database vault stores nearly all of the Entertainment media that I'm consuming (Excluding 1-off Youtube videos).

[![|sban](/0_Technical/1_Images/Setup-MediaDB.png)](/0_Technical/1_Images/Setup-MediaDB.png) *MediaDB Graph*

Originally, this used to be a database on Notion for a while before I found Obsidian.

Examples of media in the MediaDB Vault are: 
- Literature
	- Fanfics
	- Comics
- Shows
- Movies
- Games

## Resources
**CSS:**
- [ITS Theme](https://github.com/SlRvb/Obsidian--ITS-Theme)
- [All Alternate Themes Snippet](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/Theme%20-%20All%20Alternate%20Themes.css) (**Tangerine Dunes** toggled on in the Style Settings)
- [Kanban Snippet](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/S%20-%20Kanban.css)
- [Image Adjustment Snippet](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/main/S%20-%20Images%20Adjustments.css)
- Dataview Adjustments CSS (In the [Styling Section](#Dataview))

**Plugins:**
- Dataview
- Templater
- Supercharged Links
- Markdown Attributes
- Obsidian Query Language

## Pre-Face
`Outline:`
- **System**
	- Fields
	- Links/Tags
		- Tags or Links?
- **The MediaDB Vault**
	- Folders
	- Medium Pages
	- Media Pages
	- Adding Pages
	- Styling
		- Folders/Links
		- Tags
		- Dataview
- **Moving/Converting Data**
	- Adjustings Data
	- Restructuring

This is a complete write up of my setup for my MediaDB Vault, meaning that this will be a long read. For ease, I've decided to immedately jump into my system and actually put the step of converting my Data from Notion to Obsidian at the end. The latter is far too long and would be too much to read through from the get go; you've come here for the system in Obsidian not the drudgery of converting files.


---
# System

## Fields
The fields that go into an entry depend on the type of **[Medium](#Medium%20Pages)** it is. The fields are the same across the board so that when I query for the **[Current Page](#Current%20Page)** and avoiding adding every variation of that field name to cover my bases.

> Any fields specific to a medium are covered in the [Medium Pages](#Medium%20Pages) section.

```yaml
Title: 
Creator: 

Rating: 
LGBT:

Category: 
Type: 
Description: 
Link: 

Progress: 
Currently: 

Series: 
Series Number: 
Series Total: 

Added: 
Medium: 
Image: 
File: 
```

---
**File Titles** in this vault may have properties with the same name but are separate things entirely, so most files are formatted as:
`Property Title -- Creator`. 

**Example:** `The Chronicles of Verraine -- Eleanor Konik`

---

**Title** is just the name given to the property. It used to be `Name` but `Title` is just much nicer to me for a database.

---
**Creator** includes those who wrote, drew, directed, etcetera that property. 

This was one of those fields that had to be changed as it used to have different names depending on the medium (ie. Author, Director, DM, etc). Didn't want to have to keep track of them all, so *creator* is a good catch all for me.

---
**Rating** is my personal rating system on how much I liked what I just watched/read.

More on this rating system in the [Rating Tags](#Rating%20Tags) section.

---
**LGBT** is my personal "rating" system for how LGBT+ friendly/unfriendly a property is. More on this rating system in the [LGBT Ratings](#LGBT%20Ratings%20Tags) section.

It used to be `LGBT Rating` but Supercharged Links had trouble with recognizing the difference between this and the personal `Rating`. It would end up changing `Rating` as well if I set a value for `LGBT`, so `LGBT Rating` had to be changed.

---
**Category** is all the tags that belong to that property. More on this in the [Category Tags](#Category%20Tags) section.

---
**Description** is just a field for a text summary either from IMDB or my own if there aren't any summaries for it. Since these are inline properties, any paragraph breaks I use ` <br><br> ` so that it at least outputs correctly when in preview mode.

---
**Link** is just where a markdown link to a website where the property is hosted or just where it's sold/can be found from.

---
**Status/Progress** are both fields that track progress of a property. While they generally mean the same thing, in my system, there's a difference. More on this in the [Status/Progress Tags](#Status%20Progress%20Tags) section.

---
**Currently** is a field that I use to note to myself what part of the media I'm currently on. 

For example: `Ch 4 Pg 3`, `S3 EP 4`, etc.

---
**Series** and all its "sub"-fields are ones that depend on the type of media and whether it has a high probability of having series. If it does, the series field is for the title of the series.

**Series Number** is the place that entry is within the series. 

For example: `Halo: Combat Evolved` is `1` in the `Halo` series.

**Series Total** is the *total* number of entries a series has and will be manually updated if more come out.

The reason that this is *here* and not in a page for the *series* itself is just because I tend to look more at entries than I do for series since they're often complete and rarely ongoing.

---
**Added** is the date and time in ISO 8601 format for when I *add* that entry to the database, not when I found it or when I started watching it nor when I completed it.

I find that I forget to record when I consumed that property or I'll have bookmarked it to add it into the MediaDB vault later. It would just be more stress for me to really dig into when I started or finished it, so personally I just focus on when I added it into the database and that's good enough for me.

---
**Medium** is the type of media the item is (ie. Literature, Comic, Movie, etc.). This is a field on *every* item page as it allows me to use the Supercharged Links plugin and assign an icon to that item based on whatever is in that field.

**Image** is just a link to either the `![](]()` external image or the `![[]]` internal one in my vault. 

**File** is also a link to the external file or the internal one in my vault.

## Links/Tags
For the tags of my MediaDB, I was *very* glad I'd been quite zealous on Notion and had a legend for what each of the tag types were and what they meant. Moving all of those over was a bit tedious but it got me thinking far more about how I wanted my tags to work; both visually and functionally.

**Criteria:**
- I will *always* want something that I can easily glance at and recognize what it means. (eg. Tag is blue --> it's an Alternate Universe Tag)
- That means I also need something that won't force me to squint or stop to read it. 
- If it takes *too* much effort to read what something says, I refuse to even bother giving it my time. It might seem harsh, but that's what I need; **readability is my top priority.**

### Tags or Links?
So now the question was: **Do I use links or tags for my MediaDB Vault?**

**Tags**
- I was a big fan of regular tags for the ease of querying
- I liked the fact that I could get a drop down of any related subtags if I typed the tag name
- What I didn't like was how long my tags would be because of my system.
- Being unable to use spaces was also something I wasn't a fan of.

> **Note:** My issues here *can* be fixed with css which I'll go over for tags in the **[Styling](#Styling)** section.

**Links**
I was already kind of leaning towards Links as my tags over regular tags.
- I liked that links could have aliases so I wouldn't need to look at a lot of unnecessary text to read than what I needed to.
- The option to hover over the links and see a note of the explanation of what that tag is in case I forget or am unsure was something I liked.
- The final nail in the coffin to finally go all in was with the introduction of the Supercharged Links plugin to style the links based on the field value within it

---
**In the end I decided to go with Links.** The hover option to see filled pages for whatever I linked together was the main reason for this decision.

The way I structured the name of my links is similar to Nested Tags so that I could start typing `Cat-Uni-` and only see options for Universe Links.


### Rating "Tags"
This was a rating "system" that I created when I was just starting to create my database *far* before even Notion came into the picture. 

The reason I created it was because, to me, a number system just didn't feel personal enough, it was *too* objective so if I gave a property a score *lower* than 5 it would seem like I *really* didn't like it. This way, I could give a proper score without feeling like I was calling a good piece of work trash. These words give a better idea of my thoughts on it.

It's just kinda funny that it ended up lining up to being a `10` item list, so you *can* just think of it like a `10 Star Rating` and convert it to see what that looks like. I prefer this system since it's far more useful for me this way.

**Example:** `[[Rating-Liked|Liked]]`

Rating | Description |
---|---|
Loved | Absolute and *immense adoration* of the work.
Liked | The work is pretty *fantastic*.
Good | The work is pretty great.
Nice | A pleasant time can be had.
Fine | Has plenty of good elements to it isn't amazing.
Okay | Has *some* good elements but not enough.
Meh | Felt indifferent about the work; not good, not terrible.
Nah | Mild dislike for the work.
Disliked | Insufferable elements and somewhat of a bad time
Hated | Work is absolutely terrible and entirely insufferable.

> **⚠ Note:** All of these ratings are my *personal* feelings, any measure of *objectivity* is **not** taken into account when using this. It's entirely on what I felt when consuming the work. So the work could be crafted exceptionally well *"objectively"*, but end up with a `Nah` rating.

### LGBT+ Ratings "Tags"
> This is a personal field/tagging system for me to see where a property falls on it's execution of representation.

This was important for *me* as I personally feel more inclined to watch or rewatch a property that has a better LGBT Rating or to just prepare myself for the possible good or bad dynamics/events of these identities in that work if I've yet to see it.

**Example:** `[[LGBT Rating-Queer Main|Queer Main]]`

Rating | Description |
---|---|
Queer Focused | Media that focuses on the experience of being LGBT+.
Openly Queer | Multiple LGBT+ characters or relationships that are clearly and explicitly stated to be LGBT+.
Queer Main | LGBT+ main character within the media.
Queer Side | LGBT+ side character within the media
Bury Your Gays Trope | LGBT+ character is killed off.
Convenient Breakup | LGBT+ relationship where the characters break up, often for nonsensical reasons, to easily get rid of the relationship in that media.
Toxic Relationship | LGBT+ relationship is shown, but has a toxic/unhealthy dynamic.
Relationship Subtext | LGBT+ relationship is implied to exist, but is not explicitly confirmed or denied within the media.
Token LGBT+ | LGBT+ character introduced only to add diversity to the cast or media.
Confirmed Off-Screen | Relationship(s) or character(s) confirmed to be LGBT+ but said LGBT+ status not shown in their media.
Sexual Tension | There is a tension between two characters (who may or may not be LGBT+) implying a possible relationship, but never ending up in a relationship.
Straight Passing | There may be LGBT+ character(s), but it's easily deniable that it is the case.
Queerbait | The sexuality of character(s) or potential relationship are teased to be LGBT+ but are never confirmed to increase views.
LGBT+ In Background | There are LGBT+ characters/relationships but only in the background.
No LGBT+ | No LGBT+ characters/relationships.


### Medium "Tags"

**Example:** `[[Medium-Show|Show]]`

Medium | |
---|---|
`Show` | TV, YouTube Shows, etc
`Movie` | Standard hour & 30 min, Short Films, Film Series/Universes, etc
`Literature` | Books (Physical/Digital), Web Stories, etc
`Comic` | Graphic Novels, Mangas, Web Comics, etc
`Game` | PC, Console, Mobile, Board Games, Table Top Games, etc

---
**Type**
Types in this case are subtypes of any of the `Medium` tags.

**Example:** `[[Type-Video Game|Video Game]]`

Types ||
---|---|
`Live Action` | Property involves actual people.
`Animated` | Property involves artistic renditions of the world.<br>(2D, 3D, Stopmotion, etc)
||
`Fanfiction` | Works using characters from another property
`Manga`/`Manhwa`/etc | Comics that are from different countries
`Web Comic` | Comics that are primarily or only distributed on the internet
||
`Video Game` | Digital game
`Table Top` | Game's usually geared to 'around the table' play
`Let's Play` | Youtube/twitch series where creators are playing a game
||
`Non-Fiction` | Not about fictional events, characters, etc
`Fiction` | About fictional events, characters, etc


### Category "Tags"
**Example:** `[[Cat-Rel-Childhood Friends|Childhood Friends]]`

Category | Link Prefix | Example
---|---|---|
Universe | `Cat-Uni-` | Zombie Apocalypse
Relationship | `Cat-Rel-` | Childhood Friends
Emotion | `Cat-Emo-` | Horror
Warning | `Cat-Warn-` | Unbalanced Power Dynamics
Wholesomeness | `Cat-Whol-` | Problematic
Extras | `Cat-Ex-` | Society

### Status/Progress "Tags"
While generally these *mean* the same thing, in my database, they're slightly different. The reason I separated them is because while a property can be *completed* (maybe even finished years ago), I'm currently in the process of watching it. I needed some way to be able to tell which pieces of media might already be completed, but I'm still reading and haven't personally finished, *and* which property I have read as far as I can but it's still got more content planned to come out later.

---

**Status** is for the status of the *property* itself. So if a show is on hiatus it will receive a `[[Status-Hiatus|Hiatus]]` link/tag. 

**Progress** is for *my personal* progress on a piece of media. If I'm still watching a show it'll receive a `[[Progress-In Progress|In Progress]]` link/tag.

**Example:**
- `[[Status-Cancelled|Cancelled]]`
- `[[Progress-Dropped|Dropped]]`

Status/Progress | |
---|---| 
`Queued` | Planned to start, but hasn't
`In Progress` | Currently working through
`Hiatus` | Started, but then paused
`Cancelled`/`Dropped` | Started, but stopped and will no longer work through | Progress version of `Cancelled`
`Complete` | Started and finished the work


## Images
> The dilemma: internally linked images or externally linked images?

Even though I have images in some of my pages, I've avoided pulling them up with dataview for now because I'm still undecided over whether or not I want to use external images.

**Internally linked images** are my go to for ensuring that the images that I do display are always available and, but unfortunately internally linked images don't display in dataview, so my saved images can't be pulled up. There's also the possibility of just having so many images that the vault grows *too* large for Obsidian Sync's 4gb limit or the limit for Dropbox's 2gb and Onedrive's 5gb limits.

**Externally linked images** are ones that *do* work with dataview, but some of my links are definitely broken for some notes. I don't want to deal with images disappearing whenever I'm not connected to the internet either even if I go with the option of using imgur or anything similar.

---
> For now, I've just decided that I would use either one whenever I'm adding data to my pages, but not even bother trying to show them in the dataview query.

Externally linked images are for media that I don't care all that much about but still want an image for while Internally linked images are for media that I really enjoy and want a concrete image that won't disappear when a site goes down.

# The MediaDB Vault
## Workspace
I'm using the **Tangerine Dunes** CSS Snippets color scheme which was inspired by the color from my HQ Vault folder for my Databases which was an orange-red color. I just needed a different color scheme so that I quickly knew which vault I was in from any of the rest that may be open at the same time.

> As far as how I layout my vault, it's pretty simple and I try to keep the things that I search through often all laid out in front of me.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Workspace.png)](/0_Technical/1_Images/Setup-MediaDB_Workspace.png) *My general layout for the vault.*


**Left Sidebar** has the `Search` at the top so that I can easily query for something within my vault. Below that is the `File Explorer` so that I can browse through some of the files in my setup if I need to fix something, mostly I need to open either the `00 Technical` or the `10 Meta` folders quite often.

**Middle Panes** are separated but linked and allow me to easily type in the edit pane and see the changes made to preview mode. I don't tend need more than 1 media page open at a time so this simple 2 pane setup is more than enough.

**Right Sidebar** at the top has my **Starred** pages, but I tend to look through the `File Explorer` more often for those same pages mostly out of habit than efficiency... but it's still there so I can *try* to use that instead. Below that is the [Medium Pages](#Medium%20Pages) with all my queries for `Currently`, `Recently Added`, and `Queue` pages so that they're easily always accessible and don't interfere with my Middle Panes.

## Folder Structure

- **00 Technical**
	- 0 Templates
	- 1 Images
		- Covers
		- Fandom
		- Media
	- 2 Files
	- 5 Workbench
- **10 Meta**
	- 0 Tag
	- 1 Medium
	- 2 Fandoms
- **Fanfiction**
- **Games**
- **Let's Plays**
- **Movies**
- **Shows**

### 00 Technical

**Templates** contains all my template files for *every* kind of file: Media Pages, Queries, Meta Pages, etc.

---
**Images** contains all images used within the vault. 

**Media** are the images that I link to in the `Image::` field for my Media pages.

**Fandom** are the images for each of the fandoms in the Fanfiction Medium page.

**Cover** is the same as the Media images folder, but these are images that **I** created *for* specific Media pages.

---
**Files** is the folder where I store pdfs/markdown files of the Media pages that I link to in the `File::` field.

**Workbench** is just a folder of files where I test out plugins or queries.

### 10 Meta

**0 Tags** contains all the explanation pages for *every* tag. It also contains pages that the Supercharged Link plugin uses to allow me to select my tags when I [add Media pages](#Adding%20Pages).

---
**1 Medium** contains notes with the main queries that I use to list out all the media within the Media folders. The files are named similarly to the folders.

---
**2 Fandoms** contain notes with the queries for specific fandoms for the Fanfiction folder's files. 

File Title: `Fandom-Fandom Name`

If there are crossovers the file will be titled: `Crossover-Fandom1 - Fandom2`

**Example:** `Crossover-Wonder Woman - Tomb Raider`

### Media Folders

The rest of the folders in the list are where all the Media Pages are stored into their own sections. There are no sub folders to separate them, it's all a flat structure for the rest of the folders.


## Medium Pages
Most of these pages are just full of dataview queries, but the ones that I do include here are ones with either notable formatting or useful dataview queries. There is also some use of the Obsidian Query Language to generate the total number of files related to that note.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Medium-DnD-Lets-Play.png)](/0_Technical/1_Images/Setup-MediaDB_Medium-DnD-Lets-Play.png) *Example of general page format/styling*

#### Fanfiction
> Homepage for my queries and Fandoms structured in a way that's useful for me.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Medium-Fanfiction.gif)](/0_Technical/1_Images/Setup-MediaDB_Medium-Fanfiction.gif) *Gif of the Fanfiction Medium Homepage*

The page contains a general **Count** of the amount of files within the Fanfiction folder at the top using the Obsidian Query Language plugin.

---
There's a **Recently Added** section that lists the files I've added to the MediaDB vault along with a subheading that has my raindrop.io **Media Inbox** iframed into it. 

More information on this in the [Media Inbox](#Media%20Inbox) section

---
The **Fandom** section is where I manually list out the fandoms within the Fanfiction folder so that I can easily go into each and find whatever I currently want. The reason I manually sort it instead of letting Dataview do it for me is that I personally want to sort which ones I'm currently interested in at the top and least interested in at the bottom. As well as use the Kanban formatting to adjust the look of it to my liking.

There's a link to the general **Fandom** supercharged links list note so that whenever I'm on mobile and just want to quickly go into one of the Fandom pages, I can do so without having to scroll past a bunch of images. 

---
For the section with my Fandom Images, I didn't want the Kanban CSS to affect the list under the **Recently Added** header, so I adjusted the Kanban CSS snippet to allow the Markdown Attributes plugin to only affect the **Fandoms** list and turn it into a kanban board by putting `{: .kanban }` after the last item on the list.

````md
---
cssclass: dv, table, hcl
---

# Fanfiction
```oql
name: Total Fanfics
query:
	path: "Fanfiction/"
template: "string"
format: "*<strong>{name}</strong>: {count}*"
badge: false
```

## Recently Added

```dataview
LIST
FROM "Fanfiction"
SORT file.ctime desc
LIMIT 10
```

###### Raindrop Inbox
> Fanfics waiting to be Added

<iframe style="border: 0; width: 100%; height: 450px;" allowfullscreen frameborder="0" src="https://raindrop.io/"></iframe>

# Fandoms
![](/0_Technical/1_Images/Fandoms|no-title]] {: .poem }

- [![](|cover+ctr+pt+htiny|200](https://i.pinimg.com/originals/dd/4e/93/dd4e93cdb38efdce9292a72795771425.png)](<Fandom-Carmilla>)***[[Fandom-Carmilla|Carmilla]]***
- [![](/0_Technical/1_Images/Merry Xmas -- atomicant_cami.jpg|cover+ctr+htiny|200]]](<Fandom-Carmen%20Sandiego>)***[[Fandom-Carmen Sandiego|Carmen Sandiego]]***
- [![](|cover+ctr+htiny|200](https://wi.wallpapertip.com/wsimgs/85-859197_buffy-the-vampire-slayer-desktop.jpg)](<Fandom-Buffy%20The%20Vampire%20Slayer>)***[[Fandom-Buffy The Vampire Slayer|Buffy The Vampire Slayer]]***
- ![](/0_Technical/1_Images/SoundlessWind - Shall We Dance.jpg|cover+ctr+p+tcc+htiny|200]]***[[Fandom-Sailor Moon|Sailor Moon]]***
- ![](/0_Technical/1_Images/pharamercy -- pepegle.jpg|cover+ctr+pt+htiny|200]]***[[Fandom-Overwatch|Overwatch]]***
	{: .kanban }
````


#### Current Page
> Queries to pull up what I'm currently watching/reading/playing/etc. and what I've watched but am now waiting for the new season/episode/book/etc.

[![|sban](/0_Technical/1_Images/Setup-MediaDb_Current.png)](/0_Technical/1_Images/Setup-MediaDb_Current.png) *Current Page Layout*

````sql
---
cssclass: hcl, table
---

# Current
```dataview
TABLE WITHOUT ID link(rows.file.link, " ") +  "<strong>" + rows.Title + "</strong>" AS Property, rows.Currently AS Currently
FROM ""
WHERE Progress = [[Progress-In Progress|In Progress]] | Progress = [[Progress-Hiatus|Hiatus]]
GROUP BY file.link
SORT rows.Added desc
```

# Updates Awaiting
```dataview
TABLE WITHOUT ID "" + link(rows.file.link, " ") + rows.Title AS Entry, rows.Currently AS Progress
FROM ""
WHERE (Status = [[Status-Ongoing|Ongoing]] OR Status = [[Status-Hiatus|Hiatus]]) & (Progress != [[Progress-Dropped|Dropped]])
GROUP BY file.link
SORT Added desc
```
````

#### Queue Page
> Page of one query listing all the media I'm planning to read/watch/etc.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Page-Queue.png)](/0_Technical/1_Images/Setup-MediaDB_Page-Queue.png) *Queue Page Layout*

````md
---
cssclass: hcl, dvl, kanban
---

# Queue
```dataview
LIST WITHOUT ID link(rows.file.link, " ") + "<strong>" + rows.Title + "</strong>"
FROM ""
WHERE Progress = [[Progress-Queued|Queued]]
GROUP BY file.link
SORT rows.Added desc, rows.Medium asc
```
````


## Media Pages
Most of the fields within the media pages are *not* filled out automatically by pulling information from sites like IMDB. It's all filled out manually as I have my own [Tag](#Links%20Tags) system that's useful for me.

### Literature/Books

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Media-Literature.png)](/0_Technical/1_Images/Setup-MediaDB_Media-Literature.png) *Example of a Book Page*

**File Title:** `Title -- Creator`

**Medium** is where I specify if the book is `non-fiction` or `fiction`. It was just easiest to place there as I put that specification in the Medium page that Supercharged Links helps me select from.

```yaml
Title:: <% tp.file.title.split(" -- ")[0] %>
Creator:: <% tp.file.title.split(" -- ")[1] %>

Rating:: 
LGBT:: 

Cost::
Category::
Description::
Status:: 
Link::

Progress::
Currently::

Series:: 
Series Number:: 
Series Total:: 

Added:: <% tp.date.now("YYYY-MM-DD HH:MM") %>
Medium:: [[Medium-Literature|Literature]]
Image:: 
File:: 
```

### Fanfiction
> The Fanfiction media page is pretty similar to the Literature page, but with a couple differences.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Media-Fanfiction.png)](/0_Technical/1_Images/Setup-MediaDB_Media-Fanfiction.png) *Example of a Fanfiction Page*

**Fandom** is a link to a specific page that has the title of the Original work is based on. This is similar to the **Property** field and could honestly be replaced by it, but I wanted a page where I could *specifically* query only fanfiction content about this particular work. The Fandom page is formatted nearly the same as the Fanfiction page itself.

---
**Ships** are the relationships between characters.

---
**Relationship** is a field where I list out what *type* of relationship is displayed in the work.

Type | Explanation |
---|---|
Bisexual | Characters identify as bisexual
Lesbian | Characters identify as lesbian
Gay | Characters identify as gay
Heterosexual | Characters identify as heterosexual
Asexual | Characters identify as asexual
||
Female-Female | Relationship between women
Transwoman-Female | Relationship between women
Female-Male | Relationship between man and woman
Male-Male | Relationship between men
|||
Female-Male-Male | Relationship between 1 woman and 2 men
Non-Binary-Male-Male | Relationship between 1 nonbinary person and 2 men
Female-Female-Female | Relationship between 3 women

> This is just a brief list or else it would be excessively long and you get the gist.

---
**Smut:** Is there sex? Yes or no?

---
**Property** is where I link to whatever media from another part of my MediaDB vault that this fanfiction work is based on.

```yaml
Title:: <% tp.file.title.split(" -- ")[0] %>
Creator:: <% tp.file.title.split(" -- ")[1] %>

Rating:: 
Fandom:: 
Ships:: 
Relationship:: 
LGBT:: 

Category:: 
Description:: 
Status:: [[Status-Complete|Complete]]
Chapters:: 
Smut:: 
Link:: [Archive Of Our Own]()

Progress:: [[Progress-Complete|Complete]]
Currently:: 

Series:: 
Series Number:: 
Series Total:: 

Added:: <% tp.date.now("YYYY-MM-DD HH:MM") %>
Medium:: [[Medium-Literature|Literature]], [[Type-Fanfiction|Fanfiction]]
Property:: 
Image:: 
File:: 
```


### Movie

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Media-Movie.png)](/0_Technical/1_Images/Setup-MediaDB_Media-Movie.png) *Example of a Movie Page*

**File Title:** `Title` or `Title (Year)` if there's a movie with a similar name.

**Origin** is where I specify what country of origin the movie came from. Example: America, Japan, Central America, Korea, etc.

**Stream** is where I let myself know what streaming sites the movie is available on *at that time*.

**Co-Op** is where I list out *who* I watched the movie with as sometimes I tend to watch movies with friends and I use this Database to also help us track what we've watched together or not.

```yaml
Title:: <% tp.file.title %>

Rating:: 
LGBT:: 

Category:: 
Description:: 
Status:: 

Progress:: 
Series:: 
Series Number:: 
Series Total:: 

Medium:: [[Medium-Movie|Movie]]
Origin:: 

Added:: <% tp.date.now("YYYY-MM-DD HH:MM") %>
Image:: 
Link:: 
Stream:: 
Co-Op:: 
```

### Shows

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Show-Castlevania.png)](/0_Technical/1_Images/Setup-MediaDB_Show-Castlevania.png) *Example of a Show Page*

**File Title:** `Title` or `Title (Year)` if there's more than 1 with the same name.

**Seasons/Episodes** is where I write how many seasons/episodes a show has total. That will increment if the show is currently running.

**Co-Op** is the same as in the [Movie](#Movie) Page as my friends and I also watch a bunch of shows together.

```yaml
Title:: <% tp.file.title %>

Rating:: 
LGBT:: 

Category:: 
Description:: 
Status:: 
Seasons:: 
Episodes::

Progress:: 
Currently:: 

Medium:: [[Medium-Show|Show]]
Origin:: 

Added:: <% tp.date.now("YYYY-MM-DD HH:MM") %>
Image:: 
Link:: 
Stream:: 
Co-Op:: 
```

### Games

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Media-Game.png)](/0_Technical/1_Images/Setup-MediaDB_Media-Game.png) *Example of a Game Page*

**File Title:** `Title` or `Title (Year)` or `Title (Studio/Creator)`

---
**Playable** allows me to track which games are still playable or have been abandoned for browser/online games.

---
**Mechanics** is where I list out the more game-like classifications to better help me understand what type of game it is.

Tags are formatted: `[[Mech-Sandbox|Sandbox]]`

Mechanic | |
---|---|
Sandbox | Allows most/any type of play
Open World | A large map to explore where the world feels alive
Simulation | Either physics or NPC interactivity to simulate real life
Building | Designing/creating within a game
||
Shooter | Heavy emphasis on gun play
MMORPG | Massive Multiplayer Online Roleplaying Games
Survival | Gathering resources, fighting off enemies, etc
RPG | Heavy emphasis on roleplaying
Driving/Racing | Car games, either racing or just leisure driving
Sport | Skate/Snowboarding, Soccer, Tennis, etc
||
Campaign | Has a story to play through
Quests | Side quests available apart from campaign
PvE | Player verses Enemy
PvP | Player verses Player
||
First Person | Camera's 
Third Person | Camera's behind the character
Realistic | Implements real world physics

---
**Multiplayer** tells me if a game has or doesn't have the ability to play with friends and whether that's possible locally or online.

---
**Platform** lists out which consoles/hardware I got the game for. 

For example: PC, Xbox, PlayStation, Switch, etc.

---
**Games** is links to other games if this page *is* a series page.

```yaml
Title:: 
Rating:: 

Description:: 
Status:: 
Link:: 

Progress:: 
Playable:: 

Category::
Mechanics:: 
Multiplayer:: 
Platform:: 

Series:: 
Series Number:: 
Series Total:: 
Games::

Added:: <% tp.date.now("YYYY-MM-DD HH:MM") %>
Medium:: [[Medium-Game|Game]]
Image:: 
```

### Let's Plays
There's not much different from this page and a show/movie page. This is one of the more basic kinds of pages in the database.

[![|sban](/0_Technical/1_Images/Setup-MediaDb_Media-Lets-Play.png)](/0_Technical/1_Images/Setup-MediaDb_Media-Lets-Play.png) *Example of a Let's Play Page*

```yaml
Title:: <% tp.file.title.split(" -- ")[0] %>
Creator:: <% tp.file.title.split(" -- ")[1] %>

Rating:: 
LGBT:: 

Category:: 
Description:: 
Status:: 
Link:: 

Progress:: 
Currently:: 

Series:: 
Series Number:: 
Series Total:: 

Added:: <% tp.date.now("YYYY-MM-DD HH:MM") %>
Medium:: [[Medium-Show|Show]], [[Type-Let's Play|Let's Play]]
Property:: 
Image:: 
```

## Adding Pages
> I add new media that I consume to my raindrop.io Media Inbox queue and then transfer it into the MediaDB vault through the QuickAdd plugin.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Add-Media.gif)](/0_Technical/1_Images/Setup-MediaDB_Add-Media.gif) *Gif of the process of adding a Media Page into the MediaDB Vault*

### Media Inbox
The raindrop.io **Media Inbox** collection is where I send the link of what I've just read so that I can clear the page from my browser and still have it queued for me to add later if I can't do so right now. For movies, Shows, etc I'll use a link to IMBD or MyAnimeList and add that to the inbox.

I just change the description to my rating so that I can easily remember what I thought of it begin to fill out my page when I eventually add it in. I also tag it with the type of media it is so I can embed it with the correct filter for the page. For example: `#Fanfiction` or `#Movie`

I try to avoid having my bookmarks sit in my Media Inbox for over 2 weeks because I tend to forget what some of the bookmarked items were even about.

### QuickAdd
So once I'm ready to input the media, I use QuickAdd to easily add it into the correct folder with the correct template.

The setup is *very* simple and just hotkeyed the command to `alt + Q`.
- Multi is called **💽Media** and is full of Template choices for each Medium.
- **Template Path** to template is chosen
- **File Name Format** is `{{VALUE:Title}} -- {{VALUE:Creator}}.md`
- **Create in Folder** is set to the media folder for that medium
- **Open** is toggled on to open the file when created

[![|sban](/0_Technical/1_Images/Setup-MediaDB_QuickAdd.png)](/0_Technical/1_Images/Setup-MediaDB_QuickAdd.png) *Quick Add Selection Command Options*

### Supercharged Links
Once the page is added, I click the three dots (or screw/gear icon) to look for the fields that I want to add information to using the Supercharged links plugin. 

[![|sban](/0_Technical/1_Images/Setup-MediaDB_SuperChargedLinks-Update-Fields.png)](/0_Technical/1_Images/Setup-MediaDB_SuperChargedLinks-Update-Fields.png) *Supercharged 3 Dot Menu*

The setup includes all the files that have the complete tag list for *every* category in my `10 Meta/0 Tags` [folder](#10%20Meta).

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Meta-Folder.png)](/0_Technical/1_Images/Setup-MediaDB_Meta-Folder.png) *The 10 Meta Folder*

In the settings for the plugin I just **Add a New Property Manager** with all the fields that I want to target and then point the file path to the specific md file in the `10 Meta/0 Tags` folder.

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Supercharged-Links-Settings.png)](/0_Technical/1_Images/Setup-MediaDB_Supercharged-Links-Settings.png) *My settings for the Supercharged Links Plugin*

## Styling
### Links/Folders
My styling at least for the Category Links themselves *didnt* really use Supercharged Links, but the **type** of medium a note belonged to definitely used the **Target Attribute for Styling** to assign the icons.

```css
/* General Styling For Links
----------------------------*/
.internal-link:before {
    vertical-align: top;
    padding-right: 2px;
    font-weight: 10 !important;
}
/*The rest of the changes use this so I don't have to have a bunch of duplicate code. */


/* Category Icon */
.internal-link[data-href*="Cat-Rel"]:before {
    content: '\ec97';
    font-family: var(--rmx);
}
/* Category Text Color */
.internal-link[data-href*="Cat-Rel"] {
    color: #ff7cde;
}


/* Media Type Icon */
/* This is pointing to the attribute that supercharged links adds so that I can style a page based on the data inside */
.internal-link[data-link-medium*="Literature"]:before {
    content: "\E810";
    font-family: var(--its);
    color: slategray;
}
```

### Tags

If I had gone with tags, I would have used this css to hide the length of the nested tag so I would only see what I needed.

```css
/*----Hide tag text----*/

/* Example of targeting a specific tag 
if you don't want to have to rewrite EVERY Tag name
Will have to add this to all the other parts of this CSS

a[href^="#Status"], */
a[href^="#"] {
    font-size: 1px;
    letter-spacing: -1px;
    color: transparent;
    background-color: transparent;
}
a[href^="#"]:after {
    content: "";
    letter-spacing: 0px;
    font-size: 14px;
    line-height: 19px;
    color: white;
}

/*----Show Full Tag When Hovering----*/
a[href^="#"]:hover:after {
    content: "";
}
a[href^="#"]:hover { 
    font-size: 13px !important; 
    color: white !important;
    letter-spacing: 0px !important;
    background-color: var(--tag);
}

/*----Add Icon to Category Tag----*/
a[href*="Category/Universe"]:before {
    content: var(--uni-i);
    font-family: var(--uni-if);
    font-size: 16px;
    color: var(--uni);
    padding-right: 5px;
}

/*Then here just replace the specific tag to the actual wording you want*/
a[href*="Alternate-Universe"]:after { 
    content: "Alternate Universe"; 
    color: var(--uni);
}
```

[![|sban](/0_Technical/1_Images/Setup-MediaDB_Tag-Alternative.gif)](/0_Technical/1_Images/Setup-MediaDB_Tag-Alternative.gif) **CSS Result:** *Tag looks similar to the Link version*

### Dataview
```css
/*Dataview: Compact and Hide Bullets*/
.dv .dataview-ul li::before {
    visibility: hidden;
}
.dv .dataview-ul {
    list-style-type: none;
    margin-inline-start: -32px;
}

/*Dataview: Space Lists & Add BG*/
.dvl .list-view-ul li {
    padding: 10px;
    margin-top: 15px;
    background-color: var(--aside-bg);
}
.dvl .dataview.list-view-ul li::before {
    margin-left: -27px;
}
.kanban.dvl .list-view-ul li {
    background-color: var(--aside-bg);
}
.kanban.dvl ul li {
    flex: 1 1 200px !important;
}
```

All of these are used as cssclasses within a note although `dv` is one used by the ITS theme as a style settings toggle to apply to *all* dataview tables.

`dvl` will result in the list being spaced out and now have a background on it. If you have `kanban, dvl` in the cssclass, it will format it in the same style as the image for the [Queue Page](#Queue%20Page) or the example from the [Medium Pages](#Medium%20Pages) section.

---

# Moving/Converting Data
Getting the data off Notion was luckily pretty easy. I just exported to CSVs and I was pretty much set. Later on, I also exported to HTML because that option also takes any of the photos I had inside Notions database pages with it. Saved me the pain of trying to reopen every single item and copying/saving every photo to transfer it over.

I used @koala's [**CSV to Markdown python script**](https://github.com/kometenstaub/csv-to-md) to convert my CSVs into markdown. The script creates a new MD file *per* row/item in your CSVs. It's really fast and the options to specify how each field's value is formatted made it fantastic and painless to convert things.

I opted to export it in dataview's inline field syntax `::` over YAML specifically so that I could link entries to each other and actually have Obsidian recognize those connections. YAML currently doesn't support that, nor does it support wiki link syntax very well, so inline fields was my choice to organize my data.

## Adjusting The Data For My New System
Now this step in the process was the *longest* and most challenging part for me to go through. This was something I had been working on/brainstorming for a long while. 

Within Obsidian, I had Mermaid Charts to help me plan what kind of information should go into them, where, and *why* should that be there. What types of fields I decided to include or omit will be covered in more detail later, but for now the heavy focus was on designing my tagging system.

## Restructuring
> A lot of the information that I had exported into a markdown file needed heavy editing to match the system I wanted to use.

It *probably* wouldn't have taken me as long if I had known how powerful VScode search and replace regex *allowed* for storing strings among other things 😅. Here will be all the regex that I used during this process if you find you might need it. 

### Date/Time
A lot of the dates that Notion output weren't in ISO format so I used this regex to grab and change the date to ISO format.

**Search:**
```regex
Jan, (\d{2}), (\d{4})
```
- `Jan, ` find any text that has Jan with a comma and a space
- `(\d{2}), ` capture/save the text that has 2 consecutive digits, then continue searching past the comma and space
- `(\d{4})` capture and save the text that has 4 consecutive digits

**Replace:**
```regex
$2-01-$1
```
- Put the year first, which is the second group: `(\d{4})`
- Replace Jan with `01` (this has to be manual for the months)
- Put the day at the end which is the first group `(\d{2})`

**Input:** `Jan, 17, 2021`
**Output:** `2021-01-17`

### Links
CSV to Markdown exported all my tags and changed my categories and other field values to wikilinks, but they didn't have the prefixing that I decided on from the [Tags or Links](#Tags%20or%20Links) section, so now was time for painful search and replace.

Adding the prefixes for my [Category Tags](#Category%20Tags) unfortunately had no regex way to quickly automate that for me, so I had to search and replace those manually.

Adding the **aliases** to the end of those changed links was far easier for links where I might've just forgotten to add some.

**Search:**
```regex
(\[\[)(.*) - (.*) - (.*)(\]\])
```
- `(\[\[)` Capture the brackets into it's own group 
- `(.*)` Capture any text between the ` - ` and do this 3 times
- `(\]\])` Capture the brackets into its own group

**Replace:**
```regex
$1Ship-$2 - $3 - $4|$2/$3/$4$5
```
- `$1` place brackets back `[[`
- `Ship-` add text
- `$2`, `$3`, `$4` Add capture groups back
- `$5` place brackets back `]]`

**Input:** `[[Ship-Trevor - Alucard - Sypha]]`
**Output:** `[[Ship-Trevor - Alucard - Sypha|Trevor/Alucard/Sypha]]`

### Fields
#### Adding
I realized I needed a way to list out what *type* of media this note about what I consumed actually was. It wasn't a field in my original CSV and it didn't seem like VSCode could add a line at a specific number. So what I did instead was find the title of the field I wanted to add *before* that field and squeeze it in there.

**Search:**
```regex
(Added:: .*)
```
- `Added:: .*` grab the entire line that has `Added::` in it
- `()` tells regex to capture whatever is inside as a group, so the entire line is saved

---
**Replace:**
```regex
$1\nMedium:: [[Medium-Movie|Movie]]
```

- `$1` puts the group back, so all of `Added::` is put back
- `\n` adds a new line
- `Medium:: [[Medium-Movie|Movie]]` add all of this *after* everything else

#### Find Notes With Only This Tag, But Add/Change A Different Field
I reach a point where I realized I needed to add a new property to some pages, but the flat structure really made this incredibly difficult. I *did not* want to have to manually go into every note and add the new field and its values, especially since I had about 300+ files to go through.

A *lot* of trial and error and pushing the limits of my own regex knowledge finally allowed me to do exactly what I wanted.

**Search:**
```regex
Fandom:: \[\[Fandom-(.*)\]\]
((.*\n){1,})
?Property:: 
```
- `Fandom:: \[\[Fandom-` Find this line and this text in it
- `(.*)\]\]` save everything that comes before the closing brackets into a group
- `((.*\n){1,})` Copy every line in between into a group
- `?Property:: ` Stop at Property line

**Replace:**
```.
Fandom:: [[Fandom-$1]]
$2Property:: [[$1]]
```

- `Fandom:: [[Fandom-$1]]` put back the whole first line
- `$2` put back all of the lines in between
- `Property:: [[$1]]` add the new value/change to the property.

---
# Fin
I believe I covered nearly everything within my MediaDB Vault, but if there's anything that I may have glossed over that you'd like to know more about, don't hesitate to leave a question! I'm happy to answer and explain anything I missed in more detail if need be.

Any thoughts and suggestions are welcome as well! I'm still working this system out myself so things may change slightly as time goes on, but the fundamentals laid out here might stay the same.