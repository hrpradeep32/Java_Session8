import java.io.BufferedReader;
import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;


public class VowelsinFile {

	public static void main(String[] args) throws IOException {
		// TODO Auto-generated method stub
		File f=new File("c:\\destination\\file1.txt");
		FileReader fr=new FileReader(f);
		BufferedReader br=new BufferedReader(fr);
		String str=br.readLine();
		int vowels=0;
		while(str!=null)
		{
			for(int i=0;i<str.length();i++)
			{
				if(str.charAt(i)=='a'||str.charAt(i)=='e'||str.charAt(i)=='i'||str.charAt(i)=='o'||str.charAt(i)=='u')
					vowels++;
			}
			str=br.readLine();
		}
		System.out.println("total number of vowels in the file is : "+vowels);
	}

}
