curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
http://barath-task-kiaq.s3-website.eu-north-1.amazonaws.com

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::barath-task-kiaq/*"
    }
  ]
}



Review and create
General configuration
Edit
Distribution name
barath-kiaq
Description
-
Billing
Pay-as-you-go ($0/month)
Origin
Edit
Because you granted CloudFront access to your origin, CloudFront can write and update S3 bucket policies that restrict access to your S3 origin to CloudFront.
S3 origin
barath-task-kiaq.s3.eu-north-1.amazonaws.com
Origin path
-
Grant CloudFront access to origin
Yes
Enable Origin Shield
No
Connection attempts
3
Connection timeout
10
Cache settings
Edit
CloudFront will apply default cache settings tailored to serving content from a S3 origin. You can customize settings after you create your distribution.
Security
Edit
Security protections
None
Use monitor mode
No
Use existing WAF configuration
No
Cancel
Previous
Create distribution







# [Barath mern project](novamart.onrender.com) &middot; [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://legacy.reactjs.org/docs/how-to-contribute.html#your-first-pull-request)

Remember to give me your generous ⭐ Thanks you so very much !!!

Full-stack E-commerce web application built with the MERN stack(MongoDB,Express,React & Node), Bootstrap, Redux toolkit and hosted on Render.com Browse, shop, and checkout with ease! Stay alert for updates..

<img src="readmedata/home.JPG" alt="Image Description" width="800" height="500">

```javascript
return (
    <>
      {!keyword ? (
        <ProductCarousel />
      ) : (
        <Link to="/" className="btn btn-light mb-4">
          Go Back
        </Link>
      )}
      {isLoading ? (
        <Loader />
      ) : error ? (
        <Message variant="danger">
          {error?.data?.message || error.error}
        </Message>
      ) : (
        <>
          <h1>Latest Products</h1>
          <Row>
            {data.products.map((product) => (
              <Col key={product._id} sm={12} md={6} lg={4} xl={3}>
                <Product product={product} />
              </Col>
            ))}
          </Row>
          <Paginate
            pages={data.pages}
            page={data.page}
            keyword={keyword ? keyword : ""}
          />
        </>
      )}
    </>
  );
};
```

## Table of Contents

- [Features](#features)
- [Used Technologies](#used-technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

### Features

- Full featured shopping cart
- Product reviews and ratings system
- Top products carousel on main page
- Product pagination
- Product search feature
- User profile with orders
- Admin product management
- Admin user management
- Admin Order details page
- Mark orders as delivered option
- Checkout process (shipping, payment method, etc)
- PayPal / credit card integration
- Database seeder (products & users)

<img src="readmedata/product.JPG" alt="Image Description" width="800" height="500">

### Used Technologies

- **Frontend:**

  - React.js
  - Redux for state management
  - React Router for navigation
  - Bootstrap for css styling

- **Backend:**

  - Node.js
  - Express.js for middleware
  - Mongoose for object modeling
  - JSON Web Tokens (JWT) for authentication

- **Database**

  - MongoDB for product & user detail storing.

- **Payment**

  - Paypal & Card payment methods are available.

- **Hosting:**

  - Render.com for deployment and hosting
  - Web App Demo Link:


### Usage

1. **Start the backend server:**

   ```bash
   cd backend
   npm start
   ```

2. **Start the frontend development server:**

   ```bash
   cd frontend
   npm start
   ```

3. **Start both backend & frontend**

   ```bash
   cd novamart
   npm run dev
   ```

4. **Open your browser and navigate to `http://localhost:3000` to view the application.**

### Contributing

Contributors are warmly welcome! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/new-feature`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature/new-feature`).
6. Create a new Pull Request.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

