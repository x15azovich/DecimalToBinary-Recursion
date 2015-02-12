# DecimalToBinary-Recursion
public class Binarys {
	// static s in order to prevent the string from being initialized to ""
	// again and again.
	static String s = "";

	public static String decimalToBinary(int n) {
		// if n is less than 2 than the last number can only return a 1 or 0 so
		// add the 1 or 0 to the end of the string
		if (n < 2) {
			s = n + s;
			return s;
		}
		// if n does not equal 0 then the string will keep adding the modulus of
		// 2 to the string in order to convert the decimal into binary.
		// It will then recursively keep diving by 2 until n is less than 2.
		if (n != 0) {
			s = (Integer.toString(n % 2)) + s;
			decimalToBinary(n / 2);

		}
		return s;
	}

	public static void main(String[] args) {
		System.out.println(decimalToBinary(11));
	}
}
