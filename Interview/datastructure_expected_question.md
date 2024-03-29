**1. Array 와 LinkedList 의 차이가 무엇인가요 (naver 전화 면접)**


        Array 는 Random Access를 지원한다. 요소들을 인덱스를 통해 직접 접근할 수 있다. 따라서 특정 요소에 접근하는 시간복잡도는 O(1)이다.
        Linkedlist는 Sequential Access를 지원한다. 어떤 요소를 접근할 때 순차적으로 검색하며 찾아야 한다. 따라서 특정 요소에 접근할 때 시간복잡도는 O(N)이다.

        저장방식도 배열에서 요소들은 인접한 메모리 위치에 연이어 저장된다. 반면 Linkedlist에서는 새로운 요소에 할당된 메모리 위치 주소가 linkedlist의 이전 요소에 저장된다.

        저장방식도 배열에서 요소들은 인접한 메모리 위치에 연이어 저장된다.

        Linkedlist에서는 새로운 요소에 할당된 메모리 위치 주소가 linkedlist의 이전 요소에 저장된다.배열에서 삽입과 삭제는 O(N)이 소요되지만, Linkedlist에서 삽입과 삭제는 O(1)이 소요된다.

        배열에서 메모리는 선언 시 컴파일 타임에 할당이 된다.(정적 메모리 할당) 반면 Linkedlist에서는 새로운 요소가 추가될 때 런타임에 메모리를 할당한다.(동적 메모리 할당)

        배열은 Stack 섹션에 메모리 할당이 이루어 진다. 반면 Linkedlist는 Heap 섹션에 메모리 할당이 이루어진다.
<BR>

**2. 미리 예상한 것보다 더 많은 수의 data를 저장하느라 Array의 size를 넘어서게 됐다. 어떻게 해결할 수 있을까?**

        1. 기존의 size보다 더 큰 Array를 선언해 데이터를 옮겨 할당합니다. 모든 데이터를 옮긴 후에는 기존 Array는 메모리에서 삭제하면 됩니다.
        2. 다른 방법으로는, size를 예측하기 쉽지 않다면 Array 대신 Linked List를 사용함으로써 데이터가 추가될 때마다 메모리 공간을 할당받는 방식을 사용할 수 있습니다.

<BR>

**3. Array 와 Linked List 의 Memory Allocation 은 언제 일어나며, 메모리의 어느 영역을 할당받는가요?**



        배열은 컴파일 단계에서 스택 영역에 메모리를 할당 받고,
        링크드 리스트는 런타임 단계에서 새로운 노드를 추가할 때마다 힙 영역에 메모리 할당이 일어납니다.
<BR>

**4. List와 Set의 차이는 무엇인가요?**

       List는 중복된 데이터를 저장하고 들어온 순서를 유지하는 선형 자료구조이다.
       Set은 중복되지 않은 데이터를 저장하고, 들어온 순서를 유지하지 않는 선형 자료구조입니다.
<BR>

**5. Stack과 Queue의 차이점은 무엇인가요? (N사 전화면접)**

        스택은 쌓아 올리는 자료구조이다. 같은 구조와 크기의 자료를 정해진 방향으로 쌓을 수 있고, 한 방향으로만 접근할 수 있다. top을 통해서 push, pop을 하면서 삽입과 삭제가 일어난다. 후입선출 구조이다. DFS나 재귀에서 사용된다.

        큐는 원소의 줄을 세우는 자료구조이다. 큐는 한 쪽 끝에서 삽입 작업을, 다른 쪽 끝에서 삭제 작업을 진행한다. 선입선출 구조이다. 주로 데이터가 입력된 시간 순서대로 처리되어야 하는 경우 사용한다. BFS나 캐시를 구현할 때 사용한다.
<BR>

**6. Stack과 Queue의 실생활 예시에는 어떤 것이 있을까요?**

        스택은 후입선출 구조이므로 웹 브라우저 방문기록, 실행취소(undo), 역순 문자열 만들기, 후위 표기법 계산에 사용됩니다.
        큐는 선입선출 구조이므로 프린터의 출력처리, 콜센터 고객 대기 시간, 너비 우선 탐색, 캐시(Cache) 구현에 사용됩니다.
