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


kiaq-lap-174@kiaq-lap-174:~$ sudo systemctl status jenkins
[sudo] password for kiaq-lap-174: 
● jenkins.service - Jenkins Continuous Integration Server
     Loaded: loaded (/usr/lib/systemd/system/jenkins.service; enabled; preset: enabled)
     Active: active (running) since Fri 2026-06-26 09:20:31 IST; 6h ago
   Main PID: 1328 (java)
      Tasks: 48 (limit: 9235)
     Memory: 733.3M (peak: 855.6M)
        CPU: 1min 56.745s
     CGroup: /system.slice/jenkins.service
             └─1328 /usr/bin/java -Djava.awt.headless=true -jar /usr/share/java/jenkins.war --webroot=/var/cache/jenkins/war -->

Jun 26 09:20:30 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:30.958+0000 [id=54]        INFO        hudson.util.Retrier#start: >
Jun 26 09:20:31 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:31.049+0000 [id=34]        INFO        jenkins.InitReactorRunner$1>
Jun 26 09:20:31 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:31.254+0000 [id=24]        INFO        hudson.lifecycle.Lifecycle#>
Jun 26 09:20:31 kiaq-lap-174 systemd[1]: Started jenkins.service - Jenkins Continuous Integration Server.
Jun 26 09:20:40 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:40.049+0000 [id=54]        INFO        h.m.DownloadService$Downloa>
Jun 26 09:20:42 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:42.735+0000 [id=54]        INFO        h.m.DownloadService$Downloa>
Jun 26 09:20:45 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:45.119+0000 [id=54]        INFO        h.m.DownloadService$Downloa>
Jun 26 09:20:46 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:46.979+0000 [id=54]        WARNING        h.m.DownloadService$Down>
Jun 26 09:20:49 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:49.324+0000 [id=54]        INFO        h.m.DownloadService$Downloa>
Jun 26 09:20:49 kiaq-lap-174 jenkins[1328]: 2026-06-26 03:50:49.325+0000 [id=54]        INFO        hudson.util.Retrier#start: >







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

