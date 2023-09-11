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

                "private static void solve() {",
                    "$0",
                "}",

                "static class FastScanner {",
                    "BufferedReader br;",
                    "StringTokenizer st;",

                    "public FastScanner() {",
                        "try {",
                            "br = new BufferedReader(new FileReader(\"input.txt\"));",
                            "PrintStream out = new PrintStream(new FileOutputStream(\"output.txt\"));",
                            "System.setOut(out);",
                        "} catch(Exception e) {",
                            "br = new BufferedReader(new InputStreamReader(System.in));",
                        "}",
                    "}",
                    "String next() {",
                        "while (st == null || !st.hasMoreElements()) {",
                            "try {",
                                "st = new StringTokenizer(br.readLine());",
                            "} catch (IOException e) {",
                                "e.printStackTrace();",
                            "}",
                        "}",
                        "return st.nextToken();",
                    "}",

                    "String nextLine() {",
                        "String str = \"\";",
                        "try {",
                            "str = br.readLine();",
                        "} catch (IOException e) {",
                            "e.printStackTrace();",
                        "}",
                        "return str;",
                    "}",
                    
                    "int nextInt() { return Integer.parseInt(next()); }",
                    
                    "long nextLong() { return Long.parseLong(next()); }",
                    
                    "double nextDouble() { return Double.parseDouble(next()); }",
                "}",

                "public static void main(String[] args) {",
                    "int T = sc.nextInt();",
                    "for (int t = 1; t <= T; ++t) {",
                        "if (t > 1) System.out.println();",
                        "solve();",
                    "}",
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

                "private static void solve() {",
                    "$0",
                "}",

                "static class FastScanner {",
                    "BufferedReader br;",
                    "StringTokenizer st;",

                    "public FastScanner() {",
                        "try {",
                            "br = new BufferedReader(new FileReader(\"input.txt\"));",
                            "PrintStream out = new PrintStream(new FileOutputStream(\"output.txt\"));",
                            "System.setOut(out);",
                        "} catch(Exception e) {",
                            "br = new BufferedReader(new InputStreamReader(System.in));",
                        "}",
                    "}",
                    "String next() {",
                        "while (st == null || !st.hasMoreElements()) {",
                            "try {",
                                "st = new StringTokenizer(br.readLine());",
                            "} catch (IOException e) {",
                                "e.printStackTrace();",
                            "}",
                        "}",
                        "return st.nextToken();",
                    "}",

                    "String nextLine() {",
                        "String str = \"\";",
                        "try {",
                            "str = br.readLine();",
                        "} catch (IOException e) {",
                            "e.printStackTrace();",
                        "}",
                        "return str;",
                    "}",
                    
                    "int nextInt() { return Integer.parseInt(next()); }",
                    
                    "long nextLong() { return Long.parseLong(next()); }",
                    
                    "double nextDouble() { return Double.parseDouble(next()); }",
                "}",

                "public static void main(String[] args) {",
                    "int T = sc.nextInt();",
                    "for (int t = 1; t <= T; ++t) {",
                        "if (t > 1) System.out.println();",
                        "System.out.print(\"Case #\" + t + \": \");",
                        "solve();",
                    "}",
                "}",
            "}"
        ],
        "description": "template for baekjoon online judge cp in java"
    },
    "For loop i": {
        "prefix": "fori",
        "body": [
            "for (int i= 0; i < $0; ++i) {",
            "}"
        ],
        "description": "simple for loop"
    },
    "For loop j": {
        "prefix": "forj",
        "body": [
            "for (int j= 0; j < $0; ++j)"
        ],
        "description": "simple for loop"
    },
    "For loop k": {
        "prefix": "fork",
        "body": [
            "for (int k= 0; k < $0; ++k)"
        ],
        "description": "simple for loop"
    },
    "For loop l": {
        "prefix": "forl",
        "body": [
            "for (int l= 0; l < $0; ++l)"
        ],
        "description": "simple for loop"
    },
    "Print": {
        "prefix": "print",
        "body": [
            "System.out.print($0);"
        ],
        "description": "simple print method"
    },
    "Print Line": {
        "prefix": "printl",
        "body": [
            "System.out.println($0);"
        ],
        "description": "simple print line method"
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
                
                "void swap(int[] arr, int a, int b) {",
                    "int tmp = arr[a];",
                    "arr[a] = arr[b];",
                    "arr[b] = tmp;",
                "}",
                
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
                
                "TrieNode(char val) {",
                    "this.val = val;",
                    "children = new HashMap<>();",
                "}",
                
                "char getVal() {",
                    "return val;",
                "}",
                
                "void setVal(char val) {",
                    "this.val = val;",
                "}",
                
                "void addChild(TrieNode node) {",
                    "children.put(node.getVal(), node);",
                "}",
                
                "TrieNode getChild(char c) {",
                    "return children.get(c);",
                "}",
                
                "boolean findWord(String word) {",
                    "if (word.length() == 0)",
                        "return exist;",
                    "if (!children.containsKey(word.charAt(0)))",
                        "return false;",
                    "return children.get(word.charAt(0)).findWord(word.substring(1));",
                "}",
                
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
    },
    "Prime Utils": {
        "prefix": "primeutil",
        "body": [
            "static class PrimeUtil {",
                "static Map<Integer, List<Integer>> factors(int upTo) {",
                    "Map<Integer, List<Integer>> p = new HashMap<>();",
                    "p.put(1, new ArrayList<>());",
                    "for (int i = 2; i <= upTo; ++i) {",
                        "if (!p.containsKey(i)) {",
                            "for (int j = i; j <= upTo; j += i) {",
                                "p.computeIfAbsent(j, primes -> new ArrayList<>()).add(i);",
                            "}",
                        "}",
                    "}",
                    "return p;",
                "}",

                "static int countPrimeFactors(long num) {",
                    "if (num == 1) return 0;",
                    "int cnt= 0;",
                    "for (int i=2; i*i <= num; ++i) {",
                        "if (num%i == 0) {",
                            "++cnt;",
                            "while (num%i == 0) num /= i;",
                        "}",
                    "}",
                    "return num > 1 ? cnt+1 : cnt;",
                "}",

                "static boolean isPrime(long num) {",
                    "return countPrimeFactors(num) == 1;",
                "}",
            "}"
        ],
        "description": "factorization using sieve of Eratosthenes"
    },
    "Modular Utils": {
        "prefix": "modutil",
        "body": [
            "private static final int MOD= (int)1e9+7;",

            "private static int add(int a, int b) { return (int)((a+0L+b)%MOD); }",

            "private static int mul(int a, int b) { return (int)(a*1L*b%MOD); }",

            "private static int inv(int a) { return binEx(a, MOD-2); }",

            "private static int div(int a, int b) { return mul(a, inv(b)); }",

            "private static int binEx(int a, int x) {",
                "if (x == 0) return 1;",
                "int p= binEx(a, x/2);",
                "p= mul(p, p);",
                "return x%2 == 1 ? mul(p,a) : p;",
            "}"
        ],
        "description": "modular embedded basic operations"
    },
    "KMP Algorithm": {
        "prefix": "kmp",
        "body": [
            "static class Kmp {",
                "int n;",
                "char[] p;",
                "int[] lps;",
                
                "Kmp(String pattern) {",
                    "n= pattern.length();",
                    "p= pattern.toCharArray();",
                    "lps= new int[n];",
                    "int len= 0, i= 1;",
                    "while (i < n) {",
                        "if (p[len] == p[i]) {",
                            "lps[i++]= ++len;",
                        "} else {",
                            "if (len > 0) {",
                                "len= lps[len-1];",
                            "} else {",
                                "lps[i++]= 0;",
                            "}",
                        "}",
                    "}",
                "}",
        
                "List<Integer> getMatchIndices(String text) {",
                    "List<Integer> ret= new ArrayList<>();",
                    "int i= 0, len= 0;",
                    "while (i < text.length()) {",
                        "if (len == n) {",
                            "ret.add(i-n);",
                            "++i;",
                            "len= lps[len-1];",
                            "continue;",
                        "}",
                        "if (text.charAt(i) == p[len]) {",
                            "++i;",
                            "++len;",
                        "} else {",
                            "if (len > 0) len= lps[len-1];",
                            "else ++i;",
                        "}",
                    "}",
                    "return ret;",
                "}",
            "}"
        ],
        "description": "kmp algorithm class"
    }
