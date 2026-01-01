> [!CAUTION] Whenever you are building the **Dockerfile** always remember that

> ```docker
> RUN apt-get update
> RUN apt-get install -y curl
> RUN rm -rf /var/lib/apt/lists/*
> ```
>
> will run each step one after other so `Even though you deleted it, the space is still used in previous layers.`  
> instead
>
> ```docker
> RUN apt-get update \
>     && apt-get install -y curl \
>     && rm -rf /var/lib/apt/lists/*
> ```
>
> ✔ Cleanup happens before the layer is saved.
> ✔ Space is actually freed.
