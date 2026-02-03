---
title: <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
date: <% moment(tp.file.creation_date()).format("YYYY-MM-DD HH:mm:ss") %>
lastmod: <% moment(tp.file.creation_date()).format("YYYY-MM-DD HH:mm:ss") %>
categories:
tags: daily-notes
aliases:
share: false
---
---
title: Invalid date
date: 2026-02-03 22:24:00
lastmod: 2026-02-03 22:24:00
categories:
tags: daily-notes
aliases:
share: false
---

# Invalid date

❮ [[Invalid date]] / [[Invalid date]] / [[Invalid date]] / [[Invalid date]] ❯

❮ [[Invalid date]] | Invalid date | [[Invalid date]] ❯

## Today 🔆

> [!CHECK]+ Super Productivity ☑️
>
> ```tasks
> not done
> (happens on or before Invalid date) OR (status.type is IN_PROGRESS)
> (heading does not include Focus) AND (heading does not include Goals)
> group by function (task.isRecurring) ? '%%3%% Recurring Tasks' : result = task.description.includes("[[") ? '%%1%% Projects' : '%%2%% Tasks'
> ```

> [!IMPORTANT]+ Short Next Actions 🏃
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #next
> group by function task.tags.filter( (tag) => tag.includes("#next") )
> short mode
> ```

## Notes 📝



## Inbox 📥

```todoist
name: Inbox
filter: "#Inbox"
```

## Dashboard 🗺️

> [!DANGER]+ Overdue 📆
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> happens before Invalid date
> group by happens
> ```

> [!CHECK]+ Do Today 📅
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> happens on Invalid date
> group by filename
> ```

> [!WARNING]+ Upcoming 🗓️
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> happens in Invalid date Invalid date
> group by function task.happens.format("YYYY [Week] WW")
> group by happens
> ```

> [!TODO]+ Recurring 🔁
>
> ```tasks
> not done
> is recurring
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'day') || false
> group by filename
> ```

> [!IMPORTANT]+ Next Actions 🏃
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #next
> group by function task.tags.filter( (tag) => ! tag.includes("#next") )
> ```

> [!EXAMPLE]+ Upcoming Projects (by date) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by function (!task.happens.moment) ? '%%4%% *Undated*' : result = task.happens.moment.isBefore(moment(), 'day') ? '%%1%% ==Overdue==' : result = task.happens.moment.isSame(moment(), 'day') ? '%%2%% **Today**' : '%%3%% Future'
> group by function task.happens.format("YYYY > 0Q[ - Quarter] > MM[ - ]MMMM > [Week] WW", task.priorityNameGroupText)
> group by function task.happens.format("YYYY-MM-DD dddd")
> ```

> [!QUESTION]+ Waiting For 💤
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #waiting
> group by filename
> ```

> [!BUG]+ Delegated 👷‍♂️
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #delegated
> group by filename
> ```

> [!SUMMARY]+ Higher Focus 🔥 & Goals 🎯
>
> ```tasks
> not done
> is not recurring
> (path includes -Daily-Notes) OR (path includes -Periodic-Notes)
> (heading includes Focus) AND (heading includes Goals)
> group by function '%%' + (task.heading.includes("Yearly Focus 🔥 & Goals 🎯") ? "1" : task.heading.includes("Quarterly Focus 🔥 & Goals 🎯") ? "2" : task.heading.includes("Monthly Focus 🔥 & Goals 🎯") ? "3" : task.heading.includes("Weekly Focus 🔥 & Goals 🎯") ? "4" : task.heading.includes("Daily Focus 🔥 & Goals 🎯") ? "5" : "6") + '%%' + task.heading + " > " + task.file.filenameWithoutExtension + " > " + task.tags
> ```

## Passions 🎮

> [!QUOTE]+ Ongoing Passions 🎮
>
> ```tasks
> not done
> is not recurring
> filename includes Passions Backlog 🎮
> heading includes Doing
> group by heading
> ```

## Logs 🪵

> [!NOTE]+ Projects Created ➕
>
> ```tasks
> not done
> description includes ]]
> created on Invalid date
> group by filename
> ```

> [!NOTE]+ Tasks Created ➕
>
> ```tasks
> not done
> description does not include ]]
> created on Invalid date
> group by filename
> ```

> [!MISSING]+ Projects Graveyard 🪦
>
> ```tasks
> description includes ]]
> done on Invalid date
> group by filename
> ```

