# ArCom

ArCom is our Application level protocol for RS232 simple communication, between Arduinos or Arduino and Computer.


## Protocol Description:

This is a ArCom message. All lines represents a byte.
Obviously, all bytes where sent in different frames.

|Frame Num|Frame Name  |     Frame Description     |
|:-------:|:----------:|:-------------------------:|
| 0       |ID 1        |First Byte of the data ID  |
| 1       |ID 2        |Second Byte of the data ID |
| 2       |DATA 0      |Data byte number 0         |
| 3       |DATA 1      |Data byte number 1         |
| 4       |DATA 2      |Data byte number 2         |
| 5       |DATA 3      |Data byte number 3         |
| 6       |DATA 4      |Data byte number 4         |
| 7       |MSG CHECKSUM|Data Checksum              |

Thank to this protocol we can send up to 5 bytes in one message of 8 bytes, with a 2 byte ID and a checksum control.
The checksum is the sum of byte with a high value in both ID and DATA bytes.
