





**2022년 2학기/객체지향프로그래밍및실습/1차 프로그래밍 과제**



**Ⅰ.소개**

**ⅰ. BoardGame1**

|**Place**|
| :-: |
|Method|Place(...) | setNext(...)|getNext(...)|getNo(...)|toString(...)|
|Argument|int|Place|null|null|null|
|return|void|void|Place|int|String|
|구현|o|o|o|o|o|


|**Board**|
| :-: |
|Method|Board(...)|getStartPlace(...)|print()|
|Argument|int|null|null|
|return|void|Place|void|
|구현|o|o|o|



**ⅱ. BoardGame2**

|**Place**|
| :-: |
|Method|Place(...)|setNext(...)|getNext(...)|getNo(...)|toString(...)|
|Argument|int|Place|null|null|null|
|return|void|void|Place|int|String|
|구현|o|o|o|o|o|



|**Board**|
| :-: |
|Method|Board(...)|getStartPlace(...)|print()|
|Argument|int|null|null|
|return|void|Place|void|
|구현|o|o|o|



|**Horse**|
| :-: |
|Method|Horse(...)|getPlace(...)|setPlace(...)|
|Argument|String, Place|null|Place|
|return|void|Place|void|
|구현|o|o|o|
|Method|getName(...)|move(...)|print(...)|
|Argument|nul|int|null|
|return|String|void|void|
|구현|o|o|o|



|**Dice**|
| :-: |
|Method|roll(...)|
|Argument|null|
|return|int|
|구현|o|

**ⅲ. BoardGame3**

|**Place**|
| :-: |
|Method|Place(...)|setNext(...)|getNext(...)|getNo(...)|toString(...)|
|Argument|int|Place|null|null|null|
|return|void|void|Place|int|String|
|구현|o|o|o|o|o|
|Method|getSkipCount(...)|setSkipCount(...)|
|Argument|null|int|
|return|int|void|
|구현|o|o|



|**Board**|
| :-: |
|Method|Board(...)|getStartPlace(...)|print(...)|
|Argument|int|null|null|
|return|void|Place|void|
|구현|o|o|o|
|Method|setSpecialLink(...)|setSkipCount(...)|iskFinalPlace(...)|
|Argument|int, int|int, int|Place|
|return|void|void|boolean|
|구현|o|o|o|



|**Horse**|
| :-: |
|Method|Horse(...)|getPlace(...)|setPlace(...)|
|Argument|String, Place|null|Place|
|return|void|Place|void|
|구현|o|o|o|
|Method|getName(...)|move(...)|print(...)|
|Argument|nul|int|null|
|return|String|void|void|
|구현|o|o|o|



|**Dice**|
| :-: |
|Method|roll(...)|
|Argument|null|
|return|int|
|구현|o|










**ⅳ. BoardGame4**

|**Place**|
| :-: |
|Method|Place(...)|setNext(...)|getNext(...)|getNo(...)|toString(...)|
|Argument|int|Place|null|null|null|
|return|void|void|Place|int|String|
|구현|o|o|o|o|o|
|Method|getSkipCount(...)|setSkipCount(...)|
|Argument|null|int|
|return|int|void|
|구현|o|o|



|**Board**|
| :-: |
|Method|Board(...)|getStartPlace(...)|print(...)|
|Argument|int|null|null|
|return|void|Place|void|
|구현|o|o|o|
|Method|setSpecialLink(...)|setSkipCount(...)|iskFinalPlace(...)|
|Argument|int, int|int, int|Place|
|return|void|void|boolean|
|구현|o|o|o|



|**Horse**|
| :-: |
|Method|Horse(...)|getPlace(...)|setPlace(...)|
|Argument|String, Place|null|Place|
|return|void|Place|void|
|구현|o|o|o|
|Method|getName(...)|move(...)|print(...)|yourTurn(...)|
|Argument|nul|int|null|null|
|return|String|void|void|boolean|
|구현|o|o|o|o|



