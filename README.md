# cp-snippet-java
Competitive programming code snippet for java users. Feel free to clone/fork/copy.  
Make sure you hit the star⭐️ button if you like this snippet. You'll make my day.

## Getting Started

1. Install [Visual Studio Code](https://code.visualstudio.com/), and set up [JDK](https://openjdk.org/install/).

2. Go to `Settings` > `User Snippet` > `java.json`

3. Paste below inside `java.json`

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
    "For loop":{
        "prefix" : "forl",
        "body" : [
            "for(int i= 0; i < $0; i++)"
        ]
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
