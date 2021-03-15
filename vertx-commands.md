# Vert.x commands.

## Commands.
`vertx run [fileName] -cluster` 
флаг "-cluster"  придназначен для того чтобы днный Vertical мог принимать сообщения из других JVM 

`vertx run [fileName] -ha` 
етот узел если он начнет пропадать может бить реплецырован на других узлах нашего кластера 
и в том числе если другие узлы нашего кластера будут пропадать в етот узел тоже можна реплецыроватся

`jps` - show java processes
`kill -9 [processId]` - kill proces   

`vertx run [fileName] -ha -quorum 2`

`java -jar fat.jar -ha` 

`./gradlew run -PmainClass=[pathToMainClass]`
`./gradlew run -PmainClass=chapter2.hello.HelloVerticle`