# encs4380-dynamics--Chinatown-
# ENCS4380 Homework 1: Dynamic Characteristics Toolkit

**Live site:** https://shahdfarraj.github.io/encs4380-dynamics--Chinatown-/

## What is this?
A web page that shows how a sensor responds over time and frequency. It runs in the browser only.
It needs no server and no internet connection.

## Who built what

| Member | Module |
|---|---|
| Leen Zuhud | Module 1: First-order time response |
| Shahd Farraj | Module 2: First-order frequency response |
| Batoul Abu Samhadana | Module 3: second-order response |
| Laila Bahjat | Module 4: Guess the Sensor Challenge |

## Module 1: First-order time response
A thermometer is slow. It takes time to reach the real temperature.
The page shows this with a graph.

You can:
- Change the sensor gain K, the time constant tau, and the input size A.
- Switch between a step input and a ramp input.
- See the 63.2 % point at tau and the 95 % point at 3 tau.
- See how late the sensor is on a ramp (the lag equals tau).
- See the log graph, where the line has slope -1/tau.
- Answer a "Predict, then check" question before moving the sliders.

### Validation check 1
The slides say the step response reaches 63.2 % of its final value at t = tau,
and 95 % at t = 3 tau. The page checks this itself and shows PASS or FAIL.

Result: PASS

## Module 2: First-order frequency response
A first-order sensor dampens high-frequency inputs and introduces a phase lag. The page visualizes how the sensor responds to dynamic sine-wave inputs using the formulas:
$$M = \frac{1}{\sqrt{1 + (\omega\tau)^2}} \quad \vert \quad \phi = -\tan^{-1}(\omega\tau)$$

You can:
- Change the time constant tau ($\tau$) and input frequency $\omega$.
- View input and output sines on the same plot to visually inspect phase lag and attenuation.
- See the live Bode plot showing amplitude ratio $M$ across a log scale of frequencies.
- Identify the cutoff frequency at $\omega = 1/\tau$.
- Compute dynamic error $\delta = M - 1$ live.

### Validation checks 2 and 3
- **Check 2:** For $\tau = 0.2\text{ s}$ and input $\sin(2t)$, the output amplitude is 0.93 of the input with a phase lag of $21.8^\circ$.
- **Check 3:** For signals up to 50 Hz with at most 5% dynamic error, $\tau \approx 0.52\text{ ms}$, yielding a phase lag of $9.3^\circ$ at 50 Hz.

The page checks these automatically and displays PASS or FAIL.

Result: PASS

## Module 3: Second-order response
A mass on a spring with a damper (like an accelerometer) does not settle like a thermometer.
It can swing past the final value and ring, or creep slowly, depending on how much damping it has.
The page uses:
$$G(s) = \frac{K\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}$$

You can:
- Change the damping ratio zeta and the natural frequency omega_n, or switch to the mass m, damper b and spring k.
- Jump to the three cases with one click: underdamped (zeta = 0.5), critically damped (zeta = 1) and overdamped (zeta = 2).
- Tick one box to draw all three cases on the same graph.
- Read the rise time, peak time, overshoot and settling time directly off the step curve, next to the textbook formulas. The settling band can be 2 % or 5 %.
- See the poles of G(s) (x) and the eigenvalues of A (o) on the s-plane. They land on the same points.
- See the state-space matrices A and B update live as m, b and k move.
- See the phase plane (position against velocity): a spiral when underdamped, no spiral when overdamped.
- Answer a "Predict, then check" question before moving the sliders.

### Validation checks 4, 5 and 6
- **Check 4:** zeta = 0.5 gives an overshoot of 16.3 %.
- **Check 5:** zeta = 1 gives no overshoot.
- **Check 6:** m = 1, b = 2, k = 4 gives eigenvalues of A = -1 +/- j1.732, equal to the poles.

The page computes each one and shows expected value, our value and PASS or FAIL.
Buttons on the page put the same values on the graphs.

Result: PASS (all three)

## Screenshots
**Module 1: First-order time response**
**step response**
<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/184c9468-9732-4b56-8450-2a47f7a8d845" />
**ramp response**
<img width="1920" height="1023" alt="image" src="https://github.com/user-attachments/assets/b0d0f9dd-f9c0-4246-bd1a-944c00f736a0" />
**log graph**
<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/19be6311-cfae-46e9-8169-902a806621a1" />

**Module 2: First-order frequency response**
**frequency response & Bode plot**
<img width="1920" height="1016" alt="image" src="screenshot2.png" />

**Module 3: second order response**
**step response**
<img width="970" height="631" alt="image" src="https://github.com/user-attachments/assets/2a0044ad-a721-4eaf-85f1-7b3f103905dd" />
**s-plane: poles of G(s) and eigenvalues of A**
<img width="897" height="551" alt="image" src="https://github.com/user-attachments/assets/2f5356ae-623a-4f91-8f15-caaf6143ee3d" />
**State-space panel (updates live)**
# encs4380-dynamics--Chinatown-
# ENCS4380 Homework 1: Dynamic Characteristics Toolkit

