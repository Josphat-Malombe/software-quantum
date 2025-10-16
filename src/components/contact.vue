<template>
  <div>
    <!-- Floating chat button -->
    <div class="chat-icon" @click="toggleChat">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="26"
        height="26"
        viewBox="0 0 24 24"
        fill="none"
        stroke="white"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      >
        <path d="M21 15a2 2 0 0 1-2 2H8l-5 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z" />
      </svg>
    </div>

    <!-- Chat window -->
    <div v-if="showChat" class="chat-window">
      <form
        name="contact"
        method="POST"
        netlify
        netlify-honeypot="bot-field"
        @submit.prevent="handleSubmit"
      >
        <input type="hidden" name="form-name" value="contact" />
        <p class="hidden">
          <label>Don’t fill this out: <input name="bot-field" /></label>
        </p>

        <h3>Send us a message</h3>

        <div class="form-group">
          <label for="email">Email</label>
          <input
            id="email"
            name="email"
            type="email"
            v-model="form.email"
            required
            placeholder="you@example.com"
          />
        </div>

        <div class="form-group">
          <label for="message">Message</label>
          <textarea
            id="message"
            name="message"
            v-model="form.message"
            required
            placeholder="Type your message..."
          ></textarea>
        </div>

        <button type="submit" class="send-btn" :disabled="loading">
          {{ loading ? "Sending..." : "Send" }}
        </button>

        <p v-if="successMessage" class="success">{{ successMessage }}</p>
        <p v-if="errorMessage" class="error">{{ errorMessage }}</p>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactAgent",
  data() {
    return {
      showChat: false,
      form: {
        email: "",
        message: "",
      },
      loading: false,
      successMessage: "",
      errorMessage: "",
    };
  },
  methods: {
    toggleChat() {
      this.showChat = !this.showChat;
      this.successMessage = "";
      this.errorMessage = "";
    },
    async handleSubmit(e) {
      this.loading = true;
      const formElement = e.target;
      const formData = new FormData(formElement);

      try {
        await fetch("/", {
          method: "POST",
          body: formData,
        });

        this.successMessage = "✅ Message sent successfully!";
        this.form.email = "";
        this.form.message = "";

        setTimeout(() => {
          this.showChat = false;
          this.successMessage = "";
        }, 2000);
      } catch (err) {
        console.error(err);
        this.errorMessage = "❌ Failed to send. Please try again.";
      } finally {
        this.loading = false;
      }
    },
  },
};
</script>

<style scoped>
/* Floating Icon */
.chat-icon {
  position: fixed;
  bottom: 25px;
  right: 25px;
  background: linear-gradient(135deg, #5a00ff, #00c9ff);
  border-radius: 50%;
  padding: 14px;
  cursor: pointer;
  box-shadow: 0 0 25px rgba(90, 0, 255, 0.4);
  transition: all 0.3s ease;
  z-index: 9999;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.chat-icon:hover {
  transform: scale(1.15);
  box-shadow: 0 0 35px rgba(0, 201, 255, 0.5);
}

/* Chat Window */
.chat-window {
  position: fixed;
  bottom: 90px;
  right: 25px;
  width: 320px;
  background: rgba(25, 25, 35, 0.75);
  border-radius: 16px;
  box-shadow: 0 0 40px rgba(0, 0, 0, 0.4);
  padding: 20px;
  z-index: 9999;
  animation: slideUp 0.35s ease;
  backdrop-filter: blur(16px);
  border: 1px solid rgba(255, 255, 255, 0.15);
  color: #e0e0e0;
}

@keyframes slideUp {
  from {
    transform: translateY(20px);
    opacity: 0;
  }
  to {
    transform: translateY(0);
    opacity: 1;
  }
}

h3 {
  text-align: center;
  color: #ffffff;
  margin-bottom: 15px;
  font-weight: 600;
  letter-spacing: 0.5px;
}

/* Form Styles */
.form-group {
  margin-bottom: 15px;
}

label {
  display: block;
  font-weight: 500;
  margin-bottom: 6px;
  color: #b3b3b3;
  font-size: 0.9rem;
}

input,
textarea {
  width: 100%;
  padding: 10px 12px;
  border: 1px solid rgba(255, 255, 255, 0.15);
  border-radius: 10px;
  background: rgba(255, 255, 255, 0.05);
  color: #e6e6e6;
  font-size: 14px;
  resize: none;
  transition: border-color 0.3s ease, background 0.3s ease;
}

input::placeholder,
textarea::placeholder {
  color: rgba(255, 255, 255, 0.4);
}

input:focus,
textarea:focus {
  border-color: #00c9ff;
  background: rgba(255, 255, 255, 0.1);
  outline: none;
}

/* Button */
.send-btn {
  width: 100%;
  padding: 10px;
  border: none;
  background: linear-gradient(135deg, #00c9ff, #5a00ff);
  color: white;
  border-radius: 10px;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 0 20px rgba(90, 0, 255, 0.3);
}

.send-btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 25px rgba(0, 201, 255, 0.4);
}

/* Feedback */
.success {
  color: #00ffae;
  background: rgba(0, 255, 174, 0.1);
  border-radius: 8px;
  text-align: center;
  margin-top: 10px;
  padding: 6px;
  font-size: 0.9rem;
}

.error {
  color: #ff4d4d;
  background: rgba(255, 77, 77, 0.1);
  border-radius: 8px;
  text-align: center;
  margin-top: 10px;
  padding: 6px;
  font-size: 0.9rem;
}

.hidden {
  display: none;
}
</style>
