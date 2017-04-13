You're building a restaurant table reserving app that allows users to reserve tables for specified numbers of people. The app will need to show only tables that are available and the times they are available. The app will need to store reservations under a given name with a phone number and number of guests.

reservations {
  id: int
  TableNumber: int (not already reserved, valid number in tableIDs)
  Name: string (normal word chars)
  Seats: int (2-8)
  PhoneNumber: string of numbers (xxx) xxx-xxxx
  ArrivalTime: date (start of the hour)
}

table {
  id: int (matches tableIDs in allTables)
  Seats: int (matches number of seats for table)
  Reservations: [resid, resid]
  AvailableTimes: [hour blocks 5-9PM] (ints)
}

allTables {
  tableIDs: [ints] (reference the restaurant table numbers)
  availableTables: [ids for tables] (updated for every reservation)
}