|**Dice**|
| :-: |
|Method|roll(...)|
|Argument|null|
|return|int|
|구현|o|






Ⅱ.설계

**ⅰ. BoardGame1**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.001.png)

**<BoardGame1 UML class diagram>**

\- Place.Place(int n) : 생성하는 Place 객체의 번호(No)를 n으로 설정한다. 

\- Place.setNext(Place p) : Place 객체 p를 다음 칸(Next Place)으로 설정한다. 

\- Place Place.getNext() : Next Place 객체를 반환한다. 

\- int Place.getNo() : Place 객체의 No를 반환한다. 

\- String Place.toString() : Place 객체의 No 값과 다음 칸의 번호 값을 포함한 Place 객체의 정보를 하나의 String으로 만들어 반환한다. Finish Place라면 Next No. 정보 대신 null을 넣는다.

\- Board.Board(int N) : 1~N의 번호를 가지는 Place 객체 N개를 만들어 번호순으로 연결한다. Start Place를 No값이 1인 Place 객체로 설정한다. 

\- Place Board.getStartPlace() : Start Place 객체를 반환한다. 

\- void Board.print() : 칸의 개수와 모든 Place들을 순서대로 print한다.

**ⅱ. BoardGame2**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.002.png)

**<BoardGame2 UML class diagram>**

\- Horse.Horse(String n, Place p) : Horse 객체를 생성하면서 name과 place를 설정한다. 

\- Place Horse.getPlace() : 현재 위치를 반환한다. 

\- void Horse.setPlace(Place p) : 현재 위치를 p로 설정한다. 

\- String Horse.getName() : name를 반환하다. 

\- void Horse.move(n) - 말을 현재 칸에서 n칸 이동시킨다. 이동 중 Finish Place를 만나면 Finish Place에 Horse를 두고 이동을 종료한다. 

\- Horse.print() - Horse의 name과 Place No를 출력한다. 

\- int Dice.roll() - 임의의 주사위 값(1-6)을 반환한다. (static method)




**ⅲ. BoardGame3**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.003.png)

**<BoardGame3 UML class diagram>**

\- String Place.toString() : Place와 Next Place 번호 외에 special link 및 skip count도 반환 String에 포함하도록 단계 1의 toString()을 수정한다. 단, Finish Place와 같이 next link가 없다면 0으로 표시하고, special link가 없다면 0으로 표시한다.

\- int Place.getSkipCount() : Place의 Skip Count를 반환한다.

\- void Place.setSkipCount(int n) : Place의 Skip Count를 설정한다.

\- void Board.setSpecialLink(m, n) : m번-Place에 n번-Place로 가는 Special Link 설정한다.

\- void Board.setSkipCount(n, k) : n번-Place에 Skip Count를 k로 설정한다.

\- boolean Board.isFinalPlace(Place p) : p가 Finish Place이면 true, 아니면 false를 반환한다.

**ⅳ. BoardGame4**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.004.png)

**<BoardGame4 UML class diagram>**

\- Horse.yourTurn() : Horse 객체가 자신의 turn을 실행하는 메소드로 주사위를 던져 말의 이동을 처리한다. 이동 중에 종료 칸에 도달하면 true를 반환하고, 그렇지 않으면 false를 반환한다. Special Link가 있는 Place에 도착한다면 다음턴에 해당 Link를 타고 이동하고, Skip Count가 있는 Place에 도착한다면 해당 count만큼 턴을 쉬도록 설정한다.


Ⅲ.실행결과

**ⅰ. BoardGame1**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.005.png)

**<BoardGame1 실행결과1>**

\1) Place를 5개 연결하는 Board객체 bd를 만든다.

\2) Board의 시작 지점을 출력, 시작 지점의 NextPlace 출력, Board 전체를 차례로 출력한다.


**ⅱ. BoardGame2**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.006.png)

**<BoardGame2 실행결과1>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 이름이 “Rosinante”, Place가 시작지점인 Horse객체를 생성한 후 Horse 정보를 출력한다. 

