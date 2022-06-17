# PEO-Part1-
Login and registration features
public class peoTestresult {
    public String userName;
    public String password;
    public String nameAndSurname;
    public int count_P =0;
    public int count_U =0;
    public String pass_charU="_";
Scanner input= new Scanner(System.in);
   

public boolean checkUserName()
   {
        for (int i = 0; i < userName.length(); i++)
        {
           count_U ++;  
        }
        if (userName.contains(pass_charU) || count_U >5){
    return true;

       }else 
    return false;
    
   }
    
public boolean checkPasswordComplexity()
    {
String spec_charP="$&+,:;=?@#|'<>.-*()%!](A-Z)[0-9] ";
          for (int i = 0; i < password.length(); i++) 
        {
          count_P++;  
        }
        
        if (password.contains(spec_charP) || count_P >8){
    return true;

      } else 
    return false;
    } 
public void TestRegistration()
{

  //student name code start
            System.out.println("Please enter your name and last name");
        nameAndSurname = input.nextLine();
        //student name code end

        //uername code start 
            System.out.println("------------------------------------");
            System.out.println("Enter your Username ");
        userName= input.nextLine();
        
        if(checkUserName() == true)
          {
             System.out.println("Username succesfully captured");

          }
        else {
             System.out.println(" Username is not correcly formated please ensure that your user name contains an underscore and is not more than 5 charters in length");
          
             }
        // username stop
       
        // Password code start 
            System.out.println("------------------------------------");
            System.out.println("Enter your Password ");
        password= input.nextLine();

        if (checkPasswordComplexity () == true)
        {
            System.out.println("Password successfully captured");
        
        }
        else {
            System.out.println("Password is not correctly formatted please ensure that the password contains at least 8 characters, a capital letter, a number and a special character");
            
        }
        //Password stop
            System.out.println("Welcome " + nameAndSurname +". It is great to see you again!");
}  
