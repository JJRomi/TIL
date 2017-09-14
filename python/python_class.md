# [python] class, exception 관련 사용법
---

#### __클래스, 인스턴스__

```
  # 클래스 선언
    class Marvel():
      ''' 마블 '''
  # 인스턴스 생성
    marvel1 = Marvel()
    marvel2 = Marvel()

  # 클래스와 인스턴스를 이용하면 데이터와 코드를 쉽게 포장할 수 있다.
```

#### __모델링__
클래스로 현실 개념을 표현
```
  class Marvel():
    '''마블'''

  marvel1 = Marvel()
  marvel1.name = 'Iron Man'

  def create_marvel(name):
    marvel = Marvel()
    marvel.name = name
    return marvel
```

#### __메소드__
함수와 비슷
클래스에 묶여서 클래스의 인스턴스와 관계되는 일을 하는 함수
```
  # self : 메소드의 첫번째 인자 , 인스턴스의 매개변수를 전달할 때는 self 매개변수는 생략하고 전달

  class Marvel():
    '''마블'''
    def create(name, power):
      marvel = Marvel()
      marvel.name = name
      marvel.power = power
      return marvel

    def power_up(self) :
      self.power += 1
      print("{} power : {}".format(self.name, self.power))


  iron = Marvel.create('Iron', 1000)
  iron.power_up()

```

#### __특수한 메소드__

##### __초기화 함수__
__init__ : 인스턴스를 만들 때 실행되는 함수

##### __문자열화 함수__
__str__ : 인스턴스 자체를 출력 할 때의 형식을 지정해주는 함수
```
class Marvel():
  '''마블'''
  def __init__(name, power):
    marvel.name = name
    marvel.power = power

  def __str__(self) :
    self.power += 1
    print("{} power : {}".format(self.name, self.power))
```

#### __상속__
자식 클래스가 부모 클래스의 내용을 가져다 쓸 수 있음
```
class Marvel( ):
    def fight( self ):
        print( "싸운다" )

    def eat( self ):
        print( "먹는다" )

class Iron( Marvel ):
    def power( self ):
        print( "운동한다" )


iron = Iron()
iron.fight()

```

#### __오버라이드(Override)__
```
class Marvel( ):
    def fight( self ):
        print( "싸운다" )

    def eat( self ):
        print( "먹는다" )

class Iron( Marvel ):
    def eat( self ):
        print("맛있게 먹는다")

    def power( self ):
        print( "운동한다" )

```

#### __super()__
자식클래스에서 부모클래스의 내용을 사용하고 싶은 경우
```
class Marvel( ):
    def __init__( self, name ):
          self.name = name

class Iron( Marvel ):
    def __init__( self, name, hand ):
          super().__init__( name ) # 부모클래스의 __init__ 메소드 호출
          self.hand = hand

```

#### __예외 정의__
사용자가 직접 예외처리를 하면 코드의 직관성을 높일 수 있다.
파일을 하나 만들어 예외를 정의
Exception 클래스를 상속받아 만든다.
```
try:
  에러가 발생할 가능성이 있는 코드
except Exception: # 에러종류
  에러 이름을 모르는 경우에는
  except Exception: 으로 사용 가능
  에러가 발생 했을 경우 처리할 코드
```

##### __파일에서 불러올 경우__

from 예외클래스명 import 파일명
