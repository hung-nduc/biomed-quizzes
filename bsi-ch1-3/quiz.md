---
title: "Biomedical Sensors and Instrumentation: Chapters 1-3"
description: "Sensor characteristics, physical principles of sensing, and pressure measurement (direct and indirect). Built from the lecture slides in content/."
id: bsi-ch1-3
feedback: instant
shuffle_choices: true
tags: [sensors, biomedical, pressure]
---

# Chapter 1: Sensor characteristics

## In the narrow definition used in the course, what does a sensor produce in response to a stimulus? {type=single id=c1-narrow-def tags=ch1-definitions}

- [ ] A mechanical displacement proportional to the stimulus
- [ ] A change of energy form with maximum conversion efficiency
- [x] An electrical signal (voltage, current, charge, frequency, digital code...)
- [ ] An ion-transport signal of electrochemical character

::: explanation
Ch1 slide 10: "a sensor is a device that receives a stimulus and responds with an electrical signal". Ion transport is how *natural* (living) sensors respond (slide 9). Energy conversion with a focus on efficiency describes a *transducer* (slide 11), and producing motion describes an *actuator* (slide 12).
:::

## Match each term to its description. {type=matching points=2 id=c1-terms tags=ch1-definitions}

- Transducer :: Converts one type of energy into another
- Actuator :: Converts energy, normally into mechanical motion, to make a system move
- Measurand :: The stimulus, stressing its quantitative character
- Natural sensor :: Responds with electrochemical (ion-transport) signals
- :: Converts an electrical signal into a digital code

::: explanation
Ch1 slides 9-12. A transducer is any energy converter; an actuator is the output-side converter that moves something; "measurand" is the term used for the stimulus when the quantity being measured is stressed; natural sensors live in organisms and signal by ion transport. The leftover option describes an ADC, which is not one of the defined terms.
:::

## According to the classification on the slides, which pair is correct? {type=single id=c1-active-passive tags=ch1-definitions}

- [ ] Piezoelectric sensor: active; thermistor: passive
- [x] Piezoelectric sensor: passive; thermistor: active
- [ ] Both are passive, because neither needs a reference
- [ ] Both are active, because both output a voltage

::: explanation
Ch1 slide 14 classifies by the *need of an excitation signal*. A piezoelectric sensor generates charge from the force itself, so it needs no excitation (passive). A thermistor changes resistance, which can only be read by driving a current or voltage through it (active). The "reference" criterion is a different axis (absolute vs relative).
:::

## A linear displacement sensor has ideal sensitivity 1 mV/mm. At a true input of 10 mm it outputs 10.5 mV. What is its relative inaccuracy over the 10 mm range, in percent? {type=numeric id=c1-accuracy tags=ch1-static}

```answer
value: 5
tolerance: 0.1
unit: "%"
```

::: explanation
Ch1 slide 23. The reading converted back to input is $s_x = S/b = 10.5\ \text{mm}$, so the absolute error is 0.5 mm. Relative to the 10 mm span that is $0.5/10 = 5\%$. Answering 0.5 gives the absolute error in mm, not the percentage.
:::

## What is the sensitivity of a sensor with transfer function $S = f(s)$? {type=single id=c1-sensitivity tags=ch1-static}

- [ ] The ratio $S/s$ at full scale only
- [ ] The smallest increment of stimulus that can be sensed
- [ ] The difference between the outputs at maximum and minimum input
- [x] The derivative $dS/ds$ evaluated at the operating point

::: explanation
Ch1 slide 19: $b = dS/ds$ at $s_0$; for a linear function $S = a + bs$ it is the constant slope $b$. The smallest detectable increment is *resolution* (slide 32), and the output difference between maximum and minimum input is the *full-scale output* (slide 22).
:::

## Match each static characteristic to its definition. {type=matching points=3 id=c1-static-match tags=ch1-static}

- Hysteresis :: Output differs at the same input depending on the direction of approach
- Dead band :: Output stays near one value over a range of inputs
- Saturation :: Further increase in stimulus no longer gives the expected output
- Repeatability :: Failure to give the same output under identical conditions in two calibration cycles
- Resolution :: Smallest increment of stimulus that can be sensed
- :: Maximum deviation of the real transfer function from a straight line

::: explanation
Ch1 slides 26-32. Hysteresis comes from friction and structural changes; dead band is an insensitive zone; saturation is the top end of the useful range; repeatability errors come from thermal noise, charge build-up, material plasticity; resolution is the step size. The distractor is the definition of *nonlinearity* (slide 27).
:::

## Which methods can be used to choose the reference straight line when stating a sensor's nonlinearity? {type=multi id=c1-nonlin tags=ch1-static}

- [x] Terminal points
- [x] Least squares
- [ ] Peak-to-peak averaging of hysteresis loops
- [x] Tangent at a point
- [ ] Dead-band centring

::: explanation
Ch1 slide 27 lists terminal points, least squares, tangent and independent linearity. Hysteresis averaging and dead-band centring are not line-fitting methods; they relate to other characteristics.
:::

## A sensor with output impedance $Z_{out}$ is connected in voltage mode (parallel) to an amplifier with input impedance $Z_{in}$. What keeps the loading error small? {type=single id=c1-zout tags=ch1-static}

- [x] $Z_{in} \gg Z_{out}$
- [ ] $Z_{in} \ll Z_{out}$
- [ ] $Z_{in} = Z_{out}$ (matched)
- [ ] The ratio does not matter for a voltage connection