\3) roll()메소드를 통해 주사위를 굴리고 눈금 수를 출력한다. (눈금 수: 4)

\4) 눈금수 만큼 move()메소드를 통해 이동시키고 Horse가 도착한 Place를 출력한다.

(No.1에서 dice value = 4이므로 No.5 Place로 이동)

**5) Horse를 강제로 한칸 앞으로 이동시킨다.**

**(No.5에서 No.6 Place로 이동)**

**6) 3번~4번을 한 번더 반복한다.** 

**(No.6에서 dice value = 4이므로 No.10 Place로 이동)**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.007.png)

**<BoardGame2 실행결과2>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 이름이 “Rosinante”, Place가 시작지점인 Horse객체를 생성한 후 Horse 정보를 출력한다. 

\3) roll()메소드를 통해 주사위를 굴리고 눈금 수를 출력한다. (눈금 수: 1)

\4) 눈금수 만큼 move()메소드를 통해 이동시키고 Horse가 도착한 Place를 출력한다.

(No.1에서 dice value = 1이므로 No.2 Place로 이동)

\5) Horse를 강제로 한칸 앞으로 이동시킨다.

(No.2에서 No.3 Place로 이동)

\6) 3번~4번을 한 번더 반복한다. 

(No.3에서 dice value = 5이므로 No.8 Place로 이동)










**ⅲ. BoardGame3**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.008.png)

**<BoardGame3 실행결과1>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 4번 Place에 Skip Count를 1로 설정, 8번 Place에 Skip Count를 2로 설정, 5번 Place에 10번 Place로 가는 Special Link 설정, 9번 Place에 15번 Place로 가는 Special Link 설정, 12번 Place에 7번 Place로 가는 Special Link 설정한다.

\3) 이름이 “Rosinante”, Place가 시작지점인 Horse객체를 생성한 후 출력한다..

\4) Horse의 Place가 마지막 칸일 때까지 주사위를 굴려 Horse를 이동시킨다.

\5) Special Link나 Skip count가 있는 칸이 없으므로 특별한 이동이나 정지 없이 마지막 칸까지 이동한다.

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.009.png)

**<BoardGame3 실행결과2>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 4번 Place에 Skip Count를 1로 설정, 8번 Place에 Skip Count를 2로 설정, 5번 Place에 10번 Place로 가는 Special Link 설정, 9번 Place에 15번 Place로 가는 Special Link 설정, 12번 Place에 7번 Place로 가는 Special Link 설정한다.

\3) 이름이 “Rosinante”, Place가 시작지점인 Horse객체를 생성한 후 출력한다..

\4) Horse의 Place가 마지막 칸일 때까지 주사위를 굴려 Horse를 이동시킨다.

\5) No.8 Place에서 Skip Count가 2로 설정되어 있으므로, 2턴 쉬었지만, continue이기 때문에 2턴 쉬고 나서 dice를 굴린 결과 값이 나온다.

\6) No.9 Place에서 No.15로 Special Link가 설정되어 있으므로, dice value 4가 나왔을 때 No.18 Place로 이동한다.

**ⅳ. BoardGame4**

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.010.png)

**<BoardGame4 실행결과1>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 4번 Place에 Skip Count를 1로 설정, 8번 Place에 Skip Count를 2로 설정, 5번 Place에 10번 Place로 가는 Special Link 설정, 9번 Place에 15번 Place로 가는 Special Link 설정, 12번 Place에 7번 Place로 가는 Special Link 설정한다.

\3) 두 개의 Horse 객체를 만들어서 시작 지점에 놓는다.

\4) 차례로 번갈아 가며 주사위를 돌리고, Special Link가 있으면 다음 턴에 해당 Place를 따라 이동하고, Skip count가 있으면 count턴 만큼 쉰다.

(Horse 1은 No.4 Place에서 skip count 1을 만났으므로, 1턴 동안 No.4에 있다)

