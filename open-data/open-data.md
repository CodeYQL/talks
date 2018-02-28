# How to use **Open Data** without tearing your hair out
##### CodeYQL - March 22, 2016

^ Hey everyone, thanks so much for coming out tonight, I'd first
of all like to take a moment to apologize for the craziness that
constitutes my life: I haven't been able to dedicate any time to
CodeYQL over the last couple months, but I'd like to thank you
all for showing up despite that. You're all pretty awesome.

---

# Why use **Open Data**?

---

> "...when the marginal cost of making a copy and distributing it has shrunk to zero, all limitations on digital information are in a profound sense artificial."
-- Albert Wenger, "World After Capital"

^He goes on to say: 'Why are we spending money to make information less accessible? When information existed only in analog form, the cost of copying and distribution allowed us — and to some degree required us — to build an economy and a society grounded on information's scarcity.' As citizens, we are spending money every year (in the form of municipal taxes) that are going toward the production, analysis, retention, and distribution of this data. Why then, shouldn't we be allowed to see it?

---

# **Open Data**
### Technologically & Legally

^It’s information in raw form that meets two distinct criteria:
Technologically open: the data is provided in a machine-readable (preferably non-commercial/proprietary) format that can be retrieved, processed, and presented in a meaningful way
Legally open: anyone with access to the data can copy, publish, translate, adapt, or distribute the information for any lawful purpose.
So why is open data important to us? Well, here's a quote from Albert Wenger, he's a pretty smart dude who started a venture capital firm called Union Square Ventures in New York City. They've funded companies like Kickstarter, Stack Overflow, and Meetup.

---

# `<interlude>`
# a short history lesson

^So because this is CodeYQL after all, i'd like to share with you a bit of lethbridge history

---

# [fit] **"Ad occasionis januam"**

^Our city’s slogan means “gateway to opportunity”, and that means we have a responsibility as citizens to be champions of innovation and provide a sustainable quality of life for the folks who live here. We have a dynamic group of developers in the city who, by coming together to collaborate, share and learn, add to the innovation that is possible in Lethbridge.

---

![inline](nicholas-sheran.jpg)

^A good example of this attitude was this guy. Anyone know who this is? In 1872, a man named Nicholas Sheran, a man of many trades, stumbled upon Lethbridge after being shipwrecked in the far North, pioneering in Montana, and various other things. At first, he was involved heavily with the infamous whisky trade, but with the arrival of the northwest mounted police, he decided to clean his act up and in 1874 he opened up Lethbridge's first coal mine. It wasn't until 1879, when lethbridge coal was already a hot commodity, that Sir Alexander Galt and his son, Elliot Torrence Galt would open a mine of their own. Unfortunately, Sheran would never live to see the true repercussions of his decision to market lethbridge coal, he drowned in 1882. But without such a fierce pioneering attitude, Lethbridge's economy probably wouldn't have flourished, and who knows where we would be today.
His contributions to the Lethbridge economy didn't go unnoticed, so in 1974, they named a lake after him. And a swimming pool.

---

![inline fill](nicholas-sheran-lake.jpg)

---

# `</interlude>`

^End of interlude. What does any of this have to do with open data, you might say? So even though our economy was founded by pioneers in the resource sector, in order to advance in the 21st century, we've got to be pioneers of data. WE need to be as resourceful as the first settlers in Lethbridge and mine out information. So how do we stop talking about being the Nicholas Sheran of data and actually do something cool?

---

# CSV

^Let's talk about CSV: CSV is a dead simple format, but it can get really big, really fast. It's basically just a table of values, separated by commas (which denote the columns), and carriage returns (which denote new rows). There are tons of libraries out there for manipulating CSV data, and lots of languages (like Julia, R, Python and Ruby) have support baked into their standard libraries.

---

### Typical CSV Dataset [^1]
```
"Efficiency", "Individual", "ChopstickLength"
19.55, 1, 180
27.24, 2, 180
28.76, 3, 180
31.19, 4, 180
21.91, 5, 180
27.62, 6, 180
29.46, 7, 180
26.35, 8, 180
26.69, 9, 180
30.22, 10, 180
27.81, 11, 180
23.46, 12, 180
```

[^1]: Hsu, Sheng-Hsiung, and Swei-Pi Wu. "An Investigation for Determining the Optimum Length of Chopsticks." Applied Ergonomics 22.6 (1991): 395-400. Web.

---

# Shapefiles

^Shapefiles were conceived by a company called ESRI way back in the early 90's, back when the Macarena, fanny packs and AOL were all the rage. ESRI makes a ginormous and ludicrously expensive piece of software called ArcGIS that people use to make maps and in general do geospatial stuff. It's a pretty unwieldy format, but there are libraries you can use to

---

### Excerpt from a typical shapefile[^2]

