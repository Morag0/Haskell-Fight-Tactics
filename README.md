# project_Morten_Ågotnes

* Haskell Fight Tactics
HTF er en autobattler hvor du kjøper og oppgraderer brikker, som kjemper motstandere for deg. 

# Game loop
Spillet har to faser, kjøpsfasen og kampfasen. 
I kjøpsfasen kan du bruke pengene du fikk under kampfasen til å kjøpe nye brikker. Når du får nok av en sort brikke vil den kunne oppgraderes til en sterkere versjon.
I kampfasen sender du brikkene du kjøpte til en Player vs Enviorment kamp. Brikkene sloss for deg, og kampen er ferdig når enten du eller motstanderen har tapt sine brikker. Du beholder brikkene du taper under kampen. Du får penger basert på om du vant, og hvor mange av motstanderens brikker du slo ut.
Spillet er over etter tre kamper, og du får en score basert på hvor bra du gjorde det.

# Brikkene
Det vil være to forkskjellige typer brikker. En med mye liv, men lite skade og en med lite liv, men mye skade. Brikkene har 2 nivåer, level 1 og level 2. Når du kjøper en brikke får du den alltid i level 1. Sammler du 3 level 1 brikker av samme type vil de slås sammen til en level 2 brikke som har mer liv og skade.

# Ai
Brikkene styres ikke av deg under kampfasen, men bruker heller en simpel Ai. Hver brikke vil ha 2 moduser, search og destroy. I search vil brikken se etter nærmeste motstander brikke og gå mot den. Er den i en nabocelle vil brikken skifte til destroy. Da vil brikken skade motstanderbrikken helt til den er slått ut, eller brikken selv blir slått ut. Dersom motstander brikken blir slått ut vil brikken gå tilbake til search. En brikke kan bare angripe en annen brikke om gangen, og vil velge randomly dersom det er flere gyldige valg.

# Game Board
Spill Brettet vil være en 6*6 matrix, hvor du "kontrollerer" en halvdel og kan fritt sette brikkene ut på denne halvdelen.
