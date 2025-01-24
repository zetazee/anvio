# what is anvio

it is a tool that turns solid, random-looking data into clear visuals that you can understand. you can think of it as a translator, not just any translator, but one that knows many languages and shows information in a way that is easy to see and work with. 

at first, it might seem quite complicated, but it’s actually just a tool, and like any tool, you can learn how to use it. you don’t need to learn all of its features right away. you’ll start with the basic, important ones, and if you need more advanced features in the future, you can learn them as you go.

# before installation: optimize your system and set your mindset
anvio does many things, which is why installing it requires more time than a regular program where we only need to hit next repeatedly. It’s okay, take your time and do it right. if the installation goes right, things will go much more smoothly for you later. so, get ready for an installation that is different from what you are usually used to and carefully peruse the instructions. perusing means reading in detail, not skimming. we are biologists with probably very little experience with computers. in this course, you can work on your computer skills and expand your skill set. rule number 1 for doing that is to read the instructions (documentation) word by word, then it’s just copy and paste.

my installation is for windows 10, 64-bit, core i5 system with no gpu, and i have 200 gb free space on my C folder. anvio is very resource-intensive, and you need to optimize your laptop before installing.
- in my opinion, core i5 is the minimum, and if your system has less cpu power, you can ask [ASTA](https://asta-oldenburg.de/angebote/computerwerkstatt/) to borrow a laptop for the duration of the course.  
- if you have less than 50 gb free space, you can easily insert a new ssd, it’s not hard to do on your own. buy a new ssd and search online for how to install it. once done, install windows Enterprise on it because it’s much faster than the Home version (just between us, you can also find the enterprise version for free online, torrent, cough cough). i should mention that 30 gb would also do, but being so close to the system's limit will slow your computer down and make your life harder.
make sure everything is set for the best performance. this way, you can be sure that if something goes wrong, it’s your fault and not the system’s, making it much easier to troubleshoot. when your system starts acting up, it can be frustrating to pinpoint the issue.
by the way, if you choose to install windows enterprise, connect it to your windows account for recovery if needed. sometimes, changes in your ip or network can lock you out, and without a backup, you could lose all your files.  

# WSL and VS Code
there is a windows-like operating system named Linux that gives you more freedom in customization and using different tools. many applications, especially in bioinformatics, are written in a way that requires linux. for this course, you can either [set up a dual system](https://www.youtube.com/watch?v=GXxTxBPKecQ) by installing linux alongside your windows (takes a maximum of one hour) or install a small version of linux inside your windows (takes about 5 minutes). i recommend the latter, not only because it saves time but also for better compatibility.  

windows is designed to work seamlessly if you stick to tools specifically made for it. that’s why i installed wsl (windows subsystem for linux) and connected it to a program called VS Code, which is also built for windows. with this setup, i can access my linux terminal through vs code. you can ask chatgpt how to install wsl and how to access it remotely via vs code. once done, you’ll see something like this and can move on to the next step.

![anvio installation](installation/1.png)


# installing Anvio
we have two options for installing anvio: stable version and development version. we will choose to [install the development version](https://anvio.org/install/windows/dev/), not only because we are adults now :)) but also because it is actively being developed and fixed. if something during the course needs to be addressed, you will automatically have the updated version without needing to do anything actively. let's start.

# 1. check to see if you have this software named miniconda.
what is miniconda? we don't know, yet. most of the time, you don’t need to know what these software are or what they exactly do, here. FOR NOW let's agree that we just need to have them to install anvio. of course, you can always search to learn more about them. you will encounter many of these oddly named software tools that are interdependent and necessary for specific tasks, but they are not our focus in this course. we will be satisfied knowing that they are helping us get to anvio.

so copy paste this in your wsl terminal inside VS Code:
```bash
conda --version



















