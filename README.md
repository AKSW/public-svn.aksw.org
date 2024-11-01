# public-svn.aksw.org

restoration project of public svn files

**only for public files**! all files committed here will be publicly accessible via Github and also https://svn.aksw.org/ ([example](https://svn.aksw.org/papers/2020/JWS_Faceted_Search_Benchmark/public.pdf))

<i> for private files, see https://github.com/AKSW/private-svn.aksw.org </i>

## The new home for svn.aksw.org

**Howto** partial git clone

```
git clone --filter=blob:none --sparse git@github.com:AKSW/public-svn.aksw.org.git

cd public-svn.aksw.org

# check out the folder/paper where you want to upload a public.pdf
git sparse-checkout set papers/2020/JWS_Faceted_Search_Benchmark/ --cone

# later on, check out another paper you want to make public
git sparse-checkout add papers/2023/XXX_My_newest_paper/ && mkdir -p papers/2023/XXX_My_newest_paper/

# list the folders you have checked out
git sparse-checkout list
```


**typical folder and filename structure**: `papers/<year>/<venue>_<short-title>/public.pdf`
* year: publication year
* venue: short name of conference/journal/...
* short-title: short title with  1-4 words connected with hyphen-minus (`-`)