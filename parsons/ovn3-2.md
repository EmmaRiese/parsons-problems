---
layout: default
title: Parson's Problems Övning 3 DD1310
description: Dra kodrader som behövs för att konstruera programmet till den gula rutan. Tänk på att ordningen och indenteringen på kodraderna spelar roll. Du kan sedan klicka på "Get feedback" för att få reda på vilka rader som är rätt. Välj "reset" för att börja om.
---


## Parsons 1 (Funktioner)
Skriv två funktioner, en som frågar användaren om tre heltal och returnerar talen. Den andra funktionen tar emot tre heltal som parameter och returnerar produkten av heltalen. Anropa funktionerna från en main-funktion och skriv ut produkten.
<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "def inmatning():\n" +
    "    alla_tal = []\n" +
    "    for i in range(3):\n" +
    "        tal = int(input(&quot;Tal &quot;+ str(i+1) +&quot;: &quot;))\n" +
    "        alla_tal.append(tal)\n" +
    "    return alla_tal[0], alla_tal[1], alla_tal[2]     \n" +
    "def multiplicera(tal1, tal2, tal3):\n" +
    "    produkt = tal1 * tal2 * tal3\n" +
    "    return produkt\n" +
    "def main():\n" +
    "    tal_a, tal_b, tal_c = inmatning()\n" +
    "    produkten = multiplicera(tal_a, tal_b, tal_c)\n" +
    "    print(&quot;Produkt:&quot;, produkten)\n" +
    "main()";
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
