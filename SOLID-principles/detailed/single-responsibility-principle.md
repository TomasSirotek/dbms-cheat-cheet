****

#### One class should only have one responsibility 

* Instead of having one class do multiple method we should seperate it 

``` java

public class UserService 
{
	public void changeEmail(User user)
	{
		// Grant option to change 
	}
	public boolean checkAccess(User user)
	{
		// Verify if the user is valid 
	}
}
```

* **Correct**  approach to this problem to seperate into two different classes 

``` java

public class UserService 
{
	public void changeEmail(User user)
	{
		// Grant option to change 
	}
}
```

``` java

public class SecurityService
{
	public boolean checkAccess(User user)
	{
		// Verify if the user is valid 
	}
}
```
