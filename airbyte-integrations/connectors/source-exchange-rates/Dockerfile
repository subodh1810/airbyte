FROM airbyte/integration-base-python:0.1.4

# Bash is installed for more convenient debugging.
RUN apt-get update && apt-get install -y bash && rm -rf /var/lib/apt/lists/*

ENV CODE_PATH="source_exchange_rates"
ENV AIRBYTE_IMPL_MODULE="source_exchange_rates"
ENV AIRBYTE_IMPL_PATH="SourceExchangeRates"

WORKDIR /airbyte/integration_code
COPY $CODE_PATH ./$CODE_PATH
COPY setup.py ./
RUN pip install .

LABEL io.airbyte.version=0.1.1
LABEL io.airbyte.name=airbyte/source-exchange-rates
