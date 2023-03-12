# mspfaViewer
This script was made to let you host your mspfa or original comic on it's own site.

## Setup
Each folder contains all the files necessary to view your adventure when hosted. Download the folders contents and host them on your own site.

`adventure.json` is the file that contains all your adventure data. If you want to host an existing MSPFA adventure simply past in it's adventure object overtop of the template. Else copy the `template.json` file and fill it out with your own adventure data.

`adventure.json` should have at least these values:
```json
{
  "n": "Adventure name",
  "o": "Link to adventure Icon",

  "p": [ ... ]
}
```
- **n**ame is the name of your adventure
- ic**o**n is the icon of your advnture, this will be it's favicon in the viewer
- **p** pages is an array of page objects for each page of your adventure

Page objects have these values:
```json
{
  "d": 1671518387574,
  "c": "Page 1 title",
  "b": "Page 1 content",
  "n": [ 2 ]
}
```
- **d**ate is the date the page was published in as a unix timestamp
- **c**ommand is the page's command or title, using html and/or mspfa bbcode
- **b**ody is the content of the page, using html and/or mspfa bbcode
- **n**ext is an array of page indexes pointing to the next page (Page indexes start at 1)
