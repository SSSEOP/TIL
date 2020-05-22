# DateType
----------------
## TIME
- 시간을 저장할 수 있는 타입
- 기본 형식은 'HH:MM:SS'나 'HHH:MM:SS'
- 저장할 수 있는 시간의 범위는 '-838:59:59' ~ '838:59:59'

## DATE
- 날짜를 저장할 수 있는 타입
- 기본 형식은 'YYYY-MM-DD'
- 저장할 수 있는 날짜의 범위는 '1000-01-01' ~ '9999-12-31'

## DATETIME
- 날짜와 함께 시간까지 저장할 수 있는 타입
- 기본 형식은 'YYYY-MM-DD HH:MM:SS'
- 저장할 수 있는 범위는 '1000-01-01 00:00:00' ~ '9999-12-31 23:59:59'

## TIMESTAMP
- 날짜와 시간을 나타내는 타임스탬프를 저장할 수 있는 타입
- 사용자가 별다른 입력을 주지 않으면, 데이터가 마지막으로 입력되거나 변경된 시간이 저장
- 저장할 수 있는 범위는 '1970-01-01 00:00:01' UTC ~ '2038-01-19 03:14:07' UTC

----------------
## DATETIME DEFAULT로 현재시간 입력
```sql
c_date DATETIME DEFAULT CURRENT_TIMESTAMP
```