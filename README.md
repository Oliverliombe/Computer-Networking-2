Independent Submission                                      G. Cook, Ed.
Internet Draft                                     Md. Abdul Khalek, Ed.
                                                    O. Liombe Molua, Ed.
Intended status: Educational                               June 9, 2020
Expires: December 2020


                    Uplink To Mars (Latency)
                    
Status of this Memo

   This document is a group exam assignment meant for educational
   purposes.
   It represents the consensus of the group.

Abstract

   This document provides a general description on how latency can be 
   reduced in data communications between Earth and Mars.  Due to the 
   immense distance between the two planets, there is not much that be
   done about the latency due to propagation delay.  So instead, this
   proposal focuses on latency due to data retransmissions. The goal is
   to reduce retransmissions by reducing transmission errors and also to 
   reduce the distance between retransmissions to limit its propagation 
   delay.

Table of Contents

   1.  Introduction . . . . . . . . . . . . . . . . . . . . . . . . .  2
   2.  Challenges . . . . . . . . . . . . . . . . . . . . . . . . . .  2
     2.1. Vast Distance . . . . . . . . . . . . . . . . . . . . . . .  2
   3.  Proposed Solutions . . . . . . . . . . . . . . . . . . . . . .  3
     3.1. Forward Error Correction  . . . . . . . . . . . . . . . . .  3
     3.2. Relay Station . . . . . . . . . . . . . . . . . . . . . . .  3
   4.  References . . . . . . . . . . . . . . . . . . . . . . . . . .  4
   5.  Appendix . . . . . . . . . . . . . . . . . . . . . . . . . . .  5
   6.  Authors' Addresses . . . . . . . . . . . . . . . . . . . . . .  7




















Cook, et al.                  Experimental                      [Page 1]

RFC NNNN               Uplink To Mars (Latency)                June 2020


1.  Introduction

   The rapid growth in technology gives the ability for extreme
   discoveries and explorations. One of this very ambitious exploration,
   is the settling of humans in Mars in the nearest future. Before now,
   lots of different space expeditions have been carried out, and this
   therefore means the explorers have to communicate with people on
   Earth. Space communication has been a very big challenge when it
   comes to transfer of data, based on vary factors, for example
   distance.

   The distance from Earth to Mars is very vast and the time taken from
   Earth to Mars differs. Both the Earth and Mars do orbit the Sun which
   also makes it challenging for communication due to noise produced by
   the Sun. The transfer of packets from Earth to Mars can sometimes
   fail and retransmission is needed. The idea of retransmission can
   lead to huge latencies which make human-to-human interaction greatly
   unbearable.

   In this group work, a solution is proposed to address the problem of
   overall communication latency between Earth and Mars. The problem is
   latency based on retransmission. To address latency, we must address
   retransmissions.

   The solutions we propose are: forward error correction (FEC) and the
   use of relay stations. Both combined should reduce the number of
   retransmissions needed and also the time spent for each
   retransmission.

2.  Challenges

   Setting up a communication between Earth and Mars is not really a
   trivial matter because of the wide varieties of obstacles such as
   vast distance between Earth and Mars, noise from the Sun, long time
   delays and other disturbances. However, mainly our concerns are the
   vast distance from Earth to Mars, noise from the Sun and long time
   delays.

2.1.  Vast Distance

   In communication systems, distance plays a vital role. It is
   particularly tricky when trying to communicate between Earth and Mars
   since the distance between the two planets can be anywhere between
   50-400 million kilometers. The actual distance depends on where Earth 
   and Mars are respectively in their orbit around the Sun [1].

   Hence, the signal needs to travel approximately aforementioned
   distance to reach Mars. We know the speed of light is 3x10^8 km/sec.
   Assuming the signal travels at the speed of light, it takes
   approximately 3 to 30 minutes for the information to reach the other
   end [2].
Cook, et al.                  Experimental                      [Page 2]

RFC NNNN               Uplink To Mars (Latency)                June 2020


3.  Proposed Solution

   Data propagation between Earth and Mars can be anywhere from 3 to 30
   minutes. This is assuming there are no errors in transmission which
   is highly unlikely. With errors, there will be additional delays due
   to retransmissions.  With retransmissions, the overall latency can be
   up to 75 minutes.  To make any sort of human-to-human interaction
   reasonable, the overall latency needs to be 45 minutes or less.

   The proposed solution aims to meet this latency requirement by using
   Forward Error Correction in the transmitted data and also by adding
   multiple relay stations between Earth and Mars.

3.1.  Forward Error Correction

   Forward Error Correction (FEC) is a sort of self-correcting
   algorithm. In telecommunication, information theory, and coding
   theory, FEC or channel coding is a technique used for controlling
   errors in data transmission over unreliable or noisy communication
   channels. The central idea is the sender encodes the message in a
   redundant way, most often by using an error-correcting code (ECC)
   [3].

   FEC involves transmitting extra data so that certain errors can be
   corrected without data being retransmitted. This approach depends on
   a measure called Hamming Distance. It is a metric for comparing two
   bit strings of the same length. For example consider the following
   two bit strings 000 and 011. The Hamming distance between these two
   is two strings of equal length is simply the number of positions in
   which their values differ. So the first are both 0s, but then we have
   a 0 and a 1, so that is one position where they differ. And the last
   position they also differ. So the distance between these two bit
   strings: d(000, 011)=2. Given this knowledge, we can talk about
   forward error correction.

   Thus, FEC error correction increases the tolerance for errors. 
   With a higher tolerance for errors, there will be less need for
   retransmission. And less retransmission means less latency.