<BR>

**7. Stack과 Queue의 두 가지 특성을 전부 사용하고 싶을 때는 무엇을 사용하면 좋을까요?**

        덱 Deque을 사용하면 됩니다.
        덱은 큐의 양쪽 끝에서 데이터의 삽입과 삭제가 모두 가능하게 만든 자료구조로, 스택과 큐의 성질을 모두 가지고 있습니다.

<BR>

**8. 스택으로 큐를 구현하는 방법과 큐로 스택을 구현하는 방법에 대해 설명해주세요**

        1. 스택으로 큐 구현하기

        스택 2개를 활용해서 구현할 수 있습니다.
        스택 A와 B가 있을 때, 큐에 PUSH연산이 일어나면 스택 A에 PUSH 합니다.
        이후 큐에 POP연산을 한다면 스택A의 모든 데이터를 스택 B로 옮깁니다. 그렇게 되면 스택 A의 역순으로 데이터가 저장될 것이고, 스택 B를 POP하면 큐에 저장된 데이터 순서대로 출력될 것입니다.
        즉, 스택 A는 인큐의 역할, 스택 B는 디큐의 역할을 하게 됩니다.
        PUSH를 하면 스택 A에 가장 늦게 들어온 데이터가 맨 위에 쌓일 것이고, 이를 다시 스택 B로 옮기면 큐의 구조(선입선출)로 저장됩니다.
<BR>

        2. 큐로 스택 구현하기

        큐 2개를 활용해서 구현할 수 있습니다.
        큐 A와 B가 있을 때, 스택에 PUSH 연산이 일어나면, 해당 요소를 우선 큐 A에 PUSH 합니다.
        그 다음 마지막 원소(방금 PUSH한 요소)를 제외한 나머지를 큐 B에 옮긴 후, 다시 큐 A에 차례대로 PUSH한다.
        그럼 가장 나중에 들어온 값이 큐의 첫 번째 위치로 이동하게 되고, TOP이나 POP 연산이 일어날 경우 순서에 맞게 데이터를 POP할 수 있다.

<BR>

**9. 우선순위 큐란 무엇인가요?**

       우선순위 큐는 들어간 순서에 상관없이 우선순위가 높은 데이터를 먼저 꺼내기 위해 고안된 자료구조입니다.
       우선순위 큐 구현 방식에는 배열, 연결 리스트, 힙이 있고, 그중 힙 방식이 worst case라도 시간 복잡도 O(logN)을 보장하기 때문에 일반적으로 완전 이진트리 형태의 힙을 이용해 구현합니다.
<BR>

**10. 우선순위 큐의 동작원리가 어떻게 되나요? (N사 전화면접)**

        우선순위큐는 가장 우선순위가 높은 데이터를 먼저 꺼내기 위해 고안된 자료구조입니다.
        우선순위 큐를 구현하기 위해서 일반적으로 힙을 사용합니다.
        힙은 완전이진트리를 통해서 구현되었기 때문에 우선순위 큐의 시간복잡도는 O(logn)입니다.
        우선순위 큐는 힙이라는 자료구조를 가지고 구현한다. top이 최대면 최대힙, top이 최소면 최소힙으로 표현한다.
        힙으로 구현된 이진 트리는 모든 정점이 자신의 자식 요소보다 우선순위가 높다는 성질을 가지고 있다.
        이 성질을 통해 삽입과 삭제 연산을 모두 O(logN)으로 수행할 수 있다.
<BR>

**11. 자료구조 힙의 특징을 설명해주세요**

        우선 순위가 높은 요소가 먼저 나가는 특징을 가진다.
        루트가 가장 큰 값이 되는 최대 힙과 루트가 가장 작은 값이 되는 최소 힙이 있다.

<BR>

