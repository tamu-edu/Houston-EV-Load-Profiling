# Data-Driven Estimation of Residential EV Charging Loads: Houston, TX

## Overview
This repository provides realistic residential electric vehicle (EV) charging load data for the Houston, Texas area. It includes both the original dataset used for generating synthetic data and the resulting synthetic charging load data.

## Features
### Training Dataset
#### Sampled Electric Vecicle Data (`SampledVehicle.xlsx`)
- `vehicle_id`: An anonymized identifier for each vehicle.
- `vehicle_type`: Classification of the vehicle (e.g., Passenger Car, Bus, Multipurpose Vehicle).
- `electrification_level`: Specifies whether the vehicle is a BEV (Battery Electric Vehicle) or PHEV (Plug-in Hybrid Electric Vehicle).
- `state`: Indicates the vehicle's registered state (e.g., Texas).
- **Datasource**: [EVWatts Public Database](https://livewire.energy.gov/ds/evwatts/evwatts.public)

#### Sampled Electric Vehicle Charging Sessions Data (`VehicleChargingSessions.xlsx`)
- `id`: Unique identifier for each charging session.
- `vehicle_id`: Anonymized identifier linking to the vehicle data.
- `start_datetime`: Start time of the charging session, formatted as `MM/DD/YY hh:mm`.
- `stop_datetime`: End time of the charging session, formatted as `MM/DD/YY hh:mm`.
- **Datasource**: [EVWatts Public Database](https://livewire.energy.gov/ds/evwatts/evwatts.public)

#### Houston EV Registration Data (`HoustonEVCount.xlsx`)
- Provides detailed EV registration data for Houston, Texas.
- `zipcode`: The ZIP code associated with each registration.
- `carname`: The name or model of the registered vehicle.
- `evcount`: The number of EVs registered within each ZIP code.
- **Datasource**: [Texas Department of Transportation (TXDoT)](https://www.txdot.gov/)

#### Registered EV's Battery Spec Data (`BatterySizeData.xlsx`)
- Provides detailed battery specs of registrated EV data for Houston, Texas.
- `carname`: The name or model of the registered vehicle.
- `batterysize`: Battery capacity of each EV (in kWh).
- **Datasource**: Official manufacturer websites.

### Synthetic Residential EV Charging Load Data (`ChargingProfilesZipcode.xlsx`)
- Synthetic data contains 10-minute interval residential EV charging loads for all ZIP codes in Houston, Texas.
- Data Generation:
  - Based on the charging curves derived from the training dataset.
  - Combined with Houston EV registration data and battery specifications for each EV.
- Assumptions:
  - Each household is equipped with a Level 2 home charger rated at 7 kW.

- **Representative Charging Patterns for Houston, Texas (Probability)**  
  <img src="https://github.com/user-attachments/assets/dacce3df-ff15-403b-905d-8bf7dd3c87bf" alt="Representative Charging Patterns" width="800">


- **Charging Load Distribution during Peak Hours in Houston, Texas**
  <img src="https://github.com/user-attachments/assets/f0ff0359-58ef-42f0-ab35-d29df30a20d9" alt="Charging Load Distribution" width="800">


- **Daily EV charging Load Curve by ZIP Code (Sample)**
  <img src="https://github.com/user-attachments/assets/b6244a83-8373-485a-b7f5-ab9aa460a27b" alt="Charging Load ZIP Code" width="800">


- **Daily EV charging Load Curve for Entire Houston**
  <img src="https://github.com/user-attachments/assets/0dd377d6-353a-4b02-a82f-a4c85aac71b2" alt="Charging Load entire Houston" width="800">
