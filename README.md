# Practice 2 - Contact List Component

This component is structured to display a Contact List

## Installation

```sh
npm i -g polymer-cli
npm i -g bower
git clone https://github.com/igoodbad/contact-list.git
polymer serve --open
```

## Usage

a) Show list
1. Include import in page
  <link rel="import" href="../contact-list/contact-list.html">
2. Include tag <contact-list></contact-list> in block to use
  <template>
    <contact-list></contact-list>
  </template>
3. Send array of elements
  <script>
        const element = document.querySelector("contact-list");
        element.set("contacts", [
          {
            firstName: 'Aru',
            lastName: 'Akise',
            age: 15,
            image: 'https://st-listas.20minutos.es/images/2013-11/372675/4249548_249px.jpg?1385314109',
            status: 'offline'
          },
          {
            firstName: 'Minene',
            lastName: 'Uryū',
            age: 22,
            image: 'https://st-listas.20minutos.es/images/2013-11/372675/4249545_249px.jpg?1385314109',
            status: 'online'
          }
        ]);
  </script>
  b) Get info
  1. Add a event listener, the name of event is 'contact-detail'.
    element.addEventListener('contact-detail', event => {
      let convertInfo = JSON.stringify(event);
      alert(convertInfo);
        })

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

Apache License 2004