**12. 해시 테이블와 해시 테이블의 시간 복잡도에 대해 설명하시오.**  

        해시 테이블은 (Key, Value)로 데이터를 저장하는 자료구조 중 하나로 빠른 데이터 검색이 필요할 때 유용합니다.  
        해시 테이블은 Key값에 해시함수를 적용해 고유한 index를 생성하여 그 index에 저장된 값을 꺼내오는 구조입니다.  
        해시 테이블은 고유한 index로 값을 조회하기 때문에 평균적으로 O(1)의 시간복잡도를 갖습니다.  
        하지만 해시의 index값이 충돌이 발생한 경우 충돌된 index값에 대해 연결된 데이터들을 조회하여 원하는 값을 조회하기 때문에 O(N)까지 증가할 수 있습니다.

<br>

**13. 해시 테이블(Hash Table)의 검색 시간 복잡도는 어떻게 O(1)을 유지할 수 있나요?**  

        해시 테이블에 Key로 접근하면, Hash Function에 Key 값을 집어 넣어 나온 Hash 값을 저장소의 인덱스로 활용합니다.  
        해당 인덱스에 값을 저장하기 때문에, Hash Function의 시간 복잡도를 제외하면 시간 복잡도 O(1)을 보장할 수 있습니다.

<br>

**14. HashMap과 HashTable의 차이점에 대해 설명하시오.**  

        동기화 지원 여부의 차이가 있다.  
        병렬 처리를 하면서 자원의 동기화를 고려해야 하는 상황이라면 해시테이블(HashTable)을 사용해야 하며, 병렬 처리를 하지 않거나 자원의 동기화를 고려하지 않는 상황이라면 해시맵(HashMap)을 사용하면 된다.

<br>

**15. Array(List)의 가장 큰 특징과 그로 인해 발생하는 장점과 단점에 대해 설명해주세요.**  

        Array의 가장 큰 특징은 순차적으로 데이터를 저장한다는 점입니다.  
        데이터에 순서가 있기 때문에 0부터 시작하는 index가 존재하며, index를 사용해 특정 요소를 찾고 조작이 가능하다는 것이 Array의 장점입니다.  
        순차적으로 존재하는 데이터의 중간에 요소가 삽입되거나 삭제되는 경우 그 뒤의 모든 요소들을 한 칸씩 뒤로 밀거나 당겨줘야 하는 단점도 있습니다.  
        이러한 이유로 Array는 정보가 자주 삭제되거나 추가되는 데이터를 담기에는 적절치 않습니다.
<br>

 **16. Array를 적용시키면 좋을 데이터의 예를 구체적으로 들어주세요. 구체적 예시와 함께 Array를 적용하면 좋은 이유, 그리고 Array를 사용하지 않으면 어떻게 되는지 함께 설명해주세요.**  

         Array를 적용시키면 좋은 예로 주식 차트가 있습니다.  
         주식 차트에 대한 데이터는 요소가 중간에 새롭게 추가되거나 삭제되는 정보가 아니며, 날짜별로 주식 가격이 차례대로 저장되어야 하는 데이터입니다.  
         즉, 순서가 굉장히 중요한 데이터이므로 Array 같이 순서를 보장해주는 자료구조를 사용하는 것이 좋습니다.  
         Array를 사용하지 않고 순서가 없는 자료 구조를 사용하는 경우에는 날짜별 주식 가격을 확인하기 어려우며 매번 전체 자료를 읽어 들이고 비교해야 하는 번거로움이 발생합니다.

<br>

**17. Array와 ArrayList의 차이점에 대해 설명해주세요.**  

        Array는 크기가 고정적이고, ArrayList는 크기가 가변적입니다.  
        Array는 초기화 시 메모리에 할당되어 ArrayList보다 속도가 빠르고, ArrayList는 데이터 추가 및 삭제 시 메모리를 재할당하기 때문에 속도가 Array보다 느립니다.

<br>