> [!MISSING]+ Tasks Graveyard 🪦
>
> ```tasks
> description does not include ]]
> done on Invalid date
> group by filename
> ```

> [!MISSING]+ Projects Cancelled ❌
>
> ```tasks
> description includes ]]
> cancelled on Invalid date
> group by filename
> ```

> [!MISSING]+ Tasks Cancelled ❌
>
> ```tasks
> description does not include ]]
> cancelled on Invalid date
> group by filename
> ```

## Daily Focus 🔥 & Goals 🎯



## Journal 📔

Mood::

An Interesting Title :

Accomplishments | Failures | Lessons learned | Good and kind things I did | Positive and grateful for :

-


---
title: Invalid date
date: 2026-02-03 22:24:00
lastmod: 2026-02-03 22:24:00
categories:
tags: weekly-notes
aliases:
share: false
---

# Invalid date

❮ [[Invalid date]] / [[Invalid date]] / [[Invalid date]] / [[Invalid date|Invalid date]] ❯

❮ [[Invalid date]] | Invalid date | [[Invalid date]] ❯

❮ [[Invalid date]] | [[Invalid date]] | [[Invalid date]] | [[Invalid date]] | [[Invalid date]] | [[Invalid date]] | [[Invalid date]] ❯

## Dashboard 🗺️

```dataviewjs
await dv.view("_Scripts", {pages: "dv.pages().file.where(f => f.folder != '_Sources' && f.folder != '4-Archives' && f.folder != '5-Templates').tasks.where(t => !t.text.includes('🔁'))", view: "week", firstDayOfWeek: "1", options: "style8 filter", dailyNoteFolder: "-Daily-Notes"})
```

> [!CHECK]+ Projects 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'week') || false
> group by happens
> ```

> [!CHECK]+ Tasks ✅
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'week') || false
> group by happens
> ```

> [!TODO]+ Recurring 🔁
>
> ```tasks
> not done
> is recurring
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'week') || false
> group by happens
> ```

> [!IMPORTANT]+ Next Actions 🏃
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #next
> group by function task.tags.filter( (tag) => ! tag.includes("#next") )
> ```

> [!EXAMPLE]+ Upcoming Projects (by date) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by function (!task.happens.moment) ? '%%4%% *Undated*' : result = task.happens.moment.isBefore(moment(), 'day') ? '%%1%% ==Overdue==' : result = task.happens.moment.isSame(moment(), 'day') ? '%%2%% **Today**' : '%%3%% Future'
> group by function task.happens.format("YYYY > 0Q[ - Quarter] > MM[ - ]MMMM > [Week] WW", task.priorityNameGroupText)
> group by function task.happens.format("YYYY-MM-DD dddd")
> ```

> [!QUESTION]+ Waiting For 💤
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #waiting
> group by filename
> ```

> [!BUG]+ Delegated 👷‍♂️
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #delegated
> group by filename
> ```

> [!SUMMARY]+ Higher Focus 🔥 & Goals 🎯
>
> ```tasks
> not done
> is not recurring
> (path includes -Daily-Notes) OR (path includes -Periodic-Notes)
> (heading includes Focus) AND (heading includes Goals)
> group by function '%%' + (task.heading.includes("Yearly Focus 🔥 & Goals 🎯") ? "1" : task.heading.includes("Quarterly Focus 🔥 & Goals 🎯") ? "2" : task.heading.includes("Monthly Focus 🔥 & Goals 🎯") ? "3" : task.heading.includes("Weekly Focus 🔥 & Goals 🎯") ? "4" : task.heading.includes("Daily Focus 🔥 & Goals 🎯") ? "5" : "6") + '%%' + task.heading + " > " + task.file.filenameWithoutExtension + " > " + task.tags
> ```

## Underground 🚇

> [!EXAMPLE]+ Upcoming Projects (by priority) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by priority
> ```

> [!EXAMPLE]+ Upcoming Projects (by areas) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by filename
> ```

> [!INFO]+ Projects On Hold 🎯
>
> ```tasks
> status.type is NON_TASK
> description includes ]]
> group by filename
> ```

> [!INFO]+ Tasks On Hold ✅
>
> ```tasks
> status.type is NON_TASK
> description does not include ]]
> group by filename
> ```

