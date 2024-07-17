---
layout: post
title: Using Retrofit to Interact with WebAPIs in Android
published: false
---

Managing API calls can sometimes be a pain in the ass. You need to manage making calls to the server, take care of JSON serilization and deserilization and then inflate the layout form the data. Most of my time during android development previously was spent in doing this work. Recently I discovered a library which makes this task so much simpler. Square has a wonderful library called Retrofit and i have became a fan. 

**What is Retrofit?**

Retrofit is an Open Source HTTP Client library for Android developed by Square. Retrofit can be used to convert your API into Java interface. You can then define methods in your interface to interact with the API where you can declare things like request method (GET, POST, PUT, DELETE, and HEAD), query params, request body (form encoded and multipart), and http headears. These are supported with the help of JAVA annotations. You can check the details of how to use these different features in the [retrofit website](https://square.github.io/retrofit/). For now let us look at a simple example of how Retrofit can be used to fetch and parse data from some API. 


**Create a POJO class**

This is the class that links data from the API and makes it usable in JAVA. This calss will be based on what your API endpoint outputs. Below is an example of a POJO class that I used for one of my apps which consumes a API providing data for different endagred species.

public class SpeciesDetails {

    public int success;
    public DetailsData data;

    public int getSuccess() {
        return success;
    }

    public void setSuccess(int success) {
        this.success = success;
    }

    public DetailsData getData() {
        return data;
    }

    public void setData(DetailsData data) {
        this.data = data;
    }

    public class DetailsData {

        private Status status;
        private String physical_characteristics, species_ecology, large_image;
        private List<String> threats, references;

        public Status getStatus() {
            return status;
        }

        public void setStatus(Status status) {
            this.status = status;
        }

        public String getPhysical_characteristics() {
            return physical_characteristics;
        }

        public void setPhysical_characteristics(String physical_characteristics) {
            this.physical_characteristics = physical_characteristics;
        }

        public String getSpecies_ecology() {
            return species_ecology;
        }

        public void setSpecies_ecology(String species_ecology) {
            this.species_ecology = species_ecology;
        }

        public String getLarge_image() {
            return large_image;
        }

        public void setLarge_image(String large_image) {
            this.large_image = large_image;
        }

        public List<String> getThreats() {
            return threats;
        }

        public void setThreats(List<String> threats) {
            this.threats = threats;
        }

        public List<String> getReferences() {
            return references;
        }

        public void setReferences(List<String> references) {
            this.references = references;
        }

        public class Status {
            private String stat_global, stat_national;

            public String getStat_global() {
                return stat_global;
            }

            public void setStat_global(String stat_global) {
                this.stat_global = stat_global;
            }

            public String getStat_national() {
                return stat_national;
            }
        }

    }
}



**Declare an Interface**

public interface ApiInterface {

  @GET("/api/details/{id}")
  Call<SpeciesDetails> getDetails(@Path("id") int id);

}

**Create a Interface**

   public ApiInterface getApiInterface() {
        OkHttpClient.Builder httpClient = new OkHttpClient.Builder();
        httpClient = addLogging(httpClient);
        httpClient.connectTimeout(100, TimeUnit.SECONDS);
        Retrofit retrofit = new Retrofit.Builder()
                .baseUrl("https://putyourapiendpointhere.com")
                .addConverterFactory(GsonConverterFactory.create())
                .client(httpClient.build())
                .build();
        return retrofit.create(ApiInterface.class);
    }


