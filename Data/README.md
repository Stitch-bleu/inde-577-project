## Data Description

### 1. `gender_submission.csv`
This dataset contains sample predictions for the Titanic dataset, indicating whether a passenger survived based on their ID. It’s commonly used as a benchmark in classification tasks related to the Titanic dataset.

- **Fields**:
  - `PassengerId`: Unique identifier for each passenger.
  - `Survived`: Survival status (0 = No, 1 = Yes).

### 2. `day.csv`
This dataset provides daily bike rental data, capturing weather conditions, dates, and user counts. It’s useful for time series and regression analysis to understand factors influencing bike rentals.

- **Fields**:
  - `instant`: Record index.
  - `dteday`: Date in YYYY-MM-DD format.
  - `season`: Season (1 = winter, 2 = spring, 3 = summer, 4 = fall).
  - `yr`: Year (0 = 2011, 1 = 2012).
  - `mnth`: Month (1 to 12).
  - `holiday`: Whether the day is a holiday (0 = No, 1 = Yes).
  - `weekday`: Day of the week (0 = Sunday, 6 = Saturday).
  - `workingday`: If it’s a working day (0 = No, 1 = Yes).
  - `weathersit`: Weather situation (1 = clear, 2 = mist, 3 = light snow/rain, 4 = heavy rain/ice).
  - `temp`: Normalized temperature in Celsius.
  - `atemp`: Normalized "feels like" temperature.
  - `hum`: Normalized humidity.
  - `windspeed`: Normalized wind speed.
  - `casual`: Count of casual (non-registered) users.
  - `registered`: Count of registered users.
  - `cnt`: Total daily bike rental count (casual + registered).

### 3. `train.csv`
This dataset is part of the Titanic survival prediction dataset, providing passenger details for training models to predict survival.

- **Fields**:
  - `PassengerId`: Unique identifier for each passenger.
  - `Survived`: Survival status (0 = No, 1 = Yes).
  - `Pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd).
  - `Name`: Full name of the passenger.
  - `Sex`: Gender of the passenger.
  - `Age`: Age of the passenger.
  - `SibSp`: Number of siblings/spouses aboard.
  - `Parch`: Number of parents/children aboard.
  - `Ticket`: Ticket number.
  - `Fare`: Ticket fare.
  - `Cabin`: Cabin number (if available).
  - `Embarked`: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

---

