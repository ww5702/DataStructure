# DataStructure
자료구조 정리

## 📘 자료구조 📘

| Week | 정처기 실기 | 자료구조 | 알고리즘 |
| ------ | -- | -- | -- |
| 1주차 | ☑️ | ☑️ | ☑️ |
| 2주차 | ☑️ | ☑️ | ☑️ |
| 3주차 | ☑️ | ☑️ | ☑️ |


# 자료구조 공부 순서
      A. Array
      B. List
            a. ArrayList
            b. vector
            c. LinkedList (simple / doubly / double-ended / circular)
            d. Stack (array / list)
            e. Queue (array / list / priority / deque / circular)
       C. HashMap
       D. Tree (simple / binary-search / segment)
       E. Heap (max / min)
       F. Graph (array / list)
       G. HashSet
***       
       
# 자료구조(Data Structure)
자료구조의 사전적인 의미는 자료(Data)의 집합을 의미하며,    
각 원소들이 정의된 규칙에 의해 나열되며 자료에 대한 처리를 효율적으로 수행할 수 있도록 구분하여 표현한 것이다.   

자료를 더 효율적으로 저장하고 관리하기 위해 자료구조를 사용하며,   
잘 선택된 자료구조는 실행시간을 단축시키고 메모리 용량의 절약을 이끌어 낼 수 있다.   

## 자료의 처리시간
자료의 크기   
자료의 활용 빈도   
자료의 갱신 정도   
프로그램의 용이성

위와 같은 선택 기준을 통해 선택하고 사용한다.

## 자료구조의 분류
데이터가 일렬로 나열되어 있는것을 뜻하는 선형구조   
특정한 형태를 뜻하고 있는 비선형구조

### 선형구조
1. Array(배열)
2. Linked List(연결 리스트)
3. Stack(스택)
4. Queue(큐)

### 비선형구조
1. Tree(트리)
2. Graph(크래프)

***

# 배열(Array)
Array(배열)   
가장 기본적인 데이터 구조이다.   
연속적인 메모리 공간에 순차적으로 데이터를 저장한다.   
배열을 생성할 경우 설정된 셀의 수가 고정되고, 각 셀에는 인덱스 번호가 부여된다.   
부여된 인덱스를 통해 해당 셀 안에 저장되어 있는 데이터에 접근할 수 있다.

