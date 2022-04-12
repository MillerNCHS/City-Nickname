<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "cities = {&quot;New York City&quot;: &quot;The Big Apple&quot;, &quot;Chicago&quot;: &quot;The Windy City&quot;, &quot;Houston&quot;: &quot;Space City&quot;}\n" +
    " \n" +
    "# New York City is protesting apples and wants to change their nickname before it is printed\n" +
    "cities[&quot;New York City&quot;] = &quot;The City That Never Sleeps&quot;\n" +
    " \n" +
    "city = input(&quot;Enter the name of a city to get its nickname: &quot;)\n" +
    "if city in cities:\n" +
    " print(cities[city])\n" +
    "else:\n" +
    " print(&quot;I don&#039;t know that city&#039;s nickname.&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
