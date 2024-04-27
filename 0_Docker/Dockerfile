FROM nginx:stable-alpine

## LABELS
LABEL author="CyberThulhu"
LABEL name="C2-Nginx-Redirector"
LABEL description="Nginx Container with HTTP(S) Redirection"
LABEL purpose="Filter and Redirect C2 traffic to C2 Server"
LABEL tag="redirector:nginx"

## PORTS
EXPOSE 53
EXPOSE 80
EXPOSE 443

## APK PACKAGES
# Add Wireguard Repository -- Needed in Some Exercise Scenarios
RUN apk add librdkafka --repository=https://git.zx2c4.com/wireguard-linux/tree/drivers/net/wireguard
# Update Packages
RUN apk update
RUN apk upgrade --no-cache
# Install Packages
RUN apk add bash
RUN apk add curl
RUN apk add wireguard-tools
RUN apk add iptables

## DIRECTORIES
RUN mkdir -p /cert && chmod +w /cert

## CREATE LAUNCHER
COPY ./src/launcher /usr/local/bin/launcher
RUN chmod +x /usr/local/bin/launcher

## START
CMD [ "/usr/local/bin/launcher" ]