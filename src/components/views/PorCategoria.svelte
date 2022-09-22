<script>
  import { request, gql } from "graphql-request";

  const query2 = gql`
    {
      posts {
        rows {
          categories {
            name
          }
          title
          body
        }
      }
    }
  `;

  request("https://blog-backend-blush.vercel.app/graphql", query2).then(
    (data2) => console.log(data2)
  );
</script>

<div class="articulo">
  <h1>Artículos por categoría</h1>
  <p>
    Visualizar el listado de artículos por categoría en "Inspeccionar elemento"
    o "Ctrl+Shift+C" en el apartado de Consola
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
