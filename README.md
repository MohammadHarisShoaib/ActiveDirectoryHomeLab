<h1 align="center">Active Directory Home Lab</h1>

Credit: https://www.youtube.com/watch?v=MHsI8hJmggI

<h2 align="center">Description</h2>
<p align="center">
Creating a simple network in VirtualBox following this diagram:
<br/>

<p align="center">
<img src="https://i.imgur.com/FfUrxIs.png" height="80%" width="80%" alt="Active Directory Diagram"/>
<br />
<br />

<h2 align="center">Configuring the NICs</h2>
<p align="center">
I found out which NIC is connected to the Internet and which one is connected internally and renamed them accordingly.
<table align="center">
  <tr>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
      <img src="https://i.imgur.com/zqEu8gl.png" width="300px" alt="Class A private address"/>
      <br />
        <p align="center">
     Class A private address so this NIC is connected to the Internet.
    </td>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
        <img src="https://i.imgur.com/0M7XG1H.png" width="300px" alt="APIPA address"/>
      <br />
        <p align="center">
      APIPA address so this NIC is the internal NIC.
    </td>
  </tr>
</table>
<p align="center">
I then configured the internal NIC with the respective configuration from the diagram.
<p align="center">
<img src="https://i.imgur.com/pCjOmtc.png" width="400px" alt="Internal NIC Configuration"/>
  
<br />
<br />

<h2 align="center">Creating the Domain</h2>
<p align="center">
I installed and configured AD DS and created an Admin User.
<table align="center">
  <tr>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
      <img src="https://i.imgur.com/sUFpu5y.png" width="500px" alt="Class A private address"/>
      <br />
        <p align="center">
     Installing AD DS.
    </td>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
      <img src="https://i.imgur.com/kBmGxNJ.png" width="500px" alt="APIPA address"/>
      <br />
        <p align="center">
      Configuring AD DS.
    </td>
  </tr>
</table>
<p align="center">
Creating an admin user.
<p align="center">
<img src="https://i.imgur.com/cFeXJIU.png" width="800px" alt="Internal NIC Configuration"/>
<p align="center">
Signing in as an admin user
<p align="center">
<img src="https://i.imgur.com/UFB0F3x.png" width="800px" alt="Internal NIC Configuration"/>

<br />
<br />

<h2 align="center">Installing RAS / NAT</h2>
<p align="center">
I installed RAS to provide remote access to the network and NAT to translate between public and private addresses.
<table align="center">
  <tr>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
      <img src="https://i.imgur.com/nUfVyti.png" width="500px" alt="Installing RAS"/>
      <br />
        <p align="center">
     Installing RAS.
    </td>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
        <img src="https://i.imgur.com/u3vGXZD.png" width="500px" alt="Installing NAT"/>
      <br />
        <p align="center">
      Installing NAT.
    </td>
  </tr>
</table>

<br />
<br />

<h2 align="center">Installing and Configuring DHCP</h2>
<p align="center">
I installed and configured DHCP to provide addressing information for clients.
<table align="center">
  <tr>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
      <img src="https://i.imgur.com/1iT5IhH.png" width="500px" alt="Installing DHCP"/>
      <br />
        <p align="center">
     Installing DHCP.
    </td>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
        <img src="https://i.imgur.com/5MFOPgt.png" width="500px" alt="Configured DHCP"/>
      <br />
        <p align="center">
      Configured DHCP with information from the diagram.
    </td>
  </tr>
</table>

<br />
<br />

<h2 align="center">Installing A PowerShell Script To Generate Users</h2>
<p align="center">
I used the following link to download the PowerShell script and the randomly generated names: 
<a href="https://github.com/joshmadakor1/AD_PS/archive/refs/heads/master.zip">PowerShell and Names</a>
</p>

<p align="center">
I first disabled IE Enhanced Security Configuration to download files without security popups
<p align="center">
<img src="https://i.imgur.com/2Zk8fjI.png" width="400px" alt="Internal NIC Configuration"/>
  
<table align="center">
  <tr>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
      <img src="https://i.imgur.com/l09lzKF.png" width="500px" alt="Downloaded Files"/>
      <br />
        <p align="center">
     Downloaded files and added my name to the generated names.
    </td>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
        <img src="https://i.imgur.com/KOlc7kB.png" width="500px" alt="PowerShell Script"/>
      <br />
        <p align="center">
      Downloaded PowerShell script.
    </td>
  </tr>
</table>

<p align="center">
I ran the script but had to Set-ExecutionPolicy to Unrestricted
<p align="center">
<img src="https://i.imgur.com/PzoLFX2.png" width="400px" alt="Internal NIC Configuration"/>

<br />
<br />

<h2 align="center">Installing and Configuring the Client</h2>

<p align="center">
Creating the Windows 10 client with the NIC set to internal
<p align="center">
<img src="https://i.imgur.com/hrpSIMc.png" width="700px" alt="Joining Domain"/>
  
<p align="center">
Successful Ping
<p align="center">
<img src="https://i.imgur.com/QWypjX8.png" width="700px" alt="Creating Client"/>

<p align="center">
Joining the domain
<p align="center">
<img src="https://i.imgur.com/hrpSIMc.png" width="700px" alt="Joining Domain"/>

<p align="center">
Active lease
<p align="center">
<img src="https://i.imgur.com/sE1UnrE.png" width="700px" alt="Active Lease"/>

<p align="center">
Active machine
<p align="center">
<img src="https://i.imgur.com/8U8Jxr5.png" width="700px" alt="Active Machine"/>

<p align="center">
Signing in as one of the randomly generated user
<p align="center">
<img src="https://i.imgur.com/4vrNjtX.png" width="700px" alt="SignIn As Randomly Generated User"/>
