<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "# Initialize tuples with Fortnite players and their wins. Then print a table with that information and output the average number of wins.\n" +
    "players = (&quot;Arkhram&quot;, &quot;EpikWhale&quot;, &quot;Bugha&quot;, &quot;Edgey&quot;, &quot;Ninja&quot;)\n" +
    "wins = (10410, 10371, 7264, 7022, 6703)\n" +
    " \n" +
    "count = 0\n" +
    "total = 0\n" +
    " \n" +
    "print (&quot;{:&lt;25}{:&lt;25}&quot;.format(&quot;Players&quot;, &quot;Wins&quot;))\n" +
    " \n" +
    "for person in players:\n" +
    " print (&quot;{:&lt;25}{:&lt;25,}&quot;.format(person, wins[count]))\n" +
    " total = total + wins[count]\n" +
    " count = count + 1\n" +
    " \n" +
    "print (&quot;{:&lt;25}{:&lt;25,.0f}&quot;.format(&quot;Average&quot;, total/count))";
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
