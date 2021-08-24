ARG ELK_VERSION

# https://www.docker.elastic.co/
FROM docker.elastic.co/elasticsearch/elasticsearch:${ELK_VERSION}

# Add your elasticsearch plugins setup here
# Example: RUN elasticsearch-plugin install analysis-icu
COPY config/stopFilter.txt config/stopFilter.txt
COPY config/synonymsFilter.txt config/synonymsFilter.txt
COPY config/user_dictionary.txt config/user_dictionary.txt

RUN elasticsearch-plugin install analysis-nori