import java.util.Scanner;
public class Bitstuffing{
	public static void main (String[] args){
		Scanner sc = new Scanner(System.in);
                System.out.println("Enter the Binary Message:");
		String input =sc.next();
		String result="";
		int count =0;
		for(int i=0;i<input.length();i++) {
			char ch = input.charAt(i);
		result+=ch;
		if(ch=='1') {
			count++;
			if(count==5) {
				result+="0";
		        count=0;
			}
		}else {
			count=0;
		}
	}
		String flag="01111110";
		System.out.println("Original Meassage is:"+input);
		System.out.println("Stuffed Messsage"+result);
                System.out.println("Fframed Message:"+flag+result+flag);
 sc.close();
}
}
