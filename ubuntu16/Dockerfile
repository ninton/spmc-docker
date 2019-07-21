FROM ubuntu:16.04
RUN apt-get update
RUN apt-get install -y imagemagick
RUN apt-get install -y ghostscript
RUN apt-get install -y pdftk
RUN apt-get install -y bc
RUN apt-get install -y curl
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
RUN bash -c "source /root/.bashrc; source /root/.nvm/nvm.sh; nvm install v9.8.0; nvm use v9.8.0; npm install -g scanned-pdf-margin-cutter"
RUN sed --in-place 's/<policy domain="coder" rights="none" pattern="PDF" \/>/<policy domain="coder" rights="read|write" pattern="PDF" \/>/' /etc/ImageMagick-6/policy.xml
