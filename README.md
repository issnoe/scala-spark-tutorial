
 # Steps

 - Spark tutorial example
  - ~/scala-spark-tutorial
  - Config ERM
    - Select Spark
    - https://console.aws.amazon.com/elasticmapreduce/home?region=us-east-1#cluster-details:j-s
    - Config SSH Any
  - Upload data on https://console.aws.amazon.com/s3/buckets/example/?region=us-east-1&tab=overview
    - From https://insights.stackoverflow.com/survey

  - Generate .jar on lacal
    - On ~/scala-spark-tutorial
      - ./gradlew clean jar
      - Upload on
        - https://console.aws.amazon.com/s3/buckets/example/?region=us-east-1&tab=overview

  - Run  on hadoop@ip
        - ssh -i ~/develop.pem hadoop@example.compute-1.amazonaws.com
        - aws s3 cp s3://lab-surveyresultspublic/StackOverFlowSurvey-spark.jar .
        - spark-submit ./StackOverFlowSurvey-spark.jar




