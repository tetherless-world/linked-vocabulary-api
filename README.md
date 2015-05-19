linked-vocabulary-api
=====================
[![Build Status](https://travis-ci.org/tetherless-world/linked-vocabulary-api.svg?branch=master)](https://travis-ci.org/tetherless-world/linked-vocabulary-api)

Linked Data API Specification for publishing SKOS vocabulary linked data on the web

The API
-------

| Description  | Endpoint Template |
| ------------- | ------------- |
| *get list of all terms from all vocabularies published by service* | ``GET /terms`` |
| *get vocabulary resource*  | ``GET /vocab/{vocab_id}``  |
| *get vocabulary term*  | ``GET /vocab/{vocab_id}/term/{term_id}``  |
| *get list of all terms in the specified vocabulary* | ``GET /vocab/{vocab_id}/terms`` |
| *get list of all terms related to specified term* | ``GET /vocab/{vocab_id}/term/{term_id}/related`` |
| *get list of all terms in vocabulary with a label that contains the specified text* | ``GET /vocab/{vocab_id}/terms?anyLabelContains={text}`` |
| *get list of all terms that are a close match to the specified term and are in a vocabulary with the specified label* | ``GET /vocab/{vocab_id}/term/{term_id}/closeMatch?inScheme.prefLabel={name}`` |
| *get list of terms, filtered to only include the specified properties* | ``GET /vocab/{vocab_id}/terms?_properties=prefLabel,altLabel`` |
| *get paginated list of terms* | ``GET /vocab/{vocab_id}/terms?_page={index}&_pageSize={size}`` |