**Live site:** https://shahdfarraj.github.io/encs4380-dynamics--Chinatown-/

## What is this?
A web page that shows how a sensor responds over time and frequency. It runs in the browser only.
It needs no server and no internet connection.

## Who built what

| Member | Module |
|---|---|
| Leen Zuhud | Module 1: First-order time response |
| Shahd Farraj | Module 2: First-order frequency response |
| Batoul Abu Samhadana | Module 3: Second-order response |
| Laila Bahjat | Module 4: Guess the Sensor Challenge |

## Module 1: First-order time response
A thermometer is slow. It takes time to reach the real temperature.
The page shows this with a graph.

You can:
- Change the sensor gain K, the time constant tau, and the input size A.
- Switch between a step input and a ramp input.
- See the 63.2 % point at tau and the 95 % point at 3 tau.
- See how late the sensor is on a ramp (the lag equals tau).
- See the log graph, where the line has slope -1/tau.
- Answer a "Predict, then check" question before moving the sliders.

### Validation check 1
The slides say the step response reaches 63.2 % of its final value at t = tau,
and 95 % at t = 3 tau. The page checks this itself and shows PASS or FAIL.

Result: PASS

## Module 2: First-order frequency response
A first-order sensor dampens high-frequency inputs and introduces a phase lag. The page visualizes how the sensor responds to dynamic sine-wave inputs using the formulas:

$$M = \frac{1}{\sqrt{1 + (\omega\tau)^2}} \quad \vert \quad \phi = -\tan^{-1}(\omega\tau)$$

You can:
- Change the time constant tau ($\tau$) and input frequency $\omega$.
- View input and output sines on the same plot to visually inspect phase lag and attenuation.
- See the live Bode plot showing amplitude ratio $M$ across a log scale of frequencies.
- Identify the cutoff frequency at $\omega = 1/\tau$.
- Compute dynamic error $\delta = M - 1$ live.

### Validation checks 2 and 3
- **Check 2:** For $\tau = 0.2\text{ s}$ and input $\sin(2t)$, the output amplitude is 0.93 of the input with a phase lag of $21.8^\circ$.
- **Check 3:** For signals up to 100 Hz with at most 5% amplitude error, $\tau \approx 0.52\text{ ms}$, yielding a phase lag of approximately $9.3^\circ$ at 50 Hz.

The page checks these automatically and displays PASS or FAIL.

Result: PASS

## Module 3: Second-order response
A mass on a spring with a damper (like an accelerometer) does not settle like a thermometer.
It can swing past the final value and ring, or creep slowly, depending on how much damping it has.
The page uses:

$$G(s) = \frac{K\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}$$

You can:
- Change the damping ratio zeta and the natural frequency omega_n, or switch to the mass m, damper b and spring k.
- Jump to the three cases with one click: underdamped (zeta = 0.5), critically damped (zeta = 1) and overdamped (zeta = 2).
- Tick one box to draw all three cases on the same graph.
- Read the rise time, peak time, overshoot and settling time directly off the step curve, next to the textbook formulas. The settling band can be 2 % or 5 %.
- See the poles of G(s) (x) and the eigenvalues of A (o) on the s-plane. They land on the same points.
- See the state-space matrices A and B update live as m, b and k move.
- See the phase plane (position against velocity): a spiral when underdamped, no spiral when overdamped.
- Answer a "Predict, then check" question before moving the sliders.

### Validation checks 4, 5 and 6
- **Check 4:** zeta = 0.5 gives an overshoot of 16.3 %.
- **Check 5:** zeta = 1 gives no overshoot.
- **Check 6:** m = 1, b = 2, k = 4 gives eigenvalues of A = -1 +/- j1.732, equal to the poles.

The page computes each one and shows expected value, our value and PASS or FAIL.
Buttons on the page put the same values on the graphs.

Result: PASS (all three)

## Module 4: Guess the Sensor Challenge

This module is an interactive challenge where the user identifies hidden sensor parameters by analyzing noisy response curves.

The program randomly generates a first-order or second-order sensor. The user studies the graph, estimates the unknown parameters, and submits a guess to compare the estimated response with the actual sensor response.

You can:
- Generate random first-order and second-order sensors.
- Examine noisy sensor response curves without knowing the actual parameters.
- Estimate the time constant $\tau$ for first-order sensors using the 63.2% method or logarithmic error slope.
- Use phase delay to estimate $\tau$ for first-order sinusoidal responses.
- Estimate damping ratio $\zeta$ and natural frequency $\omega_n$ for second-order sensors using overshoot and peak time.
- Click "Show hint" to receive guidance.
- Enter estimated parameters and click "Check my guess".
- Reveal the actual sensor parameters and percentage estimation errors.
- Compare the actual response with the estimated response using overlaid graphs.
- Earn 10 points when the required estimated parameters are within 10% of their actual values.
- Track the running score across multiple rounds.
- Click "New sensor" to generate another challenge.