::: explanation
Ch1 slide 33: $V = V_s / (1 + Z_{out}/Z_{in})$, so $V \to V_s$ only when $Z_{in} \gg Z_{out}$. Small $Z_{in}$ is what a *current* (series) connection wants, and impedance matching maximises power, not voltage fidelity.
:::

## Calibration error is random and averages out over repeated measurements. {type=truefalse id=c1-calib tags=ch1-static}

```answer
value: false
```

::: explanation
Ch1 slide 25: calibration error is the inaccuracy allowed when the sensor is calibrated in the factory; it is added to all real transfer functions, so it is *systematic*, not random. It can also be non-uniform over the range, depending on the type of calibration error.
:::

## Match each dynamic characteristic to its meaning. {type=matching points=2 id=c1-dynamic tags=ch1-dynamic}

- Warm-up time :: From applying excitation until the sensor works within its specified accuracy
- Frequency response :: How fast the sensor reacts to a change in the stimulus
- Phase shift :: How far the output lags behind the stimulus change
- Damping :: Progressive suppression of oscillation in a higher-than-first-order sensor
- :: Long-term irreversible change from ageing of materials

::: explanation
Ch1 slides 36-37. The distractor describes *long-term stability* (slide 38), which is an environmental/ageing property, not a dynamic one.
:::

## Why should a sensor's operating frequency range be kept well away from its resonant frequency? {type=single id=c1-resonance tags=ch1-dynamic}

- [ ] Because the sensor stops producing any output at resonance
- [x] Because near resonance the output rises considerably and no longer follows the stimulus faithfully
- [ ] Because resonance increases the dead band of the sensor
- [ ] Because resonance only matters for passive sensors

::: explanation
Ch1 slide 36: at the resonant frequency the output signal increases considerably, so the sensor would report a stimulus that is larger than the real one. The output does not vanish, and the effect is a dynamic one, unrelated to dead band or to the active/passive class.
:::

## Match each stability or environmental term to its description. {type=matching points=2 id=c1-stability tags=ch1-reliability}

- Short-term stability :: Changes over minutes, hours or days; another term for repeatability
- Long-term stability :: Ageing of materials over months and years, usually unidirectional
- Storage conditions :: Non-operating limits that do not permanently alter performance
- Self-heating :: Excitation power absorbed by the sensor changes its temperature
- :: Output stays constant over an input range

::: explanation
Ch1 slides 38-39. The distractor is the dead band (slide 31). Self-heating matters most for active sensors such as thermistors, because the excitation current itself heats them.
:::

## An accelerated life test uses $n = N\left(\dfrac{\Delta T_{max}}{\Delta T_{test}}\right)^{2.5}$. A sensor's normal temperature is 25 °C, its maximum specified temperature is 50 °C, the test cycles up to 100 °C, and it sees 20 000 cycles in its 10-year life. About how many test cycles are needed? {type=numeric id=c1-alt tags=ch1-reliability}

```answer
value: 1283
rel_tolerance: 0.02
unit: cycles
```

::: hint
Both temperature swings are measured from the normal temperature, 25 °C.
:::

::: explanation
Ch1 slides 42-43. $\Delta T_{max} = 50 - 25 = 25$ °C and $\Delta T_{test} = 100 - 25 = 75$ °C, so $n = 20000 \times (1/3)^{2.5} = 20000 / 15.59 \approx 1283$ cycles. Using 50 and 100 directly (ratio 1/2) gives about 3536, which forgets that the swing is measured from the normal temperature.
:::

## Why does the course prefer accelerated life qualification over a calculated MTBF to judge sensor reliability? {type=single id=c1-mtbf tags=ch1-reliability}

- [ ] MTBF cannot be calculated for electronic components
- [ ] MTBF is a direct measure, so it is too strict for sensors
- [ ] Accelerated testing needs no knowledge of the operating cycle
- [x] MTBF reflects reliability only indirectly and misses stresses such as fast temperature changes

::: explanation
Ch1 slides 40-41: MTBF is computed from component failure rates, reflects reliability only indirectly and does not cover impacts such as fast temperature changes. Accelerated life testing emulates the real operating cycle with expanded environmental extremes, compressing years into weeks, and it *does* need the operating profile.
:::

## Uncertainty evaluated by statistical analysis of repeated readings is Type [[A]]; uncertainty evaluated from other information, such as manufacturer's specifications or calibration reports, is Type [[B]]. {type=blanks id=c1-uncert tags=ch1-reliability}

::: explanation
Ch1 slides 45-46. Type A comes from random effects and is evaluated statistically; Type B comes from systematic effects and uses previous data, experience, specifications, calibration data and handbook values. Error is what we actually get; uncertainty is how large we think that error might be.
:::

## Which tests are listed as additional performance tests to uncover packaging and bonding weaknesses? {type=multi id=c1-perf-tests tags=ch1-reliability}

- [x] High temperature and high humidity
- [ ] Measuring the dead band at room temperature
- [x] Mechanical shocks and vibration
- [x] Thermal shock or temperature cycling
- [ ] Repeating the factory calibration

::: explanation
Ch1 slide 44 lists high temperature/humidity (contamination, packaging integrity), shock and vibration (wire bonds, epoxy adhesion), extreme storage and thermal shock/cycling (die bonds, wire bonds, packaging). Dead-band checks and re-calibration measure accuracy, not durability.
:::

# Chapter 2: Physical principles of sensing

## Which effects directly generate an electrical signal from a non-electrical stimulus, without an intermediate conversion step? {type=multi id=c2-direct tags=ch2-principles}

- [x] Thermoelectric (Seebeck) effect
- [ ] Change of resistance in a thermistor
- [x] Piezoelectric effect
- [x] Photoelectric effect
- [ ] Change of capacitance with plate spacing

