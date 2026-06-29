# Feature: Hotel Search & Filtering Module

## Use Case: Search Hotels

This activity diagram illustrates the hotel search process in the TravelMate platform. The main participants are the traveler and the TravelMate system. The workflow shows how the user enters search criteria, the system retrieves and processes hotel data, and the search results are displayed.

```mermaid
flowchart TD
    A([Start]) --> B[Traveler enters destination, dates and guest information]
    B --> C[System validates search parameters]
    C --> D[Query hotel database and Channel Manager APIs]
    D --> E[Retrieve available hotels and prices]
    E --> F[Prioritize recommended partner hotels]
    F --> G[Apply marketing badges]
    G --> H[Display hotel cards with total price, rating, photo and distance]
    H --> I{View on map?}
    I -- Yes --> J[Display interactive map with price pins]
    I -- No --> K[Display hotel list]
    J --> L([End])
    K --> L
```
