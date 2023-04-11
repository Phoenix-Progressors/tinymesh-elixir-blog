%{
  title: "About Ecto Dynamic Query",
  tags: ["ecto_query","dynamic","ecto"],
  published: true,
  discussion_url: "https://hexdocs.pm/ecto/dynamic-queries.html",
  description: """The query which generates dynamically according to conditions"""
  
}

### Dynamic queries

dynamic get generated in small sections according to the conditions.

## example
 we want to write a query on the basis of value of variable data where data may have three different values, then rather than writing the the query three time we write it in two small parts and return complete query at end

 query =
  Post
  |> where(^where)
  |> order_by(^order_by)

query =
    case data do
     70 ->
        where(query, [p], p.published_at < ^published_at)
     80 ->
        where(query, [p], p.published_at > ^published_at)
      _ ->
        query
    end

## Reference
  https://hexdocs.pm/ecto/dynamic-queries.html