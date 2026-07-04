# Schema Specification

## Organizations

| Поле | Тип | Обязательное | Уникальное |
|------|-----|--------------|------------|
| OrganizationID | String | Да | Да |
| ShortName | String | Да | Нет |
| FullName | String | Да | Нет |
| INN | String | Да | Да |
| KPP | String | Нет | Нет |
| OGRN | String | Нет | Нет |
| TaxSystem | Enum | Да | Нет |
| Status | Enum | Да | Нет |

---

## Clients

| Поле | Тип |
|------|-----|
| ClientID | String |
| OrganizationID | String |
| Name | String |
| INN | String |
| Phone | String |
| Email | String |
| Address | String |
| ManagerID | String |
| Rating | Number |
| Status | Enum |

---

## Vehicles

| Поле | Тип |
|------|-----|
| VehicleID | String |
| OrganizationID | String |
| PlateNumber | String |
| Brand | String |
| Model | String |
| VIN | String |
| DriverID | String |
| Status | Enum |

---

## Trips

### Основные поля

- TripID
- OrganizationID
- RequestID
- ClientID
- VehicleID
- DriverID
- ManagerID

### Маршрут

- LoadingPoint
- UnloadingPoint
- Distance
- Cargo

### Финансы

- Revenue
- PlannedCost
- ActualCost
- Margin

### Экспедирование

- Expedition
- CarrierID

### Документы

- MailTrack
- OriginalReceived
- DocumentsReceivedDate

### Статус

- Status

---

## Payments

- PaymentID
- InvoiceID
- TripID
- OrganizationID
- Amount
- PaymentDate
- PaymentMethod
- Type

---

## Общие поля

Все сущности содержат:

- CreatedAt
- UpdatedAt
- CreatedBy
- UpdatedBy
- Version
- Deleted
- Status
