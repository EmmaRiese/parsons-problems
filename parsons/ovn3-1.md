---
layout: default
title: Parson's Problems Övning 3 DD1310
description: Dra kodrader som behövs för att konstruera programmet till den gula rutan. Tänk på att ordningen och indenteringen på kodraderna spelar roll. Du kan sedan klicka på "Get feedback" för att få reda på vilka rader som är rätt. Välj "reset" för att börja om.
---


## Parsons 1 (Multiplikationstabell)

Skriv ett program som skriver ut en multiplikationstabell där varje rad innehåller multiplikationstabellen för talen 1-5 (t.ex. Rad 1: 1 2 3 4 5).
<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "for i in range(1,6):\n" +
    "    print(&quot;Rad&quot; + str(i) + &quot;:&quot;, end=&quot; &quot;)\n" +
    "    for j in range(1,6):\n" +
    "        print(i*j, end =&quot; &quot;)\n" +
    "    print()\n" +
    "for j in range(1,5): #distractor\n" +
    "for i in range(1,5): #distractor";
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

## Parsons 2 (Udda först, jämna sedan)

Skriv ett program som får en lista med heltal och skapar en ny lista där alla udda tal hamnar i början och jämna tal i slutet.

<div id="2-sortableTrash" class="sortable-code"></div> 
<div id="2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "lista = [1, 4, 2, 5, 13, 12, 7, 23]\n" +
    "ny_lista = []\n" +
    "for i in lista:\n" +
    "    if i%2 == 1:\n" +
    "        ny_lista.append(i)\n" +
    "for j in lista:\n" +
    "    if j%2 == 0:\n" +
    "        ny_lista.append(j)\n" +
    "print(ny_lista)";
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

## Parsons 3 (Matrisutskrift)

Skriv ett program som skriver ut ett en given matris, så att varje rad är på en egen rad och det är mellanslag mellan varje element.

<div id="3-sortableTrash" class="sortable-code"></div> 
<div id="3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "matris = [[0,1,1],[1,0,0],[0,0,0]]\n" +
    "for rad in matris:\n" +
    "    for element in rad:\n" +
    "        print(element, end=&quot; &quot;)\n" +
    "    print()\n" +
    "print(rad, end= &quot; &quot;)  #distractor";
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


## Parsons 4 (Hur många nollor?)

Skriv ett program som går igenom en matris och räknar hur många gånger talet 0 finns i matrisen.

<div id="4-sortableTrash" class="sortable-code"></div> 
<div id="4-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="4-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="4-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "matrix = [[0,1,1],[1,0,0],[0,0,0]]\n" +
    "counter = 0\n" +
    "for row in matrix:\n" +
    "    for element in row:\n" +
    "        if element == 0:\n" +
    "            counter +=1\n" +
    "print(&quot;Det fanns&quot;, counter, &quot;nollor i matrisen.&quot;)\n" +
    "for element in matrix: #distractor";
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
