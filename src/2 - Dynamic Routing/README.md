## Challenge 3: Dynamic Routing

### Objective

In this challenge, you will implement a dynamic routing system that displays details of a selected product. This exercise will test your skills in Next.js, data manipulation, and page navigation.

### Instructions

#### 1. Create the Product Listing Page

- Create a new page named `produtos.js` inside the `pages` folder.
- Simulate a list of products by using an array of objects with the following fields:
  - `id` (number)
  - `nome` (string)
  - `descricao` (string)
  - `preco` (number)

**Example:**

```javascript
const products = [
  {
    id: 1,
    name: "Product A",
    description: "Product Description A",
    price: 100,
  },
  {
    id: 2,
    name: "Product B",
    description: "Product Description B",
    price: 150,
  },
];
```

2. Display the Product List

- For each product, create a card that displays the product's name and price.
- Each card should be a link that redirects to a product detail page (for example, `/produtos/[id]`).

Example of Card Structure:

```javascript
import Link from "next/link";

const ProductCard = ({ produto }) => (
  <div className="card">
    <h2>{produto.nome}</h2>
    <p>Price: ${produto.preco}</p>
    <Link href={`/produtos/${produto.id}`}>
      <a>View Details</a>
    </Link>
  </div>
);
```

3. Create the Product Detail Page

- Inside the `pages/produtos` folder, create a new dynamic page named `[id].js`.
- Utilize `getStaticPaths` to generate dynamic routes for each product based on the products array.
- Use `getStaticProps` to fetch the specific product data based on the `id` from the URL.
- Display the detailed information of the product, including name, description, and price.

Example Implementation:

```javascript
// pages/produtos/[id].js
import { useRouter } from "next/router";

const ProductDetail = ({ produto }) => {
  const router = useRouter();

  if (!produto) return <p>Loading...</p>;

  return (
    <div>
      <h1>{produto.nome}</h1>
      <p>{produto.descricao}</p>
      <p>Price: ${produto.preco}</p>
      <button onClick={() => router.push("/produtos")}>Back to Products</button>
    </div>
  );
};

export async function getStaticPaths() {
  const produtos = [
    /* array of products */
  ];
  const paths = produtos.map((produto) => ({
    params: { id: produto.id.toString() },
  }));

  return { paths, fallback: false };
}

export async function getStaticProps({ params }) {
  const produtos = [
    /* array of products */
  ];
  const produto = produtos.find((p) => p.id === parseInt(params.id));

  return { props: { produto } };
}

export default ProductDetail;
```

4. Implement Navigation

- Add a navigation feature that allows users to return to the product listing page from the detail page.
- You can implement this using a simple button that redirects back to the list of products.

### Technical Requirements

- Use the `Link` component from Next.js to create links between the product listing and detail pages.
- The detail page should be generated statically (SSG) using `getStaticPaths` and `getStaticProps`.
- Ensure that the pages are responsive and visually appealing.

### Tips

- Test the routing and data passing between pages thoroughly to ensure smooth navigation.
- Make sure that the generated URLs correspond to the product IDs.
- You may add styles using `CSS` or a library like `Tailwind CSS` to improve the presentation.

### Final Considerations

Pay attention to code structure and best practices in React and Next.js. Your implementation should demonstrate a clear understanding of dynamic routing, data fetching, and responsive design.

### Enhancements Made

- **Detailed Structure**: Each step provides clear instructions and examples for implementation.
- **Code Snippets**: Relevant code snippets are included to illustrate expected implementations.
- **User Experience Considerations**: Emphasis on navigation and user feedback for better UX.
- **Technical Requirements**: Clearly outlined expectations for routing and responsiveness.
- **Final Considerations**: Encouragement to focus on best practices in coding and design.

### How to Use

1. **Create a new Markdown file** (e.g., `dynamic_routing_challenge.md`) in your repository.
2. **Paste the content above** into the file.
3. **Save the file** and commit the changes.
