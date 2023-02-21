# Helm-Labs

# Lab 1


1. Add bitnami helm chart repository in the controlplane node.

``` helm repo add bitnami https://charts.bitnami.com/bitnami ```

![Screenshot from 2023-02-12 13-02-45](https://user-images.githubusercontent.com/57557314/218309364-b9faa28f-fe8c-47b4-8ad4-419d63da2584.png)


2. Deploy the Apache application on the cluster using the apache from the bitnami repository.Set the 
release Name to: amaze-surf

```helm install amaze-surf bitnami/apache```

![Screenshot from 2023-02-12 14-29-59](https://user-images.githubusercontent.com/57557314/218311155-31631541-5497-4bb3-8b1d-761242aa13df.png)

3. Uninstall the apache chart release from the cluster.

```helm uninstall amaze-surf```

![Screenshot from 2023-02-12 13-10-27](https://user-images.githubusercontent.com/57557314/218309458-a2085d91-376f-4635-ace4-33deb4c62da3.png)


4. install specfic version of nginx 1.22.0, then update it to specfic 1.23.1, then rollback

```helm install bitnami/nginx --version 12.0.5 ```

![Screenshot from 2023-02-12 13-25-42](https://user-images.githubusercontent.com/57557314/218309477-2a86c94e-a00d-483f-97b1-03071f8a7f7d.png)


``` helm search repo nginx --versions ```

![Screenshot from 2023-02-12 13-42-41](https://user-images.githubusercontent.com/57557314/218311103-c42f95e1-9361-44c1-8c14-078c3490f1cd.png)


```helm upgrade nginx bitnami/nginx --version 13.2.10 ```

![Screenshot from 2023-02-12 13-35-16](https://user-images.githubusercontent.com/57557314/218309551-24e5b934-2044-4f92-8f7a-dfaf2ace3921.png)


```helm rollback nginx```

![Screenshot from 2023-02-12 13-35-54](https://user-images.githubusercontent.com/57557314/218310681-14d3a4ee-d2e9-4805-9d14-742b798404f2.png)
