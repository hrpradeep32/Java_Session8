import java.io.File;


public class FileCopy {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		File f1=new File("C:\\source\\file1.txt");
		File f2=new File("C:\\destination\\file1.txt");
		f1.renameTo(f2);
	}

}
