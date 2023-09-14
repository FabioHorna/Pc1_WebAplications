<template>
  <div>
    <HeaderComponent />
    <div class="container">
      <JobCard
        :jobTitle="jobTitle"
        :companyName="companyName"
        :jobCategory="jobCategory"
        :jobSalary="jobSalary"
        :jobPublicationDate="jobPublicationDate"
        :jobDescription="jobDescription"
        :companyLogo="companyLogo"
      />
    </div>
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/Header.vue";
import FooterComponent from "./components/Footer.vue";
import JobCard from "./components/JobCard.vue";

export default {
  components: {
    HeaderComponent,
    FooterComponent,
    JobCard,
  },
  data() {
    return {
      jobTitle: "Senior Site Reliability Engineer",
      companyName: "Contra",
      jobCategory: "Software Development",
      jobSalary: "$145k - $160k",
      jobPublicationDate: "2023-09-11T21:21:04",
      jobDescription: `<p>We're looking for a <strong>Senior Site Reliability Engineer</strong>...</p>`,
      companyLogo: "URL_DE_TU_LOGO_AQUI",
    };
  },
};
</script>

<style>
/* Estilos globales aquí si es necesario */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f0f0f0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

/* Agrega aquí los estilos globales que necesites */
</style>