> [!INFO]+ Unplanned Projects 🎯
>
> ```tasks
> not done
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> (status.type is TODO) AND (no happens date)
> group by filename
> sort by created
> ```

> [!INFO]+ Unplanned One-Off Tasks ✅
>
> ```tasks
> not done
> description does not include ]]
> path includes -Daily-Notes
> (heading does not include Focus) AND (heading does not include Goals)
> (status.type is TODO) AND (no tags) AND (no happens date)
> group by filename
> sort by created
> ```

> [!INFO]+ Unplanned Projects Tasks ✅
>
> ```tasks
> not done
> description does not include ]]
> (path does not include -Daily-Notes) AND (path does not include -Periodic-Notes)
> filename does not include Passions Backlog 🎮
> (status.type is TODO) AND (no tags) AND (no happens date)
> group by filename
> sort by created
> ```

## Logs 🪵

> [!NOTE]+ Projects Created ➕
>
> ```tasks
> not done
> description includes ]]
> created on Invalid date
> group by created
> ```

> [!NOTE]+ Tasks Created ➕
>
> ```tasks
> not done
> description does not include ]]
> created on Invalid date
> group by created
> ```

> [!MISSING]+ Projects Graveyard 🪦
>
> ```tasks
> description includes ]]
> done in Invalid date
> group by done
> ```

> [!MISSING]+ Tasks Graveyard 🪦
>
> ```tasks
> description does not include ]]
> done in Invalid date
> group by done
> ```

> [!MISSING]+ Projects Cancelled ❌
>
> ```tasks
> description includes ]]
> cancelled on Invalid date
> group by filename
> ```

> [!MISSING]+ Tasks Cancelled ❌
>
> ```tasks
> description does not include ]]
> cancelled on Invalid date
> group by filename
> ```

## Weekly Focus 🔥 & Goals 🎯

1. `Declutter & mind dump.` (GET CLEAR)
2. `Reflect on the past week.` (GET CLEAR)
3. `Get current on goals & projects.` (GET CURRENT)
4. `Plan the week ahead.` (GET CURRENT)
5. `Think bigger.` (GET CREATIVE)

## Journal 📔

An Interesting Title :


---
title: Invalid date
date: 2026-02-03 22:24:00
lastmod: 2026-02-03 22:24:00
categories:
tags: yearly-notes
aliases:
share: false
---

# Invalid date

❮ [[Invalid date]] ❯

❮ [[Invalid date]] | Invalid date | [[Invalid date]] ❯

❮ [[Invalid date]] | [[Invalid date]] | [[Invalid date]] | [[Invalid date]] ❯

## Dashboard 🗺️

> [!CHECK]+ Projects 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'year') || false
> group by happens
> ```

> [!CHECK]+ Tasks ✅
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'year') || false
> group by happens
> ```

> [!TODO]+ Recurring 🔁
>
> ```tasks
> not done
> is recurring
> filter by function task.happens.moment?.isSameOrBefore('Invalid date', 'year') || false
> group by happens
> ```

> [!IMPORTANT]+ Next Actions 🏃
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #next
> group by function task.tags.filter( (tag) => ! tag.includes("#next") )
> ```

> [!EXAMPLE]+ Upcoming Projects (by date) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by function (!task.happens.moment) ? '%%4%% *Undated*' : result = task.happens.moment.isBefore(moment(), 'day') ? '%%1%% ==Overdue==' : result = task.happens.moment.isSame(moment(), 'day') ? '%%2%% **Today**' : '%%3%% Future'
> group by function task.happens.format("YYYY > 0Q[ - Quarter] > MM[ - ]MMMM > [Week] WW", task.priorityNameGroupText)
> group by function task.happens.format("YYYY-MM-DD dddd")
> ```

> [!QUESTION]+ Waiting For 💤
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #waiting
> group by filename
> ```

> [!BUG]+ Delegated 👷‍♂️
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #delegated
> group by filename
> ```

> [!SUMMARY]+ Higher Focus 🔥 & Goals 🎯
>
> ```tasks
> not done
> is not recurring
> (path includes -Daily-Notes) OR (path includes -Periodic-Notes)
> (heading includes Focus) AND (heading includes Goals)
> group by function '%%' + (task.heading.includes("Yearly Focus 🔥 & Goals 🎯") ? "1" : task.heading.includes("Quarterly Focus 🔥 & Goals 🎯") ? "2" : task.heading.includes("Monthly Focus 🔥 & Goals 🎯") ? "3" : task.heading.includes("Weekly Focus 🔥 & Goals 🎯") ? "4" : task.heading.includes("Daily Focus 🔥 & Goals 🎯") ? "5" : "6") + '%%' + task.heading + " > " + task.file.filenameWithoutExtension + " > " + task.tags
> ```

