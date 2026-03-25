# Ex.No:4(E) DESIGN PATTERN  ---- MEDIATOR PATTERN

## QUESTION:
Create a ChatRoom class (mediator) and two users (colleagues) who send and receive messages through it. No direct communication allowed. (Mediator Pattern)

## AIM:
To implement the Mediator Design Pattern in Java by creating a ChatRoom (mediator) that enables communication between users without direct interaction.

## ALGORITHM :
1.Start the program.

2.Create a ChatRoom class to act as a mediator and store users.

3.Add a method to register users in the chat room.

4.Add a method to send messages from one user to another via the mediator.

5.Create a User class with attributes name and reference to ChatRoom.

6.Register each user in the chat room when created.

7.Implement send() method in User to pass messages through ChatRoom.

8.Implement receive() method in User to display received messages.

9.In the main method, take input for two users and number of messages.

10.For each message, read sender, receiver, and message content.

11.Use the mediator (ChatRoom) to deliver the message.

12.Display appropriate output or error if user not found.

13.End the program.




## PROGRAM:
 ```
/*
Program to implement a Mediator Pattern using Java
Developed by: VISMAYA.V
RegisterNumber:212224060310  
*/
```

## SOURCE CODE:
```
import java.util.*;

class ChatRoom
{
    private Map<String,User>users=new HashMap<>();
    public void registerUser(User user)
    {
        users.put(user.getName(),user);
    }
    public void sendMessage(String from,String to,String message)
    {
        User receiver=users.get(to);
        if(receiver!=null)
        {
            receiver.receive(from,message);
        }
        else
        {
            System.out.println("User "+ to + "not found");
        }
    }
}

class User
{
    private String name;
    private ChatRoom chatRoom;
    public User(String name,ChatRoom chatRoom)
    {
        this.name=name;
        this.chatRoom=chatRoom;
        chatRoom.registerUser(this);
    }
    public String getName()
    {
        return name;
    }
    public void send(String to,String message)
    {
        chatRoom.sendMessage(name,to,message);
    }
    public void receive(String from,String message)
    {
        System.out.println(from + " to "+ name +": "+message);
    }
}

public class ChatApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        ChatRoom room=new ChatRoom();
        User user1=new User(sc.nextLine(),room);
        User user2=new User(sc.nextLine(),room);
        int n=Integer.parseInt(sc.nextLine());
        for(int i=0;i<n;i++)
        {
            String sender=sc.nextLine();
            String receiver=sc.nextLine();
            String message=sc.nextLine();
            if(sender.equals(user1.getName()))
            {
                user1.send(receiver,message);
            }
            else if(sender.equals(user2.getName()))
            {
                user2.send(receiver,message);
            }
            else
            {
                System.out.println("Unknown sender");
            }
        }
        sc.close();
    }
}




```


## OUTPUT:
<img width="1228" height="874" alt="image" src="https://github.com/user-attachments/assets/5a032d92-03ef-4509-9a31-fd4e85179361" />



## RESULT:
Therefore,the program was executed successfully.
