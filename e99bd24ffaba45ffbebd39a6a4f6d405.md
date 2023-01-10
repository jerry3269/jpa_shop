**[객체지향프로그래밍및실습 -- 14주차 실습활동지]{.ul}**

성명: 양지웅 학과: 소프트웨어 학번: 201920810 실습반번호: 1반

1\.

가)

\<수정한코드\>

Iterator\<String\> iterator = list.iterator();\
while(iterator.hasNext())\
{\
String str = iterator.next();\
System.*out*.print(str +\" \");\
}

나) NoSuchElementException이 발생한다

그 이유는 true를 하면 무한 루프를 돌게 되는데 iterater의 next가 더 이상
없으면 NoSuchElementException가 발생한다.

다)

iterater에서 해당 요소를 삭제하지 않고, collection1에서 삭제를 하면
index의 변동이 생길수 있기 때문에 해당 exception이 발생한다.

라) linked list는 arraylist와 달리 list인터페이스를 구현한
abstractlist를 상속하지 않고 abstractSequentialList 를 상속하고 있다.
Arraylist는 데이터들이 순서대로 쭉 늘어선 배열의 형식을 취하고 있는 반면
linkedlist는 순서대로 늘어선 것이 아니라 자료의 주소값으로 서로
연결하되어 있는 구조를 하고 있다.

Arraylist는 삭제시 index가 변동되어 오류가 발생하지만 linkedlist는
삭제시 주소값이 나타내는 값만 변동되기 때문에 삭제가 용이하다.

2\.

가)

\<메소드 코드\>

private static void makeList(LinkedList\<String\> list, String\[\]
colors){\
\
ListIterator\<String\> listIterator = list.listIterator();\
for (String color : colors) {\
listIterator.add(color);\
}\
\
}

\<실행결과\>

![텍스트이(가) 표시된 사진 자동 생성된
설명](vertopal_e99bd24ffaba45ffbebd39a6a4f6d405/media/image1.png){width="3.3919608486439197in"
height="1.1834361329833771in"}

나)

\<메소드코드\>

private static void removeDuplicates(LinkedList\<String\> list)\
{\
Iterator\<String\> iterator = list.iterator();\
while (iterator.hasNext()){\
String next = iterator.next();\
if(list.indexOf(next) != list.lastIndexOf(next)){\
iterator.remove();\
}\
}\
}

\<실행결과\>

![텍스트이(가) 표시된 사진 자동 생성된
설명](vertopal_e99bd24ffaba45ffbebd39a6a4f6d405/media/image2.png){width="3.2919520997375327in"
height="1.0667596237970254in"}

다)

\<메소드코드\>

private static \<T\> void removeDuplicates(LinkedList\<T\> list)\
{\
Iterator\<T\> iterator = list.iterator();\
while (iterator.hasNext()){\
T next = iterator.next();\
if(list.indexOf(next) != list.lastIndexOf(next)){\
iterator.remove();\
}\
}\
}

\<실행결과\>

![텍스트이(가) 표시된 사진 자동 생성된
설명](vertopal_e99bd24ffaba45ffbebd39a6a4f6d405/media/image3.png){width="3.266949912510936in"
height="1.1000951443569553in"}

라)

\<코드\>

Collections.*sort*(list, Collections.*reverseOrder*());

\<실행결과\>

![텍스트이(가) 표시된 사진 자동 생성된
설명](vertopal_e99bd24ffaba45ffbebd39a6a4f6d405/media/image4.png){width="3.3002865266841646in"
height="1.1834361329833771in"}
