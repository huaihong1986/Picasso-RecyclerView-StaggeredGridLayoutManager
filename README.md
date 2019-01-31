# Picasso/Glide-RecyclerView-StaggeredGridLayoutManager

![Alt Text](https://github.com/yuvaraj119/Picasso-RecyclerView-StaggeredGridLayoutManager/blob/master/bloggif_571854a507ddc.gif)

##**Picasso + RecyclerView + StaggeredGridLayoutManager**

Its the enhanced version of this project https://github.com/pohh/slotmachinepicasso were there was a problem with

Picasso + RecyclerView + StaggeredGridLayoutManager shuffles resizable recycler views infinitely
issue posted on github https://github.com/square/picasso/issues/918

I have made some changes now it works with Picasso and Glide without any shuffles and position change

Currently this project is done with Picasso

If you want to use it with Glide

# How to use with Glide

##**Glide + RecyclerView + StaggeredGridLayoutManager**

Add dependencies for Glide https://github.com/bumptech/glide

Remove Picasso library from dependency and remove all the codes of Picasso from **MyGridAdapter.java** and also from other places 
used in project.


####In onBindViewHolder add this line of code for Glide:

```
Glide.with(mContext)
                .load(item.getUrl())
                .placeholder(PlaceHolderDrawableHelper.getBackgroundDrawable(position))
                .diskCacheStrategy(DiskCacheStrategy.ALL)
                .crossFade()
                .into(vh.imageView);
```


# Thanks
* p oh https://github.com/pohh
* Picasso https://github.com/square/picasso
* Glide https://github.com/bumptech/glide



