# Console - DISPLAYS RAW RECORD

Displays the record in binary format from the last result set returned. This command needs the relative position of the record in the result set.

## Syntax

```sql
DISPLAY RAW RECORD <number>
```

Where:

- number         The number of the record in the last result set

## Example

```sql
orientdb {db=GratefulDeadConcerts}> select from V

----+-----+------+---------+-------------------------------+------+------------+---------------+--------------+-----------+--------------+-------------+----------
#   |@RID |@CLASS|song_type|name                           |type  |performances|out_followed_by|out_written_by|out_sung_by|in_followed_by|in_written_by|in_sung_by
----+-----+------+---------+-------------------------------+------+------------+---------------+--------------+-----------+--------------+-------------+----------
0   |#9:1 |V     |cover    |HEY BO DIDDLEY                 |song  |5           |[size=5]       |[size=1]      |[size=1]   |[size=4]      |null         |null      
1   |#9:2 |V     |cover    |IM A MAN                       |song  |1           |[size=2]       |[size=1]      |[size=1]   |[size=2]      |null         |null      
2   |#9:3 |V     |cover    |NOT FADE AWAY                  |song  |531         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
3   |#9:4 |V     |original |BERTHA                         |song  |394         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
4   |#9:5 |V     |cover    |GOING DOWN THE ROAD FEELING BAD|song  |293         |[size=39]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
5   |#9:6 |V     |cover    |MONA                           |song  |1           |[size=2]       |[size=1]      |[size=1]   |[size=2]      |null         |null      
6   |#9:7 |V     |null     |Bo_Diddley                     |artist|null        |null           |null          |null       |null          |[size=9]     |[size=7]  
7   |#9:8 |V     |null     |Garcia                         |artist|null        |null           |null          |null       |null          |[size=4]     |[size=-1] 
8   |#9:9 |V     |null     |Spencer_Davis                  |artist|null        |null           |null          |null       |null          |[size=1]     |[size=2]  
9   |#9:10|V     |original |JACK STRAW                     |song  |473         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
10  |#9:11|V     |original |JAM                            |song  |24          |[size=14]      |[size=1]      |[size=1]   |[size=20]     |null         |null      
11  |#9:12|V     |original |CASEY JONES                    |song  |312         |[size=-1]      |[size=1]      |[size=1]   |[size=33]     |null         |null      
12  |#9:13|V     |original |DEAL                           |song  |423         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
13  |#9:14|V     |original |TRUCKING                       |song  |519         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
14  |#9:15|V     |null     |BABY BLUE                      |song  |null        |[size=-1]      |null          |null       |[size=27]     |null         |null      
15  |#9:16|V     |original |DRUMS                          |song  |1386        |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
16  |#9:17|V     |original |STELLA BLUE                    |song  |328         |[size=31]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
17  |#9:18|V     |null     |MOUNTAIN JAM                   |song  |null        |[size=1]       |null          |null       |[size=1]      |null         |null      
18  |#9:19|V     |cover    |PROMISED LAND                  |song  |427         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
19  |#9:20|V     |cover    |BEAT IT ON DOWN THE LINE       |song  |325         |[size=-1]      |[size=1]      |[size=1]   |[size=-1]     |null         |null      
----+-----+------+---------+-------------------------------+------+------------+---------------+--------------+-----------+--------------+-------------+----------
LIMIT EXCEEDED: resultset contains more items not displayed (limit=20)

20 item(s) found. Query executed in 0.136 sec(s).
orientdb {db=GratefulDeadConcerts}> display raw record 0

Raw record content. The size is 292 bytes, while settings force to print first 150 bytes:

 Vsong_type   �name   �type   �performances   �out_followed_by   �out_written_by   �out_sung_by   �in_followed_by   � 
coverHEY BO D
```

This is a command of the Orient console. To know all the commands go to [Console-Commands](Console-Commands.md).