3.2.  Relay Stations

   The proposed relay stations operate in a similar way to intermediate
   stations in store and forward. Store and forward is a 
   telecommunications technique in which information is sent to an 
   intermediate station where it is kept and sent to the final 
   destination or to another intermediate station. The intermediate 
   station verifies the integrity of the message before forwarding it 
   [4].



Cook, et al.                  Experimental                      [Page 3]

RFC NNNN               Uplink To Mars (Latency)                June 2020


   When relay stations are introduced in communications between Earth 
   and Mars, retransmissions will be with relay stations. This 
   significantly reduces the distances involved, and therefore reduces 
   the retransmission time. That in turn will reduce the overall 
   latency.

   The more relay stations that can be deployed between Earth and Mars, 
   the less distance, and therefore time, there will be between
   retransmissions. Furthermore, the reduced distance between 
   transmissions will cause fewer errors, which will reduce the need for 
   retransmission.

   The number of relay stations, where they will be located, and how they
   will be deployed, requires further study and is not within the scope of
   this proposal. Enough satellites will be deployed as necessary to
   maximise the efficiency.

   One example would be to deploy 9 relay stations. With 9 relay stations,
   we are essentially dividing the distance into 10 chunks.  That means 
   the distance between transmission hops will only be one tenth distance
   between Earth and Mars. In other words, instead of 400 million
   kilometres, it will be 40 million kilometres. And this is only when 
   the two planets are furthest from each other.

4.  References

   [1]  https://www.space.com/14729-spacekids-distance-earth-mars.html
   [2]  https://www.mars-one.com/faq/technology/how-does-the-mars-base-
        communicate-with-earth?
   [3]  Charles Wang; Dean Sklar; Diana Johnson (Winter 2001–2002).
        “Forward Error-Correction Coding”
   [4]  https://en.wikipedia.org/wiki/Store_and_forward



















Cook, et al.                  Experimental                      [Page 4]

RFC NNNN               Uplink To Mars (Latency)                June 2020


5.  Appendix

   "include a "FEEDBACK" section in your final submission text where you
   may provide information about which reviews you did take into
   consideration, and which you have rejected, and why. You may choose
   any number of reviews (e.g. if you have too many to consider)."

From peer reviews

Peer 1

   1. "The first two pages follow the styling nicely, after which for
   seemingly no reason proper formatting disappears into thin air..."
   We hope we have done better this time with the formatting.

   2. "For example in the third chapter, it is said that a 50% overhead
   would make sending the data take 50% longer. This is likely not
   true."

   We have removed this statement, because the explanation was
   misleading.

   3. "How is the proposed retransmission handled?"
   The retransmission is between each hop and because the relay station
   operates at the TCP level. That means that the FEC in combination
   with the shorter distance between hops should greatly reduce the need
   for retransmission. But even if retransmission is needed, the shorter
   distance will introduce significantly less delay compared to
   retransmissions between Earth and Mars.

   4. "Another note, include proper sources. A google search is not a
   valid source, find the information on the NASA website and link that
   with proper syntax."

   We have addressed this in the final submission.
















Cook, et al.                  Experimental                      [Page 5]
	
RFC NNNN               Uplink To Mars (Latency)                June 2020


Peer 2

   2. "Protocol is well explained and documented, it's easy to
   understand and it addressess the initial problem well except for the
   fact that it doesn't explain properly how the Relay Stations should
   be positioned on the space. This is a quite important problem to
   solve for the initial exam assignment, since the positioning of Mars
   and Earth relative to Sun plays a key part in the communication
   (latency and packet loss) problems that arise between an
   interplanetary communication between Mars and Earth. To solve this
   problem, I suggest the writers to take a look on the Exam assignment
   Proposal 10 [1] Chapter 3.2.1. and the article mentioned [2] on that
   Chapter."

   Agree that it is very important and the whole thing fails without it,
   but it is beyond the scope of this proposal as it is a physical
   transmission issue and because the teacher explained to our group,
   that:
     "You are not expected to solve the physical layer problem. [...] 
     How the physical and link layers work is "not your problem" in all
     aspects except for retransmissions."

   Thrusters use power constantly. How do you supply enough fuel? And
   it's out of the scope of the assignment, at least according to the
   teacher, it's out of the scope.

Peer 3

   3. "Key problems: - The given solution doesnt address the problem
   with using TCP/IP application layer with a propagation delay of up to
   30 minutes. As suggested in the given task, couldn't the solution use
   some kind of proxy server to bring the data closer to Mars? Of course
   the data stored on the proxy server will become stale and need
   updating, but this wouldn't be a problem for some applications."

   Our solution uses relay stations that operate at the TCP layer.















Cook, et al.                  Experimental                      [Page 6]

RFC NNNN               Uplink To Mars (Latency)                June 2020


6.  Authors' Addresses

   Glenn Cook
   Tampere University
   Student ID: 293490/95279
   glenn.cook@tuni.fi


   Md Abdul Khalek
   Tampere University
   Student ID: 272525 
   abdul.khalek@tuni.fi


   Oliver Liombe Molua
   Tampere University
   Student ID: 256293
   oliverliombe.molua@tuni.fi

































Cook, et al.                  Experimental                      [Page 7]

© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
