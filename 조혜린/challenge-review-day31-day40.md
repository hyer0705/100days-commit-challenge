# 지난 10일 나의 목표는?!

- [x] 프로젝트 캠프 - 프로젝트 코스 기간 열심히 참여하기. 9월 13일까지 마무리 해야하는 일이 있는데 잘 마무리하도록 열심히 참여하기!!!
- [ ] 아침 6시에 기상해서 1시간은 챌린지 스터디하기
- [ ] 아침 7시에는 헬스장가서 10분 스트레칭 + 10분 속도 7~9로 런닝머신 뛰기

# 10일 돌아보면 잘한 점

- 프로젝트를 진행하면서도 하루를 제외하고는 매일 챌린지에 참여했다.
- 하루에 한 문제를 푸는 것을 목표로 했지만, 최근에는 정답 풀이 없이 풀기 어려운 문제들이 많아졌다. 그래서 복습 시간을 가지게 됐다. 어제 정답을 보고 풀이한 문제를, 오늘은 정답 없이 스스로 풀어보는 식으로 진행했더니 더 잘 이해되고, 공부도 효과가 있었다. 앞으로 익숙하지 않고 어려운 알고리즘이 많이 나올 텐데, 이 방법을 꾸준히 활용해 봐야겠다.

# 10일 돌아보며 아쉬운 점

- 목표였던 6시 기상은 지켰지만, 일어나자마자 1시간 동안 챌린지 공부를 하고, 20분 동안 운동하는 루틴은 지키지 못했습니다. 주로 일어나고 나서부터 오후 8시까지는 프로젝트에 집중하는 습관이 들어 계획을 지키기 어려웠다. 대신 저녁에 챌린지 공부를 했다.
- 하루는 커밋 내역을 인증하지 못한 날이 있었다. 주말 내내 약속이 있어 체력적으로 지친 상태였고, 결국 그날은 인증을 하지 못한 채 잠들었다. 새벽에 잠깐 깨서 인증할까 고민했지만, 이미 지나간 일이니 굳이 하지 않기로 했다. 이 일을 계기로 주말 하루는 온전히 쉬는 시간을 가져야겠다고 결심하게 됐다.

# 10일 동안 공부한 내용

- 2차원 배열 BFS로 순회하기  
  [참고 자료: Breadth First Traversal ( BFS ) on a 2D array](https://www.geeksforgeeks.org/breadth-first-traversal-bfs-on-a-2d-array/)

  ```javascript
  // Javascript program for the above approach
  var ROW = 4;
  var COL = 4;

  // Direction vectors
  var dRow = [-1, 0, 1, 0];
  var dCol = [0, 1, 0, -1];

  // Function to check if a cell
  // is be visited or not
  function isValid(vis, row, col) {
    // If cell lies out of bounds
    if (row < 0 || col < 0 || row >= ROW || col >= COL) return false;

    // If cell is already visited
    if (vis[row][col]) return false;

    // Otherwise
    return true;
  }
  // Function to perform the BFS traversal
  function BFS(grid, vis, row, col) {
    // Stores indices of the matrix cells
    var q = [];

    // Mark the starting cell as visited
    // and push it into the queue
    q.push([row, col]);
    vis[row][col] = true;

    // Iterate while the queue
    // is not empty
    while (q.length != 0) {
      var cell = q[0];
      var x = cell[0];
      var y = cell[1];

      document.write(grid[x][y] + " ");

      q.shift();

      // Go to the adjacent cells
      for (var i = 0; i < 4; i++) {
        var adjx = x + dRow[i];
        var adjy = y + dCol[i];

        if (isValid(vis, adjx, adjy)) {
          q.push([adjx, adjy]);
          vis[adjx][adjy] = true;
        }
      }
    }
  }

  // Driver Code
  // Given input matrix
  var grid = [
    [1, 2, 3, 4],
    [5, 6, 7, 8],
    [9, 10, 11, 12],
    [13, 14, 15, 16],
  ];
  // Declare the visited array
  var vis = Array.from(Array(ROW), () => Array(COL).fill(false));
  BFS(grid, vis, 0, 0);
  ```

- 트리 BFS로 순회하기

  ```javascript
  class Node {
    constructor(data) {
      this.data = data;
      this.left = null;
      this.right = null;
    }
  }

  class BinaryTree {
    constructor() {
      this.root = null;
    }

    insert(data) {
      const newNode = new Node(data);

      if (!this.root) this.root = newNode;
      else this.insertNode(this.root, newNode);
    }
    insertNode(parent, node) {
      if (parent.data.x < node.data.x) {
        if (parent.right) {
          this.insertNode(parent.right, node);
        } else {
          parent.right = node;
        }
      } else {
        if (parent.left) {
          this.insertNode(parent.left, node);
        } else {
          parent.left = node;
        }
      }
    }

    getRootNode() {
      return this.root;
    }
    preorder(node, answer) {
      if (node) {
        answer.push(node.data.idx);
        this.preorder(node.left, answer);
        this.preorder(node.right, answer);
      }
      return answer;
    }
    inorder(node, answer) {
      if (node) {
        this.inorder(node.left, answer);
        answer.push(node.data.idx);
        this.inorder(node.right, answer);
      }
      return answer;
    }
    postorder(node, answer) {
      if (node) {
        this.postorder(node.left, answer);
        this.postorder(node.right, answer);
        answer.push(node.data.idx);
      }
      return answer;
    }
  }
  ```

# 앞으로 10일 동안 나의 목표는?!

- [ ] 프로젝트 캠프 3주차 열심히 참여하기. 9월 19일 혹은 20일에 중간점검 발표가 있는데 떨지 않고 잘 해내기!
- [ ] 아침 6시에 기상해서 1시간은 챌린지 스터디하기
- [ ] 하루에 10분은 유산소 운동하기!!!
