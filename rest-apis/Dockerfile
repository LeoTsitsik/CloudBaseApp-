# Χρησιμοποιούμε μια ελαφριά έκδοση του Node.js
FROM node:alpine

# Ορίζουμε τον φάκελο εργασίας μέσα στο container
WORKDIR /app

# Εγκαθιστούμε το εργαλείο json-server
RUN npm install -g json-server

# Αντιγράφουμε το αρχείο με τα δεδομένα μας μέσα στο container
COPY db.json .

# Ανοίγουμε την πόρτα 3000
EXPOSE 3000

# Η εντολή που θα τρέξει όταν ξεκινήσει το container
CMD ["json-server", "--watch", "db.json", "--host", "0.0.0.0"]