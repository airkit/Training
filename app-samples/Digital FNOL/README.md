#Expressions with Timestamps

**5:44 - Adding Progress Bar**
```
([  "Personal Info",  "Incident Details",  "Involved Parties",  "Submit Claim"])
```

**9:00 - Passing Address Data to Map Control**
```
([  {    "longitude":      activity.location.longitude,    "latitude":      activity.location.latitude  }])
```

**15:42 - Create Incident Details 2 with Multi Select Checkboxes**
```
([  "Hood",  "Front Bumper",  "Front passenger side fender",  "Passenger door",  "Rear assenger side quarter panel",  "Rear bumper",  "Rear/Trunk",  "Rear driver side quarter panel",  "Passenger door",  "Roof",  "Undercarriage",  "Other"]) 
```

**19:45 - Insurance Providers dropdown**
```
(["Insurance Provider 1", "Insurance Provider 2", "Insurance Provider 3", "Insurance Provider 4"])
```
**20:45 - Years Dropdown for Vehicles**
```
([
  "2021",
  "2020",
  "2019",
  "2018",
  "2017",
  "2016",
  "2015",
  "2014",
  "2013",
  "2012",
  "2011",
  "2010",
  "2009",
  "2008",
  "2007",
  "2006",
  "2005",
  "2004",
  "2003",
  "2002",
  "2001",
  "2000",
  "1999",
  "1998",
  "1997",
  "1996",
  "1995",
  "1994",
  "1993",
  "1992",
  "1991",
  "1990",
  "1989",
  "1988",
  "1987",
  "1986",
  "1985",
  "1984",
  "1983",
  "1982",
  "1981",
  "1980",
  "1979",
  "1978",
  "1977",
  "1976",
  "1975",
  "1974",
  "1973",
  "1972",
  "1971",
  "1970",
  "1969",
  "1968",
  "1967",
  "1966",
  "1965",
  "1964",
  "1963",
  "1962",
  "1961",
  "1960",
  "1959",
  "1958",
  "1957",
  "1956",
  "1955"
]
)
```
**21:25 - Target URL for Makes**
("https://vpic.nhtsa.dot.gov/api/vehicles/GetMakesForVehicleType/car?format=json")

23:12 - Target URL for Models
(“"https://vpic.nhtsa.dot.gov/api/vehicles/GetModelsForMakeYear/make/{{make}}/modelyear/{{year}}?format=json"”)

**24:18 - Transform**
```
(result.Results[*].Model_Name)
```