::: explanation
Ch2 slide 2 names the Seebeck effect, piezoelectricity and the photo effect as direct generators. A thermistor or a variable capacitor changes a *parameter* (R or C), which still has to be read with an excitation signal, so it does not generate a signal by itself.
:::

## What is the triboelectric effect? {type=single id=c2-tribo tags=ch2-principles}

- [ ] Generation of charge in a crystal under mechanical stress
- [x] Separation of electric charge caused by friction or movement of objects
- [ ] An e.m.f. produced at the junction of two different metals
- [ ] A transverse voltage in a conductor carrying current in a magnetic field

::: explanation
Ch2 slide 3: charge separation due to movement, friction of fibres, air turbulence, as when walking on a carpet. The other options are the piezoelectric effect, the Seebeck effect and the Hall effect.
:::

## For a parallel-plate capacitive displacement sensor where the gap $x$ changes, how does the sensitivity $dC/dx$ behave? {type=single id=c2-cap-disp tags=ch2-capacitive}

- [ ] Constant, so the sensor is linear in $x$
- [ ] Proportional to $x$, so it grows as the gap widens
- [x] $\propto 1/x^2$, so it grows as the gap shrinks
- [ ] Independent of the dielectric between the plates

::: explanation
Ch2 slides 10 and 15: $C = \varepsilon_0\varepsilon_r A/x$, so $dC/dx = -\varepsilon_0\varepsilon_r A/x^2$. The response is nonlinear in $x$ and the sensitivity rises at small gaps; $\varepsilon_r$ appears explicitly, so the dielectric does matter.
:::

## Why is a capacitive water-level sensor usually combined with a temperature sensor? {type=single id=c2-water-level tags=ch2-capacitive}

- [ ] The plate area expands with temperature
- [x] The dielectric constant of water depends on temperature
- [ ] Water conducts better when warm, shorting the plates
- [ ] The capacitor heats the water and shifts the level

::: explanation
Ch2 slide 14: the capacitance depends on the height of water *and* on its dielectric constant, which changes with temperature, so a temperature reading is needed to correct the level. Thermal expansion of the plates is negligible in comparison.
:::

## An inductive displacement sensor, unlike a capacitive one, is NOT affected by [[the dielectric constant|dielectric constant|permittivity|the permittivity]] of the surroundings, but it IS affected by nearby magnetic materials. {type=blanks id=c2-inductive tags=ch2-inductive}

::: explanation
Ch2 slide 21. Inductance depends on the magnetic path, so ferromagnetic objects nearby disturb it, while the medium's permittivity (which drives a capacitive sensor) has no effect.
:::

## In an LVDT, why are the two secondary coils connected in series opposition? {type=single id=c2-lvdt tags=ch2-inductive}

- [ ] To double the output voltage at the centre position
- [ ] To remove the need for an AC excitation
- [ ] To make the self-inductance proportional to displacement
- [x] To obtain a wider range of linearity, with near-zero output at the centre

::: explanation
Ch2 slide 24: one primary, two secondaries connected oppositely to achieve a wider linear range. At the centre the two induced voltages cancel; moving the high-permeability core unbalances them. The LVDT still needs AC excitation and more complex signal processing (demodulation).
:::

## Which statements about inductive displacement sensors are on the slides? {type=multi id=c2-inductive-multi tags=ch2-inductive}

- [x] A self-inductance sensor's inductance is not linearly proportional to displacement
- [x] Self-inductance sensors need low power and give large changes, so they suit telemetry
- [ ] Mutual-inductance sensors give an output that is linear in coil separation
- [x] Mutual-inductance sensors are excited at the frequency where the secondary coil resonates
- [ ] An LVDT needs simpler signal processing than a potentiometer

::: explanation
Ch2 slides 22-24. The mutual-inductance output is a *nonlinear* function of separation, and the excitation frequency is chosen so the secondary resonates for maximum output (used for cardiac and vessel dimensions, infant respiration). The LVDT needs *more* complex processing.
:::

## A strain gauge's gauge factor is $G = \dfrac{\Delta R/R}{\Delta L/L} = 1 + 2\nu + \dfrac{\Delta\rho/\rho}{\varepsilon}$. Why does a semiconductor gauge have a much larger G than a metal one? {type=single id=c2-gauge tags=ch2-resistive}

- [ ] Its Poisson's ratio is much larger than that of metal
- [x] Its resistivity itself changes strongly with strain (piezoresistive effect)
- [ ] It is thinner, so its length changes more
- [ ] Semiconductors are bonded with foil, metals are not

::: explanation
Ch2 slide 30 and Ch3 slide 21. For metals the geometric terms $1 + 2\nu$ dominate, giving $G \approx 2$. In silicon the $\Delta\rho/\rho$ term (piezoresistance) dominates, giving $G$ from about $-100$ to $+140$. Poisson's ratio is at most 0.5 for any material, so it cannot explain the difference.
:::

## A wire-wound potentiometer used as a displacement sensor has a resolution set by... {type=single id=c2-pot tags=ch2-resistive}

- [ ] the excitation voltage
- [ ] the wiper's inertia
- [x] the spacing between wire turns
- [ ] whether it is excited by DC or AC

::: explanation
Ch2 slide 29: the wiper moves in steps from turn to turn, so the resolution depends on wire spacing. It can be excited by DC or AC and is linear to about 0.01% FS; friction and inertia affect its *dynamic* distortion, not its resolution.
:::

## The piezoelectric effect is reversible: applying a voltage to the crystal makes it deform. {type=truefalse id=c2-piezo-rev tags=ch2-piezo-hall}

