---
title: "Nalin-tech-an Agad"
date: 2007-10-24
tags: ["Frustrations"]
---

Techie ang post na ito kaya dapat ay sa http://tech.borap.net ito nakalagay subalit hindi ko pa naisasalin sa ingles kaya dito na lang muna. Baka ilagay ko rin dun balang-araw.

Kanina ay nag-install ako ng Ubuntu 7.10 (Gutsy Gibbon) sa isang computer na gagamitin ko para mag-develop ng mga application. Pinili ko ang bagong labas na Ubuntu sapagkat gusto ko makita kung gaano na kalayo ang narating nito dahil hindi ko naman ito ginagamit. Isa pa, gusto ko rin mag-GNOME dahil puro KDE na ako. Kailangang balansehin ang paggamit para hindi maging one-sided ang aking pananaw.

Ayun at natapos naman ang aking installation. Natuwa naman ako at mukhang pulido ang Gutsy Gibbon. Nagawa ko pang paglaruan ang mga effects na dulot ng Compiz Fusion. Mahusay talaga. Mukhang magiging maganda ang paggawa ko sa makina na ito.

Ngunit hindi pala ganun kadali ang lahat. Dumating ang tao na namumuno sa technical side ng aking mga gagawin at tinignan ang computer na nilagyan ko ng Ubuntu. Tsinek nya kung anong OS ang gamit ko at hindi nya nalaman. Sinabi ko na latest ng Ubuntu yun at medyo sumama ang kapaligiran. Sinabi nya na akala nya ay CentOS ang nilagay ko. Nakita raw nya kasi kanina yun. Nagkaroon daw sila ng problema dati sa paglipat ng data sa pagitan ng dalawang magkaibang version ng PostgreSQL.

At bigla akong napasagot ng hindi ko namalayan. Sinabi ko na walang kinalaman ang OS sa problema nila dati. Sinabi ko rin na sadyang nagbabago ang PostgreSQL sa major number nito. Kumbaga galing sa 7.x papuntang 8.x o vice versa. Kapag minor number e ok lang naman. 8.1.x papuntang 8.2.x at vice versa. At wala na akong narinig sa kanyang sagot.

Lumipas ang araw at kinalikot ko na ang computer. Naisaayos ko na ang lahat para makagawa na sana ako bukas (o mamaya, depende sa inyong oras) nang dumating ang pinakaulo sa lugar na iyon. Tinawag nya ako at may pag-uusapan daw kami. Akala ko kung ano na pero yung nasa talata sa baba lang pala.

Sinabi nya na baka hindi raw malinaw ang napag-usapan namin. Si tao kanina raw ang sagot sa lahat ng technical na bagay. May mga nabanggit pa syang iba ngunit ang kabuuan ng usapan ay kailangan kong gawing CentOS ang nakalagay sa computer na gagamitin ko. Ang dahilan daw ay iyon din ang gamit sa production server. Mas mainam na raw na CentOS din ang gamit ko sapagkat kung tumakbo na ang ginagawa ko sa computer na ginagamit ko e siguradong tatakbo na rin iyon sa production server.

May punto sila kaya pumayag na rin ako. Pero may ilang punto rin ako na siguradong may kabuluhan naman. Ito sila.
- Ang isang developer ay Windows ang gamit.
- Ang isa pang developer ay Windows din ang gamit. Nage-ssh lang sya dun mismo sa production server para gumawa.
- Ang version ng Apache at PostgreSQL na nasa server ay hindi kapareho nung mga nasa CentOS 5 na syang pinapa-install sa akin. Hindi ako sigurado sa version ng PHP.
- Kaya nga tinetest ang application ay para siguradong tumakbo ito sa production server. Walang kinalaman ang OS ng makinang ginamit para magawa ang application. Ang mahalaga ay mahusay ito pagdating sa production server.

Hindi ako galit. Nagpapaliwanag lang. Pero kahit anong gawin ko, hindi ko pa rin maunawaan hanggang ngayon kung bakit pinilit ang pagpapalit ng OS. Siguro balang araw ay malalaman ko rin ang kasagutan.

---

> Marte Raphael Soliza said...  
> Ang mas mainam sigurong solusyon ay gumamit ng virtualization (tulad ng VMWare) para magaya talaga ang specs ng software na naka-install sa production server, at du'n ka mag-test. Pwede din namang gumawa ng test server na kapareho (o halos kapareho) ng production server na accessible sa lahat. Kung meron na namang ganito, sang-ayon ako na hindi na kailangan pang palitan ang distro na gamit mo pang-develop dahil pwede ka na namang magkalikot sa test server. Kung wala pa, mas mabuti ngang gamitin 'yung CentOS para masabay mo ang pagiging sanay sa distro na ito, maliban na lang kung sanay ka na rin talaga. Ito nga pala ang mga major difference ng Debian at Red Hat na napansin ko pagdating sa deployment na maaaring maging sanhi ng problema (baka alam mo na sila):
> - hindi kusang nagsisimula ang services pag-boot (kailangan pang i-chkconfig o i-start manually)
> - SELinux (kung enabled 'to sa production server, good luck, hehe)

> Wednesday, October 24, 2007 2:32:00 AM 

> Mark Alvin Ligaya said...  
> Tama ka dyan, walang kinalaman ang OS na ginamit sa development sa sagot sa katanungan kung tatakbo ba o hindi ang application sa server, at kung mayroon man, para saan pa ang testing? hehehe. kaya nga itinetest para kapag gagamitin na talaga ang sistema eh minimal o wala na talagang problema :)  
> Wednesday, October 24, 2007 12:48:00 PM 

> Waldemar Bautista said...  
> Mahusay na insight, Myrtactle. Hindi ko naisip yung virtualization. Haha. Pero wala na. Naka-CentOS 5 na ako.
> Ang ginagawa ko sa services e may GUI naman para i-enable iyon sa iba't-ibang runlevel. Ayoko na mag-chkconfig. Yung SELinux, dinisable ko sa development machine. Pero di ko pa nakikita kung meron ang production. Hehe.  
> Wednesday, October 24, 2007 9:56:00 PM 