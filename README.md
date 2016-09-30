Query the list of CITY names from STATION which have vowels (i.e., a, e, i, o, and u) as both their first and last characters. Your result cannot contain duplicates.

SELECT DISTINCT city FROM station WHERE REGEXP_LIKE(LOWER(city), '^[aeiou].*[aeiou]$');

Query the list of CITY names from STATION that do not start with vowels. Your result cannot contain duplicates.
SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '^[aeiou].');



Query the list of CITY names from STATION that do not end with vowels. Your result cannot contain duplicates.

SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '[aeiou]$');

Query the list of CITY names from STATION that do not start with vowels and do not end with vowels. Your result cannot contain duplicates.
SELECT DISTINCT city FROM station WHERE not REGEXP_LIKE(LOWER(city), '[aeiou]$') and not REGEXP_LIKE(LOWER(city), '^[aeiou].');
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
HW extra assignment   TSM610-90 Due date Friday 30th, September, 8 AM 

1.	Assuming that each label is 1000 bytes long, how long does it take to transmit one label over the cell network, assuming that the cell phone network operates at 144 kbps (144,000 bits per second and that there are 8 bits in a byte)?  2.)  If Speedy were to upgrade to the new, faster digital phone network that transmits data at 200 Kbps (200,000 bits per second) how long would it take to transmit?
Ans: 
I.	Length of each label = 1000 bytes per second
Speed of network = 144000 bits per second
1 byte = 8 bits
Total bits = (8 * 1000) =8000 bits per second
Transmission time = 8000/144000 = 0.056 Seconds

II.	Length of each label = 1000 bytes per second
Speed of network = 200000 bits per second
1 byte = 8 bits
Total bits = (8 * 1000) =8000 bits per second
Upgraded Transmission time = 8000/200000 = 0.04 Seconds 
	   
2.	Are stop bits necessary in asynchronous transmission? Explain using a diagram.

Ans: Stop bits are required in asynchronous transmission because they convey the message to receiver that the sent bits are received. Once the bits are received the stop bits’ resets itself. which then shows the start of next start bit. It is represented as 1. In every transmission it is the last bit to be received. The diagram below shows the typical start and stop bits the message start with a start bit (0) followed by a ASCII data code and then the Parity bit followed by Stop bit.
 
Figure 1 Shows The Message Format in ASYNCHRONOUS TRANSMISSION

3.	Are large frame sizes better than small frame sizes?  Explain.
Ans: Larger frame size gives the ability to transfer larger chunks of data at once which is good as well as bad because whenever there is an error in a message bit the whole message bit has to be retransmitted which makes it harder because every time we get an error bit we have to transfer the whole large bit all at once. So smaller frame size is better than the larger frame size.
Let’s consider the example if a frame size is 10K and received 2 error bits then all the 10000 bits are to be retransmitted. Which is clearly waste of time and with bigger size of frame there are more chances of error bits occurring. So there is always a tradeoff between the larger and smaller frames because smaller frames are less efficient but have a less probability of containing errors which has less cost to retransmit the data.

4.	What are the advantages and disadvantages of host-based networks versus client-server networks?
Ans: 
i.	Host based network 
a.	Advantages
i.	There is a central server which controls the whole transaction/operation.
ii.	Updating the data is very easy because we have to make changes over single station and whole of the system will have the same changes.
b.	Disadvantages
i.	There is a single processor available to handle all the client requests which makes is harder to control all the requests if there are a huge number of requests.
ii.	Prioritizing the clients is really hard because of huge clients requests and less processing power
ii.	Client-Server based network
a.	Advantages
i.	90 percent of most organizations- total computer processing power now resides on microcomputer-based LAN-s, not in centralized mainframe computers.
ii.	Most mainframe software is not as easy to use as microcomputer software, is far more expensive, and can take years to develop.
b.	Disadvantages
i.	 The fundamental problem in client-based networks is that all data on the server must travel to the client for processing.
5.	What is the capacity of a digital circuit with a symbol rate of 10 MHz using Manchester encoding?
Ans: 
i.	The capacity of a digital circuit with a symbol rate of 10 MHz using Manchester encoding will be 10 Mbps.
a.	Capacity of the digital circuit (B) = Symbol rate (s) * bits per symbol (n)
b.	B = s * 1 bit per second
c.	B = (10 MHz) * 1 bit per second
d.	Capacity of the digital circuit (B) = 10Mbps

