# What is this repo?
It is a collection of simple scripts and tools, to improve the Quality of Life for a penetration tester. VirtualBox users will find some of the fix* tools especially useful.

# Instructions
 - `fix-vbox-clipboard` and `fix-vbox-dragndrop` are some simple scripts to **kill the processes for VirtualBox Guest Additions and reset them**, when they start acting funny. If you have been a VirtualBox user, then you know what I am talking about. These scripts are lifesavers when working, or taking an exam. Feel free to suggest improvements, or add fixes for problems that I did not think of/come across.
 
 - The `reverse-shells` script will generate various reverse shell one-liners or sequence of commands, fully coloured in the terminal. The IP address of the listener (e.g., your KALI machine's IP), the port number, and the IP address of the client (e.g., the victim's) can all be set through arguments.
     * Running `reverse-shells` without arguments will attempt to use the IP address from ***tun0*** if it is set (if connected to vpn for example). Otherwise, it highlights with red colour that the IP was not set, so that the penetration tester can notice it and set it with what they want to. The default port is **443** (because that's the one I like to use):
    
     ![image](https://user-images.githubusercontent.com/25797286/197386426-3fe63f2c-1e11-46cc-9868-30820fe2fd09.png)

     ![image](https://user-images.githubusercontent.com/25797286/197386276-0dfd86d4-6618-46ed-8b07-cb1f1357a4b9.png)
     ![image](https://user-images.githubusercontent.com/25797286/197386324-339901fd-ec84-4893-965e-2f850f9a5bcd.png)

     * Setting IP address and the port through arguments:
     
     ![image](https://user-images.githubusercontent.com/25797286/197386414-e94cc80e-3a82-44ef-9a09-9fa3a78db4d3.png)
     
     * When connected through VPN and tun0 interface is set:
     
     ![image](https://user-images.githubusercontent.com/25797286/197386513-677f2334-ae33-4a89-8112-eb83b35fb2ee.png)
     
     
 - The `stabilize-shell` command works just like the `reverse-shells` command. It provides a few ways for stabilizing your current reverse shell:
 
 ![image](https://user-images.githubusercontent.com/25797286/197386672-e887f487-a511-41c1-b1c2-76d2560e0bb6.png)

 - Finally, there are the helper scripts `set-target-ip`, `unset-target-ip` and `show-target-ip`, which do exactly what their name suggests. Instead of setting bash variables every time you open a new terminal, you can set the IP address of your target with `set-target-ip` and then just call it from any shell you open, because it is written in a file in the /tmp directory.
     * Example: `nmap -sSCV -Pn -n -v --top-ports=2000 $(show-target-ip)`




