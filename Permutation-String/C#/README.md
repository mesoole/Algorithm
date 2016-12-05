# all permutations of a given string in Java
```
namespace justHaveFun.Permutation
{
    class PermutationGivenString
    {
        public static void permutation(String str)
        {
            permutation("", str);
        }

        private static void permutation(String prefix, String str)
        {
            int n = str.Length;
            if (n == 0) Console.WriteLine(prefix);
            else
            {
                for (int i = 0; i < n; i++)
                    permutation(prefix + str[i], MySubString(str, 0, i) + MySubString(str, i + 1, n));
            }
        }
        public static string MySubString(string s, int start, int end)
        {
            return s.Substring(start, end - start);
        }
        public static void Main(string[] args)
        {
            // TODO Auto-generated method stub
            String test = "Hasn";
            int length = test.Length;
            //System.out.println(test.mysubstring(0, 0));//--NOTHING--
            //System.out.println(test.substring(1, length));//asan
            permutation(test);
        }
    }
}
```