## 시간복잡도
![image](https://user-images.githubusercontent.com/60501045/159606869-c90e8f95-4ecd-4982-9da7-6435cc97ac0c.png)

데이터를 배열에 삽입하려면 기존에 있는 데이터를 한칸씩 전부 옮긴 후 데이터를 넣어야 하기에 O(N)이 걸린다.   
삭제 또한 마찬가지이다.

## 장점
쉽게 만들어서 활용할 수 있다.   
원하는 데이터를 효율적으로 탐색, 가져올 수 있다.   
정렬에 용이하다.


## 단점
데이터를 저장할 수 있는 크기가 고정되어 있다.   
 	-> 크기를 변경하려면 새로운 배열을 만든 후, 기존의 데이터를 옮겨야 한다.   
데이터의 추가와 삭제가 비효율적이다.   
 	-> 시간복잡도가 O(N)만큼 걸리기에 비효율적이다.   
메모리 낭비가 발생하게 된다.   
 	-> 배열을 선언 후 사용하지 않는 공간이 있더라도 공간이 할당되어 데이터 낭비가 발생한다.   
구조를 재구성할 때 정렬하는 방식이 비효율적이다.

## Code
### Java
```
int arr[] = new int[10];

for(int i = 0; i < 10; i++) {
	arr[i] = i+1;
}

for(int i = 0; i < 10; i++) {
	System.out.print(arr[i]);
}
```

### Kotlin
```
fun main() {
    var arr = Array<Int>(3, {0})
	var arr = IntArray(3)
    arr[1] = 1
    arr[2] = 2

    arr.forEach { println(it) }
}
```
***
# 리스트(List) - Array,Linked
순서를 가지고 일렬로 나열한 원소들의 모임으로 정의할 수 있다.(선형 자료구조)   
리스트를 컴퓨터에서 사용할 수 있게 구현한 것이 연결 리스트이다(Linked List)  
   
스택이나 큐와 같이 접근이 front나 rear에 제한되어있는 것이 아닌,   
임의의 위치에 있는 항목에 접근이나 연산이 가능하다.   

## Linked List vs Array List

![image](https://user-images.githubusercontent.com/60501045/159821683-f5eec2cf-1422-49d6-a308-39a1ecf0098a.png)

LinkedList는 몇개의 참조자를 바꿈으로써 새로운 자료의 삽입이나 기존 자료의 삭제를 위치에 관계없이   
빠른 시간 안에 수행 할 수 있다.   

ArrayList의 경우 O(N)만큼의 연산 속도가 걸리기 때문에 자료의 최대 개수에 영향을 받는다.   
즉, ArrayList는 크기가 한정되어 있기 때문에 많은 자료를 삽입할 경우 결국 포화 상태에 이르게 된다.   
-> 이는 적은 자료의 경우 LinkedList보다 종종 속도가 더 빠른 경우가 발생하기도 한다.   

## 시간 복잡도
![image](https://user-images.githubusercontent.com/60501045/159822329-9b35269a-5575-4b25-acc3-5415fb10eea4.png)   

ArrayList는 연속적으로 메모리 상에 존재하고, LinkedList는 각 Node들이 포인터로 연결되어있기 때문에 생기는 시간차이다.   
일반적으로 get/set을 자주 사용한다면 ArrayList   
처음이나 끝에 잦은 삽입, 삭제가 발생한다면 LinkedList   


## 장점
새로운 요소들의 추가 및 삭제가 용이하고 효율적이다.   
배열처럼 메모리에 연속적으로 위치하지 않는다.   
대용량 데이터 처리에 적합하다.   

## 단점
짧은 데이터의 경우 배열보다 더 많은 메모리를 사용한다.   
처음부터 끝까지 순회하기 때문에 원하는 값을 비효율적으로 검색/가져온다.   

***

# 스택(Stack)
스택은 순서가 보존되는 선형 데이터 구조유형이다.   
가장 최근 요소부터 처리되는 LIFO(Last In First Out) 구조를 가지고 있다.  
이에 따라 push()연산과 pop()연산, peek()연산 그리고 isEmpty()연산이 있다.

## push()
push()연산은 문자 그대로 집어넣는, 즉 데이터를 스택에 삽입하는 연산이다. 

![image](https://user-images.githubusercontent.com/60501045/159611234-39a0c7f6-31f8-4651-a542-6206cbc3fae5.png)    

선입선출의 구조에 따라 가장 최근에 들어온 데이터가 가장 상단에 위치하게 된다.   

## pop()
pop, 즉 스택에 데이터를 꺼내는 연산이다.   

![image](https://user-images.githubusercontent.com/60501045/159611409-1e4c4845-a0d5-4bcb-a02a-382e7ef07161.png)  

이 또한 선입선출의 구조에 따라 현재 스택에서 top이 가리키고 있는 데이터를 꺼내게 된다.   
만약 꺼낼 top 데이터가 없을 경우 pop연산이 실행되지 않는다.   

## peek()
peek()연산은 현재 top이 가리키고 있는 데이터를 확인하는 연산이다.   
pop()과 다른점이 있다면 pop()은 데이터를 스택에서 꺼내서 읽는다면,   
peek 연산은 데이터를 꺼내지않고 값만 확인하는 것이다.   

## isEmpty()
isEmpty()연산은 스택이 비어있는지 확인하는 연산이다.   
비어있다면 True, 비어있지 않다면 False를 반환한다.   

## 시간복잡도
![image](https://user-images.githubusercontent.com/60501045/159610632-e0530036-edea-4ccd-b88a-6cd2fa0a1043.png)

삽입 연산의 경우 데이터의 개수와 상관없이 top에 데이터를 삽입하므로 O(1)이다.   
삭제 또한 위와 같으므로 O(1)이다.   
하지만 검색 연산의 경우 스택에 존재하는 모든 데이터를 찾는 것이므로   
n개의 데이터를 전부 순회해야 하기에 O(N)이다.   

## 장점
동적인 메모리 크기   
데이터를 받는 순서대로 정렬된다.   
빠른 런타임   
데이터의 삽입과 삭제가 빠르다.   

## 단점
가장 최신 요소만 가져온다.   
한번에 하나의 데이터만 처리 가능하다.   

## 사용처
가장 마지막으로 입력된 것을 순차적으로 바로 처리하고 싶을 때   
브라우저의 뒤로가기   
실행 취소   
재귀   

## Code
### Java
자바에서는 기본적으로 stack 객체를 제공해준다.   
```
import java.util.Stack;

public class StackExample {

    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
       
        stack.push(5);
        stack.push(4);
        stack.push(3);
        stack.push(2);
        stack.push(1);
       
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
        System.out.println(stack.pop());
       
        System.out.println("---------------");
       
        stack.push(5);
        stack.push(4);
        stack.push(3);
       
        System.out.println(stack.size());
        System.out.println(stack.peek());
        System.out.println(stack.size());
       
    }
}
```

### Kotlin
코틀린에는 따로 stack 객체가 존재하지 않는다.   
따라서 MutableList와 ArrayList로 stack을 구현할 수 있다.   

```
fun main() {
    var mutableList = mutableListOf<Int>()

    mutableList.add(1)
    mutableList.add(2)
    mutableList.add(3)

    mutableList.removeAt(mutableList.size-1)

    print(mutableList[mutableList.size-1])

    println(mutableList.isEmpty())
    println(mutableList.isNotEmpty())

    println(mutableList.size)
}
```
```
fun main() {
    var arrayList = arrayListOf<Int>()

    arrayList.add(1)
    arrayList.add(2)
    arrayList.add(3)

    arrayList.removeAt(arrayList.size-1)

    print(arrayList[arrayList.size-1])

    println(arrayList.isEmpty())
    println(arrayList.isNotEmpty())

    println(arrayList.size)
}
```

***
# 큐(Queue)
큐는 스택과 비슷하지만 스택의 LIFO이 아닌 가장 먼저 입력된 요소를 처리하는 FIFO(First In First Out) 구조이다.   
놀이공원에서 줄을 슬 경우로 생각하면 이해하기 쉽다.   
가장 먼저 줄을 슨 사람이 제일 먼저 빠져나가고, 맨 뒤로 사람들이 계속해서 줄을 스는 메커니즘이다.   

## enqueue()
원소를 삽입하는 연산이다.   
큐가 full인지 확인한 다음 full 상태가 아니라면 rear를 1증가 시킨 후 그 자리에 데이터를 삽입한다.   

## dequeue()
원소를 삭제하는 연산이다.   
큐가 empty인지 확인한 다음 empty가 아니라면 front를 1 증가 시킨 후 그 자리의 원소를 삭제한다.   

## 시간복잡도
![image](https://user-images.githubusercontent.com/60501045/159823227-87fc2254-1e42-4dd5-964e-7cf1678d4503.png)   
FIFO의 구조상 삽입과 추가가 O(1)로 쉬운 형태를 보이지만,   
값을 가져오는 경우 전부를 확인해봐야 한다는 점에서 O(N)의 시간 복잡도를 가지도 있다.   

## 장점
데이터를 받는 순서대로 정렬된다.   
빠른 런타임   

## 단점
가장 오래된 요소만 가져올 수 있다.   
한번에 하나의 데이터만 처리가 가능하다.   

## 사용처
순서에 민감한 데이터를 처리할 때   
프린트 대기열처럼 가장 먼저 입력 받은 데이터를 먼저 처리해야 할 때   

***
# 해시 맵(Hash map/Hash tables)
해시 맵은 대량의 정보를 저장하고 특정 요소를 효율적으로 검색할 수 있는 데이터 구조이다.   

버킷(bucket)에 키/값(key/value)쌍을 저장한다.   
키를 저장할 때 메모리 공간을 절약하기 위해 키를 "해시 함수"라는 함수를 통해 해시라는 특정 값으로 변환한다.     
키는 검색 시 사용되는 문자열이고, 값은 키와 쌍을 이룬 데이터이다.   
검색된 키는 해시함수를 통해 해시 값으로 변환되고 버킷을 가리킨다. -> 버킷은 index라는 뜻이다.   
즉, 해시 맵은 필요할 때에만 메모리 크기를 늘린다.  -> 가능한 한 작은 크기를 유지한다는 뜻이다.   

예시)   
![image](https://user-images.githubusercontent.com/60501045/160237588-4349d62f-3888-4c8e-805f-b38ff2e137fb.png)   
위 그림을 보면 John Smith를 해시 함수로 하여금 02라는 index값을 얻어낸것을 볼 수 있다.   

## 시간복잡도
![image](https://user-images.githubusercontent.com/60501045/160237492-1de59b62-be44-47cd-a0c2-cf62c36bca13.png)   
해시를 통해 데이터값을 가져오거나 추가/삭제 하기 때문에 O(1)의 복잡도를 나타낸다.   

## 장점
새로운 요소들의 추가/삭제가 용이하고 효율적이다.   
원하는 값의 검색/가져오기가 빠르고 효율적이다.   

## 단점
충돌이 일어날 수 있다. -> 입력된 키의 해시값이 이미 데이터가 저장되어 있는 버킷(index)을 가리킬 수 있다.   
해시함수의 정비가 필요한 경우가 많다.   

## 사용처
데이터베이스(주소찾기, 이름 찾기, 번호 찾기)   
사용자 로그인 인증   

***
# 트리(Tree)
트리는 노드로 구성된 계층적 자료구조이다.   
최상위 노드(루트)를 만들고 루트 노드의 자식 노드를 추가하고, 그 자식 노드의 자식 노드를 추가하는 방식으로 구현된다.   

## 알아야 할 용어들

A,B,C,D 등의 구성요소들을 노드(node)라고 한다.   
위의 A처럼 최상위 노드를 루트(root)라고 한다.   
루트를 기준으로 다른 노드로 접근하기 위한 거리를 depth라고 한다.   
같은 부모를 가지면서 같은 depth에 존재하는 노드들을 sibling 관계에 있다고 한다.   
그림에서 A는 B와 C의 부모이고, B와 C는 A의 자식이다.   
노드와 노드를 잇는 선을 edge 라고 한다.   
자식이 없는 노드를 leaf 라고 한다.   

***
