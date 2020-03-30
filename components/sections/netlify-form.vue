<template>
  <v-container
    fill-height
    id="contact-us"
  >
    <form
      name="contactus"
      action="/thanks"
      method="post"
      netlify
      netlify-honeypot="bot-field"
    >
      <input
        type="hidden"
        name="form-name"
        value="contactus"
      />
      <v-container fill-height>
        <v-card
          color="transparent"
          flat
        >
          <SectionHeader subHeader="Contacto" />
          <v-row>
            <v-col cols="12">
              <div>
                <v-text-field
                  label="Nombre*"
                  for="name"
                  type="text"
                  name="name"
                  outlined
                  required
                  color="#404b87"
                />
              </div>
            </v-col>
            <v-col cols="12">
              <div>
                <v-text-field
                  label="Email*"
                  for="email"
                  type="email"
                  name="email"
                  required
                  outlined
                  color="#404b87"
                />
              </div>
            </v-col>

            <v-col cols="12">
              <div>
                <v-text-field
                  label="Telefono*"
                  for="phone"
                  name="phone"
                  required
                  outlined
                  color="#404b87"
                />
              </div>
            </v-col>
            <v-col cols="12">
              <v-select
                :items="['Busco informacion General.', 'Me interesa formar parte de Peninsula.', ]"
                label="Razón por contactar*"
                required
                outlined
              ></v-select>
            </v-col>

            <v-col cols="12">
              <div>
                <v-textarea
                  label="Mensaje*"
                  for="message"
                  name="message"
                  required
                  outlined
                  color="#404b87"
                />
              </div>
            </v-col>
            <div>
              <v-container>
                <v-btn
                  type="submit"
                  value="Send message"
                  color="#404b87"
                  dark
                  block
                  x-large
                  outlined
                >Enviar</v-btn>
              </v-container>
            </div>
          </v-row>
        </v-card>
      </v-container>
    </form>
  </v-container>
</template>
<script>
import SectionHeader from "~/components/SectionHeader";
export default {
  components: { SectionHeader },
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: ""
      }
    };
  },
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join("&");
    },
    handleSubmit() {
      fetch("/", {
        method: "POST",
        headers: { "Content-Type": "application/x-www-form-urlencoded" },
        body: this.encode({ "form-name": "contact", ...this.form })
      })
        .then(() => alert("Success!"))
        .catch(error => alert(error));
    }
  }
};
</script>
