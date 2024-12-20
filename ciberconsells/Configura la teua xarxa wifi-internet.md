# COMPRÉN I CONFIGURA LA TEUA XARXA WIFI (INTERNET)

L'objectiu d'aquest blog és donar a entendre amenament la majoria de conceptes importants i relatius a la instal·lació d'internet en la nostra llar. Començarem explicant tota una sèrie de conceptes, aparells i protocols. Més endavant es donaràn alguns consells per configurar la nostra xarxa privada. 

## Què és internet?

Inter- és un sufixe que significa "entre varios". Net en anglés significa xarxa. Per tant, internet significa "xarxa entre varios". Podem pensar en internet com un sistema de correus amb una capàcitat de càrrega i velocitat redículament superiors a qualsevol altre servei de correus postal o paqueteria. És un servei de missatgeria que empra una insfraestructura sofisticada i novedosa per a l'ésser humà. Els missatges/paquets que transporta són dades produïdes per màquines i pensades per ser rebudes per altres màquines. El seu mitjà de transport són ones electromagnètiques (Wi-Fi, cobertura del mòbil, cobertura per satel·lit...), mitjançant impulsos elèctrics (cables de coure) o impulsos lumínics ([fibra òptica](https://www.youtube.com/watch?v=_OywbkAIJq0)). Ara ja tenim una idea pràctica de què és internet. Però, si és com un sistema de correu postal o paqueteria, quines són les adreces?

## IP 
És ben conegut el concepte de IP, però no és tan popular saber què significa i implica. IP són les sigles de Internet Protocol i és bàsicament un identificador/adreça que serveix per identificar de forma única els aparells connectats a internet. Hui dia hi ha dos versions de les IP, les IPv4 i les IPv6. La funció de cada versió és la mateixa, però canvien el seu format. Les Ipv4 estàn formades per quatre nombres entre 0 i 255 separats per un punt (.), per exemple: 192.168.1.254, 10.0.0.5, 78.233.241.1, ... Les IPv6 són més llargues i complexes. Estan formades per fins a 8 grups de 4 caràcters separats per dos punts (:) i que poden ser dígits entre 0 i 9 i lletres entre A i F. Alguns exemples són: 2001:0db8:85a3:0000:0000:8a2e:0370:7334, fe80::1ff:fe23:4567:890a, 2001:db8:85a3::8a2e:370:7334, ...

IPv6 es va desenvolupar degut a que les direccions IPv4 corren el risc d'esgotar-se per culpa de la expansió que ha patit internet a nivell global. Ara mateix ens trobem en una transició on els aparells moderns solen tindre una IPv4 i altra IPv6, l'objectiu és que en un futur sols hi hagen IPv6, ja que no correm risc de exhaurir les possibles combinacions d'aquesta versió. Fins aleshores, hi ha una classificació important sobre les IP que cal saber. Les IP poden ser:

- IP privada: són direccions que s'utilitzen per identificar aparells dintre d'una xarxa local. És a dir, són direccions IP que el nostre router assigna dinàmicament (dinàmicament vol dir que segons ens connectem a internet i eixim de casa, aquestes direccions IP poden canviar) als aparells que estàn connectats a internet a través d'ell. Per exemple, les IP del vostre mòbil, ordinador i televisió quan estan connectats a l'internet de casa són IP privades. Aquestes direccions IP estàn dintre dels següents rangs: 10.0.0.0 a 10.255.255.255, 172.16.0.0 a 172.31.255.255 i 192.168.0.0 a 192.168.255.255.
- IP pública: És l'adreça que identifica a una xarxa a nivell global. Això vol dir que "l'internet" de la nostra llar té un identificador únic i que si algú ens vol manar un whatsapp, l'enviarà a aquesta direcció IP i el nostre router s'encarregarà de reenviar-lo únicament al nostre smartphone. Per ficar altre exemple, quan vegem una pel·lícula en netflix el que fem és comunicar-nos amb els servidors de netflix emprant la IP pública d'aquestos, ells ja s'apanyen com calga per manar-nos la pel·lícula que volem vore.

Recopilem breument. Ja sabem vagament què és internet i que les IP són les nostres adreces d'intre d'internet. Podem inferir que les IP públiques i privades funcionen com si foren les direccions de carrer i nombre (IP pública) i per rematar la transmisió, la direcció de la nostra porta i pis (IP privada) dintre del nostre edifici. Però, falta una cosa: Com saben els aparells electrònics qui és qui? Com s'identifiquen els uns als altres? Si ja tenim l'adreça del missatge, no ens falta el nom del destinatari? Efectivament, vegem què són les MAC?

## MAC
Una MAC (Media Access Control) és un identificador únic de cada aparell electrònic que és capaç de connectar-se a internet. És un codi que funciona com un DNI per identificar aquestos parells. Aquest codi està gravat en les targetes de red (els xips encarregats de connectar l'aparell a internet) i són molt difícils de modificar (si bé si que es pot mitjançant programari especialitzat, suplantar temporalment una MAC). Aquestos identificadors s'utilitzen dintre d'una xarxa local (l'internet de casa) de forma que el router és capaç de redirigir els missatges que li arriben als destinataris pertinents i no a altres. L'estructura d'una MAC és pareguda a una IPv6, però molt més simple. Està formada per 6 grups de parelles de caràcters separats per dos punts (:), aquestos caràcters poden ser una vegada més numèrics (del 0 al 9) i entre la A i la F. Alguns exemples poden ser: 00:1A:2B:3C:4D:5E, 3C:5A:B4:9F:1E:2D, 00:0A:95:9D:68:16, ...

