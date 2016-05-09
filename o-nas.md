---
layout: page
title: O nás
permalink: /o-nas/
---

<script src="//code.jquery.com/jquery-1.11.3.min.js"></script>

### Kdo jsme

Parkour Praha je neregistrovaná skupina příznivců sportů označovaných jako parkour, freerunning nebo art du déplacement. Naším cílem je prostřednictvím těchto disciplín šířit dobro.

### Novinky

{% for post in site.posts limit:3 %}<a href="{{ post.url | prepend: site.baseurl }}"><i>{{ post.date | date: "%Y-%m-%d" }}</i> {{ post.title }}</a><br />{% endfor %}

### Kontakt


<form id="f">
<div class="row uniform 50%">
  <div class="6u 12u$(medium)">
    <input type="text" id="name" placeholder="Jméno a příjmení"></input>
  </div>
  <div class="6u 12u$(medium)">
    <input type="text" id="contact" placeholder="E-mail nebo telefon"></input>
  </div>
  <div class="12u 12u$(medium)">
     <textarea id="message" placeholder="Zpráva" rows="2"></textarea>
  </div>
  <div class="6u 12u$(medium)">
    <input type="submit" class="button special" id="btn" value="Odeslat">
  </div>
</div>
</form>

<script type="text/javascript">
        $(document).ready(function() {
            $('form[id=f]').submit(function(e) {
                e.preventDefault();
                var text = $('#name').val() + ' – ' + $('#contact').val() + ' – ' + $('#message').val();
                var postData = '{"text": "' + text + '", "channel": "#kontakt"}';
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

<br />

<a id="filosofie"></a>

   

### Naše filosofie a pojetí parkouru

Parkour (v našem pojetí) je soubor metod tréninku, který pomáhá rozvíjet schopnost přemístit se bezpečně a rychle z jednoho místa na druhé. Vychází z myšlenky, že člověk je sobě, svým blízkým i společnosti užitečnější, pokud je – chápáno v nejširším smyslu slova – silný. Pokud ve Vašem bytu začne hořet, nebudete se bát opustit ho přes balkón. Budete schopni zvednou svoje dítě do náručí, aniž by Vám luplo v zádech. Pokud spadnete za jízdy z kola, přistanete pohodlně v parakotoulu.

* Užitečnost pohybů má přednost před jejich pohledností
* Kvalita je důležitější než kvantita
* „Přizpůsobte si užitečné, odmítněte zbytečné a přidejte vaše vlastní.“ ~ _Bruce Lee_

Náš přístup k tréninku reflektuje tuto původní filosofii parkouru tak, jak ji vytyčili jeho zakladatelé. K tomu navíc zahrnuje zábavné prvky, které lektoři přebírají z tréninku dětí. Smyslem je tedy, kromě uchování zdraví a rozvoje kondice, poskytnutí možnosti aktivně a zábavně strávit volný čas. Sdílení zážitků je na trénincích povoleno a možná zde získáte i nové přátele, které Vás budou podporovat na této Vaší životní cestě.

<a href="/treninky/#pravidelne" class="button">Více o trénincích</a>

---

### Právní prohlášení

#### Informace na webu parkourpraha.cz

Tento web provozujeme a informace uvádíme v dobré víře v jejich pravdivost a aktuálnost, v žádném případě však nemůžeme vyloučit chyby nebo nepřesnosti, které se na stránkách parkourpraha.cz mohou objevit. Veškeré používání informací z webu parkourpraha.cz jsou pouze a jen na vlastní zodpovědnost a nebezpečí toho, kdo je používá.

<a id="podminky"></a>

   

#### Podmínky účasti na kurzu Parkour Praha

Přihlášením na lekci, tréninkovou jednotku nebo kurz pořádaný lektory Parkour Praha (dále jen lekce) potvrzujete, že jste se důkladně seznámili s následujícími podmínkami a informacemi a že je berete na vědomí a souhlasíte s nimi. Pokud se lekce účastníte bez přihlášení, je samotná účast považována za přihlášení a plynou z ní stejné povinnosti.

#### Možná rizika provozování parkouru a kondičních cvičení

Vědomě a svobodně souhlasím s přijetím všech známých i neznámých rizik účasti na lekci. Prohlašuji, že jsem měl možnost se s těmito riziky plně seznámit. Vylučuji odpovědnost lektorů a organizačních pracovníků Parkour Praha za jakékoli újmy, na zdraví či majetku, způsobené mé osobě. Tato rizika zahrnují, ale nejsou omezena na riziko: smrti, poranění hlavy a páteře, fraktur, distorze kotníku, hlezna, zápěstí, lokte a ramene, odřenin, puchýřů, hematomů, chronických onemocnění pohybového aparátu, infarktu myokardu a žloutenky.

#### Souhlas se zpracováním osobních údajů a s pořizováním audiovizuálních záznamů

Přihlášením dávám správci Parkour Praha souhlas se zpracováním uvedených osobních údajů v souladu s § 5 zákona č. 101/2000 Sb. o ochraně osobních údajů a změně některých zákonů, ve znění pozdějších předpisů. Účelem je evidence účastníků nezbytná pro zajištění akce. Sumarizované údaje mohou být použity správcem pro statistické účely pro vnitřní potřebu správce.

Uděluji neomezený souhlas s použitím, reprodukováním, prodáváním a šířením jakýchokoli fotografií, obrázků, videozáznamů, nahrávek, filmů či zobrazení mé osoby jakéhokoli druhu pořízených během lekce. Jsem si vědom toho, že mi za toto nenáleží žádná odměna.

#### Informovaný souhlas

Přečetl jsem si a plně porozuměl výše uvedeným souhlasům a vyloučením odpovědnosti a tyto svobodně, vědomě a bez ponoukání stvrzuji [svou přihláškou](/treninky/#prihlaska).