```answer
value: true
```

::: explanation
Ch2 slide 33 asks what an applied voltage does: it produces a mechanical strain (the converse piezoelectric effect), which is how piezo actuators and ultrasound transmitters work. Stress produces opposite charges on opposite faces; voltage produces deformation.
:::

## For a piezoelectric sensor with induced charge $q = kf$, the output voltage across its electrodes is... {type=single id=c2-piezo-v tags=ch2-piezo-hall}

- [x] $v = kf/C$, where $C = \varepsilon_0\varepsilon_r A/l$ is the sensor capacitance
- [ ] $v = kfC$
- [ ] $v = k/(fC)$
- [ ] $v = kf$, independent of the electrode geometry

::: explanation
Ch2 slide 35: the crystal with its electrodes is a capacitor, so $v = q/C = kf\,l/(\varepsilon_0\varepsilon_r A)$. The voltage therefore depends on electrode area and thickness, not only on the force.
:::

## The Hall voltage $V_H = h\,i\,B\sin\alpha$ can be positive or negative for the same current and field direction. Why? {type=single id=c2-hall tags=ch2-piezo-hall}

- [ ] Because $\sin\alpha$ changes sign when the plate heats up
- [ ] Because the Hall coefficient depends on the strip's length only
- [ ] Because AC current is always used
- [x] Because the charge carriers can be electrons or holes, depending on the material

::: explanation
Ch2 slide 38: $H = 1/(Ncq)$ and the carriers may be negative (electrons) or positive (holes) depending on crystalline structure, so the Hall effect can be negative or positive. The coefficient depends on material, geometry (active area) and temperature.
:::

## Match each thermocouple law to its statement. {type=matching points=2 id=c2-tc-laws tags=ch2-thermal}

- Homogeneous circuit :: No current can be maintained in a circuit of a single metal by heat alone
- Intermediate metal :: The total e.m.f. of unlike metals all at the same temperature is zero
- Intermediate temperature :: $E(T_1,T_3) = E(T_1,T_2) + E(T_2,T_3)$
- :: The e.m.f. is proportional to the square of the junction current

::: explanation
Ch2 slide 43. These laws let you insert copper leads and meters into a thermocouple circuit and use a reference junction at a known temperature. The distractor mixes up thermoelectric e.m.f. with Joule heating.
:::

## A platinum resistance thermometer follows $R = R_0(1 + \alpha T + \beta T^2)$ with a small negative $\beta$. Over a short temperature range, what is the usual approximation? {type=single id=c2-rtd tags=ch2-thermal}

- [ ] Resistance falls exponentially with temperature
- [x] Resistivity is linear in temperature: $\rho = \rho_0[1 + \alpha(T - T_0)]$
- [ ] Resistance is constant and only the e.m.f. changes
- [ ] Resistance is proportional to $T^{2.5}$

::: explanation
Ch2 slide 45: over a short range the resistivity changes linearly with temperature; the quadratic term only matters over wide ranges. An exponential law describes NTC semiconductor thermistors, not platinum.
:::

## Human hearing covers sound from about 20 Hz to [[20000|20 000|20,000|20 kHz|20kHz]] Hz; sound above that is called [[ultrasound]]. {type=blanks id=c2-sound tags=ch2-principles}

::: explanation
Ch2 slide 46. Sound is a longitudinal mechanical wave; below 20 Hz is infrasound and above 20 kHz is ultrasound, the band used in medical imaging and Doppler blood-pressure methods (Ch3 Part 2).
:::

## Match each sensor element to the order of its dynamic model. {type=matching points=2 id=c2-order tags=ch2-dynamic-models}

- Mass-spring-damper accelerometer :: Second order
- Thermal element with heat capacity C and thermal resistance R :: First order
- Ideal potentiometer with no inertia :: Zero order
- :: Third order

::: explanation
Ch2 slides 52-54. The accelerometer obeys $M\ddot{x} + b\dot{x} + kx = -M\ddot{y}$ (second order). A thermal element obeys $dT/dt + T/(RC) = \dots$ (first order, one storage element). A purely resistive sensor responds instantly, $S(t) = G\,s(t)$ (zero order).
:::

## Why are mechanical, thermal and electrical analogies useful in sensor design? {type=single id=c2-analogy tags=ch2-dynamic-models}

- [ ] They prove that every sensor element is linear
- [ ] They remove the need to model the sensor's interface
- [x] Any element can become an equivalent circuit solved by Kirchhoff's laws
- [ ] They replace calibration of the real sensor in the field

::: explanation
Ch2 slide 56: dynamic behaviour of the three kinds of element is analogous, so mass/heat capacity, friction/thermal resistance and spring can be mapped to circuit elements and analysed with circuit tools. This helps model the sensor's interface with the object and environment, but it does not replace calibration or make sensors linear.
:::

# Chapter 3 Part 1: Pressure quantities and direct measurement

## Convert a systolic pressure of 120 mmHg to kPa. {type=numeric id=c3-units tags=ch3-quantities}

```answer
value: 16
tolerance: 0.1
unit: kPa
```

::: explanation
Ch3 slide 2: 1 mmHg = 133.322 Pa, so 120 × 133.322 Pa = 15 999 Pa ≈ 16.0 kPa. Using 1 cmH₂O = 98.07 Pa by mistake would give about 11.8 kPa.
:::

## A patient's pressure is 120/80 mmHg. Estimate the mean arterial pressure with the formula from the slides. {type=numeric id=c3-map tags=ch3-quantities}

```answer
value: 93.3
tolerance: 0.5
unit: mmHg
```

::: explanation
Ch3 slide 4: $MAP \approx (2\,DP + SP)/3 = (160 + 120)/3 = 93.3$ mmHg. Diastole is weighted twice because the heart spends about two thirds of the cycle in diastole; the simple average (100 mmHg) overestimates it.
:::

## Match each clinical pressure to what it is used to estimate. {type=matching points=3 id=c3-pressures tags=ch3-quantities}

- Pulmonary wedge pressure :: Left atrial pressure
- Central venous pressure :: Venous blood volume and vein elasticity
- dp/dt of left ventricular pressure :: Force developed at the start of contraction
- Arterial pulse pressure (SP - DP) :: Properties of the heart and arterial system
- Intraocular pressure above 25 mmHg :: Glaucoma
- :: Peripheral resistance, measured directly by a cuff

::: explanation
Ch3 slides 4-9. Wedge pressure sits between capillary and left atrial pressure; CVP indexes venous volume and elasticity; LV dp/dt reflects contractile force; pulse pressure reflects heart and arterial properties; IOP above 3.3 kPa (25 mmHg) points to glaucoma. Peripheral resistance is *estimated* as MAP divided by cardiac output, not measured by a cuff.
:::

## Why is pulmonary arterial pressure much lower than systemic arterial pressure? {type=single id=c3-pulm tags=ch3-quantities}

- [ ] The right ventricle contracts more slowly
- [ ] Pulmonary blood has lower density
- [ ] The kinetic energy of blood is larger in the pulmonary artery
- [x] The pulmonary circulation's resistance is about 1/4 of the systemic resistance

::: explanation
Ch3 slide 5. With a quarter of the resistance, the same flow needs much less pressure. Very high pulmonary pressure suggests disease such as pulmonary stenosis or a ventricular septal defect, which calls for catheterization.
:::

## In the pulmonary artery the kinetic-energy term is about 0.4 kPa (3 mmHg) while the mean pressure is 2.7 kPa (20 mmHg). About what percentage of the measured pressure is this? {type=numeric id=c3-kinetic tags=ch3-quantities}

```answer
value: 15
tolerance: 1
unit: "%"
```

::: explanation
Ch3 slide 8: 0.4/2.7 ≈ 14.8%, or 3/20 = 15%. Compare the aorta, where 0.5 kPa is only about 3% of 16 kPa. So the direction of the catheter opening (upstream, side or downstream, Bernoulli) matters far more in the pulmonary artery.
:::

## How is intrapleural pressure usually obtained, given that there is almost no free fluid in the pleural space? {type=single id=c3-pleural tags=ch3-quantities}

- [x] With a balloon placed in the oesophagus
- [ ] With a saline-filled catheter inserted into the pleural space
- [ ] With a cuff around the chest
- [ ] From the central venous pressure

::: explanation
Ch3 slide 10: with no appreciable fluid, a fluid-filled catheter has nothing to couple to, so an oesophageal balloon's pressure is used instead. Mouth pressure sometimes substitutes for *intratracheal* pressure.
:::

## Which site's pressure changes least with posture, so that it serves as the reference level for blood pressure? {type=single id=c3-reference tags=ch3-reference}

- [ ] The brachial artery at heart level
- [x] The right atrium
- [ ] The left ventricle
- [ ] The femoral vein

::: explanation
Ch3 slides 12-14. Intrathoracic pressure stays close to atmospheric whatever the posture, so the external pressure on the central veins and right atrium is stable. The external reference level is the 4th intercostal space at the costal cartilage junction, about 10 cm from the back (half the antero-posterior chest diameter).
:::

## A fluid-filled catheter with an external sensor at the reference level reads the reference-level pressure exactly, whatever the height of the catheter tip. {type=truefalse id=c3-ref-density tags=ch3-reference}

```answer
value: false
```

::: explanation
Ch3 slide 15: it is convenient but not precisely accurate, because the fluid in the catheter (saline, 1.009 g/cm³) and blood (1.055 g/cm³) differ in density, so the hydrostatic columns do not cancel exactly. For CVP in moving patients a differential measurement is used.
:::

## A catheter is labelled 6 F. About what is its outer diameter? {type=numeric id=c3-french tags=ch3-direct-sensors}

```answer
value: 2
tolerance: 0.1
unit: mm
```

::: explanation
Ch3 slide 17: 1 F = 0.33 mm outer diameter, so 6 F ≈ 2 mm. The French scale gives the *outer* diameter; the lumen is smaller.
:::

## For geometrically similar diaphragms of the same material, the volume displacement is $\Delta V \propto (1-\mu^2)R^6\Delta P/(Et^3)$. If $R/t$ is kept constant and the radius is halved, by what factor does $\Delta V$ fall? {type=numeric id=c3-diaphragm tags=ch3-direct-sensors}

```answer
value: 8
tolerance: 0
unit: times
```

::: explanation
Ch3 slides 19-20. With $t \propto R$, $R^6/t^3 \propto R^3$, so halving R divides $\Delta V$ by $2^3 = 8$ while strain (and so sensitivity) stays the same. Less volume displacement means a stiffer sensor and better dynamic response, which is why small micromachined sensors are attractive.
:::

## The catheter-sensor system behaves as a resonant (second-order) system. Which three physical properties form it? {type=multi id=c3-resonant tags=ch3-catheter-dynamics}

- [x] Elasticity (elastance) of the sensor
- [x] Flow resistance of the catheter
- [x] Inertia of the fluid in the catheter
- [ ] Time lag of the pressure wave along the catheter
- [ ] Electrical resistance of the strain gauge

::: explanation
Ch3 slide 26: elastance acts as a spring, flow resistance as a damper, fluid mass as inertia. The transit time lag (about 2.5 ms per metre) is real but insignificant; distortion from resonance is the serious problem.
:::

## Air bubbles are trapped in the sensor dome. What happens to the catheter-sensor system's natural frequency, and why? {type=single id=c3-bubble tags=ch3-catheter-dynamics}

- [ ] It rises, because air is lighter than saline
- [x] It falls, because the bubble lowers the elastance K (the system becomes more compliant)
- [ ] It does not change; only the damping changes
- [ ] It falls, because the bubble increases the catheter's length

::: explanation
Ch3 slides 29-30: $f_0 = \frac{r}{2}\sqrt{K/(\pi\rho l)}$, so lower K gives lower $f_0$. Compressible air makes the system much more compliant. Remedies: fill with boiled saline or 50% alcohol, or flush with CO₂ first.
:::

## For a flat frequency response, the catheter-sensor system needs a natural frequency well above the highest signal frequency and a damping factor h of about... {type=single id=c3-damping tags=ch3-catheter-dynamics}

- [ ] 0.1 to 0.2
- [ ] 0.3 to 0.4
- [x] 0.6 to 0.7
- [ ] 1.5 to 2.0

::: explanation
Ch3 slide 32: $f_0 \gg f_{max}$ and $h = 0.6$ to $0.7$. Lower damping gives a resonant peak (connecting a catheter directly to a sensor usually gives $h \ll 0.6$); much higher damping rolls off the response early.
:::

## A mechanical damper is inserted between catheter and sensor. What does it change? {type=single id=c3-damper tags=ch3-catheter-dynamics}

- [ ] The natural frequency only
- [ ] Both natural frequency and damping, by the same factor
- [ ] Neither; it only removes air bubbles
- [x] The damping factor only, by adding adjustable flow resistance

::: explanation
Ch3 slide 34: it is a variable flow resistance c. Since r and K are unchanged, $f_0$ stays the same and only $h$ changes. Other fixes are choosing catheter size, filter/compensation circuits and numerical (Fourier) correction.
:::

## Which are disadvantages of a catheter-tip pressure sensor compared with an external sensor connected by a fluid-filled catheter? {type=multi id=c3-tip tags=ch3-tip-implant}

- [x] Inconvenient to recalibrate
- [ ] Time delay of the pressure wave
- [x] Fragile
- [x] Expensive
- [ ] Needs saline injection

::: explanation
Ch3 slide 37. The tip sensor has no time delay, a flat response up to several kHz, needs no saline and is less affected by catheter motion; its drawbacks are recalibration, fragility and cost.
:::

## Why must an implantable pressure sensor for long-term monitoring be an absolute pressure sensor? {type=single id=c3-implant tags=ch3-tip-implant}

- [x] It has no connection to the atmosphere, so it must compare against its own sealed reference (vacuum) cavity
- [ ] Absolute sensors are more sensitive than relative ones
- [ ] Relative sensors cannot be made with IC technology
- [ ] Body fluids damage the reference port of a relative sensor within hours

::: explanation
Ch3 slides 45-47: the implanted unit is isolated (often with a radio transmitter), so there is no atmospheric port. The reference vacuum cavity can be formed by silicon direct bonding and heating to 1100 °C in oxygen, which consumes the trapped oxygen.
:::

# Chapter 3 Part 1 (cont.): Small vessels, collapsible vessels, differential pressure

## In a micropipette-sensor system, reducing the pipette radius (with the same sensor) does what to the natural frequency? {type=single id=c3-pipet tags=ch3-small-collapsible}

- [ ] Raises it, because a smaller pipette holds less fluid
- [ ] Leaves it unchanged
- [x] Lowers it, so a highly rigid sensor or a servo system is needed
- [ ] Lowers the damping, so a damper is needed

::: explanation
Ch3 slides 50-51: as in the catheter case, $f_0 \propto r$ with the sensor's elastance unchanged. Fixes: a highly rigid sensor (minimal diaphragm volume displacement, rigid dome, little and incompressible fluid, no bubbles), or Wiederhielm's servo-controlled system.
:::

## Put the operation of Wiederhielm's servo-controlled micropipette system in order. {type=ordering points=2 id=c3-servo tags=ch3-small-collapsible}

1. The pipette is filled with concentrated NaCl (0.5-2 mol/L)
2. A pressure difference makes fluid flow in or out at the tip, changing the pipette's electrical resistance
3. The Wheatstone bridge detects the imbalance in pipette resistance
4. The driver unit generates a counter pressure that restores the resistance
5. An ordinary sensor on the counter-pressure unit reads the pressure

::: explanation
Ch3 slides 53-55. Concentrated saline (3 to 6 times plasma) gives a pipette resistance that is very sensitive to which fluid fills the tip. Keeping that resistance constant by counter pressure keeps the pressure difference constant (about 0.013 kPa), so the counter pressure tracks the vessel pressure, with nearly the same frequency response for a wide range of pipette sizes, down to 1 µm.
:::

## For sphincter pressure in the oesophagus, anus or urethra, which method is described as more common than the balloon catheter? {type=single id=c3-perfused tags=ch3-small-collapsible}

- [ ] An open-tipped catheter without perfusion
- [ ] A wick-in needle
- [x] A constantly perfused side-hole catheter driven by a low-compliance pump
- [ ] An implanted porous capsule

