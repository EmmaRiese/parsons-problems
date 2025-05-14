---
layout: default
title: Parson's Problems Övning 5 DD1310
description: Dra kodrader som behövs för att konstruera programmet till den gula rutan. Tänk på att ordningen och indenteringen på kodraderna spelar roll. Du kan sedan klicka på "Get feedback" för att få reda på vilka rader som är rätt. Välj "reset" för att börja om.
---


## Parsons 2 (Klasser)

Konstruera en konstruktor och en __str__-metod för klassen Bok. Skapa sedan ett objekt och testa att du kan skriva ut objektet.

<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "class Bok:\n" +
    "  \n" +
    "  def __init__(self, titel, av, sidor):\n" +
    "    self.titel = titel\n" +
    "    self.skriven_av = av\n" +
    "    self.antal_sidor = sidor\n" +
    "    \n" +
    "  def __str__(self):\n" +
    "    return self.titel +  &quot;, skriven av: &quot; + self.skriven_av + &quot;, har &quot; + str(self.antal_sidor) + &quot; sidor.&quot;\n" +
    "bok = Bok(&quot;Dansa min docka&quot;, &quot;Anna Jansson&quot;, 363)\n" +
    "print(bok)\n" +
    "self.av = skriven_av #distractor\n" +
    "self.sidor = antal_sidor #distractor\n" +
    "print(self.titel +  &quot;, skriven av: &quot; + self.skriven_av + &quot;, har &quot; + str(self.antal_sidor) + &quot; sidor.&quot;) #distractor";
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
