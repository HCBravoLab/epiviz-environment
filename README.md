### must use polymer api to add charts to environment. Js dom api does not properly initialize elements

for example

if the page contains

```
<epiviz-environment id="env">
</epiviz-environment>
```

to add an epiviz chart for example line-track.

# create a new element
```
elem = document.createElement('epiviz-line-track'); 
elem.dimS = ['affy1', 'affy2']; 
elem.dimX = 'affy1'; 
elem.dimY = 'affy2'; 
elem.className="charts"
```

# query dom for environment
`ot = document.querySelector('#env')`

# add chart
`Polymer.dom(ot).appendChild(elem)`