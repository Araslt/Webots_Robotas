<!DOCTYPE html>
<html>
<head>

</head>
<body>

<h2>LINIJA VAŽIUOJANTIS ROBOTAS</h2>
<p>Linija važiuojantis robotas, puikus būdas susipažinti tiek su Webots programa, tiek su 
robotika, kadangi sėkmingam darbo įgyvendinimui užtenka tik bazinių programavimo žinių. 
Pats darbas susideda iš trijų pagrindinių dalių: aplinkos, roboto ir programinio kodo.</p>

<h2>APLINKA</h2>

![image](https://github.com/Araslt/Webots_Robotas/assets/15888932/64eefb70-5eeb-42ec-95a9-ec71edbe1911)
<p><em>1-as pav.</em> – Aplinkos pagrindas – baltas fonas su kontrastinga juoda linija<br></p>
<p>Standartinis pagrindas (TexturedBackground) modifikuotas taip, kad dėl didesnio kontrasto 
juoda linija būtų baltame fone.<br>
Aplinkos kodas talpinams ../protos/ direktorijoje, failas su *.proto plėtiniu. Įkeliamas į darbą: 
„add -&gt; PROTO nodes -&gt; TrackOne“.<br>
Aplinkos pagrindo kodas: <a href="https://github.com/Araslt/Webots_Robotas">https://github.com/Araslt/Webots_Robotas</a></p>

<h2>ROBOTAS</h2>

![image](https://github.com/Araslt/Webots_Robotas/assets/15888932/279c974b-f6f6-4c92-a14a-850530c86e72)
<p><em>2-as pav.</em> – e-puck robotas su atvaizduotais atstumo matavimo spinduliais<br></p>
<p><Robotas – e-puck iš Webots bibliotekos, modifikuotas, t. y. pridėti IR (infraraudonieji
spinduliai) sensoriai – siustuvas ir imtuvas. IR sensoriai (arba tiesiog kameros) – kad būtų 
galimybė sekti atvaizduotą ant pagrindo liniją.<br>
Įsikeliam į darbą robotą: „add -&gt; PROTO nodes -&gt; Robots -&gt; gctronic -&gt; e-puck“.<br>
Pridedam robotui du IR sensorius: „groundSensorsSlot -&gt; add -&gt; Base nodes -&gt; 
DistanceSensor -&gt; type -&gt; infrared“.</p>

<h2>PROGRAMINIO KODO LOGIKA</h2>

![image](https://github.com/Araslt/Webots_Robotas/assets/15888932/9a8cdac6-6293-4639-8d8f-592010100a66)
<p>3-as pav. – e-puck IR spindulių siųstuvo (transmitter) ir imtuvo (receiver) </p>
<p>Kontroleris (controller) – kodas, python programavimo kalba, valdantis tokias roboto 
funkcijas kaip ratų sukimasis, IR siustuvo ir imtuvo veikimas.<br>
Programinį kodą priskiriam e-puck robotui: „e-puck -&gt; controller -&gt; select controller“.<br>
Kode aprašyti objektai - motorai sukantys ratus, su greičio ir pozicijos funkcijom, taip pat IR 
sensorių objektai su IR sensorių reikšmių nuskaitymo funkcijom.<br>
Sensorių reikšmėms patekus į aprašytą diapazoną, yra stabdomas vienas ir sukamas kitas 
motoras, tokiu būdu imituojamas posūkis ir judėjimas linija.</p>


</body>
</html>