Si teniu curiositat per aprofundir en la vostra comprensió sobre com funciona internet, vos recomane que busqueu informació sobre DNS, NAT, DHCP, Paquets de dades i ports. Més endavant pot ser us podeu intentar atrevir amb el "model OSI", però aneu amb calma, no són lectures entretingudes ni senzilles.

## "Ruter" i router
Aquest aparell és un gran aliat de tot aquell qui disfruta d'internet. És segurament el dispositiu estrictament de la xarxa que ens és més conegut i proper. Tots el reconeguem dintre de casa o el lloc de treball i és el primer culpable quan tenim problemes de connexió. Vull, però, aclarar algunes coses sobre aquest aparell que coneguem com "Router" o "Ruter". A un nivell teòric, un router és el dispositiu encarregat de connectar una xarxa local a internet. Però, l'aparell que nosaltres coneguem con ruter fa més coses. I és que hui dia, per simplificar les instal·lacions d'internet a nivell domèstic, s'han integrat en el "Ruter" els següents elements/dispositius:
- Router: dispositiu encarregat de redireccionar els paquets de dades/missatges que s'envien i es reben en una xarxa local d'internet.
- Switch: permet connecar diferents dispositius al router mitjançant cables (són les típiques connexions per a cables de xarxa que trobem en la part de darrere del "Ruter").
- Punt d'accés Wi-Fi: proporciona connexió sense cable al router mitjançant ones electromagnètiques que coneguem com Wi-Fi.
- Mòdem: dispositiu encarregat de convertir els paquets de dades/missatges enviats pels dispositius en senyals transmissibles (impulsos lumínics, impulsos elèctrics o impulsos electromagnètics) i viceversa. 

## Configura el teu router:
Ara que ja sabem què és un router i tenim una idea de què fa el nostre "Router", podem passar a configurar-lo. Aquest pas és algo que poca gent fa i és bàsic. Si som responsables de una xarxa local, hem de saber administrar-la. Tranquils no és difícil. Seguirem els següents passos (si encara no he heu fet):

1. Girem el router i revisem la etqieuta que té per baix. Hem de localitzar la direcció IP privada que per defecte té el router, normalment serà 192.168.1.1 o 192.168.0.1.
2. Anirem a algún dispositiu que estiga connectat a internét a través d'aquest ruter i ficarem en la barra de cerca la IP que hem trobat.
3. En la etiqueta del router apareixen un nom d'usuari i una contrasenya per defecte. Solen ser del tipus admin/admin, user/user, vodafone/1234... Són combinacions molt senzilles per defecte.
4. Escribim el usuari i contrasenya que hem trobat en la etqueta del ruter en el formulari d'accés de la pàgina que es carregarà al realitzar el segón pas.
5. Ara tindrem al nostre abast una sèrie de dades i opcions de configuració.
6. La primera acció i més important és canviar la contrasenya i usuari del router, les credencials que heu emprat per entrar a la pàgina web on estem. No és gens acceptable deixar les credencials per defecte, qualsevol persona que es puga connectar al nostre wifi podria guanyar molot fàcilment el control sobre ell si no fem aquest canvi.
7. Comprovar que el mode de seguretat del nostre wifi és WPA2 o WPA3, no és acceptable que el mode de seguretat del nostre internet siga WEP, WPA, WPA/WPA2 mixed o Open. Qualsevol d'aquestos últims modes de seguretat estàn desfasats o diractament no protegeixen el nostre trànsit. 

### Bones pràctiques de seguretat en la seguretat del nostre router:
- Deshabilitar que la nostra SSID (nom de la nostra xarxa wifi) siga visible. Una interfície d'internet visible és una interfície molt més expossada a atacs i connexions no desitjades.
- Canviar la contrasenya d'accés wifi a una que puguem memoritzar però que siga [llarga i complexa](https://github.com/Vicentvibes/Blog_personal/blob/main/ciberconsells/Contrasenyes.md#bones-pr%C3%A0ctiques-per-crear-contrasenyes), a prova d'atacs. 
- Habilitar un wifi per convidats el qual podem decidir deixar visible.

## Configuracions avançades però molt útils:
- Configurar el tallafocs del router.
- Si heu perdut una estona en explorar totes les dades i curiositats que té la web del nostre router, és possible que vos preocupe amb raó la vostra privacitat. Efectivament, el nostre proveidor d'internét (vodafone, movistar, digi, lowi...) saben en tot moment totes aquestes dades i més. Heu de pensar que tot el nostre tràfic de missatges passa pels seus dispositius i per tant no sols pdoen fer un seguiment del nostre consum i costum, també són capaços de saber en gran mesura quines webs estem visitant o si volen, poden també tindre accés a part del contingut que enviem o rebem. És preocupant i poc atractiu que la nostra privacitat "digital" estiga en mans d'una empresa privada amb finalitats i acords que no tenen per què alinear-se amb les nostres inquietuds. Si, com a mi, vos preocupa aquesta situació, us recomane que busqueu un servei VPN privat i el pagueu. Personalment us recomane [NordVPN](https://nordvpn.com/es/offer-site/), una opció amb connexions VPN ràpides, amb un fort compromís de confidencialitat amb els clients i preus molt competitius que ofereixen també altres serveis interessants. A més, amb aquest servei sempre podreu sortejar polítiques o manca de serveis que depenen del lloc geogràfic on us trobeu. 

GLOSSARI:

- Xarxa local:
- VPN:








