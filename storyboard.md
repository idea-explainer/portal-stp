# Chemical Thrust at Electric Efficiency: The Physics Case for Solar-Thermal Rockets

Hook: There are plans on file for 1.2 million satellites — eighty times as many as fly today — and every one of them will have to dodge, reposition, and come down on command. For fifty years there has been an awkward bargain in space: you could push hard and run out of propellant almost immediately, or you could sip propellant and take a year and a half to get anywhere. What we want to understand is how a mirror and a tank of one-dollar-a-kilogram ammonia gets you out of the bargain. And to understand it honestly, we have to begin at the beginning — with force, with momentum, and with what temperature really is.

## Audience

Background: Yale physics undergrad

Assume known:
- calculus
- classical mechanics
- basic thermodynamics
- gen chem
- linear algebra basics

Do not assume:
- graduate QFT
- measure theory
- domain jargon from the paper's subfield

Tone: direct, quantitative, no hand-holding, no pop-science analogies unless they are load-bearing

## Part: The basic building blocks

Lede: Three facts from first-year physics, then the rules of spaceflight they imply. This section ends at the fifty-year problem the paper attacks: an engine could be strong or efficient — never both.

### Force changes velocity {#f-equals-ma}

- concept: newtons-second-law
- requires: none

Teaches: A force produces acceleration, not speed: a = F/m, so force held over time adds up to velocity change.

Caption: Suppose you push on something steadily, out in space where there is nothing to rub against. What happens? It does not just move — it keeps gaining speed the whole time you push. That is Newton's law, \(F = ma\): a force produces not speed but a rate of change of speed. Push on a 500 kg spacecraft with 100 newtons and you get 0.2 m/s of new velocity every second, for as long as you care to push. So an engine is really a machine for accumulating velocity, and the whole question of rocketry is how much velocity change you can afford.

Visual: A 500 kg block on a frictionless horizontal track with a force arrow whose length is proportional to the applied force. A slider sets the force; time runs continuously. Readouts: acceleration a = F/m in m/s², live velocity in m/s, elapsed thrust time in s. A strip chart draws velocity versus time as a straight line whose slope is a. Equation displayed: F = ma.

Interactive:
- variable: applied force on a 500 kg mass
- control: slider
- range: F = 0 to 200 N
- on-screen: The force arrow lengthens, the block accelerates visibly, and the velocity-time line steepens; at F = 0 the block coasts at constant velocity.

Anchor: 100 N on 500 kg gives a = 0.2 m/s² — about 12 m/s of velocity gained per minute of thrusting.

Checks:
- The acceleration readout equals F/500 within 1% at every slider position.
- Doubling the force doubles the slope of the velocity-time line.
- At F = 0 the velocity readout stays constant and the velocity-time line is horizontal (Newton's first law).

### In space, you move by throwing mass {#momentum-recoil}

- concept: conservation-of-momentum
- requires: f-equals-ma

Teaches: Momentum is conserved, so the only way to change your velocity in empty space is to throw mass the other way and keep the recoil.

Caption: Now here is a beautiful thing. An astronaut floating in empty space has nothing whatever to push against — and yet she can move. Let her throw a 1 kg wrench away at 10 m/s: the wrench carries 10 kg·m/s of momentum one way, and she must drift the other way with exactly 10 kg·m/s, because the total was zero before the throw and nature insists it stay zero. She moves slowly — she is a hundred times heavier than the wrench — but she truly moves. A rocket is nothing but this trick done continuously: it throws part of itself overboard, fast, and rides the recoil.

Visual: An astronaut (100 kg) floating against a starfield throws a 1 kg wrench to the left; both drift apart after release. A slider sets the throw speed. Momentum vector arrows over each body scale with |p|. Readouts: wrench momentum (kg·m/s, leftward), astronaut momentum (kg·m/s, rightward), their sum (always 0), and astronaut recoil velocity in m/s.

Interactive:
- variable: speed at which the 1 kg wrench is thrown
- control: slider
- range: v = 1 to 20 m/s
- on-screen: The wrench flies away faster, the astronaut's recoil-velocity readout rises in proportion (v/100), and the two momentum arrows stay equal and opposite.

Anchor: A 1 kg wrench thrown at 10 m/s gives a 100 kg astronaut a recoil of exactly 0.1 m/s.

Checks:
- The two momentum readouts are equal in magnitude and opposite in direction at every slider position, summing to 0.
- Astronaut recoil velocity equals (1 kg × throw speed)/100 kg within 1%.
- Doubling the throw speed doubles the recoil velocity.

### Temperature is molecular speed {#temperature-is-speed}

- concept: kinetic-theory-of-temperature
- requires: none

Teaches: The temperature of a gas measures the average kinetic energy of its molecules, so typical molecular speed grows as the square root of temperature over molecular mass.

Caption: What is temperature, really? If you could look into a gas closely enough you would see the molecules flying about, and temperature is just how energetically they fly: each molecule carries on average kinetic energy \((3/2)kT\), so the typical speed is \(\sqrt{3kT/M}\). Notice there are only two ways to make the molecules go faster — make the gas hotter, or make the molecules lighter. The nitrogen in this room is already doing about 500 m/s; hydrogen at 3,000 K does better than 6,000. Keep those two knobs in mind, because they are the entire secret of the thermal rocket.

Visual: A box of bouncing dots (2D gas) whose speeds scale as √(T/M). A slider sets temperature; three buttons choose the molecule (H₂ M=2, NH₃ M=17, N₂ M=28 g/mol). Readouts: temperature in K and typical molecular speed in m/s computed from √(3kT/M). Equation displayed: ½Mv² ≈ (3/2)kT.

Interactive:
- variable: gas temperature (with molecule selectable)
- control: slider
- range: T = 300 to 3,000 K; molecule buttons: H₂ / NH₃ / N₂
- on-screen: The dots speed up as T rises and the speed readout climbs as √T; switching to a lighter molecule at fixed T makes the dots and the readout jump faster.

Anchor: N₂ at 300 K: typical speed ~500 m/s; H₂ at 3,000 K: ~6,100 m/s.

Checks:
- The speed readout scales as √T: raising T from 750 K to 3,000 K doubles the displayed speed.
- At fixed T, H₂ reads faster than NH₃, which reads faster than N₂ (ordering by 1/√M).
- N₂ at 300 K reads within ~10% of 500 m/s.

### Every maneuver spends from a fixed delta-v budget {#dv-budget}

- concept: delta-v-as-currency
- requires: f-equals-ma, momentum-recoil

Teaches: A spacecraft's fuel gauge reads in velocity change, not distance: coasting is free in space, and every maneuver spends an irreversible slice of a fixed delta-v budget.

Caption: On Earth a full tank means so many miles, because you burn fuel just to keep moving against friction. In space there is no friction: coasting is free, and a satellite will coast forever. What costs is changing your velocity — speeding up, slowing down, turning — so a spacecraft's fuel gauge does not read in miles; it reads in meters per second of velocity change. That is delta-v. Dodging a piece of debris costs about 100 m/s; climbing from low orbit to geostationary costs about 5,000. And when the gauge hits zero, the satellite is not stranded at the roadside — it keeps sailing along whatever path it last had, forever, unable to change it.

Visual: Left: an Earth diagram with three concentric orbit circles and a satellite dot. Right: a vertical 'delta-v budget' bar starting full at 5,000 m/s with a numeric readout. Three buttons fire maneuvers; each click animates the satellite to its new orbit and drains the bar by exactly the maneuver's cost. A running ledger lists each burn and the cumulative total spent.

Interactive:
- variable: maneuver size commanded
- control: buttons
- range: 100 m/s collision-avoidance / 500 m/s reposition / 5,000 m/s LEO-to-GEO transfer
- on-screen: The satellite moves to a new orbit and the budget bar drops by exactly the commanded delta-v; at zero remaining, all buttons gray out and the satellite is labeled 'stranded'.

Anchor: Small reposition ≈ 100 m/s; LEO-to-GEO transfer ≈ 5,000 m/s.

Checks:
- Budget bar decreases by exactly the commanded maneuver size each click (100, 500, or 5,000 m/s).
- Firing two 500 m/s maneuvers leaves the same remaining budget as firing one 1,000 m/s maneuver.
- When remaining budget reaches 0 m/s, maneuver buttons are disabled and the satellite no longer moves.

### Climbing to a higher orbit takes two forward burns {#hohmann-transfer}

- concept: delta-v-as-currency
- requires: f-equals-ma, dv-budget

Teaches: A prograde burn raises the opposite side of the orbit, so climbing to a higher orbit is done with two forward burns — and you arrive moving slower than you started.

Caption: How do you actually climb from low orbit to geostationary? Not by pointing the engine down at the Earth — you fire it forward, twice. Going faster here raises your orbit over there: the first burn, about 2.4 km/s on top of your 7.7, stretches the circle into an ellipse whose far side just kisses GEO altitude. Then you coast uphill for five hours while gravity slows you from 10.1 to 1.6 km/s — exactly like a ball thrown upward — and at the top you fire forward again, about 1.5 km/s, to round the ellipse into a circle. And notice the lovely surprise: two forward burns, 3.9 km/s spent, and you arrive moving slower than you started — 3.1 km/s against 7.7 — because the delta-v bought altitude, not speed.

Visual: Earth at center with two dashed circular orbits (inner LEO, outer GEO, schematic radii). A satellite dot travels the current orbit with a velocity arrow whose length scales with speed. Buttons fire the sequence: 'Burn 1 (prograde)' shows a brief thrust flame trailing behind the velocity arrow and morphs the path into a transfer ellipse tangent to both circles; the satellite then coasts up the ellipse while a speed readout falls; 'Burn 2 (prograde)' at apogee shows the flame again and rounds the path into the GEO circle. Readouts: current speed (km/s), altitude regime label (LEO / transfer / GEO), and running delta-v spent (km/s).

Interactive:
- variable: burn sequence (each burn fired prograde)
- control: buttons
- range: Burn 1: +2.4 km/s at LEO / Burn 2: +1.5 km/s at apogee / reset
- on-screen: Burn 1 stretches the circular orbit into an ellipse touching GEO altitude; during the coast the speed readout falls from 10.1 to 1.6 km/s as the satellite climbs; Burn 2 rounds the ellipse into the GEO circle with the final speed reading 3.1 km/s — slower than the 7.7 km/s start — while total delta-v spent reads 3.9 km/s.

Anchor: LEO 7.7 km/s → burn 1 +2.4 km/s → coast slows to 1.6 km/s at GEO altitude → burn 2 +1.5 km/s → 3.1 km/s circular. Total Δv ≈ 3.9 km/s.

Checks:
- After burn 1 the trajectory is an ellipse tangent to the LEO circle at the burn point and reaching the GEO circle at apogee; the satellite's altitude at the instant of the burn is unchanged.
- The speed readout decreases monotonically during the coast, from ~10.1 km/s just after burn 1 to ~1.6 km/s at apogee.
- After burn 2 the orbit is the GEO circle with speed ~3.1 km/s — lower than the initial 7.7 km/s — while the delta-v-spent readout shows ~3.9 km/s.
- Thrust flames always point opposite the velocity arrow (prograde burns); no radially outward 'upward' thrust ever appears.

### Specific impulse: the momentum a kilogram of propellant buys {#isp-is-exhaust-velocity}

- concept: rocket-equation-tyranny
- requires: momentum-recoil

Teaches: Specific impulse is the momentum a rocket buys per kilogram of propellant — its exhaust velocity, quoted as Isp = v_e/g₀.

Caption: Every rocket is in the business of buying momentum with mass, so let us ask the natural question: how much momentum do you get for each kilogram you throw away? The answer is simply the exhaust velocity — a kilogram thrown out at \(v_e\) carries \(v_e\) of momentum, no more and no less. Engineers, by an old convention, divide by \(g_0\) and quote it in seconds: \(I_{sp} = v_e/g_0\). A typical chemical thruster leaves the nozzle near 2.2 km/s (\(I_{sp}\) about 220 s); an ion thruster — the workhorse type is called a Hall thruster — hurls its atoms at some 15 km/s (\(I_{sp}\) about 1,500 s) — roughly seven times the momentum of a typical chemical thruster for every kilogram spent.

Visual: A spacecraft on a frictionless track ejects discrete 1 kg pellets to the left; pellet trail length is proportional to v_e. A slider sets v_e. Three live readouts: Isp in seconds (v_e/9.81), momentum delivered per kg expelled (kg·m/s), and propellant flow rate needed to sustain 1 N of thrust (g/s). Markers on the slider label 'typical chemical: ~2.2 km/s (220 s)' and 'Hall thruster: ~15 km/s (1,500 s)'. Equation shown: Isp = v_e / g₀.

Interactive:
- variable: exhaust velocity v_e
- control: slider
- range: v_e = 1.8 to 15 km/s
- on-screen: Pellets fly out faster, the Isp readout rises proportionally, and the grams-per-second needed for 1 N of thrust falls.

Anchor: v_e ≈ 15 km/s corresponds to Isp ≈ 1,500 s (Hall thruster); v_e ≈ 2.2 km/s corresponds to Isp ≈ 220 s (typical chemical thruster).

Checks:
- Isp readout equals v_e/9.81 within 1% at every slider position.
- Propellant flow per newton decreases monotonically as v_e increases (inverse proportionality: 15 km/s needs ~1/5 the flow of 3 km/s).
- At v_e = 2.2 km/s the Isp readout shows ~220–226 s.

### Propellant needs grow exponentially with delta-v {#rocket-equation}

- concept: rocket-equation-tyranny
- requires: dv-budget, isp-is-exhaust-velocity

Teaches: Propellant requirements grow exponentially with the delta-v demanded, because each kilogram of propellant must itself be accelerated by propellant burned earlier.

Caption: Now watch what happens when we add up the recoil over a whole burn. The propellant you burn late had to be carried — and accelerated — by the propellant you burned early, and propellant pushing propellant compounds exactly like interest. The sum is Tsiolkovsky's equation, \(Δv = I_{sp}·g_0·ln(m_{wet}/m_{dry})\), and turned around it says the propellant mass grows exponentially with the mission-required delta-v — the total velocity change you plan to execute. That exponential is merciless: a 500 kg spacecraft on chemical propellant — \(I_{sp}\) about 220 s for a typical thruster — cannot tank its way past about 700 m/s no matter how it tries. The only escape is to raise the exhaust velocity, which shrinks the exponent — and that is why \(I_{sp}\) is worth real money.

Visual: A plot of required propellant mass (y, 0–800 kg) versus mission-required delta-v (x, 0–6,000 m/s; axis labeled 'mission-required Δv — total velocity change planned') for a 500 kg dry spacecraft, computed from m_prop = m_dry·(e^(Δv/(Isp·g₀)) − 1). A slider sets Δv and drags a cursor along the curve; buttons switch Isp between 220 s (typical chemical) and 1,500 s (typical electric), redrawing the curve — no cryogenic option, because spacecraft cannot store cryogens. A vertical dashed line at ~700 m/s on the Isp = 220 s curve labeled in plain words: 'chemical tank-capacity wall — the tanks are physically full'. Equation displayed: Δv = Isp·g₀·ln(m_wet/m_dry).

Interactive:
- variable: mission-required delta-v (with Isp selectable)
- control: slider
- range: Δv = 0 to 6,000 m/s; Isp buttons: 220 s typical chemical / 1,500 s typical electric
- on-screen: The cursor climbs the propellant curve; the propellant-mass readout grows faster and faster; switching Isp buttons visibly flattens or steepens the entire curve.

Anchor: At typical chemical Isp (220 s), a 500 kg-class spacecraft on storable propellant exhausts its practical delta-v budget near 700 m/s.

Checks:
- Every curve is convex and increasing: doubling Δv from 1,000 to 2,000 m/s more than doubles the required propellant mass per kg of dry mass.
- At fixed Δv > 0, switching from Isp 220 s to Isp 1,500 s reduces the propellant readout by more than a factor of 6.
- The 'tank-capacity wall' marker sits at ~700 m/s on the Isp = 220 s curve.
- Propellant readout at Δv = 0 is exactly 0 kg.

### Thrust decides how long a maneuver takes {#thrust-sets-time}

- concept: thrust-vs-isp-dichotomy
- requires: f-equals-ma, dv-budget

Teaches: The duration of a maneuver is set by thrust alone: Δt ≈ m·Δv/F, so millinewton engines turn hours of delta-v into months of firing.

Caption: How long does a maneuver take? That depends on one thing only: how hard the engine pushes. The time is \(Δt ≈ m·Δv/F\) — the velocity change you need, times the spacecraft's mass, divided by the thrust. Give a 500 kg spacecraft 100 newtons and a 100 m/s debris dodge takes about ten minutes; give it the millinewtons of an ion engine and the same dodge takes 220 hours of continuous firing. Efficiency decides how much delta-v you can afford; thrust decides how quickly you can spend it.

Visual: A log-log plot: burn time (y, minutes to years) versus thrust (x, 1 mN to 200 N) for a 500 kg spacecraft. A slider moves a cursor along the line Δt = m·Δv/F; buttons select Δv = 100 m/s or 5,000 m/s, shifting the line vertically. A digital clock readout displays the burn time in the most natural unit (minutes / hours / days). Reference lines are labeled in plain words: 'typical ion engine (~0.05 N)' near 0.05–0.1 N and 'typical chemical engine (~100 N)' near 100 N. Each Δv line is labeled directly on the plot ('Δv = 100 m/s', 'Δv = 5,000 m/s') so no curve or dashed line is left unexplained.

Interactive:
- variable: engine thrust
- control: slider
- range: F = 1 mN to 200 N (log scale); Δv buttons: 100 m/s / 5,000 m/s
- on-screen: The cursor slides along a straight slope-−1 line on the log-log plot and the clock readout shrinks from months to minutes as thrust rises.

Anchor: For 500 kg and Δv = 100 m/s: ~10 minutes at ~100 N versus ~220 hours at millinewton ion-engine thrust.

Checks:
- Increasing thrust by 10× decreases the displayed burn time by exactly 10× (slope −1 on log-log axes).
- At typical ion-engine thrust (~0.06 N) with Δv = 100 m/s, the clock reads within ~10% of 220 hours.
- Switching Δv from 100 to 5,000 m/s at fixed thrust multiplies the burn time by 50.

### For 50 years: strong thrust or high efficiency, never both {#thrust-isp-plane}

- concept: thrust-vs-isp-dichotomy
- requires: isp-is-exhaust-velocity, thrust-sets-time

Teaches: Chemical and electric propulsion occupy opposite corners of the thrust–Isp plane because chemical exhaust velocity is capped by combustion chemistry while electric thrust is capped by available panel power.

Caption: Let us put every engine on one map: thrust up the side, \(I_{sp}\) along the bottom. The chemical rocket carries its energy in its own chemical bonds, so it can release power furiously — hundreds of newtons — but combustion decides what molecules come out, and they will not leave faster than about 3.2 km/s. The electric thruster takes its energy from solar panels, so its exhaust can be marvelously fast, 15 km/s; but thrust is \(F ≈ 2ηP/v_e\), and a few kilowatts divided by a fast exhaust is millinewtons. Slide the panel power as high as you honestly can, and the electric point never comes near 100 N. The region between them — a hundred newtons of thrust at an \(I_{sp}\) of 500 s or so, strong and efficient at once — has sat empty for fifty years.

Visual: A 2D scatter plane: x = Isp (log, 100–2,000 s), y = thrust (log, 1 mN–1 kN). A fixed red marker for storable chemical (Isp 180–330 s band, ~100–400 N). A blue marker for a Hall thruster at Isp 1,500 s whose vertical position is computed from F = 2ηP/v_e (η = 0.5) as a slider varies panel power P. A shaded region spanning Isp ≈ 350–2,000 s at thrust above ~10 N — visually centered near Isp 500 s, thrust 100 N — is labeled 'empty for 50 years'. A side readout shows the electric thrust in newtons and the burn time for 100 m/s at that thrust.

Interactive:
- variable: solar-array electrical power feeding the electric thruster
- control: slider
- range: P = 250 W to 20 kW
- on-screen: The electric marker visibly climbs the log-scale thrust axis in proportion to power (its plotted y-position must track the thrust readout, ~17 mN at 250 W to ~1.3 N at 20 kW), yet even at maximum power it remains far below the 100 N line and never enters the shaded region; the burn-time readout for a 100 m/s maneuver never falls below ~10 hours and reads hundreds of hours at few-kilowatt power.

Anchor: Hall thruster: Isp ~1,500 s at millinewton-class thrust; storable chemical: Isp 180–330 s at hundreds of newtons.

Checks:
- The electric marker's thrust scales linearly with panel power (10 kW → ~0.7 N at v_e = 15 km/s, η = 0.5).
- The electric marker's plotted position is bound to the slider: between the default and max-power screenshots the blue dot sits at visibly different heights on the log thrust axis. Implementation requirement: recompute and redraw the dot's y-coordinate from F inside the same handler that updates the thrust readout — a dot drawn once at init is a failure.
- At maximum slider power (20 kW) the electric marker reads ~1.3 N and remains at least 50× below the 100 N line.
- The chemical marker never moves and never exceeds Isp 330 s.
- The shaded region is centered near Isp ≈ 500 s and thrust ≈ 100 N, does not overlap the chemical band, and contains no marker at any slider setting.

## Part: The new technology: solar-thermal propulsion

Lede: Now the paper's machine. Focus sunlight with a mirror, heat a light gas, and both halves of the old tradeoff give way at once.

### Sunlight heating a light gas beats combustion on efficiency {#sunlight-isp}

- concept: solar-thermal-mechanism
- requires: temperature-is-speed, isp-is-exhaust-velocity, thrust-isp-plane

Teaches: Exhaust velocity of a thermally heated gas scales as the square root of temperature over molecular mass, so concentrated sunlight heating ammonia or hydrogen exceeds the chemical Isp ceiling without any combustion.

Caption: Here is where our two knobs come back. In a thermal rocket the exhaust speed is fixed by heat alone, \(v_e ∝ \sqrt{T/M}\) — and combustion, you notice, turns both knobs at once and tangles them: it makes the gas hot, but it insists on heavy product molecules. Suppose instead we heat the gas with concentrated sunlight. Then we may choose whatever molecule we please and run the temperature to the limit of the materials: ammonia, \(M = 17\), at 3,000 K gives \(I_{sp}\) around 350–450 s — above anything a storable chemical rocket can reach — and hydrogen, \(M = 2\), gives about 800 s. There is no flame anywhere; the mirror is the whole energy supply.

Visual: Cross-section diagram: a parabolic mirror focuses sun rays onto a chamber feeding a nozzle; exhaust arrow length is proportional to v_e. Controls: a chamber-temperature slider and three molecule buttons (H₂ M=2, NH₃ M=17, combustion products M≈22). Readouts: v_e in km/s and Isp in seconds, computed from v_e ∝ √(T/M) calibrated so NH₃ at 3,000 K reads ~420 s. A horizontal dashed line on an adjacent Isp gauge marks 'storable chemical ceiling: 330 s'. Equation displayed: v_e ∝ √(T_chamber/M_molar).

Interactive:
- variable: chamber temperature (with propellant molecule selectable)
- control: slider
- range: T = 1,000 to 3,000 K; molecule buttons: H₂ / NH₃ / combustion products (M ≈ 22 g/mol)
- on-screen: The exhaust arrow lengthens and the Isp readout climbs as T rises; switching to a lighter molecule at fixed T jumps the Isp readout upward, crossing the 330 s ceiling line.

Anchor: At ~3,000 K: ammonia Isp ≈ 350–450 s; hydrogen Isp ≈ 800 s.

Checks:
- Isp readout scales as √T: quadrupling T (750 K → 3,000 K equivalent range check) doubles v_e.
- At fixed T, H₂ always reads higher Isp than NH₃, which reads higher than M ≈ 22 combustion products.
- NH₃ at 3,000 K reads within the 350–450 s band; H₂ at 3,000 K reads ~800 s.
- No flame or oxidizer appears in the diagram — the only energy input drawn is focused sunlight.

### And the mirror delivers chemical-class thrust {#sunlight-thrust}

- concept: solar-thermal-mechanism
- requires: thrust-sets-time, sunlight-isp

Teaches: Concentrated sunlight delivers thermal power directly to the propellant at levels far beyond what photovoltaic conversion can supply, so thrust reaches 100–200 N instead of millinewtons.

Caption: But is the thrust any good? Thrust is \(F ≈ 2P/v_e\), so at \(v_e = 4\) km/s you need about 300 kW of jet power to make 150 N — an enormous power by spacecraft standards. The trick is that a mirror is only shaped aluminum film, better than 1,000 watts per kilogram — ten times what solar panels manage — and the heat exchanger can bank up heat between burns and spend it all at once. The sunlight goes straight into the gas: no solar cells, no ion optics, no conversion losses along the way. That is how the thrust comes out five orders of magnitude above an ion engine's.

Visual: Left: the mirror-and-nozzle diagram from the previous scene with a power-flow arrow labeled in kW. Right: a log-scale horizontal thrust bar chart with three bars — Hall thruster (fixed, ~0.05 N), storable chemical (fixed band, 100–400 N), and solar thermal (live). A slider sets concentrated thermal jet power; the solar-thermal bar length is computed from F = 2P/v_e with v_e = 4 km/s. A readout beneath shows the thrust in newtons and 'orders of magnitude above Hall'.

Interactive:
- variable: concentrated thermal power delivered to the propellant
- control: slider
- range: P = 10 to 500 kW
- on-screen: The solar-thermal thrust bar grows linearly with power, entering the 100–200 N chemical-class band around 200–400 kW while the Hall bar stays frozen near 0.05 N.

Anchor: Solar-thermal thrust ~100–200 N — approximately 5 orders of magnitude above millinewton Hall-thruster thrust; membrane reflectors deliver >1,000 W/kg versus ~100 W/kg for solar arrays.

Checks:
- Solar-thermal thrust readout scales linearly with the power slider (doubling P doubles F).
- At P ≈ 300 kW the readout shows ~150 N (F = 2P/v_e with v_e = 4 km/s).
- The solar-thermal bar exceeds the Hall bar by at least 3 orders of magnitude at every slider position, and ~5 orders at design power.
- The Hall and chemical bars are identical in both screenshots.

## Part: Why it beats existing rockets

Lede: A new engine only matters if it wins against what already flies. Here it is priced head-to-head against chemical and electric propulsion on cost, speed, and readiness.

### What a maneuver costs with each engine type {#free-energy-cost}

- concept: energy-source-decoupling
- requires: rocket-equation, sunlight-thrust

Teaches: Decoupling the energy source from the reaction mass removes the dominant recurring costs from each maneuver.

Caption: Now let us follow the money, because the physics writes the bills. The chemical stage hauls its energy up from Earth as propellant and is used up within a few burns, so its hardware cost falls on a handful of maneuvers. The ion thruster's energy is free sunlight — but it insists on xenon at $2,500 a kilogram, and its grids erode away with use, so the engine itself is a slow consumable. The solar-thermal rocket takes free sunlight, pushes ammonia at a dollar a kilogram, and its one-piece heat exchanger restarts hundreds of times. Same conservation laws; utterly different economics.

Visual: Three-panel comparison for a standardized 500 kg / $10M spacecraft performing a 100 m/s maneuver. Buttons select architecture (storable biprop / Hall electric / solar thermal). The selected panel shows an energy-flow diagram (source → propellant → exhaust) and a stacked cost bar with three labeled segments: propellant cost, hardware amortization per maneuver, energy cost per maneuver. A small table pins propellant prices: ammonia $1/kg, xenon $2,500/kg.

Interactive:
- variable: propulsion architecture
- control: buttons
- range: storable biprop / Hall electric / solar thermal
- on-screen: The energy-flow arrows re-route (onboard bonds vs panels vs mirror) and the stacked cost bar re-composes: biprop's bar is dominated by hardware amortization, Hall's by xenon plus thruster wear, solar thermal's by a thin ammonia sliver plus widely amortized hardware.

Anchor: At 100 m/s: storable biprop ≈ $1.46M per maneuver; solar thermal ≈ $222k; Hall electric ≈ $216k. Ammonia $1/kg versus xenon $2,500/kg.

Checks:
- The biprop total bar (~$1.46M) is roughly 6–7× taller than the solar-thermal bar (~$222k).
- Solar thermal's 'energy cost' segment is zero in every state where it is selected.
- Hall's propellant segment is visibly dominated by xenon price; solar thermal's propellant segment is negligible at $1/kg.
- Hall and solar-thermal totals are within a few percent of each other at this 100 m/s point.

### Solar thermal is the cheapest at nearly every delta-v {#cost-curves}

- concept: cost-per-maneuver-economics
- requires: rocket-equation, free-energy-cost

Teaches: Solar thermal is the lowest-cost propulsion class at essentially every delta-v because propellant price, hardware amortization, and free energy all bend its curve down.

Caption: Sweep the delta-v from a small debris dodge to a grand transfer and price each engine as you go. The rocket equation bends every cost curve upward — but it bends hardest on the low-\(I_{sp}\) chemical rocket, which quits altogether at its 700 m/s tank wall. The electric thruster keeps pace with solar thermal at 100 m/s, both near $220k a maneuver; but by 5,000 m/s the xenon and the worn grids have pushed it to $10.9M against solar thermal's $9.1M. Across the whole range, the mirror-and-ammonia machine holds the floor.

Visual: A chart: cost per maneuver (y, $100k–$12M, log scale) versus delta-v (x, 100–5,000 m/s). Three curves: storable biprop (red, ending abruptly at ~700 m/s with an X marker labeled 'tank capacity wall'), Hall electric (blue), solar thermal (green). A slider drags a vertical cursor line; a readout box lists the three costs at the cursor's delta-v, with unavailable classes shown as '—'.

Interactive:
- variable: delta-v of the maneuver being priced
- control: slider
- range: Δv = 100 to 5,000 m/s
- on-screen: The cursor sweeps right; readouts update; past 700 m/s the biprop readout switches to 'infeasible', and past ~3,000 m/s the green curve visibly undercuts the blue curve.

Anchor: At 100 m/s: solar thermal $222k, biprop $1.46M, electric $216k. At 700 m/s: solar thermal ~$1.39M as biprop terminates. At 5,000 m/s: solar thermal $9.1M vs electric $10.9M.

Checks:
- The red biprop curve terminates at ~700 m/s and its readout shows 'infeasible' beyond that point.
- At Δv = 100 m/s the electric and solar-thermal readouts are within ~5% of each other ($216k vs $222k), with biprop ~6.5× higher.
- At Δv = 5,000 m/s the solar-thermal readout (~$9.1M) is below the electric readout (~$10.9M).
- All curves are monotonically increasing and upward-bending in delta-v.

### Solar thermal is also the fastest: 9 hours vs 527 days {#time-curves}

- concept: maneuver-time-responsiveness
- requires: thrust-sets-time, sunlight-thrust

Teaches: Solar thermal is the only propulsion class whose maneuver times stay in single-digit hours across the entire delta-v spectrum.

Caption: And now the clocks. With 100–200 N behind it, the solar-thermal spacecraft finishes a 100 m/s debris dodge in about ten minutes and a full 5,000 m/s transfer in about nine hours. The ion engine, pushing millinewtons, needs 223 hours for the little dodge and 527 days — a year and a half of continuous spiraling — for the big one. Think what that difference means: the nine-hour spacecraft answers an emergency; the 527-day spacecraft reads about it afterward.

Visual: A chart: maneuver time (y, log scale from 1 minute to 2 years, with human-readable gridlines at 1 hr / 1 day / 1 month / 1 year) versus delta-v (x, 100–5,000 m/s). Curves: solar thermal (green), Hall electric (blue), storable biprop (red, terminating at 700 m/s). A slider drags a cursor; two clock-face readouts display green and blue times side by side, plus a ratio readout ('electric takes N× longer').

Interactive:
- variable: delta-v of the maneuver being timed
- control: slider
- range: Δv = 100 to 5,000 m/s
- on-screen: The cursor sweeps right; the green clock climbs from ~10 minutes to ~9 hours while the blue clock climbs from ~223 hours to ~527 days, and the ratio readout stays above 1,000×.

Anchor: Solar thermal: ~10 min at 100 m/s, ~9 h at 5,000 m/s. Electric: ~223 h at 100 m/s, >12,600 h (527 days) at 5,000 m/s.

Checks:
- At Δv = 5,000 m/s the green readout shows ~9 hours and the blue readout ~527 days (>12,600 h), a ratio over 1,000×.
- The green curve never exceeds the 10-hour gridline anywhere in the sweep.
- Both curves scale linearly with delta-v (50× delta-v gives ~50× time within each class).
- The red biprop curve tracks the green curve closely but ends at 700 m/s.

### Ammonia can wait in orbit; cryogenic fuels cannot {#storability}

- concept: storability-constraint
- requires: time-curves

Teaches: Responsive maneuvering requires indefinite fueled loiter on orbit, which cryogenic propellants physically cannot provide but ammonia can.

Caption: You might ask: why not simply fly a big cryogenic stage — methane and oxygen — and have strong thrust with better \(I_{sp}\)? Thermodynamics forbids it, in a sneaky way. Cryogens must be kept tens of degrees colder than anything sitting in sunlight can stay, so without refrigeration they boil away within hours — the tank empties before a waiting spacecraft ever gets to use it. That is why only launch rockets use cryogenics: their whole job is over in the first few hours. Ammonia sits happily at ordinary spacecraft temperatures for years. So the solar-thermal vehicle loiters for months and fires within minutes of the command — and being quick is worth nothing unless you are also ready.

Visual: Two side-by-side vertical tanks in orbit above Earth: 'methalox (cryogenic)' and 'ammonia (storable)', each with a fill level and a temperature label (cryo: ~90–110 K required; ammonia: ambient spacecraft temperature). A slider advances days of on-orbit loiter; the methalox level drains via a boil-off animation almost immediately — within the first slider tick — while ammonia stays full. Below each tank, a 'response time if commanded now' readout: ammonia shows 'minutes'; methalox shows 'empty — launch & fuel first: ≥24 h' once depleted.

Interactive:
- variable: days of fueled loiter on orbit before a maneuver is commanded
- control: slider
- range: t = 0 to 180 days
- on-screen: The methalox fill level drops steadily and reaches near-empty within the days-scale portion of the slider; the ammonia level is unchanged at 180 days; the methalox response-time readout flips from hours to '≥24 h re-fuel latency'.

Anchor: Cryogenic propellant boils off within hours without active cooling — only launch rockets, whose job ends within hours, can use it; methalox missions carry a minimum ~24-hour launch-and-fueling latency. Ammonia is storable indefinitely.

Checks:
- The methalox tank level drops to near-empty within the first day of loiter time (cryogens boil off in hours) and never recovers.
- The ammonia tank level is identical at day 0 and day 180.
- The methalox response-time readout never displays a value below 24 hours once its tank is depleted.
- The ammonia response-time readout displays minutes at every slider position.

## Part: Why now

Lede: The physics was proven decades ago. Three manufacturing advances made it buildable — just as orbit is about to get eighty times more crowded, with a nuclear version waiting behind it.

### Blocked by manufacturing then, buildable now {#why-now}

- concept: enabling-tech-convergence
- requires: sunlight-isp

Teaches: Solar thermal was blocked in the 1980s by buildability, and the material temperature ceiling rising from ~1,800 K to ~3,000 K converts directly into Isp via the √T scaling.

Caption: If the idea is so good, why wasn't it flown forty years ago? The physics was demonstrated — a Rockwell study in 1979, hydrogen ground tests above 800 s of \(I_{sp}\) — but three pieces could not be built. The heat exchanger needed hundreds of brazed parts; it is now printed as a single piece. The old alloys gave up near 1,800 K; today's refractory alloys hold 3,000 K, and since \(v_e\) goes as \(\sqrt{T}\), that jump alone is worth about 29% more \(I_{sp}\). And membrane mirrors, at better than 1,000 W/kg, finally made the collector light enough. All three arrived together — any one missing, and the machine stays on the shelf.

Visual: A slider labeled 'material temperature limit' spanning 1,800 K (tagged '1980s alloys, brazed assemblies') to 3,000 K (tagged '2020s refractory alloys, 3D-printed monolith'). The heat-exchanger diagram recolors from dull to white-hot and its construction callout swaps from 'hundreds of brazed parts' to 'single printed part'. Live readouts: ammonia Isp and hydrogen Isp computed with √T scaling (calibrated: NH₃ ~420 s and H₂ ~800 s at 3,000 K). A side card pins mirror specific power: >1,000 W/kg membrane vs ~100 W/kg conventional array.

Interactive:
- variable: heat-exchanger material temperature limit
- control: slider
- range: T_limit = 1,800 to 3,000 K
- on-screen: Both Isp readouts rise as √T (ammonia climbing from ~325 s toward ~420 s, hydrogen from ~620 s toward ~800 s), and the construction callout switches from brazed assembly to monolithic print.

Anchor: 1980s ground tests demonstrated >800 s Isp with hydrogen; modern refractory alloys hold ~3,000 K versus a ~1,800 K 1980s cap; membrane reflectors deliver >1,000 W/kg versus ~100 W/kg arrays.

Checks:
- Isp readouts scale as √T: moving 1,800 K → 3,000 K increases both readouts by ~29% (factor √(3000/1800) ≈ 1.29).
- Hydrogen Isp reads ~800 s at the 3,000 K end.
- The mirror specific-power card shows a 10× gap (>1,000 vs ~100 W/kg) in both screenshots.
- The heat-exchanger callout text differs between the two slider extremes (brazed vs monolithic printed).

### 80× more satellites means far more than 80× more dodging {#maneuver-demand}

- concept: demand-regime-shift
- requires: dv-budget, time-curves

Teaches: Because close-approach events scale with pairwise encounters, an 80× jump in orbital population turns collision avoidance from an edge case into continuous infrastructure operation.

Caption: For decades a satellite mostly parked: it held its slot for years and made an occasional millinewton correction. Look at what is coming instead: filings for more than 1.2 million satellites — 95,000-plus for broadband, a million in one orbital data-center filing, 88,000 more here, 51,600 there — against about 15,000 alive today. Close approaches count by pairs, so they grow roughly as \(N^2\): eighty times the satellites means on the order of thousands of times the dodging. Add deliberate military maneuvering, and moving about stops being the exception and becomes the job itself.

Visual: Left: an orbital-shell diagram (500–2,000 km band) populated with dots whose density scales with a population slider. Right: two readouts — total satellites N, and relative conjunction-event rate scaled as (N/15,000)², displayed as a multiplier versus today. Below, a stacked bar decomposes the filed total: broadband 95k+, SpaceX 1M, Starcloud 88k, Blue Origin 51.6k, against a thin baseline bar for ~15,000 active today.

Interactive:
- variable: orbital satellite population
- control: slider
- range: N = 15,000 (today) to 1.2 million (filed)
- on-screen: Dot density in the shell thickens dramatically; the conjunction-rate multiplier readout climbs quadratically, reaching ~6,400× at the slider maximum.

Anchor: ~15,000 active satellites today versus >1.2 million in filings — an ~80× increase; pairwise conjunction rate at 80× population is ~6,400× today's.

Checks:
- The conjunction-rate multiplier scales quadratically: doubling N quadruples the multiplier.
- At the slider maximum, N reads 1.2 million and the multiplier reads ~6,400×.
- At the slider minimum, N reads ~15,000 and the multiplier reads 1×.
- The filed-population stacked bar totals >1.2M and dwarfs the ~15k baseline bar in both screenshots.

### The same engine can later run on nuclear heat {#nuclear-bridge}

- concept: nuclear-thermal-bridge
- requires: sunlight-thrust, why-now

Teaches: A solar-thermal rocket and a nuclear-thermal rocket are the same heat-exchanger-and-nozzle machine with different heat sources, so solar-thermal flight heritage transfers directly to reactor-heated versions.

Caption: One last observation. Look inside a solar-thermal rocket and a nuclear-thermal rocket and you find the same machine: gas runs through a heat exchanger at some 3,000 K and out a nozzle — only the source of the heat differs, a mirror or a reactor. The solar version reportedly reaches about 90% of the nuclear performance at about 10% of the cost, with no fissile material aboard and no licensing to wait for. So every solar-thermal flight quietly builds the flight record the reactor version will need when its time comes, likely in the 2030s. The mirror, you might say, is the on-ramp.

Visual: A single engine cross-section (heat exchanger with internal channels, propellant feed line, nozzle) drawn identically in both states. A toggle swaps only the heat-source block: 'concentrated sunlight via mirror' versus 'fission reactor core'. Components shared between states are outlined in green and labeled 'unchanged'; only the source block is outlined in orange. A comparison card shows two dials: relative performance (solar ≈ 90% of nuclear) and relative cost (solar ≈ 10% of nuclear), plus a note 'no fissile material / no nuclear licensing' in the solar state.

Interactive:
- variable: heat source feeding the heat exchanger
- control: toggle
- range: concentrated sunlight ↔ fission reactor
- on-screen: Only the heat-source block and its input arrow swap; the heat exchanger, channels, propellant path, and nozzle are pixel-identical, and the performance/cost dials update to ~90% / ~10% in the solar state.

Anchor: Solar thermal ≈ 90% of nuclear-thermal performance at ≈ 10% of the cost; both operate the heat exchanger near ~3,000 K.

Checks:
- The heat exchanger, channel geometry, propellant path, and nozzle are visually identical in both toggle states — only the heat-source block differs.
- The performance dial reads ~90% and the cost dial ~10% in the solar state, both 100% in the nuclear state.
- The chamber temperature label (~3,000 K) is present and unchanged in both states.
- The 'no fissile material / no nuclear licensing' note appears only in the solar state.
