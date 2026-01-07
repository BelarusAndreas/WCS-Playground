

### Features
 - Einfache Integration
 - Leicht an deinen Bedürfnissen anpassbar

### Quellcode
```
<style>
.converter-wrapper {
  margin: 0 auto;
  width: 100%;
  max-width: 600px;
  text-align: center;
  padding: 10px;
  box-sizing: border-box;
}
.converter-wrapper input {
  font-size: 1em;
  width: 100%;
  text-align: center;
  margin-top: 10px;
  height: 40px;
  box-sizing: border-box;
}
.converter-wrapper span {
  position: relative;
  display: inline-block;
  vertical-align: middle;
  width: 100%;
}
.converter-wrapper span select {
  background-color: #263648;
  color: #fff;
  font-size: inherit;
  padding: 10px;
  width: 100%;
  border: 0;
  margin: 0;
  border-radius: 0px;
  text-indent: 0.01px;
  text-overflow: '';
  -webkit-appearance: none;
}
.converter-wrapper span::before, .converter-wrapper span::after {
  content: "";
  position: absolute;
  pointer-events: none;
}
.converter-wrapper span::after { 
  content: "\25BC";
  height: 1em;
  font-size: .625em;
  line-height: 1;
  right: 1.5em;
  top: 50%;
  margin-top: -.5em;
  color: #fff;
}
.converter-wrapper span::before {
  width: 2.5em;
  right: 0;
  top: 0;
  bottom: 0;
  border-radius: 0;
  background-color: #202E3C;
}
.converter-side-a, .converter-side-b {
  float: left;
  margin-top: 10px;
  box-sizing: border-box;
  width: 45%;
}
.converter-equals {
  float: left;
  box-sizing: border-box;
  width: 10%;
  color: #fff;
  font-size: 2.4em;
  line-height: 2;
  text-align: center;
}
.converter-side-a {
  padding-right: 10px;
}
.converter-side-b {
  padding-left: 10px;
}
</style>

<div class="converter-wrapper">
  <form name="property_form">
    <span>
      <select class="select-property" name="the_menu" size=1 onChange="UpdateUnitMenu(this, document.form_A.unit_menu); UpdateUnitMenu(this, document.form_B.unit_menu)">
      </select>
    </span>
  </form>

  <div class="converter-side-a">
    <form name="form_A" onSubmit="return false">
      <input type="text" class="numbersonly" name="unit_input" maxlength="20" value="0" onKeyUp="CalculateUnit(document.form_A, document.form_B)">
      <span>
        <select name="unit_menu" onChange="CalculateUnit(document.form_B, document.form_A)">
        </select>
      </span>
    </form>
  </div>
  
 <div class="converter-equals">
   <p>=</p>
 </div>

  <div class="converter-side-b">
    <form name="form_B" onSubmit="return false">
      <input type="text" class="numbersonly" name="unit_input" maxlength="20" value="0" onkeyup="CalculateUnit(document.form_B, document.form_A)">
      <span>
        <select name="unit_menu" onChange="CalculateUnit(document.form_A, document.form_B)">
        </select>
      </span>
    </form>
  </div>
</div>

<script>
var property = new Array();
var unit = new Array();
var factor = new Array();

property[0] = "Beschleunigung";
unit[0] = new Array("Meter/sq.sec (m/sec²)", "Foot/sq.sec (ft/sec²)", "G (g)", "Galileo (gal)", "Inch/sq.sec (in/sec²)");
factor[0] = new Array(1, .3048, 9.806650, .01, 2.54E-02);

property[1] = "Fläche";
unit[1] = new Array("Square Meter (m²)", "Acre (acre)", "Are", "Barn (barn)", "Hektar (ha³)", "Rood", "Square Zentimeter", "Square Kilometer", "Circular mil", "Square Foot (ft²)", "Square Inch (in²)", "Square Meile (mi²)", "Square Yard (yd²)");
factor[1] = new Array(1, 4046.856, 100, 1E-28, 10000, 1011.71413184285, .0001, 1000000, 5.067075E-10, 9.290304E-02, 6.4516E-04, 2589988, .8361274);

property[2] = "Drehmoment";
unit[2] = new Array("Newtonmeter (N m)", "Dyne-centimeter(dy cm)", "Kgrf-meter (kgf m)", "lbf-inch (lbf in)", "lbf-foot (lbf ft)");
factor[2] = new Array(1, .0000001, 9.806650, .1129848, 1.355818);

property[3] = "Elektrizität";
unit[3] = new Array("Coulomb (Cb)", "Abcoulomb", "Ampere/Std. (A hr)", "Faraday (F)", "Statcoulomb", "Millifaraday (mF)", "Microfaraday (mu-F)", "Picofaraday (pF)");
factor[3] = new Array(1, 10, 3600, 96521.8999999997, .000000000333564, 96.5219, 9.65219E-02, 9.65219E-05);

property[4] = "Energie";
unit[4] = new Array("Joule (J)", "BTU (mean)", "BTU (thermochemical)", "Kalorie (SI) (cal)", "Kalorie (mean)(cal)", "Kalorie (thermo)", "Elektronischer Volt (eV)", "Erg (erg)", "Foot-Pfund force", "Foot-poundal", "Pferdestärke / Std.", "Kilokalorie (SI)(kcal)", "Kilokalorie (mean)(kcal)", "Kilowattstunde (kW hr)", "Tonnen TNT", "Volt-coulomb (V Cb)", "Wattstunde (W hr)", "Wattsekunde (W sec)");
factor[4] = new Array(1, 1055.87, 1054.35, 4.1868, 4.19002, 4.184, 1.6021E-19, .0000001, 1.355818, 4.214011E-02, 2684077.3, 4186.8, 4190.02, 3600000, 4.2E9, 1, 3600, 1);

property[5] = "Kraft";
unit[5] = new Array("Newton (N)", "Dyne (dy)", "Kilogramm force (kgf)", "Kilopfundd force (kpf)", "Kip (k)", "Ounce force (ozf)", "Pfund force (lbf)", "Poundal");
factor[5] = new Array(1, .00001, 9.806650, 9.806650, 4448.222, .2780139, .4535924, .138255);

property[6] = "Kraft / Länge";
unit[6] = new Array("Newton/Meter (N/m)", "Pfund force/Inch (lbf/in)", "Pfund force/Foot (lbf/ft)");
factor[6] = new Array(1, 175.1268, 14.5939);

property[7] = "Längeneinheiten";
unit[7] = new Array("Meter (m)", "Angstrom (A')", "Astronomische Einheit (AU)", "Caliber (cal)", "Zentimeter (cm)", "Kilometer (km)", "Ell", "Em", "Fathom", "Furlong", "Fermi (fm)", "Foot (ft)", "Inch (in)", "League (int'l)", "League (UK)", "Lichtjahr (LY)", "Micrometer (mu-m)", "Mil", "Millimeter (mm)", "Nanometer (nm)", "Meile (int'l nautical)", "Meile (UK nautical)", "Meile (US nautical)", "Meile (US statute)", "Parsec", "Pica (printer)", "Picometer (pm)", "Point (pt)", "Rod", "Yard (yd)");
factor[7] = new Array(1, 1E-10, 1.49598E11, .000254, .01, 1000, 1.143, 4.2323E-03, 1.8288, 201.168, 1E-15, .3048, .0254, 5556, 5556, 9.46055E+15, .000001, .0000254, .001, 1E-9, 1852, 1853.184, 1852, 1609.344, 3.08374E+16, 4.217518E-03, 1E-12, .0003514598, 5.0292, .9144);

property[8] = "Lichteinheiten";
unit[8] = new Array("Lumen/sq.meter (Lu/m^2)", "Lumen/sq.centimeter", "Lumen/sq.foot", "Foot-candle (ft-cdl)", "Foot-lambert", "Candela/sq.meter", "Candela/sq.centimeter", "Lux (lux)", "Phot");
factor[8] = new Array(1, 10000, 10.76391, 10.76391, 10.76391, 3.14159250538575, 31415.9250538576, 1, 10000);

property[9] = "Masse";
unit[9] = new Array("Kilogramm (kgr)", "Gramm (gr)", "Milligramm (mgr)", "Microgramm (mu-gr)", "Carat (metric)(ct)", "Hundredweight (long)", "Hundredweight (short)", "Pfund mass (lbm)", "Pfund mass (troy)", "Ounce mass (ozm)", "Ounce mass (troy)", "Slug", "Tonne (assay)", "Tonne (long)", "Tonne (short)", "Tonne (metric)", "Tonne");
factor[9] = new Array(1, .001, 1e-6, .000000001, .0002, 50.80235, 45.35924, .4535924, .3732417, .02834952, .03110348, 14.5939, .02916667, 1016.047, 907.1847, 1000, 1000);

property[10] = "Massestrom";
unit[10] = new Array("Kilogram/Sek. (kgr/sec)", "Pfund Mass/Sek. (lbm/sec)", "Pfund Mass/Min. (lbm/min)");
factor[10] = new Array(1, .4535924, .007559873);

property[11] = "Gewichte";
unit[11] = new Array("Kilogramm/Cub.Meter", "Grain/Galon", "Grams/cm³ (gr/cc)", "Pfund Mass/Cubic Foot", "Pfund Mass/Cubic-Inch", "Ounces/Gallon (UK,liq)", "Ounces/Gallon (US,liq)", "Ounces (Mass)/Inch", "Pfund Mass/Gal (UK,liq)", "Pfund mass/Gal (US,liq)", "Slug/Cubic Foot", "Tons (long,mass)/Cub.Yard");
factor[11] = new Array(1, .01711806, 1000, 16.01846, 27679.91, 6.236027, 7.489152, 1729.994, 99.77644, 119.8264, 515.379, 1328.939);

property[12] = "Leistung";
unit[12] = new Array("Watt (W)", "Kilowatt (kW)", "Megawatt (MW)", "Milliwatt (mW)", "BTU (SI)/Stunde", "BTU (thermo)/Sekunde", "BTU (thermo)/Minute", "BTU (thermo)/Stunde", "Calorie (thermo)/Sekunde", "Calorie (thermo)/Minute", "Erg/Sekunde", "Foot-Pfund Force/Stunde", "Foot-Pfund Force/Minute", "Foot-Pfund force/Sekunde", "Horsepower(550 ft lbf/s)", "Pferdestärke (electric)", "Pferdestärke (boiler)", "Pferdestärke (metric)", "Pferdestärke (UK)", "Kilokalorie (thermo)/Min.", "Kilokalorie (thermo)/Sek.");
factor[12] = new Array(1, 1000, 1000000, .001, .2930667, 1054.35, 17.5725, .2928751, 4.184, 6.973333E-02, .0000001, .0003766161, .02259697, 1.355818, 745.7, 746, 9809.5, 735.499, 745.7, 69.7333, 4184);

property[13] = "Druckeinheiten";
unit[13] = new Array("Newton/sq.meter", "Atmosphere (normal)", "Atmosphere (techinical)", "Bar", "Zentimeter mercury(cmHg)", "Zentimeter Wasser (4'C)", "Decibar", "Kgr force/sq.centimeter", "Kgr force/sq.meter", "Kip/square Inch", "Millibar", "Millimeter Mercury(mmHg)", "Pascal (Pa)", "Kilopascal (kPa)", "Megapascal (Mpa)", "Poundal/sq.foot", "Pfund-force/sq.foot", "Pfund-force/sq.Inch (psi)", "Torr (mmHg,0'C)");
factor[13] = new Array(1, 101325, 98066.5, 100000, 1333.22, 98.0638, 10000, 98066.5, 9.80665, 6894757, 100, 133.3224, 1, 1000, 1000000, 47.88026, 47.88026, 6894.757, 133.322);

property[14] = "Temperaturen";
unit[14] = new Array("Celsius ('C)", "Fahrenheit ('F)", "Kelvin ('K)", "Rankine ('R)");
factor[14] = new Array(1, 0.555555555555, 1, 0.555555555555);
tempIncrement = new Array(0, -32, -273.15, -491.67);

property[15] = "Zeiten";
unit[15] = new Array("Sekunde", "Tag (Solar)", "Tag (Sidereal)", "Stunde (Solar)", "Stunde (Sidereal)", "Minute (Solar)", "Minute (Sidereal)", "Monat", "Sekunde (Sidereal)", "Jahr", "Jahr (Tropical)", "Jahr (Sidereal)");
factor[15] = new Array(1, 8.640E4, 86164.09, 3600, 3590.17, 60, 60, 2628000, .9972696, 31536000, 31556930, 31558150);

property[16] = "Geschwindigkeiten";
unit[16] = new Array("Meter/Sekunde (m/sec)", "Foot/Minute (ft/min)", "Foot/Sekunde (ft/sec)", "Kilometer/Stunde (kph)", "Knot (int'l)", "Meile (US)/Stunde (mph)", "Meile (nautical)/Stunde", "Meile (US)/Minute", "Meile (US)/Sekunde", "Lichtgeschwindigkeit (c)", "Mach (STP)(a)");
factor[16] = new Array(1, 5.08E-03, .3048, .2777778, .5144444, .44707, .514444, 26.8224, 1609.344, 299792458, 340.0068750);

property[17] = "Viskosität";
unit[17] = new Array("Newton-Sekunde/Meter", "Centipoise", "Centistoke", "Sq.Foot/Second", "Poise", "Poundal-Sekunde/sq.Foot", "Pfundmasse/Foot-Sekunde", "Pfund Force-Sekunde/sq.Foot", "Rhe", "Slug/Foot-Sekunde", "Stoke");
factor[17] = new Array(1, .001, .000001, 9.290304E-02, .1, 1.488164, 1.488164, 47.88026, 10, 47.88026, .0001);

property[18] = "Volumen & Kapazitäten";
unit[18] = new Array("Kubikmeter (m³)", "Kubikzentimeter", "Kubikmillimeter", "Acre-foot", "Barrel (Öl)", "Board Foot", "Bushel (US)", "Cup", "Fluid ounce (US)", "Cubic foot", "Gallon (UK)", "Gallone (US,dry)", "Gallon (US,liq)", "Gill (UK)", "Gill (US)", "Cubic inch (in³)", "Liter", "Liter (alt)", "Ounce (UK,fluid)", "Ounce (US,fluid)", "Peck (US)", "Pint (US,dry)", "Pint (US,liq)", "Quart (US,dry)", "Quart (US,liq)", "Stere", "Tablespoon", "Teaspoon", "Tonnen", "Cubic yard");
factor[18] = new Array(1, .000001, .000000001, 1233.482, .1589873, .002359737, .03523907, .0002365882, .00002957353, .02831685, .004546087, .004404884, .003785412, .0001420652, .0001182941, .00001638706, .001, .001000028, .00002841305, .00002957353, 8.8097680E-03, .0005506105, 4.7317650E-04, .001101221, 9.46353E-04, 1, .00001478676, .000004928922, 2.831685, .7645549);
    
property[19] = "Volumenstrom";
unit[19] = new Array("Cubic Meter/Sekunde", "Cubic Foot/Sekunde", "Cubic Foot/Minute", "Cubic Inches/Minute", "Gallons (US,liq)/Minute)");
factor[19] = new Array(1, .02831685, .0004719474, 2.731177E-7, 6.309020E-05);
function UpdateUnitMenu(propMenu, unitMenu) {
  var i;
  i = propMenu.selectedIndex;
  FillMenuWithArray(unitMenu, unit[i]);
}
function FillMenuWithArray(myMenu, myArray) {
  var i;
  myMenu.length = myArray.length;
  for (i = 0; i < myArray.length; i++) {
    myMenu.options[i].text = myArray[i];
  }
}
function CalculateUnit(sourceForm, targetForm) {
  var sourceValue = sourceForm.unit_input.value;
  sourceValue = parseFloat(sourceValue);
  if (!isNaN(sourceValue) || sourceValue == 0) {
    sourceForm.unit_input.value = sourceValue;
    ConvertFromTo(sourceForm, targetForm);
  }
}
function ConvertFromTo(sourceForm, targetForm) {
  var propIndex;
  var sourceIndex;
  var sourceFactor;
  var targetIndex;
  var targetFactor;
  var result;
  propIndex = document.property_form.the_menu.selectedIndex;
  sourceIndex = sourceForm.unit_menu.selectedIndex;
  sourceFactor = factor[propIndex][sourceIndex];
  targetIndex = targetForm.unit_menu.selectedIndex;
  targetFactor = factor[propIndex][targetIndex];
  result = sourceForm.unit_input.value;
  if (property[propIndex] == "Temperatur") {
    result = parseFloat(result) + tempIncrement[sourceIndex];
  }
  result = result * sourceFactor;
  result = result / targetFactor;
  if (property[propIndex] == "Temperatur") {
    result = parseFloat(result) - tempIncrement[targetIndex];
  }
  targetForm.unit_input.value = result;
}
window.onload = function(e) {
  FillMenuWithArray(document.property_form.the_menu, property);
  UpdateUnitMenu(document.property_form.the_menu, document.form_A.unit_menu);
  UpdateUnitMenu(document.property_form.the_menu, document.form_B.unit_menu)
}
document.getElementByClass('numbersonly').addEventListener('keydown', function(e) {
  var key = e.keyCode ? e.keyCode : e.which;
  if (!([8, 9, 13, 27, 46, 110, 190].indexOf(key) !== -1 ||
      (key == 65 && (e.ctrlKey || e.metaKey)) ||  
      (key == 67 && (e.ctrlKey || e.metaKey)) || 
      (key == 86 && (e.ctrlKey || e.metaKey)) || 
      (key >= 35 && key <= 40) || 
      (key >= 48 && key <= 57 && !(e.shiftKey || e.altKey)) ||
      (key >= 96 && key <= 105)
      (key == 190)
    )) e.preventDefault();
});
</script>
```

### Benutzung:
1.  Gehe zu:  Inhalt  ➞  Boxen
2.  Klicke auf  + Box hinzufügen  und wähle als Inhalt HTML aus.
3.  Füge den nachfolgenden Quellcode ein und passe diesen nach deinen Wünschen an.
