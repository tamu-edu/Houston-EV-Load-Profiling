# Data-Driven Estimation of Residential EV Charging Loads: Houston, TX

## Overview
This repository provides realistic residential electric vehicle (EV) charging load data for the Houston, Texas area. It includes both the original dataset used for generating synthetic data and the resulting synthetic charging load data.

## Features
### Training Dataset
#### Sampled Electric Vecicle Data
- `vehicle_id`: An anonymized identifier for each vehicle.
- `vehicle_type`: Classification of the vehicle (e.g., Passenger Car, Bus, Multipurpose Vehicle).
- `electrification_level`: Specifies whether the vehicle is a BEV (Battery Electric Vehicle) or PHEV (Plug-in Hybrid Electric Vehicle).
- `state`: Indicates the vehicle's registered state (e.g., Texas).
- **Datasource**: EVWatts

#### Sampled Electric Vehicle Charging Sessions Data
- `id`: Unique identifier for each charging session.
- `vehicle_id`: Anonymized identifier linking to the vehicle data.
- `start_datetime`: Start time of the charging session, formatted as `MM/DD/YY hh:mm`.
- `stop_datetime`: End time of the charging session, formatted as `MM/DD/YY hh:mm`.
- **Datasource**: EVWatts

#### Houston EV Registration Data
- Provides detailed EV registration data for Houston, Texas.
- `zipcode`: The ZIP code associated with each registration.
- `carname`: The name or model of the registered vehicle.
- `evcount`: The number of EVs registered within each ZIP code.
- **Datasource**: Texas Department of Transportation (TXDoT)


### Synthetic Residential EV Charging Load Data
- Synthetic data contains 10-minute interval residential EV charging loads for all ZIP codes in Houston, Texas.
- Data Generation:
  - Based on the charging curves derived from the training dataset.
  - Combined with Houston EV registration data and battery specifications for each EV.
- Assumptions:
  - Each household is equipped with a Level 2 home charger rated at 7 kW.

- Representative Charging Patterns for Houston, Texas (Probability)
![image](https://github.com/user-attachments/assets/c746f47b-374d-4c8d-a3ae-22433ad780ce)

- Charging Load Distribution during Peak Hour in Houston, Texas
![image](https://github.com/user-attachments/assets/f0ff0359-58ef-42f0-ab35-d29df30a20d9)

- Daily EV charging Load Curve for each Zipcode (Sampled)
![image](https://github.com/user-attachments/assets/b635a2df-f262-4c65-b80e-91492b3477c0)

- Daily EV Charging Load Curve for Houston, Texas
![image](https://github.com/user-attachments/assets/abc5facd-04c3-4239-ab9b-4140e4775232)