```

4. Try to use snippet inside the editor. Make sure you format the whole content.  
   It's ugly when it appears.

### FYI. Keyboard shortcut for auto-format

- Mac: `⌥` + `⇧` + `F`
- Windows: `alt` + `shift` + `F`

## Template Preview

### Codeforces

> prefix: "cft"

```java
import java.util.*;
import java.io.*;

public class Main {
    private static FastScanner sc = new FastScanner();

    private static void solve() {

    }

    static class FastScanner {
        BufferedReader br;
        StringTokenizer st;

        public FastScanner() {
            try {
                br = new BufferedReader(new FileReader("input.txt"));
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

        String nextLine() {
            String str = "";
            try {
                str = br.readLine();
            } catch (IOException e) {
                e.printStackTrace();
            }
            return str;
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
    }

    public static void main(String[] args) {
        int T = sc.nextInt();
        for (int t = 1; t <= T; ++t) {
            if (t > 1)
                System.out.println();
            solve();
        }
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

    private static void solve() {

    }

    static class FastScanner {
        BufferedReader br;
        StringTokenizer st;

        public FastScanner() {
            try {
                br = new BufferedReader(new FileReader("input.txt"));
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

        String nextLine() {
            String str = "";
            try {
                str = br.readLine();
            } catch (IOException e) {
                e.printStackTrace();
            }
            return str;
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
    }

    public static void main(String[] args) {
        int T = sc.nextInt();
        for (int t = 1; t <= T; ++t) {
            if (t > 1)
                System.out.println();
            System.out.print("Case #" + t + ": ");
            solve();
        }
    }
}
```
