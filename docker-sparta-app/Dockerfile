FROM node:20-slim

LABEL maintainer="sparta-developer"

WORKDIR /usr/src/app

COPY app/package*.json ./

# The --ignore-scripts flag stops the failing postinstall seed script
RUN npm install --ignore-scripts

# Now copy the seeds folder and everything else safely
COPY app/ .

EXPOSE 3000

CMD ["node", "index.js"]
