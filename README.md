Download Link: https://assignmentchef.com/product/solved-cs-3700-computer-networks-homework-6
<br>
<strong>Problem A.</strong> Consider transferring an enormous file of L bytes from Host A to Host B. Assume an MSS of 536 bytes. (hint: MSS: Maximum Segment Size, i.e., the maximum size of the payload of a TCP segment, not including the TCP segment header.  It’s essentially the largest amount of application-layer data, in Bytes, that a TCP segment can carry.)

<ul>

 <li>What is the maximum value of L such that TCP sequence numbers are not exhausted? Recall that the TCP sequence number field has 4 bytes.</li>

 <li>For the L you obtain in (a), find how long it takes to transmit the file. Assume that a total of 66 bytes of transport, network, and data-link header are added to each segment before the resulting packet is sent out over a 155 Mbps link. Ignore flow control and congestion control so A can pump out the segments back to back and continuously. (Hint: it is assumed that the window size N is large enough such that the segments can be sent out back to back without the need to wait for the next sequence number to be available and there is no loss of packet or ack.)</li>

</ul>




<strong>Problem B</strong>. Host A and B are communicating over a TCP connection, and Host B has already received from A all bytes up through byte 126. Suppose Host A then sends two segments to Host B back- to- back. The first and second segments contain 80 and 40 bytes of data, respectively. In the first segment, the sequence number is 127, the source port number is 302, and the destination port number is 80. Host B sends an acknowledgment whenever it receives a segment from Host A.

<ul>

 <li>In the second segment sent from Host A to B, what are the sequence number, source port number, and destination port number?</li>

 <li>If the first segment arrives before the second segment, in the acknowledgment of the first arriving segment, what is the acknowledgment number, the source port number, and the destination port number?</li>

 <li>If the second segment arrives before the first segment, in the acknowledgment of the first arriving segment, what is the acknowledgment number? (Hint: The reliability control used in TCP is basically a GBN approach with some variation.)</li>

 <li>Suppose the two segments sent by A arrive in order at B. The first acknowledgment is lost and the second acknowledgment arrives after the first time-out interval. Draw a timing diagram, showing <strong>these segments and all other segments and acknowledgments</strong> (Assume there is no additional packet loss.) For each segment in your figure, provide the sequence number and the number of bytes of data; for each acknowledgment that you add, provide the acknowledgment number. <strong>(hint: draw all the segments and ACKs that are exchanged between Hosts A and B involved in delivering these two segments)</strong></li>

</ul>




<strong>Problem C.</strong> Referring to the Slide 38 titled “TCP Flow Control”, if RcvBuffer = 4096 bytes, 1280 bytes data is buffered,  (a) what is the <strong>rwnd</strong> value in the TCP header of the next receiver-to-sender segment?

(b) When the sender receives the above TCP segment, it has sent out 2560 bytes not yet ACKed.  At most how many more bytes can the sender send out before receiving any ACK?




<strong>Problem D.</strong> (a) List the following three TCP segments in the order of being transmitted in the TCP 3-way handshake for establishing a TCP connection; (b) describe the sender and receiver of EACH TCP segment as <em>client-to-server</em> or <em>server-to-client</em>; (c) what is the initial sequence number chosen by the client; (d) what is the initial sequence number chosen by the server?

TCP Segment [SYNBit = 1, Seq = 58, ACKbit = 1, ACKnum = 126]

TCP Segment [ACKbit = 1, ACKnum = 59]

TCP Segment [SYNBit = 1, Seq = 125]

<strong> </strong>

<strong>Problem E.</strong> Given that the client initiates the procedure of closing a TCP connection, the <strong>last byte</strong> sent from client to server <strong>before</strong> the FIN segment is <strong>byte #1,742</strong>, the <strong>last byte</strong> sent from server to client <strong>before</strong> the FIN segment is <strong>byte #6,029</strong>, (a) list four TCP segments exchanged between client and server for closing a TCP connection, where EACH TCP Segment must be described in the <strong>format</strong> used in Problem B; (b) describe the sender and receiver of EACH TCP segment as <em>client-to-server</em> or <em>server-to-client</em>.













<strong>                                                                                                (more on next page!) </strong>

<strong>                 </strong>

MSU Denver, M&amp;CS                                                  CS 3700: Computer Networks, Spring 2020                                                      Dr. Weiying Zhu

<strong>Problem F</strong>. The initial ssthresh is 16, the sender experiences a <strong><em>3-duplicate-ACKs</em></strong> event <strong>right after the</strong> <strong>9<sub>th</sub> transmission round</strong> in both Tahoe and Reno cases, and then the sender experiences <strong><em>a timeout</em></strong> event <strong>right after the 16<sub>th</sub> round in a TCP Tahoe case</strong> and <strong>after right after the 19<sub>th</sub> round in a TCP Reno case</strong>, FILL the following table to illustrate the congestion window size in segments (<strong>cwnd</strong>) and <strong>ssthresh</strong> as functions of transmission round for the time from the <strong>1<sub>st</sub></strong> to the <strong>22<sub>th</sub></strong> round if (a) TCP Tahoe is used for congestion control; and (b) TCP Reno is used for congestion control.  (<strong>Hint</strong>: be aware that the figure in the slide titled “TCP: switching from slow start to CA” illustrates both cases in the same graph.)




<sup>                </sup>

<table width="560">

 <tbody>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>TCP Tahoo </strong> </td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>TCP Reno </strong> </td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"> </td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"><strong> </strong></td>

   <td width="86"> </td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>Trans. Round </strong><strong> </strong></td>

   <td width="72"><strong>cwnd </strong> </td>

   <td width="78"><strong>ssthresh </strong> </td>

   <td width="48"> </td>

   <td width="86"><strong>Trans. Round </strong><strong> </strong></td>

   <td width="64"><strong>cwnd </strong> </td>

   <td width="64"><strong>Ssthresh </strong> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>1</strong><strong>st</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>1</strong><strong>st</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>2</strong><strong>nd</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>2</strong><strong>nd</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>3</strong><strong>rd</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>3</strong><strong>rd</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>4</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>4</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>5</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>5</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>6</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>6</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>7</strong><strong>th</strong><strong>  </strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>7</strong><strong>th</strong><strong>  </strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"><strong> </strong></td>

   <td width="90"><strong>8</strong><strong>th</strong><strong>  </strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>8</strong><strong>th</strong><strong>  </strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>9</strong><strong>th</strong><strong>  </strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>9</strong><strong>th</strong><strong>  </strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>10</strong><strong>th</strong><strong>  </strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>10</strong><strong>th</strong><strong>  </strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"><strong> </strong> </td>

   <td width="90"><strong>11</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>11</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>12</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>12</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>13</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>13</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"><strong> </strong></td>

   <td width="90"><strong>14</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>14</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>15</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>15</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57">  </td>

   <td width="90"><strong>16</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>16</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>17</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>17</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>18</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>18</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>19</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>19</strong><strong>th</strong></td>

   <td width="64">  </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>20</strong><strong>th</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>20</strong><strong>th</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>21</strong><strong>st</strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>21</strong><strong>st</strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

  <tr>

   <td width="57"> </td>

   <td width="90"><strong>22</strong><strong>nd</strong><strong>  </strong></td>

   <td width="72"> </td>

   <td width="78"> </td>

   <td width="48"> </td>

   <td width="86"><strong>22</strong><strong>nd</strong><strong>  </strong></td>

   <td width="64"> </td>

   <td width="64"> </td>

  </tr>

 </tbody>

</table>


