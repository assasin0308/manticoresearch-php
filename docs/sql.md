# SQL
Allows running a SQL command.
For complete reference of payload and response see Manticore's [SQL API](https://docs.manticoresearch.com/latest/html/http_reference/sql.html).
`body` must have `query` parameter with the desired SQL command to be executed. 

```
$params = [
    'body' => [
        'query' => "SELECT * FROM movies where MATCH('@movie_title star trek')"
    ]
];

$response = $client->sql($params);
```