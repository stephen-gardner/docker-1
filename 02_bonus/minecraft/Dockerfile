# Minecraft server

FROM anapsix/alpine-java
RUN ["apk", "update"]
RUN ["apk", "add", "wget"]
WORKDIR minecraft
RUN ["wget", "https://s3.amazonaws.com/Minecraft.Download/versions/1.12.2/minecraft_server.1.12.2.jar"]
RUN ["/bin/sh", "-c", "echo eula=true > eula.txt"]
EXPOSE 25565
ENTRYPOINT ["java", "-Xmx1024M", "-Xms1024M", "-jar", "minecraft_server.1.12.2.jar", "nogui"]
