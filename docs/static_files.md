# Static Files

### Adding a static file to a plugin
1. create an assets folder under public:

```
.
├── common
├── public
│  ├── application
│  ├── assets
│  ├── services
│  └── visualizations
├── server
│  ├── routes
│  └── saved_objects
└── target
    └── public

```

2. put the static file inside the assets folder

3. include the file relatively from your code (todo: does this work for non-svgs?)

```
import indexPatternSvg from '../../assets/indexPattern.svg';
///...
<EuiIcon type={indexPatternSvg}/>;
```

That variable ```indexPatternSvg``` contains a data link to the file at runtime ```data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9eG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZmlsbC1ydW ... NzMiLz4KPC9zdmc+Cg==```


