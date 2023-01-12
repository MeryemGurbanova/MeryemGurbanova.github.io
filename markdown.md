## Useful Links

1. [Wikipedia](https://www.wikipedia.org/)
1. [Canvas](https://snow.instructure.com/)
1. [BadgerWeb](https://sso.snow.edu/authenticationendpoint/login.do?Name=PreLoginRequestProcessor&commonAuthCallerPath=%252Fcas%252Flogin&forceAuth=true&passiveAuth=false&service=https%3A%2F%2Fprod.snow.edu%3A443%2Fssomanager%2Fc%2FSSB&tenantDomain=carbon.super&sessionDataKey=9ca55edb-b9b4-462a-8c0e-7e10584bb244&relyingParty=PROD_SSOMgr&type=cas&sp=PROD_SSOMgr&isSaaSApp=false&authenticators=BasicAuthenticator%3ALOCAL)
## Some Code
#### My fav method (Input validation)

```
public static string CheckValidInputs(string actualInput, params string[] validinputs)
    {
        try
        {
            if (!validinputs.Contains(actualInput))
            {
                throw new Exception();
            }
            return actualInput;
        }
        catch (System.Exception)
        {
            Console.ForegroundColor = ConsoleColor.Yellow;
            Console.Write("Please type index or options you have in order to continue: ");
            Console.ForegroundColor = ConsoleColor.White;
            return CheckValidInputs(Console.ReadLine().ToLower(), validinputs);
        }
    }
```