## Underground 🚇

> [!EXAMPLE]+ Upcoming Projects (by priority) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by priority
> ```

> [!EXAMPLE]+ Upcoming Projects (by areas) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by filename
> ```

> [!INFO]+ Projects On Hold 🎯
>
> ```tasks
> status.type is NON_TASK
> description includes ]]
> group by filename
> ```

> [!INFO]+ Tasks On Hold ✅
>
> ```tasks
> status.type is NON_TASK
> description does not include ]]
> group by filename
> ```

> [!INFO]+ Unplanned Projects 🎯
>
> ```tasks
> not done
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> (status.type is TODO) AND (no happens date)
> group by filename
> sort by created
> ```

> [!INFO]+ Unplanned One-Off Tasks ✅
>
> ```tasks
> not done
> description does not include ]]
> path includes -Daily-Notes
> (heading does not include Focus) AND (heading does not include Goals)
> (status.type is TODO) AND (no tags) AND (no happens date)
> group by filename
> sort by created
> ```

> [!INFO]+ Unplanned Projects Tasks ✅
>
> ```tasks
> not done
> description does not include ]]
> (path does not include -Daily-Notes) AND (path does not include -Periodic-Notes)
> filename does not include Passions Backlog 🎮
> (status.type is TODO) AND (no tags) AND (no happens date)
> group by filename
> sort by created
> ```

## Logs 🪵

> [!NOTE]+ Projects Created ➕
>
> ```tasks
> not done
> description includes ]]
> created on Invalid date
> group by created
> ```

> [!NOTE]+ Tasks Created ➕
>
> ```tasks
> not done
> description does not include ]]
> created on Invalid date
> group by created
> ```

> [!MISSING]+ Projects Graveyard 🪦
>
> ```tasks
> description includes ]]
> done in Invalid date
> group by done
> ```

> [!MISSING]+ Tasks Graveyard 🪦
>
> ```tasks
> description does not include ]]
> done in Invalid date
> group by done
> ```

> [!MISSING]+ Projects Cancelled ❌
>
> ```tasks
> description includes ]]
> cancelled on Invalid date
> group by filename
> ```

> [!MISSING]+ Tasks Cancelled ❌
>
> ```tasks
> description does not include ]]
> cancelled on Invalid date
> group by filename
> ```

## Yearly Focus 🔥 & Goals 🎯

- `Add some goals for the year`

## Journal 📔

An Interesting Title :



# <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>

<%*
const currentMoment = moment(tp.file.title, "YYYY-MM-DD");
const hash = '# ';
const slash = ' / ';
const pipe = ' | ';
const leftAngle = '❮ ';
const rightAngle = ' ❯';
tR += leftAngle;
tR += '[[' + currentMoment.format('YYYY') + ']]' + slash;
tR += '[[' + currentMoment.format('YYYY-[Q]Q|[Q]Q') + ']]' + slash;
tR += '[[' + currentMoment.format('YYYY-MM|MMMM') + ']]' + slash;
tR += '[[' + currentMoment.format('GGGG-[W]WW|[Week] WW') + ']]';
tR += rightAngle;
tR += '\n';
tR += '\n';
tR += leftAngle;
currentMoment.add(-1,'days');
tR += '[[' + currentMoment.format('YYYY-MM-DD|dddd Do') + ']]' + pipe;
currentMoment.add(1,'days');
tR += currentMoment.format('dddd Do') + pipe;
currentMoment.add(1,'days');
tR += '[[' + currentMoment.format('YYYY-MM-DD|dddd Do') + ']]';
currentMoment.add(-1,'days');
tR += rightAngle;
%>

## Today 🔆

> [!CHECK]+ Super Productivity ☑️
>
> ```tasks
> not done
> (happens on or before <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>) OR (status.type is IN_PROGRESS)
> (heading does not include Focus) AND (heading does not include Goals)
> group by function (task.isRecurring) ? '%%3%% Recurring Tasks' : result = task.description.includes("[[") ? '%%1%% Projects' : '%%2%% Tasks'
> ```

