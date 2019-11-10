## Algorithm

[单词接龙](https://leetcode-cn.com/problems/word-ladder/description/) && [Code](https://github.com/learnITpossible/leetcode/blob/master/src/main/java/com/markdown/leetcode/editor/cn/LeetCode_127_WordLadder.java)

[单词接龙ii](https://leetcode-cn.com/problems/word-ladder-ii/description/) && [Code](https://github.com/learnITpossible/leetcode/blob/master/src/main/java/com/markdown/leetcode/editor/cn/LeetCode_126_WordLadderIi.java)

## Review

[Clean Code : Book Review](https://markhneedham.com/blog/2008/09/15/clean-code-book-review/)

1. 像报纸一样组织你的代码结构 -- 自顶向下的编程方法。
1. 对第三方代码编写测试用例。
1. 如果测试代码很烂，那么你的所有代码都很烂 -- 单元测试的重要性。
1. 专家级程序员把系统看成一个要讲故事，而不是要写的程序 -- 程序的可读性。

## Tip

在做**单词接龙**题的过程中，一开始自己提交的代码的**执行用时**总是很长，高达 1000+ ms。最后终于弄明白，原来是因为题目参数中的词库`wordList`是一个 List。一开始，判断变换后的单词是否在词库中，是直接调用的 List 的 contains 函数，相当于每次都去遍历这个 List。后来将其包装成`wordSet`，速度瞬间提高了两个数量级。

```
public int ladderLength(String beginWord, String endWord, List<String> wordList) {
    Set<String> wordSet = new HashSet<>(wordList);
```

```
if (!visited.contains(newWord) && wordSet.contains(newWord)) {
    visited.add(newWord);
    temp.add(newWord);
}
```

![提交记录](https://github.com/learnITpossible/ARTS/blob/master/image/%E5%8D%95%E8%AF%8D%E6%8E%A5%E9%BE%99.png)

## Share

数据结构是真的有用！