```
<A6>><D8>H@<B6><85><8E><A8>j3\<C0>^N<D6>M<C5>><D8>H@<C1>}#<91>j3\<C0><E7><F6><A4>
<E4>><D8>H@<F4>b<C5>yj3\<C0>=<FF>&^D?<D8>H@P;<83>bj3\<C0>[ž#?<D8>H@<F5><FA>VKj3\
<C0><AE><E2>sC?<D8>H@<F0><B9>=4j3\<C0>^SLJc?<D8>H@<AD><FD>D^]j3\<C0>L<D6>2<83>?
<D8>H@:A_^Fj3\<C0>^N<85><<A3>?<D8>H@^T`<86><EF>i3\<C0><AC>^Vm<C3>?<D8>H@<FC>^U<D7>
<D8>i3\<C0>|;<A4><E3>?<D8>H@à1<C2>i3\<C0>e7^F^D@<D8>H@]<AB><A0><AB>i3\<C0>|<<8D>
$@<D8>H@<A2>43<95>i3\<C0><A4><B6>^\E@<D8>H@<9E>U<DD>~i3\<C0>a<B6><C7>e@<D8>H@cўhi3
$@<D8>HELP I'M>43<TRAPPED<A>INSIDE<D8>AN ESRI<D8>H@]<C0>FILE FORMAT<D8<B7>q<AF>9_3\
\<C0>p:<8E><86>@<D8>H@><CD>nRi3\<C0><A2><84>}<A7>@<D8>H@<A5><C7>`<i3\<C0><CA>^Z{
<C8>@<D8>H@A5d&i3\<C0><DB><F4><99><E9>@<D8>H@f^V<82>^Pi3\<C0>^S<<D4>A<D8>H@^]<D0>
<D5><FA>h3\<C0>s<9B><F8>+A<D8>H@>v<BD><E5>h3\<C0><87>^XtLA<D8>H@_<C6><F9>e_3\<C0>
6^W<81><FE>O<D8>H@r<8E>^TO_3\<C0><DA>r<A2>!P<D8>H@<B7>q<AF>9_3\<C0>^C]<E2>AP<D8>
H@<9A>^@^T$_3\<C0>Z<E1>aP<D8>H@)<DF>=^N_3\<C0><84>Y<A5><81>P<D8>H@<F2><DC>5<F8>
^3\<C0><BE><C0><BA><B7><A1>aV<D8>H@i<E6><A4>^QW3\<C0><FB>31jV<D8>H@<AE>Dr<F1>V3\
<C0><89><99>erV<D8>H@<9D><C6>7<D1>V3\<C0><BE>G9zV<D8>H@@^]<EE><B0>V3\<C0><93><F4>
<AF><81>V<D8>H@s<BC><93><90>V3\<C0>ӗɈV<D8>H@<C5>#6pV3\<C0>O<9C><82><8F>V<D8>H@4A
<C6>OV3\<C0>^D<91><E0><95>V<D8>H@<92><94>W/V3\<C0>G<FC>ۛV<D8>H@^TC<CF>^NV3\<C0>
<AE>.z<A1>V<D8>H@*.9<EE>U3\<C0><BA>A<BD><A6>V<D8>H@WB<AA><CD>U3\<C0>f^R<9E><AB>
```

[^2]: City of Lethbridge. "Neighborhoods" (modified excerpt). https://www.arcgis.com/home/item.html?id=81568ca5241e409696f1bb59159eb4c6

---

# JSON

---

### Simple JSON API response[^3]

```javascript
{
  "facts": [
    "While many cats enjoy milk, it will give some cats diarrhea.",
    "In relation to their body size, cats have the largest eyes of any mammal."
  ],
  "success": "true"
}
```

[^3]: Cat Facts API Documentation. http://catfacts-api.appspot.com/doc.html

---

# GeoJSON

---

### Some GeoJSON[^4]

```javascript
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [49.7354671, -112.8025357]
  },
  "properties": {
    "name": "Chris"
  }
}
```

[^4]: Crabl location API. http://not-so-fast-there-nsa/location/crabl.geojson

^ GeoJSON is a standardized schema for encoding geospatial information in JSON so it can be parsed really easily

---

## **Demo:** converting a shapefile to GeoJSON and using it in a web app

---

# Licensing

### City of Lethbridge Open Data License 1.0

- Worldwide, royalty-free, non-exclusive license
- Free to copy, modify, publish, translate, adapt, distribute, use for any lawful purpose
- Does not cover information as defined in FOIP
- No warranty: what you see is what you get
- You're responsible for your own use/reproduction of datasets
- Indemnification

This is an example of a typical license, your mileage may vary

^ The Indemnification clause here is basically legal for "you can't sue us"

---

# Where to Find Open Data

- opendata.lethbridge.ca
- data.calgary.ca
- data.edmonton.ca
- open.alberta.ca
- open.canada.ca

---

# Hackathons

### canadianopendataexperience.com
### intelligentyql.ca

---

# Some upcoming events

- IntelligentYQL "Code-a-Thon": intelligentyql.ca
  - April 14-16 at **tec**connect
  - $25/person, $20/student, $100/team (maximum 5)

- Startup Weekend
  - October 21-23 at **tec**connect
  - pricing TBA, website TBA

---

# Thanks!
