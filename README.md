# Reverse_Display-Recursion
public class reverseNums {

	static int i = 0;// keep the counter outside of the method so that it does
						// not get reinitialized

	public static void reverseDisplay(int n) {
		// change the int value to a string

		String number = Integer.toString(n);

		// if the string length equals the counter, then the method is finished
		if (i == number.length()) {
			System.out.println(number);
		} else {
			// if i is 0 then switch the last index to the front. Other wise
			// insert the last number in the list right before the number that
			// was added previously
			if (i == 0)
				number = number.substring(number.length() - 1)
						+ number.substring(i, number.length() - 1);
			else
				number = number.substring(0, i)
						+ number.charAt(number.length() - 1)
						+ number.substring(i, number.length() - 1);

			i++;
			reverseDisplay(Integer.parseInt(number));
		}
	}

	public static void main(String[] args) {
		reverseDisplay(12345);
	}

}

