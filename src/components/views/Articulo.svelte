<script>
  import { request, gql } from "graphql-request";

  const query = gql`
    {
      posts {
        pages
        rows {
          id
          title
          body
          reactions
        }
      }
    }
  `;

  request("https://blog-backend-blush.vercel.app/graphql", query).then(
    (data) => console.log(data)
  );
</script>

<div class="articulo">
  <h1>Listado de articulos</h1>
  <p>
    Visualizar el listado de artículos en "Inspeccionar elemento" o "Ctrl+Shift+C" en el
    apartado de Consola
  </p>
</div>

<style>
  .articulo {
    padding-top: 15%;
    text-align: left;
    padding-left: 85px;
    color: white;
  }
</style>
