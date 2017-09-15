# [python] String left, right, center sorting
---
- ljust(), rjust(), center()
  - 지정한 자리수에 맞춰 공백 또는 문자열로 채워짐
#### ljust() 함수 :  왼쪽 정렬
```
str = "I Love Marvel"
print(str.ljust(20))
# result : I Love Marvel

print(str.ljust(20, '#'))
# result : I Love Marvel#######
```

#### rjust() 함수 :  오른쪽 정렬
```
str = "I Love Marvel"
print(str.rjust(20))
# result :         I Love Marvel

print(str.rjust(20, '#'))
# result : #######I Love Marvel
```

#### center() 함수 :  가운데 정렬
```
str = "I Love Marvel"
print(str.center(20))
# result :   I Love Marvel

print(str.center(20, '#'))
# result : ###I Love Marvel####
```
