# Magazine API (Strapi)

Strapi CMS pre-configured for [Next.js Magazine Starter](https://github.com/edgarlr/magazine). Deploy to Heroku in one click.

If you want to deploy to any other platform or set up a different [upload provider](https://strapi.io/documentation/developer-docs/latest/plugins/upload.html#using-a-provider) you can use the [strapi-template-magazine](https://github.com/edgarlr/strapi-template-magazine) instead.

## Features

- 4 Content types: Article, Category, Contributor, Pages.
- Publication system (draft & published).
- Preview unpublished content: Articles, pages.
- Slug system
- 2 Contributor types: Featured, default.
- SEO and social media friendly
- Role based access controls

## API Routes

- `/articles`
- `/categories`
- `/contributors`
- `/pages`

## Getting started

Create your own copy of this project by clicking the ["Use this template"]('https://github.com/edgarlr/magazine-api/generate') button and filling the form.

### Running locally

Create a folder and `git clone` from your own repository.

Install the dependencies and start the dev server.

```bash
    yarn install
    yarn develop
```

The strapi server will run on [http://localhost:1337](http://localhost:1337)

Go to the admin panel [(http://localhost:1337/admin)](http://localhost:1337), create an account and start adding sample content.

### Deployment

First, you'll need a [Cloudinary](https://cloudinary.com) and a [Heroku](https://www.heroku.com/) account.

1. From your copy of the repo click the "Deploy to Heroku" button

<a href="https://www.heroku.com/deploy/?template=https://github.com/edgarlr/magazine-api">
<img src="https://assets.strapi.io/uploads/Deploy_button_heroku_b1043fc67d.png" />
</a>

2. Fill the Cloudinary ENV variables.
3. Deploy
4. Once is deployed, go to the admin panel e.g. `https://yourherokudomain.com/admin` and create an account.
5. Last, go to "Setting" > "Users & permissions plugins" > "Public" > "Permissions" and check `find` on Article, Category, Contributor and Pages.

### Adding Content

The recommended flow for adding new content is:

- Add contributor
- Add category
- Add article or page

### Preview Content

Once you have your frontend deployed go to "Settings" > "Preview Content"

Fill it with your info, the URL should look like this.
`https://<yoursite.com>/api/:contentType-preview?secret=<your-secret>&id=:id`

Now, go to any article or page and click on "Preview".

## License

[MIT License](https://github.com/edgarlr/magazine-api/blob/main/LICENSE).