**18. 배열과 벡터의 차이점은 무엇인가요?**

        데이터 구조적인 관점에서 배열은 일반적으로 동일한 데이터 유형을 가진 원소들의 정렬된 모임입니다. 배열은 메모리 상에 연속적으로 배치되며, 인덱스를 사용하여 각 원소에 접근할 수 있습니다. 벡터는 일반적으로 1차원 배열을 의미합니다. 따라서 벡터는 배열의 일종이며, 개념적으로는 유사하지만 일반적으로 수학적인 의미에서 크기와 방향을 갖는 양을 나타내기 위해 사용됩니다.

<br>

**19. 벡터의 용량(capacity)과 크기(size)의 차이는 무엇인가요?**

        용량은 벡터가 현재 할당된 메모리 공간의 크기를 나타내고, 크기는 벡터에 저장된 원소의 개수를 나타냅니다.

<br>

**20. 벡터에서의 메모리 할당과 해제는 어떻게 이루어지나요?**

        메모리 할당은 동적 배열의 크기 조절 시에 이루어지며, 해제는 벡터가 파괴될 때 이루어집니다.

<br>

**21. BST와 Binary Tree에 대해서 설명하세요.**

        이진탐색트리(Binary Search Tree)는 이진 탐색과 연결 리스트를 결합한 자료구조이다. 이진 탐색의 효율적인 탐색 능력을 유지하면서, 빈번한 자료 입력과 삭제가 가능하다는 장점이 있다. 이진 탐색 트리는 왼쪽 트리의 모든 값이 반드시 부모 노드보다 작아야 하고, 반대로 오른쪽 트리의 모든 값이 부모 노드보다 커야 하는 특징을 가지고 있어야 한다. 이진 탐색 트리의 탐색, 삽입, 삭제의 시간복잡도는 보통은 O(logn)이지만 트리의 균형이 맞지 않아 선형의 모양을 띄는 최악의 경우 O(n)이 될 수도 있다. 그래서 이 균형을 맞춘 구조가 AVL Tree이고 시간 복잡도는 O(logn)이다.

<br>

**22. 트리의 깊이(Depth)와 높이(Height)의 차이는 무엇인가요?**

        트리의 깊이는 루트에서 특정 노드까지의 길이(에지의 수), 높이는 트리에서 가장 깊은 노드까지의 길이(루트에서 가장 깊은 리프 노드까지의 에지 수)를 나타냅니다

<br>

**23. 트리 자료구조를 사용하는 대표적인 알고리즘은 어떤 것이 있나요?**

    - 이진 탐색 트리 (BST)
        : 탐색, 삽입, 삭제 등의 연산을 수행하는데 사용됩니다. 각 노드의 왼쪽 서브트리에는 현재 노드보다 작은 값의 노드가 위치하고, 오른쪽 서브트리에는 큰 값의 노드가 위치합니다.
    - 균형 잡힌 이진 탐색 트리 (Balanced BST):
        : AVL 트리, 레드-블랙 트리 등이 있습니다. 이러한 트리는 삽입, 삭제 연산을 수행하면서 트리의 균형을 유지하여 탐색 성능을 최적화합니다.
    - 힙 (Heap)
        : 최대 힙 또는 최소 힙으로 구현되며, 우선순위 큐를 구현하는 데 사용됩니다. 힙은 특정 순서에 따라 노드를 정렬하여 최댓값 또는 최솟값에 효율적으로 접근할 수 있게 합니다.
    - 트라이 (Trie)
        : 문자열 검색과 관련된 작업에 사용되는 트리 자료구조입니다. 각 노드는 문자를 나타내며, 루트에서부터 리프까지의 경로는 문자열을 표현합니다. 문자열 검색, 자동 완성, 사전 검색 등에 활용됩니다.
    - 세그먼트 트리 (Segment Tree)
        : 구간 쿼리 연산을 효율적으로 처리하는 데 사용되는 트리 자료구조입니다. 배열의 각 구간에 대한 정보를 저장하고, 구간 쿼리에 대한 연산을 빠르게 수행할 수 있습니다.
    - 트립 (Treap)
        : 이진 검색 트리와 힙의 특성을 결합한 자료구조로, 우선순위에 따라 노드를 정렬합니다. 탐색과 동시에 우선순위를 유지하므로, 삽입, 삭제 등의 연산을 빠르게 수행할 수 있습니다.

