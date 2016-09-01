Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

SELECT DISTINCT city FROM station WHERE REGEXP_LIKE(LOWER(city), '^[aeiou].*[aeiou]$');

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '^[aeiou].');



Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.

SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '[aeiou]$');

Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.
SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '[aeiou]$') and not REGEXP_LIKE(LOWER(city), '^[aeiou].');
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
610
TSM610-02 HW1
True/False Questions
1.	According to John Chambers, CEO of Cisco (a leading networking technology company), the information age is the second Industrial Revolution. True
2.	It is not uncommon for companies to end up spending more money on network management and security tasks than they do on the actual computer equipment itself. True
3.	A local area network (LAN) connects other LANs and backbone networks (BNs) located in different areas to each other and to wide area networks in a span from 3 to 30 miles.
4.	A car manufacturer may give access to certain portions of its network to some of its suppliers via the Internet. This is an example of an extranet.
5.	The network layer performs the same functions in both the OSI and Internet models and is responsible for routing messages from the source computer to the destination computer.
6.	The application layer is the seventh layer of the Internet model and specifies the type of connection and the electrical signals that pass through it.
7.	Ethernet is an example of a network layer protocol.
8.	The specification stage of the de jure standardization process consists of developing nomenclature and identifying the problems to be addressed.
9.	The Internet has always been open to commercial traffic.
10.	An Application Service Provider (ASP) develops a specific system and companies purchase or rent the service without installing the system on their own computers.

Multiple Choice Questions
1.	Data communications and networking can be considered as a global area of study because:
a.	new technologies and applications emerge from a variety of countries and spread around the world
b.	the technologies enable global communication
c.	the political and regulatory issues are exactly the same in every country  
d.	a and b
e.	none of the above
2.	Networks that are designed to connect similar computers that share data and software with each other are called:
a.	client/server networks
b.	peer-to-peer networks
c.	host networks
d.	client networks
e.	local area networks


3.	A local area network is:
a.	a large central network that connects other networks in a distance spanning exactly 5 miles.   
b.	a group of personal computers or terminals located in the same general area and connected by a common cable (communication circuit) so they can exchange information such as a set of rooms, a single building, or a set of well-connected buildings.
c.	a network spanning a geographical area that usually encompasses a city or county area (3 to 30 miles).
d.	a network spanning a large geographical area (up to 1000s of miles).
e.	a network spanning exactly 10 miles with common carrier circuits.
4.	Which of the following is not a property of a WAN:
a.	connects backbone networks and MANS.
b.	spans hundreds or thousands of miles
c.	provides data transmission speeds from 56Kbps to 10Gbps.
d.	connects a group of computers in a small geographic area such as room, floor, building or campus.
e.	uses leased lines from IXCs like ATT, MCI, and Sprint
5.	A(n) _________ is a LAN that uses the same technologies as the Internet but is provided to invited users outside the organization who access it over the Internet.  
a.	WAN
b.	BN
c.	extranet
d.	intranet
e.	MAN
6.	Which layer of the OSI model is responsible for ensuring flow control so that the destination station does not receive more packets that it can process at any given time?
a.	presentation
b.	transport
c.	physical
d.	session
e.	application 
7.	The fourth layer of the OSI model is called the __________ layer.

a.	network 
b.	transport 
c.	session 
d.	data link
e.	presentation 
8.	In the Internet model, the application layer corresponds to the ________ layer(s) of the OSI model.

a.	data link and network
b.	session, presentation and application
c.	application layer
d.	application and presentation
e.	network, transport and presentation
9.	Which is not a function of the physical layer:

a.	transmission of bits.
b.	defining the rules by which one and zeroes are transmitted.
c.	providing error-free transmission of data.
d.	providing the physical connection between sender and receiver.
e.	specifying the type of connection and type of signals, waves or pulses that pass through it.
10.	Which of the following is not a function of the data link layer?
a.	deciding when to transmit messages over the media
b.	formatting the message by indicating where messages start and end, and which part is the address
c.	detecting and correcting any errors that have occurred in the transmission of the message
d.	specifying the type of connection, and the electrical signals, radio waves, or light pulses that pass through it
e.	controlling the physical layer by determining when to transmit
11.	Which of the following is a term used to group together the physical and data link layers? 
a.	Internetwork layers
b.	Hardware layers
c.	Software layers
d.	Middleware layers
e.	Application layers
12.	In which layer of the Internet model would the HTTP protocol be used?
a.	physical
b.	application
c.	transport
d.	network
e.	data link
13.	The network layer of the Internet model uses the _____________ protocol to route messages though the network.
a.	TCP
b.	HTTP
c.	FTP
d.	SMTP
e.	IP

14.	Which of the following is not true about de jure standards?
a.	They are always developed before de facto standards.
b.	One example exists for network layer software (IP).
c.	They can be developed by an official industry body.
d.	They can take several years to develop. 
e.	They can be developed by a government body.
15.	The three stages of the de jure standardization process are ______________________.
a.	specification, identification of choices and acceptance.
b.	planning, implementing and acceptance.
c.	brainstorming, identification and implementing.
d.	specification, formalization, and acceptance.
e.	none of the above.
16.	Which of the following is not true about ITU-T: 
a.	It is the technical standards-setting organization of the United Nations International Telecommunications Union
b.	It is the International Telecommunications Union – Telecommunications Group
c.	Its membership is limited to U.S. telephone companies
d.	It is based in Geneva, Switzerland 
e.	Its membership is comprised of representatives from over 200 member countries
17.	The Internet standards organization that will allow anyone to join is __________________.
a.	ANSI
b.	ISO
c.	IETF
d.	IEEE
e.	ITU-T
18.	Which of the following is not an application layer standard?
a.	HTTP
b.	POP
c.	T1
d.	IMAP
e.	HTML
19.	Which of the following is not an important future trend in communication and networking? 
a.	development of online batch systems 
b.	integration of voice, video, and data
c.	pervasive networking 
d.	provision of new information services on rapidly expanding networks 
e.	development of extremely high speed broadband networks

20.	A _____________ is the input-output hardware device at the end user’s end of a communication circuit in a client-server network.
a.	server
b.	circuit
c.	client
d.	host  

Short Answer and Essay Questions
1.	How can data communications networks affect businesses?
2.	From your own knowledge or background, discuss and describe three important applications of data communications networks for strategic, competitive advantage in business use.  Give examples of three real world firms who have used networks for competitive advantage in the marketplace and discuss why these networks contributed to their expertise or competitive advantage.
3.	How do LANs differ from WANs, and BNs?
4.	Draw a diagram of the Internet model and describe what each of the five layers do.  Put three examples of standards on each of your layers in the diagram.  Do this in detail, explaining how a message is transmitted from one computer to another using this model.
5.	What is the difference between an extranet and intranet?  
6.	 What are the seven layers of the OSI model and what does each of these layers do?  How does the OSI model compare to the Internet model?  What does OSI stand for, and who developed this model?
7.	What is VOIP? What are some examples of companies that provide VOIP as a service to their customers? 
8.	Explain why it is such a great time to be an IT professional. 

