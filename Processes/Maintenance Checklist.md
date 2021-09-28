# Maintenance Checklist

## Security

### Functions

- [ ] The application has disabled function calls
- [ ] The application has deprecated function calls

### Integrity

#### Frameworks

- [ ] PHP framework integrity is valid
- [ ] JS framework integrity is valid

#### Modules

- [ ] Module models integrity is valid
- [ ] Module views integrity is valid
- [ ] Module controller integrity is valid
- [ ] Module themes integrity is valid

#### Application

- [ ] Core application integrity is valid
- [ ] Core model integrity is valid
- [ ] Default applications integrity is valid (e.g. API, Backend)

### Unicode

#### Frameworks

- [ ] PHP framework has no unicode
- [ ] JS framework has no unicode

#### Modules

- [ ] Module models have no unicode
- [ ] Module views have no unicode
- [ ] Module controller have no unicode
- [ ] Module themes have no unicode

#### Application

- [ ] Core application has no unicode
- [ ] Core models have no unicode
- [ ] Default applications have no unicode

## Database

- [ ] Database seems healthy
- [ ] If cache is used, at least 50% of the requests hit the cache (query cache, data cache)
- [ ] Average database response times are less than 50ms
- [ ] The server hardware and assigned resources fulfill the recommendations

## Application

- [ ] The application usage feels normal (decent response time, no errors, etc.)
- [ ] The server has at least 50% of free storage space available

### Updates

- [ ] The application has the newest version
- [ ] The customer requested to update the application
- [ ] The customer is informed to create a backup first
- [ ] The application is updated during the maintenance

### Logs

- [ ] Has logs: _____________________________________________
- [ ] Logs are sent to OMS after approval from customer for further checks

#### Levels

| Level       | Count |
| ----------- | ----- |
| Emergencies |       |
| Criticals   |       |
| Errors      |       |
| Warnings    |       |
| Alerts      |       |
| Notices     |       |
| Info        |       |
| Debug       |       |

## Closing

Date:

Performed by (OMS):

Customer name:

Supervised by (customer):