<br>

**24. 트리의 회전 연산(Rotation)은 무엇이며 어떤 상황에서 사용하나요?**

        트리의 회전 연산은 특정 노드를 중심으로 서브트리를 회전시키는 연산입니다. 주로 이진 탐색 트리 (BST)에서 사용되며, 삽입이나 삭제시 트리가 불균형한 상태가 될 때 균형잡힌 상태로 변경하는 데 활용됩니다. 예를 들어, AVL 트리에서 노드를 삽입하거나 삭제할 때, 해당 노드의 부모 노드로부터 루트까지 올라가면서 균형을 맞추기 위해 회전 연산을 사용할 수 있습니다. 이러한 회전 연산을 통해 트리의 높이를 최소화하고 탐색, 삽입, 삭제 연산의 효율성을 향상시킵니다.

<br>

**25. 이진 트리의 순회 방법에는 어떤 것이 있고, 각각 어떤 상황에서 사용하나요?**

    - 전위 순회(Pre-order Traversal):
        - 루트를 먼저 방문하고, 왼쪽 서브트리를 전위 순회한 후에 오른쪽 서브트리를 전위 순회합니다.
        - 상황에 따라 트리의 구조를 볼 때 사용하며, 복사 작업이나 트리의 복제에 활용됩니다.
    - 중위 순회(In-order Traversal):
        - 왼쪽 서브트리를 중위 순회한 후에 루트를 방문하고, 마지막으로 오른쪽 서브트리를 중위 순회합니다.
        - 이진 탐색 트리의 경우 중위 순회 결과는 정렬된 순서로 출력됩니다. 탐색 작업에 많이 사용됩니다.
    - 후위 순회(Post-order Traversal):
        - 왼쪽 서브트리를 후위 순회한 후에 오른쪽 서브트리를 후위 순회하고, 마지막으로 루트를 방문합니다.
        - 리프 노드부터 시작하여 상위 레벨로 올라가며 작업을 수행할 때 사용됩니다. 메모리의 해제나 트리의 삭제 작업에 활용될 수 있습니다.
    - 레벨 순서 순회(Level Order Traversal 또는 Breadth-First Traversal):
        - 각 레벨을 순서대로 좌측에서 우측으로 방문합니다. 큐를 사용하여 구현됩니다.
        - 트리의 레벨 순서대로 작업을 수행할 때 유용합니다. 트리의 너비를 우선으로 탐색할 때 사용됩니다.

<br>

**26. 트라이의 구조와 동작 원리에 대해 설명해주세요.**

        트라이는 트리 구조로, 각 노드는 문자를 나타내며 경로는 문자열을 형성합니다. 각 노드는 해당 문자를 표현하며, 노드의 연결은 문자열의 글자들 간의 연결을 나타냅니다. 루트 노드에서부터 특정 노드까지 이동하면서 문자열을 검색하거나 삽입하는데 사용됩니다. 이 구조는 검색 연산에 있어서 시간 복잡도를 크게 개선할 수 있습니다.

<br>

**27. 왜 문자열을 탐색할때 이진 트리가 아닌 트라이 구조가 더 효율적인가요?**

        트라이는 문자열 검색에서 접두사 검색에 특화되어 있어 이진 트리보다 효율적입니다. 트라이는 메모리를 효율적으로 사용하며, 중복된 문자열을 효과적으로 처리할 수 있습니다. 노드가 문자를 나타내고 경로는 문자열의 부분을 형성하므로, 문자열의 길이에 따른 시간 복잡도도 향상됩니다. 이러한 특성은 트라이를 문자열 관련 작업에 적합하게 만듭니다.

<br>

