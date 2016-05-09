---
layout: treninky
title: Spoty
permalink: /spoty/
---

## Hlavní parkourové spoty (tréninková místa) v Praze

<div id="map1" style="width: 100%; height: 300px;"></div>

   

<ul>
{% for post in site.spot %}<li><a href="{{ post.url }}">{{ post.title }}</a></li>{% endfor %}
</ul>


<script type="text/javascript">
  var locations1 = [
    ['cerny-most', 50.1076086, 14.5776950, 'Černý Most'],
    ['dejvicka', 50.1015478, 14.3936108, 'Dejvická'],
    ['ftvs', 50.0920844, 14.3346131, 'FTVS'],
    ['ke-katerinkam', 50.0256867, 14.5155078, 'Ke Kateřinkám'],
    ['koh-i-noor', 50.0671678, 14.4643783, 'Koh-i-noor'],
    ['kublov', 50.0549511, 14.4189242, 'Kublov'],
    ['letna', 50.0948653, 14.4157875, 'Letná'],
    ['muzeum-policie', 50.0682611, 14.4297511, 'Muzeum policie (I. P. Pavlova)'],
    ['palmovka', 50.1075242, 14.4662344, 'Palmovka'],
    ['park-pratelstvi', 50.1231819, 14.4943708, 'Park Přátelství'],
    ['strasnicka', 50.0708108, 14.4893928, 'Strašnická'],
    ['velka-ohrada', 50.0375922, 14.3394222, 'Velká Ohrada (Lužiny)'],
    ['vitkov', 50.0882400, 14.4482044, 'Vítkov'],
    ['vltavska', 50.0992783, 14.4388758, 'Vltavská'],
    ['vysehrad', 50.0630400, 14.4290778, 'Vyšehrad'],
    ['zerotinova', 50.0869803, 14.4598481, 'Žerotínova (Žižkov)'],
  ];
  var map = new google.maps.Map(document.getElementById('map1'), {
    zoom: 11,
    center: new google.maps.LatLng(50.0806, 14.4447),
    mapTypeId: google.maps.MapTypeId.ROADMAP
  });
  var infowindow = new google.maps.InfoWindow();
  var marker, i;
  for (i = 0; i < locations1.length; i++) {  
    marker = new google.maps.Marker({
      position: new google.maps.LatLng(locations1[i][1], locations1[i][2]),
      map: map,
      title: locations1[i][3],
    });
    google.maps.event.addListener(marker, 'click', (function(marker, i) {
      return function() {
        window.open("/" + locations1[i][0]);
        //infowindow.setContent(locations[i][0]);
        //infowindow.open(map, marker);
      }
    })(marker, i));
  }
</script>


## Podrobnější mapa spotů

