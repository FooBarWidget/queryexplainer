`query_extractor` extracts all SQL queries from a Rails log file and prints them to stdout.

`query_explainer` reads SQL queries from stdin, analyzes each of them with EXPLAIN, and prints out those queries that affect more than 10 rows.

Normal usage:

    ./query_extractor production.log > queries.txt
    tail -f queries.txt | ./query_explainer