**28. 배열과 연결 리스트의 차이점을 설명해보세요.**

        배열과 연결 리스트는 데이터를 저장하기 위한 자료구조로, 데이터 저장 방식에 차이가 있다. 배열은 연속된 메모리 공간에 데이터를 저장한다. 그렇기 때문에 특정 인덱스의 데이터에 한 번에 접근할 수 있어서 읽는 속도가 빠르다. 하지만 데이터 삭제, 삽입 시 요소들의 인덱스를 수정해야 하기 때문에 비교적 시간이 오래 걸린다.

        반면, 연결 리스트는 노드를 이용해 메모리 공간에 데이터를 불연속적으로 저장한다. 각 노드는 데이터와 다음 노드의 주소 값을 저장하고 있어서 다른 노드에 접근할 수 있다. 배열과 달리 인덱스가 없기 때문에 한 번에 특정 데이터에 접근할 수는 없지만 데이터의 삽입, 삭제 시 노드가 가리키는 주소 값만 변경하면 되기 때문에 속도가 빠르다는 장점이 있다.

<br>

**29. 단순 연결 리스트를 역순으로 출력하는 방법을 설명해보세요.**

        단순 연결 리스트를 역순으로 출력하는 방법으로는 스택에 연결 리스트의 요소를 순차적으로 넣고 빼는 방법이 있다. 이 방법은 스택을 사용하므로 추가 메모리가 필요하다. 메모리에 여유가 없다면 반복문을 이용해 다음 노드가 가리키는 노드를 이전 노드로 바꿔서 역순으로 된 연결 리스트를 얻는 방법도 있다.

<br>

**30. 배열의 가장 큰 특징과 그로 인해 발생하는 장점과 단점에 대해 설명해주세요.**

        배열의 가장 큰 특징은 순차적으로 데이터를 저장한다는 점이다. 데이터에 index를 부여하여 순서를 가지고 있기 때문에 index를 사용해 특정 요소를 빠르게 찾고 조작이 가능하다는 것이 Array의 장점이다. 다만, 데이터의 중간에 요소가 삽입되거나 삭제되는 경우 기존 요소를 이동해야 하는 단점도 있다. 이러한 이유로 Array는 정보가 자주 삭제되거나 추가되는 데이터를 저장하기에는 적절하지 않다.

<br>

**31. 배열을 사용하면 좋을 데이터의 예를 구체적으로 들어주세요. 또한, Array를 적용하면 좋은 이유와 Array를 사용하지 않으면 어떻게 되는지 함께 설명해주세요.**

        배열을 사용하면 좋은 예로 주식 차트가 있다. 주식 차트에 대한 데이터는 요소가 중간에 새롭게 추가되거나 삭제되는 정보가 아니라 날짜 별로 주식 가격이 차례대로 저장되어야 한다.즉, 순서가 굉장히 중요한 데이터이므로 배열과 같이 순서를 보장해주는 자료구조를 사용하는 것이 좋다. 배열을 사용하지 않고 순서가 없는 자료 구조를 사용하는 경우에는 날짜 별 주식 가격을 확인하기 어려우며 매번 전체 자료를 읽어 들이고 비교해야 하는 번거로움이 발생하게 된다.

<br>

**32. 맵(Map)이란 무엇인가요?**

        맵은 키와 값으로 이루어진 자료구조이다. 키를 통해 해당 값에 접근할 수 있다. 키는 유일해야 한다는 특징이 있지만 키와 연결된 값은 중복이 가능하다.

<br>

**32. 맵과 배열(Array)의 차이점은 무엇인가요?**

        맵과 배열은 데이터를 저장하고 접근하는 방식에서 차이가 있다. 배열은 인덱스를 사용하여 데이터에 접근하며, 데이터의 순서가 중요하다. 하지만 맵은 키-값 쌍으로 데이터를 저장하고, 키를 통해 값을 접근한다. 맵은 데이터의 순서를 보장하지 않으며, 키를 통해 빠르게 값을 찾을 수 있는 장점이 있습니다.

<br>

**33. 우선순위 큐에 대해 설명해주세요.**

        우선순위 큐는 우선순위가 높은 데이터부터 꺼내는 자료구조로, 각 요소가 우선순위를 가진다. 우선순위 큐를 활용해 정렬하거나 다익스트라 알고리즘을 구현할 때 사용한다. 우선순위 큐는 주로 힙을 이용해 구현한다.