> [!IMPORTANT]+ Short Next Actions 🏃
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #next
> group by function task.tags.filter( (tag) => tag.includes("#next") )
> short mode
> ```

## Notes 📝



## Inbox 📥

```todoist
name: Inbox
filter: "#Inbox"
```

## Dashboard 🗺️

> [!DANGER]+ Overdue 📆
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> happens before <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by happens
> ```

> [!CHECK]+ Do Today 📅
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> happens on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

> [!WARNING]+ Upcoming 🗓️
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> happens in <% moment(tp.file.title, "YYYY-MM-DD").add(1,"days").format("YYYY-MM-DD") %> <% moment(tp.file.title, "YYYY-MM-DD").add(30,"days").format("YYYY-MM-DD") %>
> group by function task.happens.format("YYYY [Week] WW")
> group by happens
> ```

> [!TODO]+ Recurring 🔁
>
> ```tasks
> not done
> is recurring
> filter by function task.happens.moment?.isSameOrBefore('<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>', 'day') || false
> group by filename
> ```

> [!IMPORTANT]+ Next Actions 🏃
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #next
> group by function task.tags.filter( (tag) => ! tag.includes("#next") )
> ```

> [!EXAMPLE]+ Upcoming Projects (by date) 🎯
>
> ```tasks
> not done
> is not recurring
> description includes ]]
> filename does not include Passions Backlog 🎮
> (heading does not include Focus) AND (heading does not include Goals)
> group by function (!task.happens.moment) ? '%%4%% *Undated*' : result = task.happens.moment.isBefore(moment(), 'day') ? '%%1%% ==Overdue==' : result = task.happens.moment.isSame(moment(), 'day') ? '%%2%% **Today**' : '%%3%% Future'
> group by function task.happens.format("YYYY > 0Q[ - Quarter] > MM[ - ]MMMM > [Week] WW", task.priorityNameGroupText)
> group by function task.happens.format("YYYY-MM-DD dddd")
> ```

> [!QUESTION]+ Waiting For 💤
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #waiting
> group by filename
> ```

> [!BUG]+ Delegated 👷‍♂️
>
> ```tasks
> not done
> is not recurring
> description does not include ]]
> tags include #delegated
> group by filename
> ```

> [!SUMMARY]+ Higher Focus 🔥 & Goals 🎯
>
> ```tasks
> not done
> is not recurring
> (path includes -Daily-Notes) OR (path includes -Periodic-Notes)
> (heading includes Focus) AND (heading includes Goals)
> group by function '%%' + (task.heading.includes("Yearly Focus 🔥 & Goals 🎯") ? "1" : task.heading.includes("Quarterly Focus 🔥 & Goals 🎯") ? "2" : task.heading.includes("Monthly Focus 🔥 & Goals 🎯") ? "3" : task.heading.includes("Weekly Focus 🔥 & Goals 🎯") ? "4" : task.heading.includes("Daily Focus 🔥 & Goals 🎯") ? "5" : "6") + '%%' + task.heading + " > " + task.file.filenameWithoutExtension + " > " + task.tags
> ```

## Passions 🎮

> [!QUOTE]+ Ongoing Passions 🎮
>
> ```tasks
> not done
> is not recurring
> filename includes Passions Backlog 🎮
> heading includes Doing
> group by heading
> ```

## Logs 🪵

> [!NOTE]+ Projects Created ➕
>
> ```tasks
> not done
> description includes ]]
> created on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

> [!NOTE]+ Tasks Created ➕
>
> ```tasks
> not done
> description does not include ]]
> created on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

> [!MISSING]+ Projects Graveyard 🪦
>
> ```tasks
> description includes ]]
> done on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

> [!MISSING]+ Tasks Graveyard 🪦
>
> ```tasks
> description does not include ]]
> done on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

> [!MISSING]+ Projects Cancelled ❌
>
> ```tasks
> description includes ]]
> cancelled on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

> [!MISSING]+ Tasks Cancelled ❌
>
> ```tasks
> description does not include ]]
> cancelled on <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
> group by filename
> ```

## Daily Focus 🔥 & Goals 🎯



## Journal 📔

Mood::

An Interesting Title :

Accomplishments | Failures | Lessons learned | Good and kind things I did | Positive and grateful for :

-

<% await tp.file.move("/-Daily-Notes/" + tp.file.title) %>
