# NOKIAChallenge
The input for the program is a log file that contains a list of requests of different URLs. Each line of the log file contains (1) a timestamp, (2) a user
id, and (3) a URL, separated by commas. You can assume that the input file is well formatted.
The program should compute the number of all second-order co-occurrences of page requests. A co-occurrence between URLs A and B is
defined as a single user accessing each of the URLs A and B at least once. The order of requests is not significant (i.e., co-occurrences A-B and
B-A are the same). The time elapsed between the visits does not matter either, and multiple visits to the same page by one user should be
counted as one. Furthermore, 3rd or higher order co-occurrences do not need to be considered, but a single user accessing URLs A, B, and C will
be counted as three separate co-occurrences A-B, A-C and B-C.
The program should output a list of co-occurrences with the following information on each line: (1) first URL of the co-occurrence, (2) second URL
of the co-occurrence, (3) number of users that accessed both URLs. The list should contain all co-occurrences that happened at least once,
sorted in the descending order by the number of users.

Input file:
2016-01-01T22:44:29+00:00,user0,http://a.com/
2016-01-01T22:44:31+00:00,user1,http://a.com/store
2016-01-01T22:44:31+00:00,kilroy,http://a.com/store
2016-01-01T22:44:32+00:00,user0,http://a.com/contact
2016-01-01T22:44:47+00:00,user0,http://a.com/store
2016-01-01T22:44:52+00:00,user1,http://a.com/contact
2016-01-01T22:44:57+00:00,user1,http://a.com/about
2016-01-01T22:44:58+00:00,user0,http://a.com/store
2016-01-01T22:44:59+00:00,kilroy,http://a.com/

Sample output:
http://a.com/ , http://a.com/store , 2
http://a.com/contact , http://a.com/store , 2
http://a.com/about , http://a.com/contact , 1
http://a.com/ , http://a.com/contact , 1
http://a.com/about , http://a.com/store , 1
