# Stealth Keylogger To Attack Home Network

![Screenshot 2024-01-01 at 10 59 46 PM](https://github.com/EricMcclellan1/keylogger/assets/147299619/0374f090-75fc-40bb-ad07-574b5dddb765)

## Summary

❗❗ Warning Don’t Use This Maliciously! Run Malware In Your Personal Home-Labs For Fun/Learning! ❗❗

In this project I configure a keylogger and have it set to run silently on a our “home desktop”, to be able  get the credentials from our “relatives” and any other user who is using our machine for this practice set-up. 


## Technologies & Components Used

- Windows 10 Pro
- Microsoft Azure (Virtual Machine)
- Visual Studio Community 2022 
	-.NET desktop Development
- File and Storage Services
- Keylogger
- C#
- Windows Task Scheduler


<details> 
  <summary><h2>Set-Up</h2></summary>
  
I used Azure to create my virtual machine (running Windows 10 Pro) for my mock “home/family network” that was to run the keylogger malware on.

![1 azure vm](https://github.com/EricMcclellan1/keylogger/assets/147299619/cbf904b0-a316-43df-b006-c5c76ecc6276)

From here, I downloaded Visual Studio Community 2022 (with the >Net desktop development package), to test out and configure our keylogger.

![2 visual studio](https://github.com/EricMcclellan1/keylogger/assets/147299619/2a52a75a-4403-4752-8264-a783eb43ea6d)

![3 visual studio](https://github.com/EricMcclellan1/keylogger/assets/147299619/80429502-973a-4974-87ca-c9a34fdb1d95)

After getting our VM created and installing Visual Studio, I then downloaded our keylogger file from the net and saved the malware project code (for this test I kept the default name assets so it’s easier to follow along, but in actuality I would change this to something more random).

![4 save keylogger](https://github.com/EricMcclellan1/keylogger/assets/147299619/81bb5a3e-19da-43d7-881a-33a5e6a7c267)

  </details>


<details> 
  <summary><h2>Testing Keylogger</h2></summary>

Getting into the practical part of the project, I then opened up the keylogger in Visual Studio to be able to view the code and make any changes if needed (the default code is fine for this particular project)

![5 source code](https://github.com/EricMcclellan1/keylogger/assets/147299619/9ffc894b-6844-4106-bc74-7b5ff8f226a4)

Testing out the Keylogger, I was able to go to several different sites, put in credentials in web-sites, etc. and was able to see live in the console window each of our keys being recorded. Great, we’re up to a fantastic start!

![6 google](https://github.com/EricMcclellan1/keylogger/assets/147299619/c58b49b5-2d3c-4938-b1bb-930fdb48e1e4)

![7 credit score](https://github.com/EricMcclellan1/keylogger/assets/147299619/5dc4fb55-1ab6-416b-bd57-a6c41a4fe1fe)

![8 chase](https://github.com/EricMcclellan1/keylogger/assets/147299619/e007b19b-7e37-4b92-9002-e29206a3216d)


I was also able to test out the archive feature of this keylogger as well, being able to find previous tracked keylogged information in a notepad folder.

![9 archive](https://github.com/EricMcclellan1/keylogger/assets/147299619/aeab9f8e-8344-47d2-9bc1-8b8d66504f6d)

  </details>



<details> 
  <summary><h2>Setting Up Task Scheduler</h2></summary>

  So after seeing that the keylogger worked correctly, I went into the final steps of my project with setting up the Task Scheduler so that we would be able to have the keylogger running in the background to catch the credentials of any one accessing our family/home pc.

The first step is removing the large black console from popping up when the Keylogger is running. You can remove this in ‘Properties’ changing the Output type from “Console Application” to “Windows Application”. And then testing it out to make sure it’ll run without showing up. 

![10 windows app](https://github.com/EricMcclellan1/keylogger/assets/147299619/02c2473c-3034-4342-8216-408bfef5c174)

Going to Task Scheduler, I set a trigger to start at Log On, with the ‘Action’ being running the program, i.e Keylogger executable.

![11 trigger](https://github.com/EricMcclellan1/keylogger/assets/147299619/0ca5185e-263a-4576-a041-30958f903497)

![12 program](https://github.com/EricMcclellan1/keylogger/assets/147299619/6e37f163-9eac-46de-bf71-ceda451689a1)


 </details>



<details> 
  <summary><h2>Testing "Stealth" Keylogger</h2></summary>
 
For the fun part! So after setting up our Task Scheduler I then restarted my VM and then logged back into the family computer to test to see if everything would work (keylogger functioning in background as well as the removal of the black command console popping up).

I tested out several sites and everything worked as expected, totally stealth.

![13 fb](https://github.com/EricMcclellan1/keylogger/assets/147299619/04d17c0c-1de6-4a92-b3f0-3bd00d25939b)

![14 google](https://github.com/EricMcclellan1/keylogger/assets/147299619/ab470f57-910c-4228-854c-ade14a422bc3)

I then found my archive txt file and was able to confirm that the information I was typing was actually being recorded here.

![15 final check](https://github.com/EricMcclellan1/keylogger/assets/147299619/aec06a34-c4c8-40c5-9928-40c575904eb4)


 </details>
 

 <details> 
  <summary><h2>Analysis Of Ransomware</h2></summary>

   Lastly, I wanted to view the contents of our malware and see it being analysed by a virus checker. I went to VirusTotal for this final check.

![16 vt](https://github.com/EricMcclellan1/keylogger/assets/147299619/9e3d684f-74fa-4de4-a2b1-776ddc4ec36b)

From here, we’re able to see that our malware was detected by 47 out of 72 machines.

![17 vt 2](https://github.com/EricMcclellan1/keylogger/assets/147299619/9aac2bbc-bd43-4c19-8416-b5dee500ef1c)

In the details section, we can also find more information regarding the Keylogger including the hashing & additional info.

![18 vt 3](https://github.com/EricMcclellan1/keylogger/assets/147299619/0810cc6f-d32a-4686-8c66-1b632ea16cd7)

The ones that weren’t able to detect our keylogger malware were probably because their anti-virus engine was not utilizing anomaly based or behavior based detection, instead using signature-based detection whereas which wouldn’t detect this code since it was customized.

![18 vt 4](https://github.com/EricMcclellan1/keylogger/assets/147299619/e92d386b-6d60-44cc-be6a-0065f1d08d7a)

 </details>


 
 <details> 
  <summary><h2>Conclusion</h2></summary>

In closing, I was able to learn a lot about how a keylogger worked, as well as gaining knowledge on how malicious actors use keyloggers to steal valuable credentials from users to then be able to log into their accounts, sale their account info, use what they typed for extortion at a later date, etc. 

In addition I was able to use Task Scheduler in a completely new way (something that Microsoft probably did not intend) and found new way fun ways to implement future projects.



