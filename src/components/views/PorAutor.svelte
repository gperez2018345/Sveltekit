<script>
  import { request, gql } from "graphql-request";

  const query1 = gql`
    {
      posts {
        rows {
          author {
            name
          }
          title
          body
        }
      }
    }
  `;

  request("https://blog-backend-blush.vercel.app/graphql", query1).then(
    (data1) => console.log(data1)
  );
</script>

<div class="articulo">
  <h1>Articulos por autor</h1>
  <p>
    Visualizar el listado de artículos por Autor en "Inspeccionar elemento" o
    "Ctrl+Shift+C" en el apartado de Consola
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
