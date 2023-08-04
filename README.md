# cp-snippet-java

Competitive programming code snippet for java users. Feel free to clone/fork/copy.  
Make sure you hit the star⭐️ button if you like this snippet. You'll make my day.

## Getting Started

1. Install [Visual Studio Code](https://code.visualstudio.com/), and set up [JDK](https://openjdk.org/install/).

2. Go to `Settings` > `User Snippet` > `java.json`

3. Paste below key-value's into `java.json`

```json
    "Template for codeforces CP" : {
        "prefix": "cft",
        "body":[
            "import java.util.*;",
            "import java.io.*;",

            "public class Main {",
                "private static FastScanner sc = new FastScanner();",

                "private static String solve() {",
                    "return \"\";$0",
                "}",

                "static class FastScanner {",
                    "BufferedReader br;",
                    "StringTokenizer st;",

                    "public FastScanner()",
                    "{ try {br = new BufferedReader(",
                        "new FileReader(\"input.txt\"));",
                        "PrintStream out = new PrintStream(new FileOutputStream(\"output.txt\"));",
                        "System.setOut(out);}",
                    "catch(Exception e) { br = new BufferedReader(new InputStreamReader(System.in));}",
                    "}",

                    "String next()",
                    "{",
                        "while (st == null || !st.hasMoreElements()) {",
                            "try {st = new StringTokenizer(br.readLine());}",
                            "catch (IOException e) {",
                                "e.printStackTrace();}",
                        "}",
                        "return st.nextToken();",
                    "}",

                    "int nextInt() { return Integer.parseInt(next()); }",
                    "long nextLong() { return Long.parseLong(next()); }",
                    "double nextDouble() {return Double.parseDouble(next()); }",

                    "String nextLine()",
                    "{",
                        "String str = \"\";",
                        "try {",
                        "str = br.readLine();",
                        "}",
                        "catch (IOException e) {",
                            "e.printStackTrace();",
                        "}",
                        "return str;",
                    "}",
                "}",

                "public static void main(String[] args) {",
                    "StringBuilder sb= new StringBuilder();",
                    "int T= sc.nextInt();",
                    "for (int t=1; t <= T; ++t) {",
                        "if (t > 1) sb.append(\"\\n\");",
                        "sb.append(solve());",
                    "}",
                    "System.out.print(sb);",
                "}",
            "}"
        ],
        "description": "template for codeforces cp in java"
    },
    "Template for baekjoon online judge CP" : {
        "prefix": "bojt",
        "body":[
            "import java.util.*;",
            "import java.io.*;",

            "public class Main {",
                "private static FastScanner sc = new FastScanner();",

                "private static String solve() {",
                    "return \"\";$0",
                "}",

                "static class FastScanner {",
                    "BufferedReader br;",
                    "StringTokenizer st;",

                    "public FastScanner()",
                    "{ try {br = new BufferedReader(",
                        "new FileReader(\"input.txt\"));",
                        "PrintStream out = new PrintStream(new FileOutputStream(\"output.txt\"));",
                        "System.setOut(out);}",
                    "catch(Exception e) { br = new BufferedReader(new InputStreamReader(System.in));}",
                    "}",

                    "String next()",
                    "{",
                        "while (st == null || !st.hasMoreElements()) {",
                            "try {st = new StringTokenizer(br.readLine());}",
                            "catch (IOException e) {",
                                "e.printStackTrace();}",
                        "}",
                        "return st.nextToken();",
                    "}",

                    "int nextInt() { return Integer.parseInt(next()); }",
                    "long nextLong() { return Long.parseLong(next()); }",
                    "double nextDouble() {return Double.parseDouble(next()); }",

                    "String nextLine()",
                    "{",
                        "String str = \"\";",
                        "try {",
                        "str = br.readLine();",
                        "}",
                        "catch (IOException e) {",
                            "e.printStackTrace();",
                        "}",
                        "return str;",
                    "}",
                "}",

                "public static void main(String[] args) {",
                    "StringBuilder sb= new StringBuilder();",
                    "int T= sc.nextInt();",
                    "for (int t=1; t <= T; ++t) {",
                        "if (t > 1) sb.append(\"\\n\");",
                        "sb.append(\"Case #\" + t + \": \");",
                        "sb.append(solve());",
                    "}",
                    "System.out.print(sb);",
                "}",
            "}"
        ],
        "description": "template for baekjoon online judge cp in java"
    },
    "For loop": {
        "prefix": "forl",
        "body": [
            "for (int i= 0; i < $0; ++i)"
        ],
        "description": "simple for loop"
    },
    "Next Permutation": {
        "prefix": "permu",
        "body": [
            "static class Permu {",
                "int[] nextPermutation(int[] arr) {",
                    "int n = arr.length;",
                    "int[] ret = new int[n];",
                    "for (int i = 0; i < n; ++i)",
                    "ret[i] = arr[i];",
                    "int pivot = n - 1;",
                    "while (pivot > 0 && ret[pivot - 1] >= ret[pivot])",
                    "--pivot;",
                    "if (pivot > 0) {",
                        "--pivot;",
                        "int idx = n - 1;",
                        "while (ret[idx] <= ret[pivot])",
                        "--idx;",
                        "swap(ret, pivot, idx);",
                        "reverse(ret, pivot + 1, n - 1);",
                    "} else {",
                        "Arrays.sort(ret);",
                    "}",
                    "return ret;",
                "}",
                "\n",
                "void swap(int[] arr, int a, int b) {",
                    "int tmp = arr[a];",
                    "arr[a] = arr[b];",
                    "arr[b] = tmp;",
                "}",
                "\n",
                "void reverse(int[] arr, int l, int r) {",
                    "int[] buf = new int[r - l + 1];",
                    "for (int i = l; i <= r; ++i)",
                        "buf[i - l] = arr[r - (i - l)];",
                    "for (int i = 0; i < r - l + 1; ++i)",
                        "arr[l + i] = buf[i];",
                "}",
            "}"
        ],
        "description": "next permutation implementation in java"
    },
    "Trie": {
        "prefix": "trie",
        "body": [
            "static class TrieNode {",
                "char val;",
                "boolean exist;",
                "Map<Character, TrieNode> children;",
                "\n",
                "TrieNode(char val) {",
                    "this.val = val;",
                    "children = new HashMap<>();",
                "}",
                "\n",
                "char getVal() {",
                    "return val;",
                "}",
                "\n",
                "void setVal(char val) {",
                    "this.val = val;",
                "}",
                "\n",
                "void addChild(TrieNode node) {",
                    "children.put(node.getVal(), node);",
                "}",
                "\n",
                "TrieNode getChild(char c) {",
                    "return children.get(c);",
                "}",
                "\n",
                "boolean findWord(String word) {",
                    "if (word.length() == 0)",
                        "return exist;",
                    "if (!children.containsKey(word.charAt(0)))",
                        "return false;",
                    "return children.get(word.charAt(0)).findWord(word.substring(1));",
                "}",
                "\n",
                "void addWord(String word) {",
                    "if (word.length() == 0) {",
                        "exist = true;",
                        "return;",
                    "}",
                    "TrieNode child = children.get(word.charAt(0));",
                    "if (child == null) {",
                        "addChild(new TrieNode(word.charAt(0)));",
                        "child = children.get(word.charAt(0));",
                    "}",
                    "child.addWord(word.substring(1));",
                "}",
            "}"
        ],
        "description": "trie data structure"
    }
```

4. Try to use snippet inside the editor. Make sure you format the whole content.  
   It's ugly when it appears.

### FYI. Keyboard shortcut for auto-format

- Mac: `opt` + `shift` + `F`
- Windows: `alt` + `shift` + `F`

## Template Preview

### Codeforces

> prefix: "cft"

```java
import java.util.*;
import java.io.*;

public class Main {
    private static FastScanner sc = new FastScanner();

    private static String solve() {
        return "";
    }

    static class FastScanner {
        BufferedReader br;
        StringTokenizer st;

        public FastScanner() {
            try {
                br = new BufferedReader(
                        new FileReader("input.txt"));
                PrintStream out = new PrintStream(new FileOutputStream("output.txt"));
                System.setOut(out);
            } catch (Exception e) {
                br = new BufferedReader(new InputStreamReader(System.in));
            }
        }

        String next() {
            while (st == null || !st.hasMoreElements()) {
                try {
                    st = new StringTokenizer(br.readLine());
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            return st.nextToken();
        }

        int nextInt() {
            return Integer.parseInt(next());
        }

        long nextLong() {
            return Long.parseLong(next());
        }

        double nextDouble() {
            return Double.parseDouble(next());
        }

        String nextLine() {
            String str = "";
            try {
                str = br.readLine();
            } catch (IOException e) {
                e.printStackTrace();
            }
            return str;
        }
    }

    public static void main(String[] args) {
        StringBuilder sb = new StringBuilder();
        int T = sc.nextInt();
        for (int t = 1; t <= T; ++t) {
            if (t > 1)
                sb.append("\n");
            sb.append(solve());
        }
        System.out.print(sb);
    }
}
```

### Baekjoon Online Judge

> prefix: "bojt"

```java
import java.util.*;
import java.io.*;

public class Main {
    private static FastScanner sc = new FastScanner();

    private static String solve() {
        return "";
    }

    static class FastScanner {
        BufferedReader br;
        StringTokenizer st;

        public FastScanner() {
            try {
                br = new BufferedReader(
                        new FileReader("input.txt"));
                PrintStream out = new PrintStream(new FileOutputStream("output.txt"));
                System.setOut(out);
            } catch (Exception e) {
                br = new BufferedReader(new InputStreamReader(System.in));
            }
        }

        String next() {
            while (st == null || !st.hasMoreElements()) {
                try {
                    st = new StringTokenizer(br.readLine());
                } catch (IOException e) {
                    e.printStackTrace();
                }
            }
            return st.nextToken();
        }

        int nextInt() {
            return Integer.parseInt(next());
        }

        long nextLong() {
            return Long.parseLong(next());
        }

        double nextDouble() {
            return Double.parseDouble(next());
        }

        String nextLine() {
            String str = "";
            try {
                str = br.readLine();
            } catch (IOException e) {
                e.printStackTrace();
            }
            return str;
        }
    }

    public static void main(String[] args) {
        StringBuilder sb = new StringBuilder();
        int T = sc.nextInt();
        for (int t = 1; t <= T; ++t) {
            if (t > 1)
                sb.append("\n");
            sb.append("Case #" + t + ": ");
            sb.append(solve());
        }
        System.out.print(sb);
    }
}
```
