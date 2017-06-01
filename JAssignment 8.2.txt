class negativeageexception extends Exception
{
	public void display()
	{
		System.out.println("the age is negative which cant be so throwing the exception");
	}
}
public class NegativeAge {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		int age=-10;
		if(age<0)
		{
			try
			{
				negativeageexception nae=new negativeageexception();
				throw nae;
			}
			catch(negativeageexception nae1)
			{
				nae1.display();
			}
		}
		
	}

}
