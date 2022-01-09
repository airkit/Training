# Expressions with Timestamps

**0:40 - Disabling Track a claim button**
```
IF(ISEMPTY(session.claim))
```

**3:37 session.claim.__id**
```
session.claim_statuses
```


**5:17 - Displaying Claim Statuses**
```
"{{session.claim_statuses[0].status}}"
```

**6:18 - Displaying Claim Date**
```
"{{
  FORMAT_DATE(
    session.claim_statuses
      [0]
      .created_date,
    "MMMM Do, YYYY"
  )
}}"
```

**7:11 - Displaying Claim Incident Address**
```
"{{
  session.claim
    .incident_address
}}"
```



**11:00 - Displaying List Data**
```
IF(
  ISEMPTY(
    session.claim_statuses
      [*]
  ),
  [
    {
      "__id":
        "d22edb5e-8a8f-4320-97a5-de443581b83f",
      "Claim":
        NULL,
      "created_date":
        {
          "year":
            2021,
          "month":
            10,
          "day":
            26
        },
      "status":
        "SUBMITTED"
    },
    {
      "__id":
        "d22edb5e-8a8f-4320-97a5-de443581b93f",
      "Claim":
        NULL,
      "created_date":
        {
          "year":
            2021,
          "month":
            10,
          "day":
            28
        },
      "status":
        "IN REVIEW"
    },
    {
      "__id":
        "d22edb5e-8a8f-4620-97a5-de443581b83f",
      "Claim":
        NULL,
      "created_date":
        {
          "year":
            2021,
          "month":
            10,
          "day":
            30
        },
      "status":
        "APPROVED"
    }
  ],
  session.claim_statuses[*]
)
```


**12:44 - Display list of Claim Statuses**
```
"{{
  IF(
    ISEMPTY(
      session.claim_statuses
        [0]
        .status
    ),
    "EXAMPLE STATUS",
    item.status
  )
}}"
```

**14:40 - Display Claim Status Dates**
```
"{{
  IF(
    ISEMPTY(
      session.claim_statuses
        [0]
    ),
    "EXAMPLE DATE",
    FORMAT_DATE(
      item.created_date,
      "MMMM Do, YYYY"
    )
  )
}}"
```

**17:40 - Display Other Party car**
```
"{{
  session.involved_party
    .vehicle_make
}} {{
  session.involved_party
    .vehicle_model
}}"
```

**18:09 - Display Other Party Name**
```
"{{
  session.involved_party
    .first_name
}} {{
  session.involved_party
    .last_name
}}"
```


**19:29 - actor first name**
```
actor.first_name
```

**19:40 - claim status text**
```
session.claim_statuses[0].status
```

