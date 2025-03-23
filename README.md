<!-- @format -->

# Philippine Standard Geographic Code (PSGC)

The **Philippine Standard Geographic Code (PSGC)** is a systematic
classification and coding system for geographical locations in the Philippines.
Maintained by the **Philippine Statistics Authority (PSA)**, it serves as the
official reference for administrative divisions, including regions, provinces,
cities, municipalities, and barangays.

---

## Data Structure

The PSGC database follows a hierarchical structure:

### **Regions**

```json
{
	"id": 1,
	"created_at": "2023-05-02T19:38:38.000000Z",
	"updated_at": "2023-05-02T19:38:38.000000Z",
	"name": "Region I (Ilocos Region)",
	"code": "0100000000"
}
```

Each region is uniquely identified by a region code.

### **Provinces**

```json
{
	"id": 1,
	"created_at": "2023-05-02T19:38:38.000000Z",
	"updated_at": "2023-05-02T19:38:38.000000Z",
	"name": "Ilocos Norte",
	"code": "0102800000",
	"region_id": 1
}
```

Provinces belong to a specific region, as indicated by the region_id.

### **Cities**

```json
{
	"id": 5,
	"created_at": "2023-05-02T19:38:39.000000Z",
	"updated_at": "2023-05-02T19:38:39.000000Z",
	"name": "City of Batac",
	"code": "0102805000",
	"zip_code": "",
	"district": "Lone",
	"type": "City",
	"region_id": 1,
	"province_id": 1
}
```

Cities belong to a region and a province, referenced by region_id and
province_id.

### **Cities Municipalities**

```json
{
	"id": 1,
	"created_at": "2023-05-02T19:38:38.000000Z",
	"updated_at": "2023-05-02T19:38:38.000000Z",
	"name": "Adams",
	"code": "0102801000",
	"zip_code": "",
	"district": "Lone",
	"type": "Mun",
	"region_id": 1,
	"province_id": 1
}
```

Cities Municipalities are distinct from regular municipalities and belong to a
region and a province, referenced by region_id and province_id.

### **Municipalities**

```json
{
	"id": 1,
	"created_at": "2023-05-02T19:38:38.000000Z",
	"updated_at": "2023-05-02T19:38:38.000000Z",
	"name": "Adams",
	"code": "0102801000",
	"zip_code": "",
	"district": "Lone",
	"type": "Mun",
	"region_id": 1,
	"province_id": 1
}
```

Municipalities belong to a region and a province, referenced by region_id and
province_id.

### **Sub-Municipalities**

```json
{
	"id": 1350,
	"created_at": "2023-05-02T19:39:22.000000Z",
	"updated_at": "2023-05-02T19:39:22.000000Z",
	"name": "Tondo I/II",
	"code": "1380601000",
	"zip_code": "",
	"district": "Lone",
	"type": "SubMun",
	"region_id": 14,
	"province_id": 65
}
```

Sub-municipalities also belong to a region and a province.

### **Barangays**

```json
{
	"id": 1,
	"created_at": "2023-05-02T19:38:38.000000Z",
	"updated_at": "2023-05-02T19:38:38.000000Z",
	"name": "Adams",
	"code": "0102801001",
	"status": "Active",
	"region_id": 1,
	"province_id": 1,
	"city_municipality_id": 1
}
```

Barangays are the smallest administrative unit and belong to a region, province,
and city/municipality.

---

## Official PSGC Source

Visit the **Philippine Statistics Authority (PSA) PSGC database**:
[PSGC Website](https://psa.gov.ph)

## ⚡ Usage

- Used for government planning, statistics, and geographic classification.
- Essential for address standardization in logistics, census, and data
  management.

## License

This dataset is publicly available under the **Philippine Statistics Authority
(PSA)** data policy.

## Contributors

Maintained and updated by the **Philippine Statistics Authority (PSA)**.
Contributions are welcome!

Stay updated with official PSGC revisions!
