class bankatm
{
	int atmid;
	String bankname;
	String location;
	int balance;
	bankatm(int atmid1,String bankname1,String location1,int balance1)
	{
		atmid=atmid1;
		bankname=bankname1;
		location=location1;
		balance=balance1;
	}
	void withdraw(int amount)
	{
		
		if(amount>balance||balance<10000)
		{
			try
			{
				bankAtmException b=new bankAtmException();
				throw b;
			}
			catch(bankAtmException b1)
			{
				b1.nobalance();
			}
		}
		else
		{
			balance=balance-amount;
		}
		
	}
}
class bankAtmException extends Exception
{
	public void nobalance()
	{
		System.out.println("not enough balance");
	}
}
public class BankException {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		bankatm ba1=new bankatm(1234,"axis","bangalore",50000);
		bankatm ba2=new bankatm(2345,"hdfc","bangalore",70000);
		bankatm ba3=new bankatm(3456,"icici","bangalore",85000);
		ba1.withdraw(60000);
		ba2.withdraw(20000);
		ba2.withdraw(20000);
		ba2.withdraw(20000);
		ba2.withdraw(20000);
		ba3.withdraw(30000);
		ba3.withdraw(30000);
		ba3.withdraw(30000);
	}

}
