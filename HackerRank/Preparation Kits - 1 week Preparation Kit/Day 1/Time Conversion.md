# Time Conversion



```
def timeConversion(s):
    # Write your code here
    date_format = s.split(":")
    hour = date_format[0]
    minute = date_format[1]
    second = date_format[2][:-2]
    
    hour_clock_format = date_format[2][2:]
    
    if hour_clock_format == "PM" and int(hour) < 12:
        hour = str(int(hour) + 12)
    if hour_clock_format == "AM" and hour == "12":
        hour = "00"
    
    result = '{}:{}:{}'.format(hour, minute, second)
    
    return result
```



```
12-hour format => 24-hour format으로 시간 변환 문제
(input - 12:01:00PM -> output - 12:01:00)

우선 시 분 초로 나누고, 초에 AM/PM을 통해 시+12를 하려고 함.

1
str 형식의 input을 ":" 기호를 기준으로 배열을 받는다.
(ex. 07:05:45PM => ['07', '05', '45PM'])
2
hour, minute, second의 변수를 만들어 배열의 값을 할당한다.
(ex. hour = date_format[1]...)
3
AM/PM 정보에 따라 24-hour 포맷을 변경해야 하니, 정보 파악을 위해
hour_clock_format 변수에 해당 정보를 할당한다.
4
12AM 인 경우 => 00으로 변경되어야 하고, ~12PM까지는 +12 되어야 하기 때문에 조건문을 작성해준다.
    if hour_clock_format == "PM" and int(hour) < 12:
        hour = str(int(hour) + 12)
    if hour_clock_format == "AM" and hour == "12":
        hour = "00"
5
더할 때의 경우 input이 str 형식으로 들어왔기 때문에 형변환 해준다.
6
마지막에 {} 포맷팅으로 작성해주고, result를 return해준다.
```