(Horse 2는 No.9 Place에서 No.15로 연결된 Special Link를 만났으므로, 다음턴에 No.15로 연결된 Link를 따라 이동해서 No.15로 이동했다) 

(Horse 1은 No.8 Place에서 skip count 2을 만났으므로, 2턴 동안 No.8에 있다)

\5) Horse 2가 먼저 마지막 칸에 도착하여서 2번째 말이 승리했다.

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.011.png)

**<BoardGame4 실행결과2>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 4번 Place에 Skip Count를 1로 설정, 8번 Place에 Skip Count를 2로 설정, 5번 Place에 10번 Place로 가는 Special Link 설정, 9번 Place에 15번 Place로 가는 Special Link 설정, 12번 Place에 7번 Place로 가는 Special Link 설정한다.

\3) 두 개의 Horse 객체를 만들어서 시작 지점에 놓는다.

\4) 차례로 번갈아 가며 주사위를 돌리고, Special Link가 있으면 다음 턴에 해당 Place를 따라 이동하고, Skip count가 있으면 count턴 만큼 쉰다.

(Horse 2는 No.4 Place에서 skip count 1을 만났으므로, 1턴 동안 No.4에 있다)

(Horse 1은 No.8 Place에서 skip count 2을 만났으므로, 2턴 동안 No.8에 있다)

(Horse 2는 No.12 Place에서 No.7로 연결된 Special Link를 만났으므로, 다음턴에 No.7로 연결된 Link를 따라 이동해서 No.11로 이동했다) 

\5) Horse 1이 먼저 마지막 칸에 도착하여서 1번째 말이 승리했다.

![](Aspose.Words.bbf9a719-eaed-455a-9391-79d7d5d77022.012.png)

**<BoardGame4 실행결과3>**

\1) Place를 20개 연결하는 Board객체 bd를 만든다.

\2) 4번 Place에 Skip Count를 1로 설정, 8번 Place에 Skip Count를 2로 설정, 5번 Place에 10번 Place로 가는 Special Link 설정, 9번 Place에 15번 Place로 가는 Special Link 설정, 12번 Place에 7번 Place로 가는 Special Link 설정한다.

\3) 두 개의 Horse 객체를 만들어서 시작 지점에 놓는다.

\4) 차례로 번갈아 가며 주사위를 돌리고, Special Link가 있으면 다음 턴에 해당 Place를 따라 이동하고, Skip count가 있으면 count턴 만큼 쉰다.

(Horse 2는 No.5 Place에서 No.10으로 연결된 Special Link를 만났으므로, 다음턴에 No.10으로 연결된 Link를 따라 이동해서 No.12로 이동했다) 

(Horse 1은 No.9 Place에서 No.15로 연결된 Special Link를 만났으므로, 다음턴에 No.15로 연결된 Link를 따라 이동해서 No.20으로 이동했다) 

\5) Horse 1이 먼저 마지막 칸에 도착하여서 1번째 말이 승리했다.




Ⅳ.결론

` `자바에서 서로 다른 클래스의 메소드를 이용할 때, 같은 클래스 내에 public으로 선언되어 있으면 접근할 수 있지만, 다른 클래스의 메소드를 이용할 때에는 import를 이용하여야 한다는 것을 알게 되었다. 또한, 자바라는 언어에서는 여러 클래스들을 선언하여 객체를 만들고 이러한 객체를 중심으로한 프로그래밍을 하면서, main함수에서 객체생성, 메소드 호출 등 코드가 더 간결하고 알아보기 쉬웠다.

` `과제를 하면서 어려웠던 점은, 마지막 칸의 next place를 어떻게 처리할지였다. 처음 코드에서는 No.0 Place를 쓰지 않아서 마지막 칸의 다음 칸을 0번으로 설정했었는데, 0보다는 아무것도 넣지 않을 때 default값이 null이 되기 때문에 이를 이용하여 toString을 할 때 if문을 넣어서 만약 nextPlace의 값이 null이라면 nextNo를 null으로 나오게 하였다. 






