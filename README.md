package foobar;

public class foobar {
	public static void main(String[] args) {
		String s = 	"01100110 01101001 01101110 01100100 00101110 01100110 01101111 01101111 00101111 01100101 01101101 01100101 01100001 01100011 01101000 01100001 01101100 01101100 01100101 01101110 01100111 01100101 00110010 00110011";
		String[] arrs = s.split(" ");
		StringBuilder sb = new StringBuilder();
		for(String e : arrs) {
			int i = convertBinaryToDecimal(Long.parseLong(e));//convert from binary to decimal
		 
			char ch = (char) i;//ascci code  
			sb.append(ch);
		} 
		System.out.println(sb.toString());
	}
	 public static int convertBinaryToDecimal(long num) {
		    int decimalNumber = 0, i = 0;
		    long remainder;
		    
		    while (num != 0) {
		      remainder = num % 10;
		      num /= 10;
		      decimalNumber += remainder * Math.pow(2, i);
		      ++i;
		    }  return decimalNumber;
	  }
}
