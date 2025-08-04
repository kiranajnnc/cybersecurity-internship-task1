Task1: Scan Your Local Network for Open Ports
Objective:
         Learn how to discover open ports on devices in your local network using tools like Nmap,and understand network exposure and potential security risks
Tools Used:
       Nmap
       Wireshark
steps performed
      Installled Nmap on my system.
      Identified my local ip address and subnet.
      Ran an Nmap scan to find devices and open ports.
          nmap -sS 192.168.1.0/24
      captured network packets using Wireshark during the scan.
      Notred down the detected devices,open ports,and observed services.

      Finding
      Device       IP Address     Open Ports   Services
      My Laptop   10.0.2.15        22,80        SSH,HTTP
      Phone       192.168.1.5      5555         ADB
      Router      192.168.1.1      80,443       HTTP,HTTPS


      Screenshots
          Add images of your Nmap scan results and Wireshark packet capture:
          ![Nmap Scan Result](./screenshot.png)
          ![Wireshark Capture](./wireshark1.pcapng)

Wireshark Analaysis :
  Noted SYN Packets sent to various devices and corresponding SYN-ACK reponses for open ports.
  Used filter tcp.flags.syn==1 to observe TCP handshake initation during the scan.
Key Concepts Learned :
   How to use Nmap for port scanning and basic network enumeration.
   The importance of open ports and associated security risks.
   Basics of packet analysis with wireshark.
   
Interview Questions & Answers:
   1.What is port scanning ?
     port scanning is the process of probing a network host for open ports to identify available services and potential vulnerabilities.
   2.Difference between TCP SYN scan & UDP Scan?
      TCP SYN scan uses SYN packets to detect open ports without completing the TCP handshake, while UDP scan sends UDP packets,making it harder to detect but less reliable.
   3.Why are open ports a Security risk?
      Open ports can expose services susceptible to exploitaion by attackers.
   4.How does Nmap discover open ports?
      By sending specially crafted packets and analysing the responses form the target systems.
   5.What does nmap -sS do?
      Performs a TCP SYN (stealth) scan to detect open ports discreetly.
   6.How to minimize risks from open ports?
      close unnecessary ports,restrict exposure to public networks,and use firewalls.
