# Hourglass
This project prints an hourglass figure in the console. All you need to do is input the size you would like, and the program will calculate the correct sizing and formatting to print the desired hourglass. Here are some key samples taken from this project:
# public static String base(int n) {
		String base = "";
		for (int i = 0;i < n; i++) {
			base += "\"";
		}
		return "|" + base + "|";
		
	}
This method creates the base of the hourglass with a for loop

# public static String elapseTop(int n) {
		String sand;
		int white = 0;
		for(int i = 0; i <n/2-1; i++) { 
			System.out.println();	
			white+=1;
			for(int p = 0; p<white;p++) {
				System.out.print(" ");
			}	
			sand = "";
			for(int j = 0; j<n-(2*(i+1)); j++){
				sand += ":";
			}
			System.out.print("\\" + sand + "/");
		}return "";
	}
This method creates the sand effect for the top half of the hourglass in the console, which is comprised of colons. It also used slashes for the containment vessel.
  
# public static String midsection(int n) {
		System.out.println();
		if (n%2==1) {
			System.out.print("");
		}
		for(int i = 0; i<n/2; i++) {
			System.out.print(" ");
		}
		if (n%2==0) {
		System.out.print("||");
		}else {
			System.out.print("| |");
		}
		return "";
	}
This code creates the "neck" of the hourglass. It tests wheter or not the neck is larger or smaller in accordance with its overall size so that it appears centered. If it is an even size, the neck will be small, but if it is odd, an extra space will be added within the neck.
	
# public static String elapseBottom(int n) {
		int white = n/2-1;
		String sand;
		for(int i = 0; i<n/2-1; i++){
			System.out.println();
			for (int k = 0; k < white; k++) {
				System.out.print(" ");  
			}			
			white-=1;
			sand = "";
			for(int j = n-(2*(i+1)); j<n; j++){     
				sand += ":";
			} 
			if(n%2!=0) {
				sand += ":";
			}
			System.out.print("/" + sand + "\\");
		}
		return "\n";
This method creates the sand effect for the bottom half of the hourglass in the console, which is comprised of colons. It also used slashes for the containment vessel. 
