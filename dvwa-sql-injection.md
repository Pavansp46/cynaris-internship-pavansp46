# DVWA SQL Injection Lab

## Vulnerability
SQL Injection

## Environment
- Application: DVWA
- Security Level: Low
- Target: localhost

## Testing

### Normal Input
Input:
`1`

Result:
`ID: 1`
`First name: admin`
`Surname: admin`

### SQL Injection Test
Payload:
`1' OR '1'='1`

Result:
The application returned multiple database records instead of a single record.

## Impact
An attacker may be able to manipulate database queries and access information that should not be returned for the requested user ID.

## Mitigation
- Use prepared statements / parameterized queries.
- Validate and sanitize input.
- Avoid constructing SQL queries directly from user-supplied input.
- Apply least-privilege permissions to database accounts.