<br>

**34. 이진트리의 전위/중위/후위 순회가 무엇인가요? 설명해보고 자신의 직무 언어로 순회 결과를 코딩해보세요.**

**35. BST의 성능을 개선하기 위한 방법에는 무엇이 있나요?**

        BST의 양쪽 높이의 균형을 맞추는 것이 성능을 개선하는 방식입니다
        대표적으로 개량된 BST 트리로써, AVL 트리, Red-Black 트리가 있습니다.

<br>

**36. Heap이 무엇인지, 삽입/삭제 시 어떻게 동작하는지 설명해보세요.**

        힙(Heap)은 '완전이진트리'면서, 모든 부모노드와 자식노드 간에 '크거나 같은' 혹은 '작거나 같은'의 관계를 가지고 있는 트리를 의미합니다.

 
        이진트리는 자식노드를 최대 2개까지 가질 수 있는 트리를 의미하며, 완전이진트리는 리프노드 레벨을 제외한 나머지 트리는 포화 이진트리의 구조를 갖고, 리프노드 레벨의 노드들은 왼쪽 인덱스부터 차례로 채워진 트리를 의미합니다.

        포화 이진 트리는 리프노드들을 제외한 나머지 노드들은 모두 자식을 2개를 가지며, 리프노드들은 자식을 갖지 않는 트리를 의미합니다.

 

        삽입 및 삭제를 하면 Heap의 구조가 무너지게 되는데, 다시 Heap으로 만드는 과정을 Heapify라고 합니다.

        삽입 시 트리의 가장 마지막 노드 다음 인덱스에 새로운 노드를 집어넣고 Heapify 연산을 통해 힙으로 구성합니다.

        삭제 시 트리의 루트노드를 반환 및 제거하고, 트리의 가장 마지막 인덱스를 가진 노드의 위 치를 리프노드로 이동시킵니다. 그 후 Heapfiy 연산을 통해 다시 힙으로 구성합니다.

        삽입과 삭제 연산 모두 트리의 높이에 따라 연산횟수가 결정되며, worst case의 시간 복잡도는 둘 다 O(logN)을 보장합니다.

<br>

**37. 해시 테이블(Hash Table)의 검색 시간 복잡도는 어떻게 O(1)을 유지할 수 있나요?**

        해시 테이블에 Key로 접근하면, Hash Function에 Key 값을 집어 넣어 나온 Hash 값을 저장소의 인덱스로 활용합니다. 해당 인덱스에 값을 저장하기 때문에, Hash Function의 시간 복잡도를 제외하면 시간 복잡도 O(1)을 보장할 수 있습니다.

<br>

**38. 그렇다면 Hash Collision (해시 충돌)에 대해 설명할 수 있나요? 해결 방법은 어떻게 되나요?**

        해시 테이블에 접근하는 Key 값은 무한하고, Hash Function을 통해 나온 Hash 값은 유한합니다. (값이 저장되는 메모리는 한계가 있으므로.)

 

        비둘기집의 원리는 N+1마리의 비둘기가 N개의 비둘기 집에 들어간다면, 반드시 하나의 비둘기 집에는 두 마리 이상의 비둘기가 들어가 있다는 것입니다.

        해시 테이블의 Key는 비둘기고, Hash 인덱스가 비둘기 집이라고 했을 때, Key는 무한하고 Hash 는 유한하므로 특정 Hash Index에 대해서 겹치는 Key가 존재할 수 밖에 없습니다.

        이렇게 서로 다른 Key에 대해 같은 해시값을 갖는 경우를 해시 충돌이라고 합니다.

        해결 방법은, Chaining 방식과 Open Addressing 방식이 있습니다.

        - 체이닝(Chaining) : 인덱스의 버킷을 연결리스트로 구현해, 이미 값이 존재하더라도 연결리스트에 해당 값을 삽입하는 방식
        - 개방주소법(Open Addressing) : 해시 충돌이 일어난 경우, 특정한 간격만큼 이동 후 비어있는 주소 값에 저장하는 방식

