---
layout: treninky
title: Tréninky
permalink: /treninky/
---

<script src="//code.jquery.com/jquery-1.11.3.min.js"></script>

<a href="#" class="image fit"><img src="/images/training.jpg" alt="" /></a>

<a id="pravidelne"></a>

   

## Pravidelné tréninky

Pravidelné tréninky momentálně neprobíhají.

<!-- <a href="#prihlaska" class="button special">Přihlas se zde</a> -->

### Pro koho jsou tréninky určené

Tréninky jsou určené pro dospělé – začátečníky, kteří nemají s parkourem žádné nebo téměř žádné zkušenosti. Jsou vhodné i pro ty, kteří dlouho (třeba i od základní školy) nesportovali, i pro ty, kdo se zabývají jiným sportem a chtějí doplnit trénink nebo se naučit něco nového.

### Struktura tréninku

<div class="svg-container">
<svg id="svg2" xmlns:rdf="http://www.w3.org/1999/02/22-rdf-syntax-ns#" xmlns="http://www.w3.org/2000/svg" version="1.1" xmlns:cc="http://creativecommons.org/ns#" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xlink="//www.w3.org/1999/xlink" viewBox="0 0 600 60" preserveAspectRatio="xMinYMin meet" class="svg-content">
<metadata id="metadata6"><rdf:RDF><cc:Work rdf:about=""><dc:format>image/svg+xml</dc:format><dc:type rdf:resource="http://purl.org/dc/dcmitype/StillImage"/><dc:title/></cc:Work></rdf:RDF></metadata>

<rect height="50" width="100" fill="#5aff00"/>
<rect height="50" width="50" x="100" fill="#369900"/>
<a xlink:href="/rozcvicka"><text x="2" y="35" font-weight="bold" font-size="22px" font-family="Sans" fill="#ffffff">ROZCVIČKA</text></a>                    

<rect height="50" width="150" x="150" fill="#00c8a5"/>
<a xlink:href="/techniky"><text x="162" y="35" font-weight="bold" font-size="22px" font-family="Sans" fill="#ffffff">TECHNIKY</text></a>                    

<rect height="50" width="100" x="300" fill="#1dcaff"/>
<a xlink:href="/flow"><text x="315" y="35" font-weight="bold" font-size="22px" font-family="Sans" fill="#ffffff">FLOW</text></a>                    

<rect height="50" width="100" x="400" fill="#ff1212"/>
<rect height="50" width="50" x="500" fill="#f9ad10"/>
<a xlink:href="/kondice"><text x="422" y="35" font-weight="bold" font-size="22px" font-family="Sans" fill="#ffffff">KONDICE</text></a>                    

<rect height="50" width="50" x="550" fill="#f9f610"/>
<a xlink:href="/cooldown"><text font-size="14px" font-family="Sans">
<tspan x="555" y="20">COOL</tspan><tspan x="552" y="40">DOWN</tspan></text></a>

</svg>
</div>

### Jdu na první trénink

Co s sebou: pohodlnou obuv, která dobře drží na noze (např. běžeckou), oblečení, které neomezuje v pohybu; u obuvi i oblečení je třeba počítat s mírným znečištěním, případně poškozením.

<a id="prihlaska"></a>

### Přihláška na trénink

<form id="f">
<div class="row uniform 50%">
  <div class="3u 12u$(medium)">
    <input type="text" id="name" placeholder="Jméno a příjmení" />
  </div>
  <div class="3u 12u$(medium)">
    <input type="text" id="contact" placeholder="E-mail nebo telefon" />
  </div>
  <div class="3u 12u$(medium)">
    <div class="select-wrapper">
      <select id="date">
      </select>
    </div>
  </div>
  <div class="3u$ 12u$(medium)">
    <input type="submit" id="btn" value="Odeslat">
  </div>
</div>
</form>

[Chceš nám ještě něco napsat nebo se na něco zeptat? Kontaktuj nás!](/o-nas/#kontakt)

<a id="spoty"></a>

### Podmínky účasti

Pro účast Ti musí být 18 let nebo více. Před tréninkem jsi také povinnen(-na) seznámit se s možnými riziky trénování parkouru, která jsou uvedena v [Podrobných podmínkách účasti](/o-nas/#podminky).

## Chceš trénovat sám/sama?

[Zde je seznam vybraných pražských spotů.](/spoty/)

<script type="text/javascript">
        $(document).ready(function() {
            $('form[id=f]').submit(function(e) {
                e.preventDefault();
                var text = $('#date').val() + ' – ' + $('#name').val() + ' – ' + $('#contact').val();
                var postData = '{"text": "' + text + '", "channel": "#prihlasky"}';
                var btn = $('#btn');
                $.ajax({
                    type: 'POST',
                    cache: false,
                    url: 'https://hooks.slack.com/services/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',
                    data: postData,
                    success: function() {window.location.href = "#";}
                });
                btn.val("Odesláno ✓");
            });
        });
</script>
