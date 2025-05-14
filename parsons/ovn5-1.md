
---
layout: default
title: Parson's Problems Övning 5 DD1310
description: Dra kodrader som behövs för att konstruera programmet till den gula rutan. Tänk på att ordningen och indenteringen på kodraderna spelar roll. Du kan sedan klicka på "Get feedback" för att få reda på vilka rader som är rätt. Välj "reset" för att börja om.
---


## Parsons 1 (Felhantering)
<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def positivt_heltal(inmatning):\n" +
    "    try:\n" +
    "        inmatning = int(inmatning)\n" +
    "        if inmatning &lt; 0:\n" +
    "            print(&quot;Inte positivt.&quot;)\n" +
    "    except ValueError:\n" +
    "        print(&quot;Inte en siffra&quot;)\n" +
    "        \n" +
    "def huvudfunktion():\n" +
    "    positivt_heltal(-4)\n" +
    "huvudfunktion()";
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