6.	What is the maximum capacity of an analog circuit with a bandwidth of 4,000 Hz using QAM?  
Ans:
i.	Under perfect circumstances, the maximum symbol rate is about 4000 symbols per second.
ii.	We are using QAM (4 bits per symbol)
iii.	Maximum data rate = 4 bits per symbol * 4000 symbols per second.
iv.	Maximum data rate = 16000 bps.


7.	What is the symbol rate of a digital circuit providing 100 Mbps if it uses bipolar NRz signaling?
Ans: 
i.	Bandwidth of circuit = 100 Mbps
ii.	Symbol rate in bipolar NRz is twice the current bandwidth.
iii.	One voltage changes per Symbol = 2 * 100 Mbps = 200 Mbps.

8.	Smith, Smith, Smith, and Smith is a regional accounting firm that is building a new headquarters building.  The building will have a backbone network that connects eight LANs (two on each floor).  They are very concerned with network errors.  What advice would you give them in the design of the building and network cable planning that would help reduce network errors?
Ans: I would first advise that the backbone network is the correct for the organization setup. I would stress that errors occurs in all networks. The primary sources of errors are impulse noises, cross talk, echo and attenuation. Errors can be prevented or at least reduced by shielding the cables, moving the cables away from sources of noise and power sources; using repeaters, amplifiers and improving the quality of the equipment, media, and their connections.

9.	Compare and contrast stop-and-wait ARQ and continuous ARQ.
Ans:
i.	With stop-and-wait ARQ, the sender stops and waits for a response from the receiver after each message or data packet. After receiving a packet, the receiver sends either an acknowledgment (ACK) if the message was received without error, or a negative acknowledgment (NAK) if the message contained an error. If it is an NAK, the sender resends the previous message. If it is an ACK, the sender continues with the next message. Stop-and-wait ARQ is by definition, a half-duplex transmission technique.
ii.	With continuous ARQ, the sender does not wait for an acknowledgment after sending a message; it immediately sends the next one. While the messages are being transmitted, the sender examines the stream of returning acknowledgments. If it receives an NAK, the sender retransmits the needed messages. Continuous ARQ is by definition a full duplex transmission technique, because both the sender and the receiver are transmitting simultaneously.

10.	Describe three approaches to detecting errors, including how they work, the probability of detecting an error, and any other benefits or limitations.
Ans: The three approaches to detecting errors are Parity checking, Longitudinal redundancy checking and polynomial checking we will explain each of them in detail below.
i.	Parity Checking: - With parity checking one additional bit is added to each byte in the message. The value of this additional parity bit is based upon the number of 1’s in the byte (including the parity bit) either an even or an odd number. The probability of detecting an error using this technique is about 50 percent.
ii.	Longitudinal redundancy checking (LRC): - it adds one additional character called the block check character (BCC) to the end of the entire message or packet of data. The value of the BCC is determined in the same manner as the parity bit, but by counting longitudinally through the message rather than by counting vertically through each character. The error detection rate is above 98 percent for typical burst errors of 10 bits or more because it uses in conjunction with parity.
iii.	Polynomial checking: - it adds a character or series of characters, based on a mathematical algorithm, to the end message. There are two types of polynomial checking: check sum and cyclical redundancy check (CRC). The probability of detecting bursts errors longer than CRC-16 bits is 99.998 percent and for CRC-32 its about 99.99999998 percent.


















