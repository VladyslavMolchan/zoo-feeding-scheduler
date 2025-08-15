  # Entities

## Animal
- **id** (UUID) — unique identifier
- **name** (string) — animal's name
- **species** (string) — species of the animal
- **age** (integer) — age in years

## FeedingSchedule
- **id** (UUID) — unique identifier
- **animalId** (UUID) — foreign key to Animal
- **feedingTime** (datetime) — scheduled feeding time
- **foodType** (string) — type of food
- **quantity** (string) — quantity to feed (e.g., "2 kg")

## NutritionAlert
- **id** (UUID) — unique identifier
- **animalId** (UUID) — foreign key to Animal
- **alertTime** (datetime) — time of alert
- **message** (string) — alert message content
