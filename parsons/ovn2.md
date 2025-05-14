---
layout: default
title: Parson's Problems Övning 2 DD1310
description: Dra kodrader som behövs för att konstruera programmet till den gula rutan. Tänk på att ordningen och indenteringen på kodraderna spelar roll. Du kan sedan klicka på "Get feedback" för att få reda på vilka rader som är rätt. Välj "reset" för att börja om.
---


## Parsons 1 (Udda eller jämnt?)

Skriv ett program som kontrollerar om ett inmatat tal är jämt eller udda.

<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number = int(input(&quot;Please type in a number: &quot;))\n" +
    "if number%2 == 1:\n" +
    "    print(&quot;Your number is odd.&quot;)\n" +
    "else:\n" +
    "    print(&quot;Your number is even&quot;)\n" +
    "if number%2 == 2: #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Parsons 2 (Jämföra resultat)

Skriv ett program som jämför ett resultat. 10 är max, över 5 är bra, annars behövs lite uppmuntran.

<div id="2-sortableTrash" class="sortable-code"></div> 
<div id="2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "result = int(input(&quot;Please type your result: &quot;))\n" +
    "if result &gt; 10:\n" +
    "    print(&quot;That is strange, max was 10.&quot;)\n" +
    "elif result == 10:\n" +
    "    print(&quot;You got all points! Awesome!&quot;)\n" +
    "elif result &gt; 5:\n" +
    "    print(&quot;You did well!&quot;)\n" +
    "else:\n" +
    "    print(&quot;Try again, practice makes perfect!&quot;)\n" +
    "elif result &gt; 6: används inte #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Parsons 3 (När ska vi sluta slingan?)

Skriv ett program som skriver ut heltal upp till ett önskat värde.

<div id="3-sortableTrash" class="sortable-code"></div> 
<div id="3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "number = int(input(&quot;Please type in the highest number you like to print: &quot;))\n" +
    "i = 1\n" +
    "while i &lt;= number:\n" +
    "    print(i, end=&quot; &quot;)\n" +
    "    i+=1\n" +
    "i-=1 #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "3-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "3-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


## Parsons 4 (Hello?)

#Skriv ett program som skriver ut "Hello!" fram till det användaren väljer att avsluta.

<div id="4-sortableTrash" class="sortable-code"></div> 
<div id="4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "keep_going = True\n" +
    "while keep_going:\n" +
    "    print(&quot;Hello&quot;)\n" +
    "    choice = input(&quot;Would you like another Hello? (yes/no) &quot;)\n" +
    "    if choice[0] != &quot;y&quot;:\n" +
    "        keep_going = False\n" +
    "if choice[0] != &quot;n&quot;: #distractor\n" +
    "while not keep_going: #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "4-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "4-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#4-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#4-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
