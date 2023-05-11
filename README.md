# Airline Company Data Warehouse Project

This project focuses on analyzing the flight activity and reservation processes of a major airline company. The aim of the project is to support decision-making by providing insights into the company's business processes.

## Business Processes

The following are the business processes that this project focuses on:

| Business Process | Granularity | Facts | Dimensions |
| --- | --- | --- | --- |
| Booking | Per selling ticket | Booking flight | Date, Passenger, Flight, Agency, Website, Promotion |
| Frequent Flyer Program | Per transaction (upgrading, earning or redeeming miles, respond to promotions) | Loyalty fact | Date, Flight, FQ, Points redeeming key, Passenger |
| Checking | Per inquiry | Factless table | Date, Passenger, Inquiry, Flight, Staff |
| Upgrading | Per transaction (upgrading, earning or redeeming miles, respond to promotions) | Loyalty fact | Date, Flight, FQ, Points redeeming key, Passenger |
| Cancelling | Per selling ticket | Booking flight | Date, Passenger, Flight |
| Flight | Per flight | Flight | Date, Passenger, Airplane, Pilot, Crew, Flight, Route |
| Landing/Takeoff | Per flight | Flight | Date, Passenger, Airplane, Flight, Route |
| Transit | Per flight | Flight | Date, Passenger, Airplane, Flight, Route |
| Booking Hotel | Per stay | Staying fact | Date, Flight, FQ, Hotel, Passenger |
| Car Rent | Per transaction | Factless table | Date, Passenger, Flight |
| Report Accident | Per incident | Factless table | Date, Flight |
| Maintenance | Per airplane | Factless table | Airplane |
| Report Inquiry | Per inquiry | Factless table | Date, Passenger, Inquiry, Flight, Staff |
| Promote | Per transaction (upgrading, earning or redeeming miles, respond to promotions) | Loyalty fact | Date, Flight, FQ, Points redeeming key, Passenger |
| Redeem Points | Per transaction (upgrading, earning or redeeming miles, respond to promotions) | Loyalty fact | Date, Flight, FQ, Points redeeming key, Passenger |

## Data Vault Model

The project uses the Data Vault modeling approach due to the following reasons:

- Quick data extraction: The Data Vault model is faster, and the aviation industry operates around the clock.
- Structured format: The data is presented in a structured format.
- Easy integration: Sources can be easily integrated.
- Reduce 3NF complexity: The existing data links are typically modeled by a third normal form model, which might result in a solution that is rather rigid and requires a lot of rework as new sources are added.
- Historical management and raw data persistence: The Data Vault model is perfect for historical management and raw data persistence.

### Dimensions

| Dimension | Description |
| --- | --- |
| Date | Date dimension |
| Passenger | Passenger dimension |
| Flight | Flight dimension |
| Airplane | Airplane dimension |
| Pilot | Pilot dimension |
| Crew | Crew dimension |
| Agency | Agency dimension |
| Website | Website dimension |
| Promotion | Promotion dimension |
| Hotel | Hotel dimension |
| FQ | FQ dimension |
| Inquiry | Inquiry dimension |
| Staff | Staff dimension |
| Points redeeming key | Points redeeming key dimension |

### Facts

| Fact | Description |
| --- | --- |
| Booking flight | Fact table for bookings |
| Loyalty fact | Fact table for loyalty program transactions |
| Staying fact | Fact table for hotel bookings |
| Factless table | Factless table used for checking, car rent, report inquiry, report accident, and maintenance |

## Conclusion

This project provides a comprehensive solution for analyzing the flight activity and reservation processes of a major airline company. The use of the Data Vault modeling approach provides a structured format for data presentation, easy integration, and historical management and raw data persistence.
