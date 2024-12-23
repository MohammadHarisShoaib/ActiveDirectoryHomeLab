<h1 align="center">Active Directory Home Lab</h1>

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
      <img src="https://i.imgur.com/zqEu8gl.png" width="400px" alt="Class A private address"/>
      <br />
        <p align="center">
     Class A private address so this NIC is connected to the Internet.
    </td>
    <td style="text-align: center; vertical-align: middle; padding: 10px;">
      <p align="center">
        <img src="https://i.imgur.com/0M7XG1H.png" width="400px" alt="APIPA address"/>
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
