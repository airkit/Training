# Expressions with Timestamps

**5:58 - Sending customer object to AirData**
```
[ customer ]
```

**7:14 - Transform - grabbing ID of saved Customer**
```
airData.results[0].__id
```

**10:31 - Passing Claim to AirData**
```
[ claim ]
```

**11:12 - Transform - grabbing ID of saved Claim **
```
airData.results[0].__id
```

**14:12 - Sending Involved Party to AirData**
```
[ involved_party ]
```

**14:25 - Sending Involved Party to AirData**
```
airData.results[0].__id
```

**15:12 - Sending Involved Party to AirData**
```
[
  {
    "Claim":
      claim_id,
    "status":
      "SUBMITTED",
    "created_date":
      NOW().date
  }
]
```

**17:28 - session.customer**
```
{
  "first_name":
    first_name,
  "last_name":
    last_name,
  "policy_type":
    policy_type,
  "policy_number":
    policy_number,
  "phone":
    phone
}
```

**18:25 - session.customer**
```
session.customer.__id
```

**19:18 - session.incident_details_1**
```
{
  "incident_address":
    location.formattedAddress,
  "incident_time":
    time_input,
  "incident_date":
    date_input,
  "am_pm":
    am_pm
}
```

**20:04 - session.incident_details_2**
```
{
  "Customer":
    session.customer.__id,
  "created_date":
    NOW(),
  "incident_damaged_areas":
    activity.selected,
  "incident_damage_further_details":
    activity.text_area,
  "photo_damage":
    activity.media_upload
}
```

**20:22 - session.claim**
```
MERGE_OBJECTS(
  session.incident_details_1,
  session.incident_details_2
)
```


**21:17 - session.involved_party**
```
{
  "first_name":
    activity.first_name,
  "last_name":
    activity.last_name,
  "vehicle_year":
    activity.year_dropdown,
  "vehicle_make":
    activity.make_dropdown,
  "vehicle_model":
    activity.model_dropdown,
  "insurance_provider":
    activity.insurance_dropdown,
  "policy_number":
    activity.policy_number,
  "insurance_document":
    activity.upload_insurance_documents,
  "drivers_license":
    activity.upload_drivers_license,
  "phone":
    activity.phone,
  "claim":
    session.claim.__id
}
```
