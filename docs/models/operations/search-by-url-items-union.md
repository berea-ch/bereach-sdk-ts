# SearchByUrlItemsUnion


## Supported Types

### `operations.SearchByUrlItemsPost[]`

```typescript
const value: operations.SearchByUrlItemsPost[] = [
  {
    type: "POST",
    postUrl: "https://suburban-mantua.biz",
    text: "<value>",
    date: 228456,
    likesCount: 100858,
    commentsCount: 507906,
    sharesCount: 966259,
    postUrn: "<value>",
    postId: "<id>",
    author: {
      name: "<value>",
      profileUrl: "https://wide-eyed-violin.com",
      headline: "<value>",
      profilePicture: "<value>",
      isCompany: false,
      publicIdentifier: "<value>",
      profileUrn: "<value>",
    },
    isRepost: false,
  },
];
```

### `operations.SearchByUrlItemsPeople[]`

```typescript
const value: operations.SearchByUrlItemsPeople[] = [];
```

### `operations.SearchByUrlItemsCompany[]`

```typescript
const value: operations.SearchByUrlItemsCompany[] = [
  {
    type: "COMPANY",
    name: "<value>",
    profileUrl: "https://portly-divine.biz/",
    summary: "<value>",
    industry: "<value>",
    location: "<value>",
    followersCount: 155643,
  },
];
```

### `operations.SearchByUrlItemsJob[]`

```typescript
const value: operations.SearchByUrlItemsJob[] = [
  {
    type: "JOB",
    title: "<value>",
    company: "D'Amore - Pfeffer",
    companyUrl: "https://scientific-bump.name",
    companyLogo: "<value>",
    location: "<value>",
    workplaceType: null,
    postedAt: "<value>",
    jobUrl: "https://unfinished-community.net",
    listingId: "<id>",
  },
];
```