::: explanation
Ch3 slide 58: a small flow (typically 0.3-2 ml/min) is perfused; the sensor reads the pressure needed to keep it flowing past the sphincter. An open-tipped catheter fails because the collapsed wall blocks it. Wick-in needles and capsules are for interstitial pressure.
:::

## Why is a glass syringe pump or pneumohydraulic pump preferred for perfused catheters? {type=single id=c3-pump tags=ch3-small-collapsible}

- [ ] They deliver a much higher perfusion flow rate
- [x] Low compliance: better frequency response, fewer flow artifacts
- [ ] They remove the need for a separate pressure sensor
- [ ] They keep the perfusate sterile during long recordings

::: explanation
Ch3 slides 58-60: response is limited by perfusion rate and pump compliance. A glass syringe has about 1/6 the compliance of a plastic one; a pneumohydraulic pump (high-pressure gas chamber plus flow resistance) gives a nearly constant flow: a 13.3 kPa rise reduces flow by only 1.3% at 1000 kPa drive.
:::

## Which techniques are listed for interstitial fluid pressure? {type=multi id=c3-interstitial tags=ch3-small-collapsible}

- [x] Chronically implanted perforated capsule
- [x] Wick-in needle
- [ ] Constantly perfused side-hole catheter
- [x] Micropipette with servo-controlled counter pressure
- [ ] Catheter-tip fibre-optic sensor

::: explanation
Ch3 slides 61-64 list perforated capsules, porous capsules, micropipettes and the wick-in needle. Each keeps saline in equilibrium with the gel-trapped interstitial fluid. Perfused catheters are for sphincters, and catheter-tip sensors for blood vessels.
:::

## Implanted capsules are inadequate for pressure changes that happen in less than a few hours. {type=truefalse id=c3-capsule tags=ch3-small-collapsible}

```answer
value: true
```

::: explanation
Ch3 slide 65: capsule readings are easily influenced by changes in colloid osmotic pressure; during acute dehydration only capsular pressures changed, unlike wick and needle readings. They are still useful for diagnosing compartment syndrome.
:::

## Why is it better to measure a small differential pressure directly with one differential sensor than to subtract the readings of two independent sensors? {type=single id=c3-diff tags=ch3-differential}

- [ ] Two separate sensors cannot be sampled at the same time
- [ ] A differential sensor never needs any calibration
- [x] Small zero and gain drifts in each become large errors in the difference
- [ ] Two sensors double the transmission time lag

::: explanation
Ch3 slide 66: when the difference is small compared with each pressure's variation, tiny sensitivity or zero changes in either sensor dominate the result. A single diaphragm with one pressure on each side measures the difference itself.
:::

## Why do some differential pressure sensors for respiratory gases use two diaphragms? {type=single id=c3-two-diaph tags=ch3-differential}

- [ ] To double the sensitivity
- [ ] To measure two different gases at once
- [ ] To make the sensor linear at high pressure
- [x] To keep the sensing element away from moist, corrosive gases

::: explanation
Ch3 slides 67-68: many capacitive differential sensors are only for dry, non-corrosive, non-condensable gases, so they are unsuited to humid breath. With two diaphragms the force set by the differential pressure moves a structure whose displacement is read by capacitance electrodes sealed away from the gas.
:::

# Chapter 3 Part 2: Indirect pressure measurement

## According to the British Hypertension Society, the cuff bladder should have... {type=single id=c3-bhs tags=ch3-cuff}

- [ ] width ≥ 20% and length ≥ 40% of arm circumference
- [x] width ≥ 40% and length ≥ 80% of arm circumference
- [ ] width = arm diameter and length = 2 × width
- [ ] width ≥ 80% and length ≥ 100% of arm circumference

::: explanation
Ch3 Part 2 slide 4. The American Heart Association gives width ≥ 40% of circumference (or 20% wider than the diameter) and length = 2 × width. The bladder must be large enough to transmit its pressure fully to the artery.
:::

## A cuff that is too narrow for the patient's arm (width-to-diameter ratio below about 1.2) tends to give blood pressure readings that are... {type=single id=c3-small-cuff tags=ch3-cuff}

- [x] falsely high
- [ ] falsely low
- [ ] accurate, but with more noise
- [ ] accurate for systolic, but not diastolic only

::: explanation
Ch3 Part 2 slides 6-7: a narrow cuff does not transmit its pressure to the centre of the arm, so more cuff pressure is needed to occlude the artery and readings come out high. This is why 12 × 23 cm bladders are recommended for normal arms and 14 × 38 cm for obese arms.
:::

## In the auscultatory method, systolic pressure is the cuff pressure when clear tapping Korotkoff sounds first [[appear|are heard|start]], and diastolic pressure is the cuff pressure when the sounds [[disappear|stop|vanish]]. {type=blanks id=c3-korotkoff tags=ch3-cuff}

::: explanation
Ch3 Part 2 slide 8: the sounds exist only while cuff pressure is between systolic and diastolic. Their origin (turbulence, wall flutter, water hammer, cavitation...) is not completely understood, but the method is widely accepted.
:::

## In the oscillometric method, the cuff pressure at which the pressure oscillations reach maximum amplitude corresponds to the... {type=single id=c3-osc tags=ch3-oscillometric-doppler}

- [ ] systolic pressure
- [ ] diastolic pressure
- [x] mean arterial pressure
- [ ] pulse pressure

::: explanation
Ch3 Part 2 slide 11: the arterial volume pulsation, and hence the cuff oscillation, is largest when cuff pressure is close to MAP; comparisons with direct measurement agree closely. Systolic pressure can also be read, while diastolic must be *estimated*, for example $P_d = (P_m - kP_s)/(1-k)$.
:::

