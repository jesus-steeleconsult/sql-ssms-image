# Set up SQL Server Docker Image From Scratch

<ol>

<li> Install Docker and Git. </li>

- [Link to Docker for Desktop](https://docs.docker.com/desktop/install/mac-install/)
- [Link to Git Tool](https://git-scm.com/downloads)

<li> Clone the SqlServer repo </li>
- [Link to the repo](https://github.com/theonlyjesus/sqlserver)

<li>Open Docker</li>

<li>Open a terminal and go to the sqlserver folder.</li>

<li>Run this command to build the SQL Server image in Docker.</li>

`docker build -t sqlserver .`

<li>Run this command to run the SQL Server image.</li>

`docker run -p 1433:1433 -d sqlserver`

<li>Connect to your database.</li>

- Open your database GUI.
- The db connection is localhost, port 1433.
- Username is sa
- Password is Appl3s123

# If you need to connect from a Windows VM.

- Run Notepad as Administrator

- From Notepad, File > Open, open System32 > drivers > etc > hosts (may need to change file extension to show all file types)

- Inside the hosts file, add `10.211.55.2  localmac`. (This IP address is the default value for Mac Terminal > ifconfig > vnic0 > inet. If the default value doesn’t work, find the inet address for your device and add it to the hosts file.)

- http://localmac:[port] will be able to access apps and ports in your Windows VM served from your mac
</ol>

