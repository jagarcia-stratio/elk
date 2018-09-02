FROM python

# Install SentimentAPI
WORKDIR /tmp
RUN \
  git clone https://github.com/melvynator/toy_sentiment_API && \
  mv toy_sentiment_API /sentiment && \
  cd /sentiment && \
  
  #Install Scikit-Learn (for the machine learning)
  pip install -r requirements.txt && \
  python -m textblob.download_corpora

  #Run the local server
ENTRYPOINT python /sentiment/sentiment_server.py

EXPOSE 5001 5000