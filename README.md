# Reverse_Display-Recursion
public class reverseNums {

	static int i = 0;// keep the counter outside of the method so that it does
						// not get reinitialized

	public static void reverseDisplay(int n) {
		// change the int value to a string
		String number = Integer.toString(n);
		// if the string length equals the counter, then the method is finished
		if (number.length() == i) {
			System.out.println(number);
		} else {
			// keep switching the string at the array of 0 to the end of the
			// string until i is equal to the string length
			String x = number.substring(1) + number.charAt(0);

			i++;

			reverseDisplay(Integer.parseInt(x));
		}
	}

	public static void main(String[] args) {
		reverseDisplay(12345);
	}

}