### Parameter estimation formulas

**First-order step response:**

$$y(t) = K(1-e^{-t/\tau})$$

$$y(\tau) \approx 0.632K$$

**Logarithmic error method:**

$$\ln\left(\frac{y_\infty-y(t)}{y_\infty}\right)=-\frac{t}{\tau}$$

**Second-order overshoot:**

$$M_p=e^{-\pi\zeta/\sqrt{1-\zeta^2}}$$

$$\zeta=\frac{-\ln(M_p)}{\sqrt{\pi^2+\ln^2(M_p)}}$$

**Peak time and natural frequency:**

$$t_p=\frac{\pi}{\omega_n\sqrt{1-\zeta^2}}$$

$$\omega_n=\frac{\pi}{t_p\sqrt{1-\zeta^2}}$$

### Module 4: Automatic self-tests

Five additional automatic self-tests verify the sensor response calculations, parameter estimation formulas, and scoring tolerance.

These tests are supplementary and separate from the six official homework validation checks.

Result: PASS (all five self-tests)

### Implementation and testing

The module uses JavaScript to generate random sensor parameters, simulate noisy measurements, calculate response curves, evaluate user estimates, and update the running score.

The module was tested locally and integrated into the main branch through Pull Request #5.

Related issue: #4

Pull Request: #5

## Screenshots

**Module 1: First-order time response**

**step response**

<img width="1920" height="1021" alt="image" src="https://github.com/user-attachments/assets/184c9468-9732-4b56-8450-2a47f7a8d845" />

**ramp response**

<img width="1920" height="1023" alt="image" src="https://github.com/user-attachments/assets/b0d0f9dd-f9c0-4246-bd1a-944c00f736a0" />

**log graph**

<img width="1920" height="1016" alt="image" src="https://github.com/user-attachments/assets/19be6311-cfae-46e9-8169-902a806621a1" />

**Module 2: First-order frequency response**

**frequency response & Bode plot**

<img width="1920" height="1016" alt="image" src="screenshot2.png" />

**Module 3: second order response**

**step response**

<img width="970" height="631" alt="image" src="https://github.com/user-attachments/assets/2a0044ad-a721-4eaf-85f1-7b3f103905dd" />

**s-plane: poles of G(s) and eigenvalues of A**

<img width="897" height="551" alt="image" src="https://github.com/user-attachments/assets/2f5356ae-623a-4f91-8f15-caaf6143ee3d" />

**State-space panel (updates live)**

<img width="977" height="372" alt="image" src="https://github.com/user-attachments/assets/a1311696-0589-448f-aca9-745f385a4a20" />

**Phase plane (x₁, x₂) during the step**

<img width="903" height="536" alt="image" src="https://github.com/user-attachments/assets/1918483c-5e81-4ed2-aabc-8e5bdf301329" />

**Module 4: Guess the Sensor Challenge**


**Hidden sensor response**

<img width="910" height="630" alt="image" src="https://github.com/user-attachments/assets/e9a4d624-c264-4e49-9658-4c87857c787a" />

**Parameter estimation and feedback**

<img width="764" height="598" alt="image" src="https://github.com/user-attachments/assets/e1a04aec-43b6-46c3-b2bb-999538282a8a" />

<img width="759" height="543" alt="image" src="https://github.com/user-attachments/assets/4c20ab2a-cd31-456b-85b2-bdd7fa903d88" />

<img width="761" height="564" alt="image" src="https://github.com/user-attachments/assets/5fe2637f-f5b8-4892-b98b-501f579c8c00" />

**Actual vs. estimated response**
<img width="761" height="564" alt="image" src="https://github.com/user-attachments/assets/92a23a71-8f18-4652-af51-e89e2b421fa4" />

**Automatic self-tests**

<img width="767" height="440" alt="image" src="https://github.com/user-attachments/assets/ec0146ef-dd91-4545-bbd8-02944132219d" />

## Use of AI tools

We used Claude and ChatGPT to help write the code.
We tested it and can explain every line.

Related issues: #1, #2, #3, #4

<img width="977" height="372" alt="image" src="https://github.com/user-attachments/assets/a1311696-0589-448f-aca9-745f385a4a20" />
**Phase plane (x₁, x₂) during the step**
<img width="903" height="536" alt="image" src="https://github.com/user-attachments/assets/1918483c-5e81-4ed2-aabc-8e5bdf301329" />


## Use of AI tools
We used Claude and ChatGPT to help write the code.
We tested it and can explain every line.
Related issues: #1, #2, #3
