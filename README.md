## HDFS Example

To store some data:

    curl -H "Content-Type: text/plain" http://localhost:8081/raw-data -d "210145,2012-10-26T21:32:52,135.23"
    curl -H "Content-Type: text/plain" http://localhost:8081/raw-data -d "210145,2012-10-26T21:36:52,99.9"
    
To check the stored data:
    
    hadoop fs -ls /tmp/data
    hadoop fs -tail /tmp/data/210145/20121026/raw.dat

To clear up all test data:

    hadoop fs -rmr -skipTrash '/tmp/data'