<br>

**39.그렇다면, 체이닝 방식과 개방주소법의 장단점을 비교해주세요.**
        체이닝 방식 : 

        - 장점 :
        1) 한정된 저장소(Bucket)을 효율적으로 사용할 수 있다.
        2) 해시 함수(Hash Function)을 선택하는 중요성이 상대적으로 적다.
        3) 상대적으로 적은 메모리를 사용한다. 미리 공간을 잡아 놓을 필요가 없다.

        - 단점 :
        1) 한 Hash에 자료들이 계속 연결된다면(쏠림 현상) 검색 효율을 낮출 수 있다.
        2) 외부 저장 공간을 사용한다.
        3) 외부 저장 공간 작업을 추가로 해야 한다.

 
        개방주소법 방식 : 

        - 장점 :
        1) 또 다른 저장공간 없이 해시테이블 내에서 데이터 저장 및 처리가 가능하다.
        2) 또 다른 저장공간에서의 추가적인 작업이 없다.

        -단점 :
        1) 해시 함수(Hash Function)의 성능에 전체 해시테이블의 성능이 좌지우지된다.
        2) 데이터의 길이가 늘어나면 그에 해당하는 저장소를 마련해 두어야 한다.
<br>

**40. 해시 테이블의 단점은 무엇이 있을까요? 언제 사용하면 안 될까요?**

<br>

**41. BST (Binary Search Tree)와 BST의 특징에 대해 설명할 수 있나요?**

        데이터의 빠른 검색을 위해 만들어진 트리 자료구조입니다.

        아래와 같은 조건을 만족하는 트리에 대해 BST라고 부를 수 있습니다.

        이진 트리 (자식을 최대 2개까지 가질 수 있는 트리)
        루트노드에 대해서 왼쪽 자식은 루트 노드보다 더 작은 값을, 오른쪽 자식은 루트 노드보다 더 큰 값을 저장한다.
        루트노드의 왼쪽 서브트리, 오른쪽 서브트리에 대해 위의 조건을 만족한다.
 

        탐색에 유리한 자료구조로, 특정 값에 대해 탐색하는 시간 복잡도가 트리의 높이에 의존하기 때문에 평균적으로 logN의 시간복잡도를 갖습니다.

        다만, 이진탐색트리의 왼쪽 서브 트리와 오른쪽 서브 트리의 균형이 맞지 않고 한 쪽으로만 치우쳐진 경우에는 트리의 높이 자체가 N이 되므로 Worst Case의 경우 O(N)의 시간복잡도를 갖습니다.
<br>

**42. 트리와 그래프의 차이에 대해서 설명할 수 있나요?**

        그래프는 트리보다 더 포괄적인 개념입니다. 즉, 트리는 그래프라고 부를 수 있으나 모든 그래프를 트리라고 부를 순 없습니다.

        그래프는 각 요소를 나타내는 노드와 노드 사이의 관계를 나타내는 엣지로 나타낼 수 있습니다.

        트리는 그래프와 동일하나, 사이클이 없는 그래프를 의미하며 계층 구조를 나타낼 때 용이합니다.
<br>

**43. 우선순위 큐의 구현 방법은?**

        배열, 링크드리스트, 힙으로 구현할 수 있습니다.
        - 배열과 링크드리스트로 구현할 경우 enqueue는 O(1), dequeue는 O(N)의 시간복잡도를 갖습니다
        - 힙으로 구현할 경우, 그 자체로 우선순위 큐의 역할을 할 수 있고, enqueue/dequeue 연산에서 모두 O(logN)을 보장합니다.

<br>

**44. 힙을 배열로 구현하는 이유는?**

        힙은 새로운 노드를 힙의 '마지막 위치'에 추가한 뒤 정렬하는데, 이때 array기반으로 구현하면 이 과정이 수월해진다.
        또한 완전 이진트리 기반이므로 배열의 인덱스로 부모-자식 인덱스를 쉽게 찾을 수 있습니다
<br>