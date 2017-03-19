# \<dc-schedule\>

A material (ish) design schedule view WebComponent - built upon Polymer 2.0.
Simply pass an array of events and we'll schedule them to fit & display them for you.

## Demo
<!---
```
<custom-element-demo>
  <template>
    <script src="../webcomponentsjs/webcomponents-lite.js"></script>
    <link rel="import" href="dc-schedule.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html
<dom-bind id="demo-dom">
  <template>
    <dc-schedule date="[[date]]"
             min-time="[[minTime]]"
             max-time="[[maxTime]]"
             empty-message="That day appears to be empty!">
    </dc-schedule>
  </template>
</dom-bind>

<script>
  var demo = document.querySelector('#demo-dom');
  demo.date = new Date(2013, 2, 13, 9, 20);
  demo.events = [
    {
      name: 'Keynote',
      description: 'The keynote speech',
      location: 'Grand Hall',
      start: new Date(2013, 2, 1, 9, 20),
      end: new Date(2013, 2, 1, 13, 50),
      colour: '#00E4FF'
    },
    {
      name: 'Redux Talk',
      description: 'Flux Guise',
      location: 'AB123',
      start: new Date(2013, 2, 1, 13, 20),
      end: new Date(2013, 2, 1, 14, 50),
      colour: '#FFD500'
    },
    {
      name: 'Polymer Talk',
      description: 'Web components Guise',
      location: 'Grand Hall',
      start: new Date(2013, 2, 1, 13, 50),
      end: new Date(2013, 2, 1, 15, 50)
    },
  ];
  demo.minTime = new Date(2013, 2, 1, 9, 0);
  demo.maxTime =  new Date(2013, 2, 1, 16, 0);
</script>
```