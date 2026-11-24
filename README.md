# CRYO — Solar cold-storage digital twin

Interactive, accelerated lumped thermal simulation inspired by a modular solar cold room. Adjust ambient temperature, PV capacity, water storage and door heat gain; inject a pump fault and export simulated telemetry.

## Run
Open `index.html` or serve this directory with `python -m http.server 8000`. No dependencies.

## Model
Room energy balance: C dT/dt = envelope gain + door gain + internal gain − fan-coil transfer. Tank balance: C dT/dt = fan-coil transfer − solar-driven charging. Water heat capacity 4.186 kJ/kg/K; assumed room effective heat capacity 0.32 kWh/K; envelope conductance 45 W/K; COP 2.7. Fixed five-minute Euler steps.

## Limitations
Synthetic irradiance and lumped temperatures; no spatial CFD, humidity, compressor cycling or hardware telemetry. Tank bounds are simplified. Not validated for equipment sizing or food safety.
