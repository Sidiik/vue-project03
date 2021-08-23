<template>
  <form>
    <label for="Email">Email</label>
    <input type="text" id="Email" class="form-control" v-model="email" />
    <label for="password">password</label>
    <input
      type="password"
      id="password"
      class="form-control"
      v-model="password"
    />
    <label for="role" id="">Role</label>
    <select class="form-select" v-model="role">
      <option value="designer">Designer</option>
      <option value="developer">Developer</option>
    </select>
    <div class="check">
      <input type="checkbox" class="form-check-input " v-model="terms" /> Accept
      terms and conditions
    </div>

    <div class="skills">
      <label for="">SKILLS (alt + , )</label>
      <input
        type="text"
        class="form-control"
        v-model="tempSkills"
        @keyup.alt="addSkill"
      />
      <div
        v-for="skill in skills"
        class="badge bg-secondary p-2 m-1"
        :key="skill"
      >
        {{ skill }}
      </div>
    </div>

    <button class="btn btn-primary rounded mt-3">Create account</button>
  </form>
  <p>{{ email }}</p>
</template>

<script>
export default {
  name: "SignUp",
  data() {
    return {
      password: "",
      email: "",
      role: "",
      terms: false,
      tempSkills: [],
      skills: [],
    };
  },
  methods: {
    addSkill(e) {
      if (e.key === "," && this.tempSkills) {
        this.skills.push(this.tempSkills);
        this.tempSkills = "";
      }
    },
  },
};
</script>

<style>
form {
  width: 40%;
  background: #fff;
  padding: 2rem;
  border-radius: 0.6rem;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 10px 15px -3px,
    rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
  text-align: left;
  margin: auto;
}

label,
.check {
  margin-top: 1rem;
}
input[type="checkbox"] {
  margin-right: 0.5rem;
}
</style>