Děkujeme [kamjitskakat.cz](http://www.dpsc.8u.cz) za poskytnuté údaje. Pokud potřebuješ hlavně posilovat, podívej se na [mapu míst pro street workout](https://www.google.com/maps/d/u/0/viewer?mid=zdu1FeaZX_sg.kfBq5Gfuc-5c "Mapa workoutišť").   

<div id="map2" style="width: 100%; height: 300px;"></div>

   
<!--
[Barrandov – Billa (raily)](http://www.dpsc.8u.cz/spoty/barrandov-billa-raily) \| [Barrandov – dětské hřiště](http://www.dpsc.8u.cz/spoty/barrandov-detske-hriste) \| [Barrandov – most](http://www.dpsc.8u.cz/spoty/barrandov-most) \| [Barrandov – parkoviště](http://www.dpsc.8u.cz/spoty/barrandov-parkoviste) \| [Barrandov – raily](http://www.dpsc.8u.cz/spoty/barrandov-raily) \| [Barrandov – V Remízku](http://www.dpsc.8u.cz/spoty/barrandov-v-remizku) \| [Budějovická](http://www.dpsc.8u.cz/spoty/budejovicka) \| [Černý Most](http://www.dpsc.8u.cz/spoty/cerny-most) \| [Černý Most – Workout / Lache hřiště](http://www.dpsc.8u.cz/spoty/cerny-most-workout-lache-hriste) \| [Černý Most 2](http://www.dpsc.8u.cz/spoty/cerny-most-2) \| [Čimice – lache](http://www.dpsc.8u.cz/spoty/cimice-lache) \| [Čimice – raily](http://www.dpsc.8u.cz/spoty/cimice-raily) \| [Čimice – zídky](http://www.dpsc.8u.cz/spoty/cimice-zidky) \| [Dejvice – Cube](http://www.dpsc.8u.cz/spoty/dejvice-cube) \| [Dejvice – dětské hřiště](http://www.dpsc.8u.cz/spoty/dejvice-detske-hriste) \| [Dejvice – Nádraží podbaba](http://www.dpsc.8u.cz/spoty/dejvice-nadrazi-podbaba) \| [Dejvice – raily](http://www.dpsc.8u.cz/spoty/dejvice-raily) \| [Dejvice – V Sedlci](http://www.dpsc.8u.cz/spoty/dejvice-v-sedlci) \| [FTVS – Lappset park](http://www.dpsc.8u.cz/spoty/ftvs-lappset-park) \| [Grébovka](http://www.dpsc.8u.cz/spoty/grebovka) \| [Háje – metro](http://www.dpsc.8u.cz/spoty/haje-metro) \| [Háje – most](http://www.dpsc.8u.cz/spoty/haje-most) \| [Háje – Norma](http://www.dpsc.8u.cz/spoty/haje-norma) \| [Háje – Základní škola](http://www.dpsc.8u.cz/spoty/haje-zakladni-skola) \| [Holešovice – Maniny](http://www.dpsc.8u.cz/spoty/holesovice-maniny) \| [Holešovice – Přívozní](http://www.dpsc.8u.cz/spoty/holesovice-privozni) \| [Holešovice – V přístavu](http://www.dpsc.8u.cz/spoty/holesovice-v-pristavu) \| [Hořejší nábřeží](http://www.dpsc.8u.cz/spoty/horejsi-nabrezi) \| [Hostivař – Budapešťská](http://www.dpsc.8u.cz/spoty/hostivar-budapestska) \| [Hostivař – náměstí Přátelství](http://www.dpsc.8u.cz/spoty/hostivar-namesti-pratelstvi) \| [Hostivař – Toulcův dvůr – bílé zdi](http://www.dpsc.8u.cz/spoty/hostivar-toulcuv-dvur-bile-zdi) \| [Hostivař – Toulcův dvůr – raily](http://www.dpsc.8u.cz/spoty/hostivar-toulcuv-dvur-raily) \| [Hůrka – bigfoot](http://www.dpsc.8u.cz/spoty/hurka-bigfoot) \| [Hůrka – dětské hřiště](http://www.dpsc.8u.cz/spoty/hurka-detske-hriste) \| [Hůrka – Kaufland](http://www.dpsc.8u.cz/spoty/hurka-kaufland) \| [Hůrka – most](http://www.dpsc.8u.cz/spoty/hurka-most) \| [Hůrka – raily](http://www.dpsc.8u.cz/spoty/hurka-raily) \| [Hůrka – raily 2](http://www.dpsc.8u.cz/spoty/hurka-raily-2) \| [Hůrka – sídliště](http://www.dpsc.8u.cz/spoty/hurka-sidliste) \| [Hůrka – Sluneční náměstí](http://www.dpsc.8u.cz/spoty/hurka-skola) \| [Hůrka – Suchý vršek](http://www.dpsc.8u.cz/spoty/hurka-slunecni-namesti) \| [Hůrka – Škola](http://www.dpsc.8u.cz/spoty/hurka-suchy-vrsek) \| [Hůrka – u Šatlavy](http://www.dpsc.8u.cz/spoty/hurka-u-satlavy) \| [Hůrka – XXXLutz](http://www.dpsc.8u.cz/spoty/hurka-xxxlutz) \| [Chodov – catleapová zeď a okolí](http://www.dpsc.8u.cz/spoty/chodov-catleapova-zed-a-okoli) \| [Chodov – Centrum Chodov](http://www.dpsc.8u.cz/spoty/chodov-centrum-chodov) \| [Chodov – Dědinova](http://www.dpsc.8u.cz/spoty/chodov-dedinova) \| [Chodov – Filipova](http://www.dpsc.8u.cz/spoty/chodov-filipova) \| [Chodov – Hlavní](http://www.dpsc.8u.cz/spoty/chodov-hlavni) \| [Chodov – Chodovská tvrz](http://www.dpsc.8u.cz/spoty/chodov-chodovska-tvrz) \| [Chodov – Jírovcovo náměstí](http://www.dpsc.8u.cz/spoty/chodov-jirovcovo-namesti) \| [Chodov – Ke Kateřinkám](http://www.dpsc.8u.cz/spoty/chodov-ke-katerinkam) \| [Chodov – Ke Kateřinkám 2](http://www.dpsc.8u.cz/spoty/chodov-ke-katerinkam-2) \| [Chodov – metro](http://www.dpsc.8u.cz/spoty/chodov-metro) \| [Chodov – Penny Market](http://www.dpsc.8u.cz/spoty/chodov-penny-market) \| [Chodov – Petýrkova](http://www.dpsc.8u.cz/spoty/chodov-petyrkova) \| [Chodov – Pošepného náměstí](http://www.dpsc.8u.cz/spoty/chodov-posepneho-namesti) \| [Chodov – Šperlova](http://www.dpsc.8u.cz/spoty/chodov-sperlova) \| [Chodov – Tererova](http://www.dpsc.8u.cz/spoty/chodov-tererova) \| [Chodov – u mostu](http://www.dpsc.8u.cz/spoty/chodov-u-mostu) \| [Chodov – u Tesca](http://www.dpsc.8u.cz/spoty/chodov-u-tesca) \| [IP Pavlova](http://www.dpsc.8u.cz/spoty/ip-pavlova) \| [IP Pavlova – strides](http://www.dpsc.8u.cz/spoty/ip-pavlova-strides) \| [Kobylisy – bílá zeď a okolí](http://www.dpsc.8u.cz/spoty/kobylisy-bila-zed-a-okoli) \| [Kobylisy – dětské hřiště](http://www.dpsc.8u.cz/spoty/kobylisy-detske-hriste) \| [Kobylisy – dřevěný most](http://www.dpsc.8u.cz/spoty/kobylisy-dreveny-most) \| [Kobylisy – Krakov](http://www.dpsc.8u.cz/spoty/kobylisy-krakov) \| [Kobylisy – Mazurská – Škola (zbořeno)](http://www.dpsc.8u.cz/spoty/kobylisy-mazurska-skola-zboreno) \| [Kobylisy – metro (kongy)](http://www.dpsc.8u.cz/spoty/kobylisy-metro-kongy) \| [Kobylisy – metro (raily)](http://www.dpsc.8u.cz/spoty/kobylisy-metro-raily) \| [Kobylisy – most](http://www.dpsc.8u.cz/spoty/kobylisy-most) \| [Kobylisy – most 2](http://www.dpsc.8u.cz/spoty/kobylisy-most-2) \| [Kobylisy – Odra](http://www.dpsc.8u.cz/spoty/kobylisy-odra) \| [Kobylisy – Poliklinika Mazurská](http://www.dpsc.8u.cz/spoty/kobylisy-poliklinika-mazurska) \| [Kobylisy – raily u Albertu](http://www.dpsc.8u.cz/spoty/kobylisy-raily-u-albertu) \| [Kobylisy – Řešovská](http://www.dpsc.8u.cz/spoty/kobylisy-resovska) \| [Kobylisy – u polikliniky](http://www.dpsc.8u.cz/spoty/kobylisy-u-polikliniky) \| [Koh-I-Noor](http://www.dpsc.8u.cz/spoty/koh-i-noor) \| [Kublov – Lappset park](http://www.dpsc.8u.cz/spoty/kublov-lappset-park) \| [Ládví – Lappset hřiště](http://www.dpsc.8u.cz/spoty/ladvi-lappset-hriste) \| [Ládví – metro a okolí](http://www.dpsc.8u.cz/spoty/ladvi-metro-a-okoli) \| [Ládví – raily u školy](http://www.dpsc.8u.cz/spoty/ladvi-raily-u-skoly) \| [Ládví – Třebenická](http://www.dpsc.8u.cz/spoty/ladvi-trebenicka) \| [Ládví – u parkoviště](http://www.dpsc.8u.cz/spoty/ladvi-u-parkoviste) \| [Letňany – stridy](http://www.dpsc.8u.cz/spoty/letnany-stridy) \| [Luka – JAM spot](http://www.dpsc.8u.cz/spoty/luka-jam-spot) \| [Luka – metro](http://www.dpsc.8u.cz/spoty/luka-metro) \| [Luka – most](http://www.dpsc.8u.cz/spoty/luka-most) \| [Lužiny – dětské hřiště](http://www.dpsc.8u.cz/spoty/luziny-detske-hriste) \| [Lužiny – garáž](http://www.dpsc.8u.cz/spoty/luziny-garaz) \| [Lužiny – kamenné lavičky](http://www.dpsc.8u.cz/spoty/luziny-kamenne-lavicky) \| [Lužiny – Lappset hřiště](http://www.dpsc.8u.cz/spoty/luziny-lappset-hriste) \| [Lužiny – schody](http://www.dpsc.8u.cz/spoty/luziny-schody) \| [Lužiny – u hřiště](http://www.dpsc.8u.cz/spoty/luziny-u-hriste) \| [Lužiny – u metra](http://www.dpsc.8u.cz/spoty/luziny-u-metra) \| [Lužiny – zídky](http://www.dpsc.8u.cz/spoty/luziny-zidky) \| [Michle – Ohradní](http://www.dpsc.8u.cz/spoty/michle-ohradni) \| [Modřany – Belárie](http://www.dpsc.8u.cz/spoty/modrany-belarie) \| [Modřany – bílé zdi](http://www.dpsc.8u.cz/spoty/modrany-bile-zdi) \| [Modřany – Černý kůň](http://www.dpsc.8u.cz/spoty/modrany-cerny-kun) \| [Modřany – Družná](http://www.dpsc.8u.cz/spoty/modrany-druzna) \| [Modřany – Hasova](http://www.dpsc.8u.cz/spoty/modrany-hasova) \| [Modřany – Kaufland](http://www.dpsc.8u.cz/spoty/modrany-kaufland) \| [Modřany – Labe](http://www.dpsc.8u.cz/spoty/modrany-labe) \| [Modřany – Modřanská rokle](http://www.dpsc.8u.cz/spoty/modrany-modranska-rokle) \| [Modřany – Modřanská škola](http://www.dpsc.8u.cz/spoty/modrany-modranska-skola) \| [Modřany – Nádraží Braník – most](http://www.dpsc.8u.cz/spoty/modrany-nadrazi-branik-most) \| [Modřany – Nádraží Braník – roof gap](http://www.dpsc.8u.cz/spoty/modrany-nadrazi-branik-roof-gap) \| [Modřany – náměstíčko](http://www.dpsc.8u.cz/spoty/modrany-namesticko) \| [Modřany – Poliklinika Modřany – náměstí](http://www.dpsc.8u.cz/spoty/modrany-poliklinika-modrany-namesti) \| [Modřany – Poliklinika Modřany – raily](http://www.dpsc.8u.cz/spoty/modrany-poliklinika-modrany-raily) \| [Modřany – Poliklinika Modřany – schody](http://www.dpsc.8u.cz/spoty/modrany-poliklinika-modrany-schody) \| [Modřany – Přístaviště](http://www.dpsc.8u.cz/spoty/modrany-pristaviste) \| [Modřany – rail kong](http://www.dpsc.8u.cz/spoty/modrany-rail-kong) \| [Modřany – Sídliště Lhotka](http://www.dpsc.8u.cz/spoty/modrany-sidliste-lhotka) \| [Modřany – Tylova čtvrť](http://www.dpsc.8u.cz/spoty/modrany-tylova-ctvrt) \| [Modřany – u Billy](http://www.dpsc.8u.cz/spoty/modrany-u-billy) \| [Modřany – Ve Lhotce](http://www.dpsc.8u.cz/spoty/modrany-ve-lhotce) \| [Modřany – VOSA](http://www.dpsc.8u.cz/spoty/modrany-vosa) \| [Nádraží Holešovice](http://www.dpsc.8u.cz/spoty/nadrazi-holesovice) \| [Nádraží Vršovice](http://www.dpsc.8u.cz/spoty/nadrazi-vrsovice) \| [Nádraží Vršovice 2](http://www.dpsc.8u.cz/spoty/nadrazi-vrsovice-2) \| [Nové Butovice – Fingerova](http://www.dpsc.8u.cz/spoty/nove-butovice-fingerova) \| [Nové Butovice – metro](http://www.dpsc.8u.cz/spoty/nove-butovice-metro) \| [Nové Butovice – rail kong](http://www.dpsc.8u.cz/spoty/nove-butovice-rail-kong) \| [Opatov](http://www.dpsc.8u.cz/spoty/opatov) \| [Pankrác](http://www.dpsc.8u.cz/spoty/pankrac) \| [Petrovice – Livornská](http://www.dpsc.8u.cz/spoty/petrovice-livornska) \| [Petrovice – Livornská – bus](http://www.dpsc.8u.cz/spoty/petrovice-livornska-bus) \| [Petrovice – Nad Přehradou](http://www.dpsc.8u.cz/spoty/petrovice-nad-prehradou) \| [Petrovice – Úřad](http://www.dpsc.8u.cz/spoty/petrovice-urad) \| [Petrovice – Veronské náměstí 1](http://www.dpsc.8u.cz/spoty/petrovice-veronske-namesti-1) \| [Petrovice – Veronské náměstí 2](http://www.dpsc.8u.cz/spoty/petrovice-veronske-namesti-2) \| [Podolí – Nové Podolí](http://www.dpsc.8u.cz/spoty/podoli-nove-podoli) \| [Podolí – Pod Pekařkou](http://www.dpsc.8u.cz/spoty/podoli-pod-pekarkou) \| [Podolí – u garáží](http://www.dpsc.8u.cz/spoty/podoli-u-garazi) \| [Pražského Povstání – most](http://www.dpsc.8u.cz/spoty/prazskeho-povstani-most) \| [Pražského Povstání – schody](http://www.dpsc.8u.cz/spoty/prazskeho-povstani-schody) \| [Pražského Povstání – vjzed do garáže](http://www.dpsc.8u.cz/spoty/prazskeho-povstani-vjzed-do-garaze) \| [Přehrada](http://www.dpsc.8u.cz/spoty/prehrada) \| [Prosek](http://www.dpsc.8u.cz/spoty/prosek) \| [Prosek – červený plechy](http://www.dpsc.8u.cz/spoty/prosek-cerveny-plechy) \| [Radotín](http://www.dpsc.8u.cz/spoty/radotin) \| [Řepy – Bazovského](http://www.dpsc.8u.cz/spoty/repy-bazovskeho) \| [Řepy – Blatiny](http://www.dpsc.8u.cz/spoty/repy-blatiny) \| [Řepy – Drahoňovského](http://www.dpsc.8u.cz/spoty/repy-drahonovskeho) \| [Řepy – kanály](http://www.dpsc.8u.cz/spoty/repy-kanaly) \| [Řepy – Slánská](http://www.dpsc.8u.cz/spoty/repy-slanska) \| [Řepy – u Albertu](http://www.dpsc.8u.cz/spoty/repy-u-albertu) \| [Řepy – Vondroušova](http://www.dpsc.8u.cz/spoty/repy-vondrousova) \| [Skalka](http://www.dpsc.8u.cz/spoty/skalka) \| [Slivenec](http://www.dpsc.8u.cz/spoty/slivenec) \| [Stodůlky](http://www.dpsc.8u.cz/spoty/stodulky) \| [Stodůlky – Flöglova](http://www.dpsc.8u.cz/spoty/stodulky-floglova) \| [Stodůlky – Hábova](http://www.dpsc.8u.cz/spoty/stodulky-habova) \| [Stodůlky – kameny](http://www.dpsc.8u.cz/spoty/stodulky-kameny) \| [Stodůlky – runcatleap](http://www.dpsc.8u.cz/spoty/stodulky-runcatleap) \| [Strahov](http://www.dpsc.8u.cz/spoty/strahov) \| [Strahov – menza](http://www.dpsc.8u.cz/spoty/strahov-menza) \| [Strašnice – Gutova](http://www.dpsc.8u.cz/spoty/strasnice-gutova) \| [Strašnice – U hráze](http://www.dpsc.8u.cz/spoty/strasnice-u-hraze) \| [Strašnická](http://www.dpsc.8u.cz/spoty/strasnicka) \| [Střešovice – Billa](http://www.dpsc.8u.cz/spoty/stresovice-billa) \| [Střešovice – Břevnovská](http://www.dpsc.8u.cz/spoty/stresovice-brevnovska) \| [Střešovice – catleap](http://www.dpsc.8u.cz/spoty/stresovice-catleap) \| [Střešovice – černé raily](http://www.dpsc.8u.cz/spoty/stresovice-cerne-raily) \| [Střešovice – garáž](http://www.dpsc.8u.cz/spoty/stresovice-garaz) \| [Střešovice – Hládkov](http://www.dpsc.8u.cz/spoty/stresovice-hladkov) \| [Střešovice – Na Petynce](http://www.dpsc.8u.cz/spoty/stresovice-na-petynce) \| [Střešovice – schody](http://www.dpsc.8u.cz/spoty/stresovice-schody) \| [Střešovice – Za Hládkovem – garáž](http://www.dpsc.8u.cz/spoty/stresovice-za-hladkovem-garaz) \| [Střešovice – Za Hládkovem – raily](http://www.dpsc.8u.cz/spoty/stresovice-za-hladkovem-raily) \| [Troja – Kovárna](http://www.dpsc.8u.cz/spoty/troja-kovarna) \| [Troja – Kovárna – Dětské hřiště](http://www.dpsc.8u.cz/spoty/troja-kovarna-detske-hriste) \| [Troja – Trojská](http://www.dpsc.8u.cz/spoty/troja-trojska) \| [Velká Ohrada – Bašteckého](http://www.dpsc.8u.cz/spoty/velka-ohrada-basteckeho) \| [Velká Ohrada – Bašteckého 2](http://www.dpsc.8u.cz/spoty/velka-ohrada-basteckeho-2) \| [Velká Ohrada – náměstí a okolí](http://www.dpsc.8u.cz/spoty/velka-ohrada-namesti-a-okoli) \| [Velká Ohrada – u polikliniky](http://www.dpsc.8u.cz/spoty/velka-ohrada-u-polikliniky) \| [Velká Ohrada – u školy](http://www.dpsc.8u.cz/spoty/velka-ohrada-u-skoly) \| [Vinohrady – Workout / Lache hřiště](http://www.dpsc.8u.cz/spoty/vinohrady-workout-lache-hriste) \| [Vltavská](http://www.dpsc.8u.cz/spoty/vltavska) \| [Vltavská – flow](http://www.dpsc.8u.cz/spoty/vltavska-flow) \| [Vltavská – most](http://www.dpsc.8u.cz/spoty/vltavska-most) \| [Vltavská – raily](http://www.dpsc.8u.cz/spoty/vltavska-raily) \| [Vltavská – strides](http://www.dpsc.8u.cz/spoty/vltavska-strides) \| [Vysočany – park Podviní](http://www.dpsc.8u.cz/spoty/vysehrad-garaze) \| [Vysočany – stridy](http://www.dpsc.8u.cz/spoty/vysehrad-kongresak) \| [Vysočany – u Polikliniky](http://www.dpsc.8u.cz/spoty/vysehrad-u-gymnazia) \| [Vyšehrad – garáže](http://www.dpsc.8u.cz/spoty/vysocany-park-podvini) \| [Vyšehrad – Kongresák](http://www.dpsc.8u.cz/spoty/vysocany-stridy) \| [Vyšehrad – U Gymnázia](http://www.dpsc.8u.cz/spoty/vysocany-u-polikliniky) \| [Zahradní Město – centrum](http://www.dpsc.8u.cz/spoty/zahradni-mesto-centrum) \| [Zahradní Město – Ke skalkám](http://www.dpsc.8u.cz/spoty/zahradni-mesto-ke-skalkam) \| [Zahradní Město – Na Slatince](http://www.dpsc.8u.cz/spoty/zahradni-mesto-na-slatince) \| [Zahradní Město – Na Slatince 2](http://www.dpsc.8u.cz/spoty/zahradni-mesto-na-slatince-2) \| [Zahradní Město – Poliklinika Zahradní Město](http://www.dpsc.8u.cz/spoty/zahradni-mesto-poliklinika-zahradni-mesto) \| [Zahradní Město – střecha](http://www.dpsc.8u.cz/spoty/zahradni-mesto-strecha) \| [Zahradní Město – U Zahradního města](http://www.dpsc.8u.cz/spoty/zahradni-mesto-u-zahradniho-mesta) \| [Zahradní Město – vjezd](http://www.dpsc.8u.cz/spoty/zahradni-mesto-vjezd) \| [Zahradní Město – výlezy](http://www.dpsc.8u.cz/spoty/zahradni-mesto-vylezy) \| [Žižkov – Kostnické náměstí](http://www.dpsc.8u.cz/spoty/zizkov-kostnicke-namesti) \| [Žižkov – Rokycanova](http://www.dpsc.8u.cz/spoty/zizkov-rokycanova) \| [Žižkov – V Zahrádkách](http://www.dpsc.8u.cz/spoty/zizkov-v-zahradkach) \| [Žofín – dětské hřiště](http://www.dpsc.8u.cz/spoty/zofin-detske-hriste)
-->


<script type="text/javascript">
  var locations2 = [
    ['barrandov-detske-hriste', 50.0282406, 14.3679357, 'Barrandov – dětské hřiště'],
    ['barrandov-most', 50.0302337, 14.3664575, 'Barrandov – most'],
    ['barrandov-parkoviste', 50.0282489, 14.3669757, 'Barrandov – parkoviště'],
    ['barrandov-raily', 50.0282816, 14.3680364, 'Barrandov – raily'],
    ['barrandov-v-remizku', 50.0261068, 14.3685588, 'Barrandov – V Remízku'],
    ['budejovicka', 50.0450054, 14.4471994, 'Budějovická'],
    ['cerny-most', 50.1075480, 14.5773978, 'Černý Most'],
    ['cerny-most-workout-lache-hriste', 50.1050057, 14.5624084, 'Černý Most – Workout / Lache hřiště'],
    ['cerny-most-2', 50.1029883, 14.5737533, 'Černý Most 2'],
    ['cimice-lache', 50.1391704, 14.4295759, 'Čimice – lache'],
    ['cimice-raily', 50.1412986, 14.4284328, 'Čimice – raily'],
    ['cimice-zidky', 50.1406179, 14.4278636, 'Čimice – zídky'],
    ['dejvice-cube', 50.0947557, 14.3387984, 'Dejvice – Cube'],
    ['dejvice-detske-hriste', 50.1309580, 14.3794035, 'Dejvice – dětské hřiště'],
    ['dejvice-nadrazi-podbaba', 50.1131601, 14.3923647, 'Dejvice – Nádraží podbaba'],
    ['dejvice-raily', 50.0980772, 14.3593342, 'Dejvice – raily'],
    ['dejvice-v-sedlci', 50.1282820, 14.3951043, 'Dejvice – V Sedlci'],
    ['ftvs-lappset-park', 50.0922511, 14.3349044, 'FTVS – Lappset park'],
    ['grebovka', 50.0691283, 14.4473763, 'Grébovka'],
    ['haje-metro', 50.0314304, 14.5307783, 'Háje – metro'],
    ['haje-most', 50.0293148, 14.5286174, 'Háje – most'],
    ['haje-norma', 50.0284942, 14.5291909, 'Háje – Norma'],
    ['haje-zakladni-skola', 50.0335165, 14.5317599, 'Háje – Základní škola'],
    ['holesovice-maniny', 50.1033671, 14.4571549, 'Holešovice – Maniny'],
    ['holesovice-privozni', 50.1095119, 14.4518656, 'Holešovice – Přívozní'],
    ['holesovice-v-pristavu', 50.1090268, 14.4530243, 'Holešovice – V přístavu'],
    ['horejsi-nabrezi', 50.0701172, 14.4124862, 'Hořejší nábřeží'],
    ['hostivar-budapestska', 50.0441563, 14.5154554, 'Hostivař – Budapešťská'],
    ['hostivar-namesti-pratelstvi', 50.0448866, 14.5181054, 'Hostivař – náměstí Přátelství'],
    ['hostivar-toulcuv-dvur-bile-zdi', 50.0472756, 14.5197784, 'Hostivař – Toulcův dvůr – bílé zdi'],
    ['hostivar-toulcuv-dvur-raily', 50.0476161, 14.5189125, 'Hostivař – Toulcův dvůr – raily'],
    ['hurka-bigfoot', 50.0484625, 14.3426088, 'Hůrka – bigfoot'],
    ['hurka-detske-hriste', 50.0518422, 14.3414416, 'Hůrka – dětské hřiště'],
    ['hurka-kaufland', 50.0517316, 14.3362399, 'Hůrka – Kaufland'],
    ['hurka-most', 50.0507016, 14.3409474, 'Hůrka – most'],
    ['hurka-raily', 50.0523076, 14.3434188, 'Hůrka – raily'],
    ['hurka-raily-2', 50.0539977, 14.3458056, 'Hůrka – raily 2'],
    ['hurka-sidliste', 50.0525219, 14.3471316, 'Hůrka – sídliště'],
    ['hurka-skola', 50.0511909, 14.3407801, 'Hůrka – Sluneční náměstí'],
    ['hurka-slunecni-namesti', 50.0499727, 14.3448475, 'Hůrka – Suchý vršek'],
    ['hurka-suchy-vrsek', 50.0477908, 14.3447026, 'Hůrka – Škola'],
    ['hurka-u-satlavy', 50.0534052, 14.3408060, 'Hůrka – u Šatlavy'],
    ['hurka-xxxlutz', 50.0540440, 14.3340497, 'Hůrka – XXXLutz'],
    ['chodov-catleapova-zed-a-okoli', 50.0304008, 14.5149796, 'Chodov – catleapová zeď a okolí'],
    ['chodov-centrum-chodov', 50.0304524, 14.4897631, 'Chodov – Centrum Chodov'],
    ['chodov-dedinova', 50.0336744, 14.4836410, 'Chodov – Dědinova'],
    ['chodov-filipova', 50.0326049, 14.4838130, 'Chodov – Filipova'],
    ['chodov-hlavni', 50.0466491, 14.4873602, 'Chodov – Hlavní'],
    ['chodov-chodovska-tvrz', 50.0367699, 14.4973066, 'Chodov – Chodovská tvrz'],
    ['chodov-jirovcovo-namesti', 50.0251894, 14.4930368, 'Chodov – Jírovcovo náměstí'],
    ['chodov-ke-katerinkam', 50.0258166, 14.5156261, 'Chodov – Ke Kateřinkám'],
    ['chodov-ke-katerinkam-2', 50.0252033, 14.5152204, 'Chodov – Ke Kateřinkám 2'],
    ['chodov-metro', 50.0307077, 14.4910798, 'Chodov – metro'],
    ['chodov-penny-market', 50.0378080, 14.5151214, 'Chodov – Penny Market'],
    ['chodov-petyrkova', 50.0309460, 14.4869828, 'Chodov – Petýrkova'],
    ['chodov-posepneho-namesti', 50.0326532, 14.4825488, 'Chodov – Pošepného náměstí'],
    ['chodov-sperlova', 50.0337393, 14.5116262, 'Chodov – Šperlova'],
    ['chodov-tererova', 50.0247610, 14.5218980, 'Chodov – Tererova'],
    ['chodov-u-mostu', 50.0258166, 14.5156261, 'Chodov – u mostu'],
    ['chodov-u-tesca', 50.0322092, 14.5140328, 'Chodov – u Tesca'],
    ['ip-pavlova', 50.0691046, 14.4294694, 'IP Pavlova'],
    ['ip-pavlova-strides', 50.0716158, 14.4284684, 'IP Pavlova – strides'],
    ['kobylisy-bila-zed-a-okoli', 50.1279617, 14.4250065, 'Kobylisy – bílá zeď a okolí'],
    ['kobylisy-detske-hriste', 50.1307005, 14.4286815, 'Kobylisy – dětské hřiště'],
    ['kobylisy-dreveny-most', 50.1293599, 14.4317894, 'Kobylisy – dřevěný most'],
    ['kobylisy-krakov', 50.1281060, 14.4183137, 'Kobylisy – Krakov'],
    ['kobylisy-mazurska-skola-zboreno', 50.1278630, 14.4098243, 'Kobylisy – Mazurská – Škola (zbořeno)'],
    ['kobylisy-metro-kongy', 50.1246120, 14.4556754, 'Kobylisy – metro (kongy)'],
    ['kobylisy-metro-raily', 50.1246120, 14.4556754, 'Kobylisy – metro (raily)'],
    ['kobylisy-most', 50.1286282, 14.4161825, 'Kobylisy – most'],
    ['kobylisy-most-2', 50.1279097, 14.4168366, 'Kobylisy – most 2'],
    ['kobylisy-odra', 50.1308384, 14.4233700, 'Kobylisy – Odra'],
    ['kobylisy-poliklinika-mazurska', 50.1262626, 14.4134780, 'Kobylisy – Poliklinika Mazurská'],
    ['kobylisy-raily-u-albertu', 50.1312659, 14.4104401, 'Kobylisy – raily u Albertu'],
    ['kobylisy-resovska', 50.1303818, 14.4090308, 'Kobylisy – Řešovská'],
    ['kobylisy-u-polikliniky', 50.1263458, 14.4151354, 'Kobylisy – u polikliniky'],
    ['koh-i-noor', 50.0677925, 14.4675410, 'Koh-I-Noor'],
    ['kublov-lappset-park', 50.0548822, 14.4189166, 'Kublov – Lappset park'],
    ['ladvi-lappset-hriste', 50.1303304, 14.4671901, 'Ládví – Lappset hřiště'],
    ['ladvi-metro-a-okoli', 50.1275268, 14.4687043, 'Ládví – metro a okolí'],
    ['ladvi-raily-u-skoly', 50.1312687, 14.4757251, 'Ládví – raily u školy'],
    ['ladvi-trebenicka', 50.1298235, 14.4813759, 'Ládví – Třebenická'],
    ['ladvi-u-parkoviste', 50.1296620, 14.4794468, 'Ládví – u parkoviště'],
    ['letnany-stridy', 50.1420586, 14.5079806, 'Letňany – stridy'],
    ['luka-jam-spot', 50.0422963, 14.3236890, 'Luka – JAM spot'],
    ['luka-metro', 50.0450032, 14.3228653, 'Luka – metro'],
    ['luka-most', 50.0423672, 14.3269874, 'Luka – most'],
    ['luziny-detske-hriste', 50.0449423, 14.3301882, 'Lužiny – dětské hřiště'],
    ['luziny-garaz', 50.0425075, 14.3329768, 'Lužiny – garáž'],
    ['luziny-kamenne-lavicky', 50.0467986, 14.3370691, 'Lužiny – kamenné lavičky'],
    ['luziny-lappset-hriste', 50.0446756, 14.3354224, 'Lužiny – Lappset hřiště'],
    ['luziny-schody', 50.0444969, 14.3293773, 'Lužiny – schody'],
    ['luziny-u-hriste', 50.0421334, 14.3297210, 'Lužiny – u hřiště'],
    ['luziny-u-metra', 50.0456258, 14.3356606, 'Lužiny – u metra'],
    ['luziny-zidky', 50.0427199, 14.3335500, 'Lužiny – zídky'],
    ['michle-ohradni', 50.0515246, 14.4521123, 'Michle – Ohradní'],
    ['modrany-belarie', 50.0136252, 14.4018697, 'Modřany – Belárie'],
    ['modrany-bile-zdi', 50.0260631, 14.4522437, 'Modřany – bílé zdi'],
    ['modrany-cerny-kun', 50.0226609, 14.4038515, 'Modřany – Černý kůň'],
    ['modrany-druzna', 50.0123046, 14.4167678, 'Modřany – Družná'],
    ['modrany-hasova', 50.0152266, 14.4287468, 'Modřany – Hasova'],
    ['modrany-kaufland', 50.0134403, 14.4194967, 'Modřany – Kaufland'],
    ['modrany-labe', 50.0137276, 14.4211751, 'Modřany – Labe'],
    ['modrany-modranska-rokle', 50.0065064, 14.4291118, 'Modřany – Modřanská rokle'],
    ['modrany-modranska-skola', 50.0081010, 14.4025934, 'Modřany – Modřanská škola'],
    ['modrany-nadrazi-branik-most', 50.0269331, 14.4038475, 'Modřany – Nádraží Braník – most'],
    ['modrany-nadrazi-branik-roof-gap', 50.0271297, 14.4053599, 'Modřany – Nádraží Braník – roof gap'],
    ['modrany-namesticko', 50.0258787, 14.4550627, 'Modřany – náměstíčko'],
    ['modrany-poliklinika-modrany-namesti', 50.0060017, 14.4176012, 'Modřany – Poliklinika Modřany – náměstí'],
    ['modrany-poliklinika-modrany-raily', 50.0051033, 14.4195867, 'Modřany – Poliklinika Modřany – raily'],
    ['modrany-poliklinika-modrany-schody', 50.0042284, 14.4182017, 'Modřany – Poliklinika Modřany – schody'],
    ['modrany-pristaviste', 50.0395437, 14.4093018, 'Modřany – Přístaviště'],
    ['modrany-rail-kong', 50.0254014, 14.4384652, 'Modřany – rail kong'],
    ['modrany-sidliste-lhotka', 50.0176767, 14.4350061, 'Modřany – Sídliště Lhotka'],
    ['modrany-tylova-ctvrt', 50.0079886, 14.4156478, 'Modřany – Tylova čtvrť'],
    ['modrany-u-billy', 50.0127681, 14.4208517, 'Modřany – u Billy'],
    ['modrany-ve-lhotce', 50.0187562, 14.4332102, 'Modřany – Ve Lhotce'],
    ['modrany-vosa', 50.0122004, 14.4251608, 'Modřany – VOSA'],
    ['nadrazi-holesovice', 50.1092967, 14.4401243, 'Nádraží Holešovice'],
    ['nadrazi-vrsovice', 50.0667572, 14.4443085, 'Nádraží Vršovice'],
    ['nadrazi-vrsovice-2', 50.0670871, 14.4484093, 'Nádraží Vršovice 2'],
    ['nove-butovice-fingerova', 50.0487160, 14.3464779, 'Nové Butovice – Fingerova'],
    ['nove-butovice-metro', 50.0504231, 14.3501685, 'Nové Butovice – metro'],
    ['nove-butovice-rail-kong', 50.0474908, 14.3493281, 'Nové Butovice – rail kong'],
    ['opatov', 50.0278804, 14.5070189, 'Opatov'],
    ['pankrac', 50.0476904, 14.4346398, 'Pankrác'],
    ['petrovice-livornska', 50.0412159, 14.5565190, 'Petrovice – Livornská'],
    ['petrovice-livornska-bus', 50.0415082, 14.5518309, 'Petrovice – Livornská – bus'],
    ['petrovice-nad-prehradou', 50.0420024, 14.5517111, 'Petrovice – Nad Přehradou'],
    ['petrovice-urad', 50.0360010, 14.5563401, 'Petrovice – Úřad'],
    ['petrovice-veronske-namesti-1', 50.0403674, 14.5598366, 'Petrovice – Veronské náměstí 1'],
    ['petrovice-veronske-namesti-2', 50.0401755, 14.5608194, 'Petrovice – Veronské náměstí 2'],
    ['podoli-nove-podoli', 50.0429402, 14.4274682, 'Podolí – Nové Podolí'],
    ['podoli-pod-pekarkou', 50.0440426, 14.4237292, 'Podolí – Pod Pekařkou'],
    ['podoli-u-garazi', 50.0438910, 14.4219965, 'Podolí – u garáží'],
    ['prazskeho-povstani-most', 50.0573853, 14.4354340, 'Pražského Povstání – most'],
    ['prazskeho-povstani-schody', 50.0574339, 14.4361651, 'Pražského Povstání – schody'],
    ['prazskeho-povstani-vjzed-do-garaze', 50.0568389, 14.4328961, 'Pražského Povstání – vjzed do garáže'],
    ['prehrada', 50.1077490, 14.4662345, 'Přehrada'],
    ['prosek', 50.1186299, 14.4965339, 'Prosek'],
    ['prosek-cerveny-plechy', 50.1186372, 14.5071681, 'Prosek – červený plechy'],
    ['radotin', 49.9848460, 14.3593050, 'Radotín'],
    ['repy-bazovskeho', 50.0660796, 14.3064755, 'Řepy – Bazovského'],
    ['repy-blatiny', 50.0655788, 14.3024377, 'Řepy – Blatiny'],
    ['repy-drahonovskeho', 50.0660384, 14.3031576, 'Řepy – Drahoňovského'],
    ['repy-kanaly', 50.0634622, 14.3011987, 'Řepy – kanály'],
    ['repy-slanska', 50.0683281, 14.3096745, 'Řepy – Slánská'],
    ['repy-u-albertu', 50.0650662, 14.3075241, 'Řepy – u Albertu'],
    ['repy-vondrousova', 50.0641552, 14.3020304, 'Řepy – Vondroušova'],
    ['skalka', 50.0682271, 14.5079329, 'Skalka'],
    ['slivenec', 50.0217686, 14.3645062, 'Slivenec'],
    ['stodulky', 50.0481619, 14.3064090, 'Stodůlky'],
    ['stodulky-floglova', 50.0476106, 14.3093606, 'Stodůlky – Flöglova'],
    ['stodulky-habova', 50.0461493, 14.3100930, 'Stodůlky – Hábova'],
    ['stodulky-kameny', 50.0485199, 14.3110237, 'Stodůlky – kameny'],
    ['stodulky-runcatleap', 50.0461855, 14.3108816, 'Stodůlky – runcatleap'],
    ['strahov', 50.0783158, 14.3882140, 'Strahov'],
    ['strahov-menza', 50.0792670, 14.3929400, 'Strahov – menza'],
    ['strasnice-gutova', 50.0701131, 14.4880778, 'Strašnice – Gutova'],
    ['strasnice-u-hraze', 50.0699409, 14.4865076, 'Strašnice – U hráze'],
    ['strasnicka', 50.0706220, 14.4892567, 'Strašnická'],
    ['stresovice-billa', 50.0876410, 14.3665328, 'Střešovice – Billa'],
    ['stresovice-brevnovska', 50.0852257, 14.3644119, 'Střešovice – Břevnovská'],
    ['stresovice-catleap', 50.0877717, 14.3653603, 'Střešovice – catleap'],
    ['stresovice-cerne-raily', 50.0877106, 14.3636347, 'Střešovice – černé raily'],
    ['stresovice-garaz', 50.0882218, 14.3660533, 'Střešovice – garáž'],
    ['stresovice-hladkov', 50.0889297, 14.3864888, 'Střešovice – Hládkov'],
    ['stresovice-na-petynce', 50.0875241, 14.3815512, 'Střešovice – Na Petynce'],
    ['stresovice-schody', 50.0881006, 14.3646395, 'Střešovice – schody'],
    ['stresovice-za-hladkovem-garaz', 50.0880655, 14.3829456, 'Střešovice – Za Hládkovem – garáž'],
    ['stresovice-za-hladkovem-raily', 50.0887862, 14.3831600, 'Střešovice – Za Hládkovem – raily'],
    ['troja-kovarna', 50.1152183, 14.4171026, 'Troja – Kovárna'],
    ['troja-kovarna-detske-hriste', 50.1155028, 14.4191343, 'Troja – Kovárna – Dětské hřiště'],
    ['troja-trojska', 50.1162846, 14.4340213, 'Troja – Trojská'],
    ['velka-ohrada-basteckeho', 50.0401538, 14.3362110, 'Velká Ohrada – Bašteckého'],
    ['velka-ohrada-basteckeho-2', 50.0383551, 14.3358413, 'Velká Ohrada – Bašteckého 2'],
    ['velka-ohrada-namesti-a-okoli', 50.0378750, 14.3383929, 'Velká Ohrada – náměstí a okolí'],
    ['velka-ohrada-u-polikliniky', 50.0358791, 14.3424909, 'Velká Ohrada – u polikliniky'],
    ['velka-ohrada-u-skoly', 50.0352466, 14.3411601, 'Velká Ohrada – u školy'],
    ['vinohrady-workout-lache-hriste', 50.0723293, 14.4444183, 'Vinohrady – Workout / Lache hřiště'],
    ['vltavska', 50.0994143, 14.4386665, 'Vltavská'],
    ['vltavska-flow', 50.0990838, 14.4368247, 'Vltavská – flow'],
    ['vltavska-most', 50.0981905, 14.4376182, 'Vltavská – most'],
    ['vltavska-raily', 50.1004491, 14.4378434, 'Vltavská – raily'],
    ['vltavska-strides', 50.0990838, 14.4368247, 'Vltavská – strides'],
    ['vysehrad-garaze', 50.0636068, 14.4367896, 'Vysočany – park Podviní'],
    ['vysehrad-kongresak', 50.0629515, 14.4301327, 'Vysočany – stridy'],
    ['vysehrad-u-gymnazia', 50.0602718, 14.4325430, 'Vysočany – u Polikliniky'],
    ['vysocany-park-podvini', 50.1113455, 14.4936033, 'Vyšehrad – garáže'],
    ['vysocany-stridy', 50.1077940, 14.4943434, 'Vyšehrad – Kongresák'],
    ['vysocany-u-polikliniky', 50.1083006, 14.4917158, 'Vyšehrad – U Gymnázia'],
    ['zahradni-mesto-centrum', 50.0565481, 14.5074570, 'Zahradní Město – centrum'],
    ['zahradni-mesto-ke-skalkam', 50.0553134, 14.4887567, 'Zahradní Město – Ke skalkám'],
    ['zahradni-mesto-na-slatince', 50.0556940, 14.4923186, 'Zahradní Město – Na Slatince'],
    ['zahradni-mesto-na-slatince-2', 50.0557508, 14.4918600, 'Zahradní Město – Na Slatince 2'],
    ['zahradni-mesto-poliklinika-zahradni-mesto', 50.0569042, 14.4970613, 'Zahradní Město – Poliklinika Zahradní Město'],
    ['zahradni-mesto-strecha', 50.0537256, 14.5000219, 'Zahradní Město – střecha'],
    ['zahradni-mesto-u-zahradniho-mesta', 50.0531282, 14.4966294, 'Zahradní Město – U Zahradního města'],
    ['zahradni-mesto-vjezd', 50.0558197, 14.4953093, 'Zahradní Město – vjezd'],
    ['zahradni-mesto-vylezy', 50.0543593, 14.4908756, 'Zahradní Město – výlezy'],
    ['zizkov-kostnicke-namesti', 50.0861120, 14.4483304, 'Žižkov – Kostnické náměstí'],
    ['zizkov-rokycanova', 50.0869931, 14.4598612, 'Žižkov – Rokycanova'],
    ['zizkov-v-zahradkach', 50.0895319, 14.4877451, 'Žižkov – V Zahrádkách'],
    ['zofin-detske-hriste', 50.0770510, 14.4132440, 'Žofín – dětské hřiště'],
  ];
  var map = new google.maps.Map(document.getElementById('map2'), {
    zoom: 11,
    center: new google.maps.LatLng(50.0806, 14.4447),
    mapTypeId: google.maps.MapTypeId.ROADMAP
  });
  var infowindow = new google.maps.InfoWindow();
  var marker, i;
  for (i = 0; i < locations2.length; i++) {  
    marker = new google.maps.Marker({
      position: new google.maps.LatLng(locations2[i][1], locations2[i][2]),
      map: map,
      title: locations2[i][3],
    });
    google.maps.event.addListener(marker, 'click', (function(marker, i) {
      return function() {
        window.open("http://www.dpsc.8u.cz/spoty/" + locations2[i][0]);
        //infowindow.setContent(locations[i][0]);
        //infowindow.open(map, marker);
      }
    })(marker, i));
  }
</script>
