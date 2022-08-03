---
has_children: true
has_toc: false
layout: default
title: Obsidian Stress Test
full-width: true
nav_order: 2
---
# ObsidianStressTest (H1)
## H2 Quick Test

  You can also create quick links, like my page [[Good Trip List]]   Here is an external link being [a YouTube video](https://www.youtube.com/watch?v=VPBmshzmtVM) of **mine** from near *Apollo Bay.*  Inline `code` sample.
 
```sql
# For testing, ensure they have the text 'love' in the Songname
SELECT *
FROM SongsWithBook
WHERE Songname LIKE %love%'
````

### Heading 3 and some lists
Things to buy:
- Cat
- Dog with collar
- Something else

1. But something
2. Put a record into the database
3. Check you can find it via *browse* and then *search*.
#### Heading 4
Basic code/log_listing:

```
# Log file listing
Log begins
  1010 Start up
  1011 Error with socket
    Error code A3D
  1022 Exit return code -4
Log file ends
```

Here's a Powershell script code block

```powershell
# stop and start Print Spoooler
# must be run from Admin PowerShell prompt
#   https://www.lifehacker.com.au/2021/07/how-to-avoid-windows-printnightmare-security-threat/
param ($action)
if ($action -eq 'stop') {
Write-Host 'will be STOPPING and DISABLING the Spooler'
Write-Host '..stopping..'
Stop-Service -Name Spooler -Force
Write-Host '....Disabling auto_startup'
Set-Service -Name Spooler -StartupType Disabled
Get-Service -Name Spooler | Select-Object -Property *
}
```

I can draw your ==attention== to something or even indicate that it ~~no longer applies~~  Here is a **table**:

Item | Description
---- | ---
Keyboard | Allows you to type into the computer
Printer | Creates printed output onto paper
Mouse | Freeform input device 
Monitor  | Display screen. May have speakers 

Now a wide table

Item | Description | Last Column
---- | --- | ---
Keyboard | Allows you to type into the computer | Not so wide
Mouse | Now is the time for all good men to come to the aid of the party and see if they can help us with whatver we need | An input device | 
Screen | [A long movie title](https://www.imdb.com/title/tt0031381)


And this is a block quote with attribution:

>Imagination is more important than knowledge. Knowledge is limited. Imagination encircles the world.

\- Albert Einstein

This is a tag
#tips

## Link  testing

#### External
Just the link:

https://sidwell.id.au/2020/06/29/photos-williamstown-sunset-mt-macedon-and-hanging-rock/

[My own link description](https://sidwell.id.au/2020/06/29/photos-williamstown-sunset-mt-macedon-and-hanging-rock/)

** Image link (imbedded)** : 
Streeton (1934).  '....."He was deeply concerned when he came back to Australia in the 1920s, seeing much-loved landscapes being cut down." In 'The vanishing forest', Streeton is making a statement. It's a large-scale painting, intentionally similar in size to his most famous works, and, as Tunnicliffe tells us, he's asking Australians to take the destruction seriously....' [source](https://concreteplayground.com/sydney/arts-entertainment/five-key-paintings-by-impressionist-arthur-streeton-and-why-theyre-still-relevant-today)
![here it is](https://images.theconversation.com/files/368447/original/file-20201110-18-1alpa7a.jpg)


#### Internal Links

Can we can jump straight to [[docs]] (that is Wikilink format) ?

What about to a place within this same page/note?  [[#H2 Quick Test]]

## Others

### Callouts (Rubrics) *new*

>[!Note] My title
>Need to update version 2 

### Checklist

- [x] This
- [ ] is a
- [ ] checklist

#star