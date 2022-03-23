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

# Array
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
데이터를 저장할 수 있는 크기가 고정되어 있다. -> 크기를 변경하려면 새로운 배열을 만든 후, 기존의 데이터를 옮겨야 한다.
데이터의 추가와 삭제가 비효율적이다. -> 시간복잡도가 O(N)만큼 걸리기에 비효율적이다.
메모리 낭비가 발생하게 된다. -> 배열을 선언 후 사용하지 않는 공간이 있더라도 공간이 할당되어 데이터 낭비가 발생한다.
구조를 재구성할 때 정렬하는 방식이 비효율적이다.

## Code
####Java
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



