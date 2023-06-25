# grEEEn
<iframe width="450" height="260" style="border: 1px solid #cccccc;" src="https://thingspeak.com/channels/2149974/charts/1?bgcolor=%23ffffff&color=%23d62020&dynamic=true&api_key=5TQGBVEM7FR1IZ4Y&results=60&type=line&update=15"></iframe>

<title>Apps - Plugins - ThingSpeak IoT</title>
<html>
  <head>

  <!-- 
  
  NOTE: This plugin will not be visible on public views of a channel. 
        If you intend to make your channel public, consider using the
        MATLAB Visualization App to create your visualizations.
  
  -->  
  
  <title>Google Gauge - ThingSpeak</title>

  <style type="text/css">
  body { background-color: #ddd; }
  #container { height: 100%; width: 100%; display: table; }
  #inner { vertical-align: middle; display: table-cell; }
  #gauge_div { width: 150px; margin: 0 auto; }
</style>


  <script type='text/javascript' src='https://ajax.googleapis.com/ajax/libs/jquery/1.9.1/jquery.min.js' integrity="sha384-EaUkI/FiMJtEXWAl0dCczvbFvjfzsIF1UNKGJvu9p5JIG71Kih7/kQJvYbBL7HOn" crossorigin="anonymous"></script>
<script type='text/javascript' src='https://www.google.com/jsapi'></script>
<script type='text/javascript'>

  // set your channel id here
  var channel_id = 2149974;
  // set your channel's read api key here if necessary
  var api_key = '5TQGBVEM7FR1IZ4Y';
  // maximum value for the gauge
  var max_gauge_value = 1023;
  // name of the gauge
  var gauge_name = 'Light Level';

  // global variables
  var chart, charts, data;

  // load the google gauge visualization
  google.load('visualization', '1', {packages:['gauge']});
  google.setOnLoadCallback(initChart);

  // display the data
  function displayData(point) {
    data.setValue(0, 0, gauge_name);
    data.setValue(0, 1, point);
    chart.draw(data, options);
  }

  // load the data
  function loadData() {
    // variable for the data point
    var p;

    // get the data from thingspeak
    $.getJSON('https://api.thingspeak.com/channels/' + channel_id + '/feed/last.json?api_key=' + api_key, function(data) {

      // get the data point
      p = data.field1;

      // if there is a data point display it
      if (p) {
        p = Math.round((p / max_gauge_value) * 100);
        displayData(p);
      }

    });
  }

  // initialize the chart
  function initChart() {

    data = new google.visualization.DataTable();
    data.addColumn('string', 'Label');
    data.addColumn('number', 'Value');
    data.addRows(1);

    chart = new google.visualization.Gauge(document.getElementById('gauge_div'));
    options = {width: 120, height: 120, redFrom: 90, redTo: 100, yellowFrom:75, yellowTo: 90, minorTicks: 5};

    loadData();

    // load new data every 15 seconds
    setInterval('loadData()', 15000);
  }

</script>


  </head>

  <body>
    <div id="container">
      <div id="inner">
        <div id="gauge_div"></div>
      </div>
    </div>
  </body>
</html>
