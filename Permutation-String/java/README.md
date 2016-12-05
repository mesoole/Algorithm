# all permutations of a given string in Java
```
package permutation;

public class PermutationGivenString {

	public static void permutation(String str) { 
	    permutation("", str); 
	}

	private static void permutation(String prefix, String str) {
	    int n = str.length();
	    if (n == 0) System.out.println(prefix);
	    else {
	        for (int i = 0; i < n; i++)
	            permutation(prefix + str.charAt(i), str.substring(0, i) + str.substring(i+1, n));
	    }
	}
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		String test= "Hasan";
		int length = test.length();
		System.out.println(test.substring(0,0));//--NOTHING--
		System.out.println(test.substring(1,length));//asan
		permutation(test);
	}

}
```