## Which are advantages of the oscillometric method over auscultation? {type=multi id=c3-osc-adv tags=ch3-oscillometric-doppler}

- [x] The maximum oscillation amplitude can be detected objectively and easily
- [x] It can be automated
- [ ] It measures diastolic pressure directly
- [x] It can use cuff pressure or a plethysmogram (mechanical, photoelectric or impedance)
- [ ] Clinicians are more familiar with the mean pressure it gives

::: explanation
Ch3 Part 2 slides 14-15. The drawbacks are the reverse: diastolic must be estimated, and clinicians are used to systolic and diastolic values, not mean pressure.
:::

## Put the Doppler wall-motion method for blood pressure in order as the cuff deflates. {type=ordering points=2 id=c3-doppler tags=ch3-oscillometric-doppler}

1. The cuff is inflated above systolic pressure, so the artery stays closed
2. The first opening signal appears: cuff pressure = systolic pressure
3. Each cycle shows an opening and a closing Doppler signal
4. The closing signal falls later and later in the cycle
5. The closing signal merges with the next cycle's opening signal: cuff pressure = diastolic pressure

::: explanation
Ch3 Part 2 slides 16-17. The wall moves at each opening and closing, shifting the Doppler frequency. The method works even in shock, when Korotkoff sounds are inaudible, but the narrow ultrasound beam makes it sensitive to probe movement.
:::

## In the vascular unloading (Peňáz) method for continuous finger pressure, what does the closed-loop servo do? {type=single id=c3-unloading tags=ch3-unloading}

- [ ] Keeps cuff pressure constant at mean arterial pressure
- [ ] Inflates and deflates the cuff once per minute
- [x] Adjusts cuff pressure instantly so the arterial volume stays clamped at its unloaded level
- [ ] Keeps the plethysmogram amplitude at its maximum during every beat

::: explanation
Ch3 Part 2 slides 20-21. In open loop the DC cuff pressure is set where the plethysmogram amplitude is largest (wall unloaded). In closed loop, with high gain, any volume change is cancelled at once, so cuff pressure equals intra-arterial pressure continuously. Peňáz used a water-filled cuff and Yamakoshi an air-filled one.
:::

## On the upper arm, the unloading method uses Doppler blood velocity instead of photoplethysmography and holds the brachial velocity at about [[3]] cm/s. {type=blanks id=c3-upper-arm tags=ch3-unloading}

::: explanation
Ch3 Part 2 slides 23-24: photoplethysmography is hard to use in the upper arm, so a range-gated Doppler probe is used. Holding velocity at about 3 cm/s keeps the artery partially occluded and its wall unloaded. The site is closer to the central artery but cannot be used for long periods; alternating arms is suggested.
:::

## In the applanation method, internal pressure equals force divided by contact area ($P = f/a$) only when... {type=single id=c3-applanation tags=ch3-applanation}

- [ ] the contact area is larger than the object
- [x] the elastic force from deforming the surface layer at the edge of contact is negligible
- [ ] the force is applied as a short air pulse
- [ ] the object's internal pressure is below atmospheric

::: explanation
Ch3 Part 2 slide 26. A guard ring coplanar with the measuring surface takes up the edge bending forces, so the centre measures only the internal pressure. The force must be measured without displacement, so a servo or an extremely low-compliance force sensor is needed (slide 27).
:::

## Match each tonometer to its key feature. {type=matching points=3 id=c3-tonometers tags=ch3-applanation}

- Goldmann :: Fluorescein and blue light; force adjusted until a standard pattern appears
- Halberg :: Constant gravitational force; diameter of flattened area measured
- Mackay-Marg :: 1.5 mm servo plunger in a guard ring; first dip in force gives IOP
- Quartz crystal :: Very low-compliance force sensor instead of a servo
- Noncontact :: Air pulse of rising force; reflected light peaks at applanation
- :: Rod indentation depth read on a scale

::: explanation
Ch3 Part 2 slides 28-34. The distractor is the older *indentation* method, which is less accurate than applanation. Mackay-Marg contact lasts about 1 s, so no anaesthetic is needed. Noncontact readings rise slightly with corneal thickness.
:::

## In a Mackay-Marg tonometer, why does the plunger force show a dip at the moment that gives intraocular pressure? {type=single id=c3-mackay tags=ch3-applanation}

- [ ] The plunger's servo saturates and briefly loses control
- [ ] The cornea is momentarily punctured
- [ ] The intraocular pressure drops as aqueous humour escapes
- [x] When the flattened area exceeds the plunger, the guard ring takes the corneal bending force

::: explanation
Ch3 Part 2 slide 31. Force rises while the flattened area grows to cover the plunger; then the guard ring carries the bending force at the boundary and the plunger force dips; further indentation raises IOP and force again. The first dip is pure pressure × plunger area.
:::

## Match each indirect measurement to the site or method used. {type=matching points=2 id=c3-indirect-sites tags=ch3-applanation}

- Intracranial pressure in newborns :: Applanation or oscillometry through the anterior fontanelle
- Arterial tonometry :: Radial artery, waveform calibrated by auscultation
- Intra-amniotic pressure :: Spring-supported applanation sensor with guard ring on the abdomen
- :: Balloon in the oesophagus

::: explanation
Ch3 Part 2 slides 35-40. The fontanelle gives a soft window to the skull (APT-16 applanation sensor correlated 0.98 with ventricular puncture). Arterial tonometry cannot be quantified alone, so its maximum and minimum are calibrated to auscultatory systolic and diastolic values. The oesophageal balloon is for intrapleural pressure (Part 1).
:::
