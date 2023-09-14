<template>
  <div class="job-card">
    <div class="job-title">{{ jobTitle }}</div>
    <div class="job-company">
      <img :src="companyLogo" alt="Company Logo" class="company-logo" />
      {{ companyName }}
    </div>
    <div class="job-category">{{ jobCategory }}</div>
    <div class="job-salary">{{ jobSalary }}</div>
    <div class="job-date">{{ formatDate(jobPublicationDate) }}</div>
    <div class="job-description" v-html="jobDescription"></div>
  </div>
</template>

<script>
export default {
  props: {
    jobTitle: String,
    companyName: String,
    jobCategory: String,
    jobSalary: String,
    jobPublicationDate: String,
    jobDescription: String,
    companyLogo: String,
  },
  methods: {
    formatDate(date) {
      const options = {
        year: "numeric",
        month: "long",
        day: "numeric",
        hour: "numeric",
        minute: "numeric",
        second: "numeric",
        timeZoneName: "short",
      };
      return new Date(date).toLocaleDateString("en-US", options);
    },
  },
};
</script>

<style scoped>
.job-card {
  background-color: #ffffff;
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  padding: 16px;
  margin: 16px;
}

.job-title {
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 8px;
}

.job-company {
  display: flex;
  align-items: center;
  font-size: 18px;
  margin-bottom: 8px;
}

.company-logo {
  width: 30px;
  height: 30px;
  margin-right: 8px;
}

.job-category {
  font-size: 18px;
  margin-bottom: 8px;
}

.job-salary {
  font-size: 18px;
  margin-bottom: 8px;
}

.job-date {
  font-size: 18px;
  margin-bottom: 8px;
}

.job-description {
  font-size: 18px;
}
</style>
