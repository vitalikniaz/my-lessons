FROM quay.io/keycloak/keycloak:latest

#COPY --from=builder /opt/keycloak/ /opt/keycloak/
#WORKDIR /opt/keycloak
# for demonstration purposes only, please make sure to use proper certificates in production instead
#RUN keytool -genkeypair -storepass password -storetype PKCS12 -keyalg RSA -keysize 2048 -dname "CN=server" -alias server -ext "SAN:c=DNS:localhost,IP:127.0.0.1" -keystore conf/server.keystore
# change these values to point to a running postgres instance
#ENV KC_DB_URL=<DBURL>
#ENV KC_DB_USERNAME=<DBUSERNAME>
#ENV KC_DB_PASSWORD=<DBPASSWORD>
#ENV KC_HOSTNAME=localhost
ENV KEYCLOAK_ADMIN=admin
ENV KEYCLOAK_ADMIN_PASSWORD=change_me

EXPOSE 8080

#For Production
#ENTRYPOINT ["/opt/keycloak/bin/kc.sh", "start"]
#For Development
ENTRYPOINT ["/opt/keycloak/bin/kc.sh", "start-dev"]