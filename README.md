# Huffman-Coding
## Aim
To implement Huffman coding to compress the data using Python.

## Software Required
1. Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>


### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

 
## Program:

 Python
#  SIMPLE CHAT BETWEEN  CLIENT AND SERVER 
```import java.io.*; 
import java.net.*; 
public class Client {
public static void main(String[] args) 
{
try
{
Socket s=new Socket("localhost",7564);
DataOutputStream dos=new DataOutputStream(s.getOutputStream()); 
dos.writeUTF("Hiiii");
dos.close();
s.close();
}
catch(Exception e)
{
}
}
}
```
## server side
```
import java.io.*;
import java.io.DataInputStream;
import java.net.*;
public class Server {
public static void main(String[] args) {
try
{
ServerSocket ss=new ServerSocket(7564); Socket s=ss.accept();
DataInputStream dis=new DataInputStream(s.getInputStream());
String str=(String)dis.readUTF(); 
System.out.println("Message="+str);
ss.close();
}
catch(Exception e)
{
System.out.println(e);
}
}
}
```


#  SIMULATION OF ARP USING JAVA
```
import java.io.*; 
import java.net.*; 
import java.util.*;
public class ClientARP {
public static void main(String[] args) {
try
{
BufferedReader in=new BufferedReader(new InputStreamReader(System.in));
Socket s=new Socket("100.0.0.1",140);
DataInputStream din=new DataInputStream(s.getInputStream());
DataOutputStream dout=new DataOutputStream(s.getOutputStream());
System.out.println("Enter the logical address(IP):");
String str1=in.readLine(); dout.writeBytes(str1+'\n'); String str=in.readLine();
System.out.println("The physical address is"+str); s.close();
}
catch(Exception e)
{
System.out.println(e);
}
}
}
```
## server side:
```
import java.io.*; 
import java.net.*; 
import java.util.*;
public class ServerARP
{
public static void main(String[] args) 
{
try
{
ServerSocket ss=new ServerSocket(139); Socket s=ss.accept();
while(true)
{
DataInputStream din=new DataInputStream(s.getInputStream());
DataOutputStream dout=new DataOutputStream(s.getOutputStream());
System.out.println("Enter the logical address(IP):");
String str=din.readLine();
String ip[]= {"111.55.90.80","170.165.79.1"};
String mac[]= {"6A:08:AB:C2","8A:AC:E3:FA"};
for(int i=0;i<ip.length;i++)
{
if(str.equals(ip[i]))
{
dout.writeBytes(mac[i]+'\n');
break;
}
}
ss.close();
}
}
catch(Exception e)
{
System.out.println(e);
}
}
```




# SIMULATION OF RARP USING JAVA
```
ServerRARP.java:
import java.io.*; 
import java.net.*; 
class ServerRARP
{
public static void main(String args[])
EX NO: 04
DATE:
 
 SIMULATION OF RARP USING JAVA
{
try
{
ServerSocket obj=new ServerSocket(2422); 
Socket obj1=obj.accept();
while(true)
{
DataInputStream din=new DataInputStream(obj1.getInputStream());
DataOutputStreamdout=newDataOutputStream(obj1.getOutputStream()); 
String str=din.readLine();
String ip[]={"165.165.80.80","165.165.79.1"};
String mac[]={"6A:08:AA:C2","8A:BC:E3:FA"};
for(int i=0;i<mac.length;i++)
{
if(str.equals(mac[i]))
{
dout.writeBytes(ip[i]+'\n');
break;
}
}
obj.close();
}
}
catch(Exception e)
{
System.out.println(e);
}
}
}
```
## client
```
import java.io.*;
import java.net.*; 
class ClientRARP
{
public static void main(String args[])
{
try
{
BufferedReader in=new BufferedReader(new
InputStreamReader(System.in)); Socket clsct=new
Socket("127.0.0.1",2422);
DataInputStream din=new DataInputStream(clsct.getInputStream());
DataOutputStream dout=new
DataOutputStream(clsct.getOutputStream());
System.out.println("Enter the Physical address (MAC):");
String str1=in.readLine(); dout.writeBytes(str1+'\n');
Stringstr=din.readLine();
System.out.println("The Logical Address is(IP): "+str); clsct.close();
}
catch (Exception e)
{
System.out.println(e);
}
}
}
```



# SIMULATION OF ECHO SERVER USING JAVA
```
import java.io.DataInputStream;
import java.io.PrintStream; 
import java.net.InetAddress;
import java.net.Socket;

public class EClient 
{
public static void main(String[] args)
{
try 
{
InetAddress ia=InetAddress.getLocalHost(); 
Socket c=new Socket(ia,5786);
String line;
PrintStream os=new PrintStream(c.getOutputStream()); 
DataInputStream is=new DataInputStream(System.in); 
DataInputStream is1=new DataInputStream(c.getInputStream()); 
while(true)
{
System.out.println("Client : "); line=is.readLine(); os.println(line);
System.out.println("Server : " +is1.readLine());
}
}
catch(Exception e)
{
System.out.println("Socket Closed !");
}
}
```
## server
```
import java.io.DataInputStream; 
import java.io.PrintStream;
import java.net.ServerSocket; import java.net.Socket;
public class EServer 
{
public static void main(String[] args) 
{
try
{
ServerSocket s=new ServerSocket(5786); 
String line;
Socket c=s.accept();
DataInputStream is=newDataInputStream(c.getInputStream());
PrintStream ps=new PrintStream(c.getOutputStream());
while(true) {
line=is.readLine();
ps.println(line);
}
}
catch(Exception e) {
System.out.println(e)
}
}
}

```
# SIMULATION OF TRACET USING JAVA
```
Tracert.java:
import java.io.*; 
public class Tracert
{
public static void runSystemCommand(String Command)
{
try{
Process p=Runtime.getRuntime().exec(Command);
BufferedReader InputStream=new BufferedReader(new 
InputStreamReader(p.getInputStream()));
String s=" "; 
while((s=InputStream.readLine())!=null)
{
System.out.println(s);
}
}
catch(Exception e)
{
e.printStackTrace();
}
}
public static void main(String[]args)
{
String Ip=" 67.195.160.76"
runSystemCommand("traceroute" +Ip); 
java.util.Date date=new java.util.Date(); 
System.out.println(date);
}
}

```
#  SIMULATION OF PING USING JAVA
```
import java.io.*; 
public class Ping
{
public static void runSystemCommand(String Command)
{
try{
Process p=Runtime.getRuntime().exec(Command);
BufferedReader InputStream=new BufferedReader(new 
InputStreamReader(p.getInputStream()));
String s=" "; while((s=InputStream.readLine())!=null)
{
System.out.println(s);
}
}
catch(Exception e)
{
e.printStackTrace();
}
}
public static void main(String[]args)
{
String Ip="localhost";
runSystemCommand("ping " +Ip);
java.util.Date date=new java.util.Date();
System.out.println(date);
}
}
```



## Output:

### Print the characters and its huffmancode
<br>
<br>
<br>
<br>
<br>
<br>



## Result
Thus the huffman coding was implemented to compress the data using python programming.
