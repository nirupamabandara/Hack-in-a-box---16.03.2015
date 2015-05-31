# Hack-in-a-box---16.03.2015
Hacking kvsir using kali linux

Name: K.M. Nirupama Bandara
Registration Number: MS13961718

#Step1:
Run the Two Vms  Kvasir Vm and Kvasir Vm
Connet the two Vms by setting the network settings of both VMs to NAT

![1 nat](https://cloud.githubusercontent.com/assets/12378369/7900079/1fd39bc2-0761-11e5-825c-a921fdf5dbb4.PNG)


#Step2:
Once the connection is made between the two VMs 

Task :Find the IP address of the Kvasir VM using Kali Linux VM

Go to the root level

root@Kali:/# ifconfig


![2 ip](https://cloud.githubusercontent.com/assets/12378369/7900082/38f2b908-0761-11e5-9bd3-d99fa666b340.PNG)

output 192.168.152.132  :ip address of the Kali Linux VM

#Step3:

Since the two Vms are connected try to find the ip address of the Kvasir VM by performing a network discovery through KaliLinux

Command:
root@Kali:/# netdiscover  –r  192.168.152.0/24

![3 ip](https://cloud.githubusercontent.com/assets/12378369/7900085/664113c8-0761-11e5-9849-c8c6b16a576e.PNG)

#Step4: 

Using the network discovery find the ip of the kvasir vm

Ip of kvasir vm :- 192.168.152.130

![4 findip](https://cloud.githubusercontent.com/assets/12378369/7900089/c74c89c2-0761-11e5-83e0-ac114cf9add6.PNG)

#step5:
Using the nmap try to find the open port addresses

![5 findopenportsnmap](https://cloud.githubusercontent.com/assets/12378369/7900091/e4654454-0761-11e5-8989-dd237693fbef.PNG)

Open the Iceweasel web browser from KaliLinux and try to connect to the kvasir Vm by typing the ip address 192.168.152.130

#Step6:
Run the Burpsuit tool available in KaliLinux

![6 burpsuit](https://cloud.githubusercontent.com/assets/12378369/7900095/17289120-0762-11e5-8356-5c1cc907aa99.PNG)

#Step7:
Go to the proxy -> intersept  and set it to intercept response

Forward the request and see the output

Change the http header to bypass the defaul redirection and forward the packet
 The Burpsuit output

![7 changehttpheader](https://cloud.githubusercontent.com/assets/12378369/7900105/41100fc2-0762-11e5-8624-602dbc2697d4.PNG)

#Step8:
Type 192.168.152.130/admin.php in the web browser

Type apache2 in the browser

You will get the message as Apache2 is running.

![8 runadmin php](https://cloud.githubusercontent.com/assets/12378369/7900109/698d50ae-0762-11e5-9e59-75c8793cbfbd.PNG)


#Step9:
Type the command nano and copy the given script and save the content to a file. I gave the file name as Nirupama.pl

![9 executiscript](https://cloud.githubusercontent.com/assets/12378369/7900112/848570ee-0762-11e5-9f80-cb3b572ee7f3.PNG)

#Step10:
Once the  message Permission denied is appeared we have to change the access permissions of the file Nirupama.pl

![10 nirupama pl](https://cloud.githubusercontent.com/assets/12378369/7900114/a9693742-0762-11e5-80d7-88923a3fda78.PNG)


#Step11:
Provide the access permissions to the file

![11 p](https://cloud.githubusercontent.com/assets/12378369/7900116/d0121404-0762-11e5-9014-4edc5e8bd824.PNG)

![12 changeaccesspermission](https://cloud.githubusercontent.com/assets/12378369/7900117/d3ca73a2-0762-11e5-90d1-86cfa71653ed.PNG)

![13 p](https://cloud.githubusercontent.com/assets/12378369/7900121/00464bf4-0763-11e5-850b-12652d227b18.PNG)

![14 changepermission](https://cloud.githubusercontent.com/assets/12378369/7900122/08495134-0763-11e5-95d2-fd3249939aad.PNG)

#Step12:
After changing the access permissions

![15 afterchanging](https://cloud.githubusercontent.com/assets/12378369/7900125/244fd380-0763-11e5-8f46-db6d4994624b.PNG)


#Step13:

Open a new terminal and  

![16 p](https://cloud.githubusercontent.com/assets/12378369/7900130/462a7e88-0763-11e5-8072-565c55ab4a53.PNG)

#Step14:
Then

![17 p](https://cloud.githubusercontent.com/assets/12378369/7900132/5ddba32c-0763-11e5-8bc4-fb9d2678ef45.PNG)

#Step15:
Now type any command from the other terminal

![18 p](https://cloud.githubusercontent.com/assets/12378369/7900133/6239ebc2-0763-11e5-9ed5-44b0cf2c4b9f.PNG)

![19 p](https://cloud.githubusercontent.com/assets/12378369/7900137/84ca5686-0763-11e5-93f0-7e257045cb33.PNG)

![20 p](https://cloud.githubusercontent.com/assets/12378369/7900138/8a51a8f2-0763-11e5-9191-d5b34568b6ba.PNG)


#Step16:
Task 3
Remove the proxy and Type 192.168.152.130\upload.php in the web browser

![21 p](https://cloud.githubusercontent.com/assets/12378369/7900141/afb404dc-0763-11e5-9b4e-537f4ff09449.PNG)

![22 upload php](https://cloud.githubusercontent.com/assets/12378369/7900142/b2c5730e-0763-11e5-8b43-1bce4d957c4b.PNG)

