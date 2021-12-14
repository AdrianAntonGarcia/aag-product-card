# AAG-Product-Card

Este es un paquete de pruebas de despliegue en npm

## Adrián Antón

```
import {
    ProductCard,
    ProductImage,
    ProductTitle,
    ProductButtons
} from 'aag-product-card'
```

```
const product1 = {
  id: '1',
  title: 'Coffee Mug - Card',
  img: './coffee-mug.png',
};

const product2 = {
  id: '2',
  title: 'Coffee Mug - Meme',
  img: './coffee-mug2.png',
};
const products = [product1, product2];
const product = products[0];

<ProductCard
        key={product.id}
        product={product}
        className="bg-dark text-white"
        initialValues={{ count: 0, maxCount: 10 }}
      >
    {({ reset, count, increaseBy, isMaxCountReached, maxCount }) => (
        <>
        <ProductCard.Image className="custom-image" />
        <ProductCard.Title className="text-bold" />
        <ProductCard.Buttons className="custom-buttons" />
        <button onClick={reset}>Reset</button>
        <button onClick={() => increaseBy(-2)}>-2</button>
        {!isMaxCountReached && (
            <button onClick={() => increaseBy(2)}>+2</button>
        )}
        <span>
            {count}-{maxCount}
        </span>
        </>
    )}
</ProductCard>
```
