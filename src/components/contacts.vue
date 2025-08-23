<template>
  <div class="contact-container">
    <div class="contact-wrapper">
      <!-- Header Section -->
      <div class="header" :class="animationClasses.header">
        <h1>Get in Touch</h1>
        <p>Let's work together to bring your ideas to life.</p>
      </div>

      <div class="content-grid">
        <!-- Contact Information -->
        <div class="contact-info" :class="animationClasses.contactInfo">
          <h2>Contact Information</h2>
          
          <div class="info-items">
            <div 
              v-for="(item, index) in contactInfo" 
              :key="index"
              class="info-item"
            >
              <div class="icon-wrapper">
                <component :is="item.icon" />
              </div>
              <span>{{ item.text }}</span>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="form-container" :class="animationClasses.form">
          <form @submit.prevent="handleSubmit">
            <div v-for="field in formFields" :key="field.name" class="form-group">
              <label :for="field.name">{{ field.label }}</label>
              <component
                :is="field.type === 'textarea' ? 'textarea' : 'input'"
                :id="field.name"
                :type="field.type"
                :name="field.name"
                v-model="formData[field.name]"
                :rows="field.type === 'textarea' ? 4 : undefined"
                required
              />
            </div>

            <button type="submit" :disabled="isSubmitting">
              <svg v-if="!isSubmitting" class="send-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M22 2L11 13M22 2l-7 20-4-9-9-4 20-7z" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <span>{{ isSubmitting ? 'Sending...' : 'Send Message' }}</span>
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactPage',
  data() {
    return {
      formData: {
        name: '',
        email: '',
        message: ''
      },
      isSubmitting: false,
      contactInfo: [
        {
          icon: 'PhoneIcon',
          text: '+91 8240395691'
        },
        {
          icon: 'MailIcon',
          text: 'swarnavapaul8@gmail.com'
        },
        {
          icon: 'MapPinIcon',
          text: '547,Radhanagr,.Garulia,North 24 parganas'
        }
      ],
      formFields: [
        {
          name: 'name',
          label: 'Name',
          type: 'text'
        },
        {
          name: 'email',
          label: 'Email',
          type: 'email'
        },
        {
          name: 'message',
          label: 'Message',
          type: 'textarea'
        }
      ],
      animationClasses: {
        header: 'animate-fade-in-down',
        contactInfo: 'animate-slide-in-left',
        form: 'animate-slide-in-right'
      }
    }
  },
  methods: {
    async handleSubmit() {
      this.isSubmitting = true
      try {
        await new Promise(resolve => setTimeout(resolve, 1000))
        console.log('Form submitted:', this.formData)
        this.formData = {
          name: '',
          email: '',
          message: ''
        }
      } catch (error) {
        console.error('Error submitting form:', error)
      } finally {
        this.isSubmitting = false
      }
    }
  }
}
</script>

<style scoped>
/* Base Styles */
.contact-container {
  min-height: 100vh;
  background-color: #11071f;
  padding: 3rem 1rem;
  color: #e5e7eb;
}

.contact-wrapper {
  max-width: 1200px;
  margin: 0 auto;
}

/* Header Styles */
.header {
  text-align: center;
  margin-bottom: 4rem;
}

.header h1 {
  font-size: 2.5rem;
  color: #fff;
  margin-bottom: 1rem;
  font-weight: 700;
  text-shadow: 0 0 10px rgba(255, 255, 255, 0.1);
}

.header p {
  font-size: 1.125rem;
  color: #9ca3af;
}

/* Grid Layout */
.content-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 3rem;
}

@media (min-width: 768px) {
  .content-grid {
    grid-template-columns: 1fr 1fr;
  }
}

/* Contact Info Styles */
.contact-info {
  padding: 1rem;
}

.contact-info h2 {
  font-size: 1.5rem;
  color: #fff;
  margin-bottom: 2rem;
  font-weight: 600;
}

.info-items {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.info-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  transition: color 0.3s ease;
  color: #9ca3af;
}

.info-item:hover {
  color: #a855f7;
}

.icon-wrapper {
  background-color: rgba(168, 85, 247, 0.1);
  padding: 0.75rem;
  border-radius: 50%;
  transition: all 0.3s ease;
  border: 1px solid rgba(168, 85, 247, 0.2);
}

.info-item:hover .icon-wrapper {
  background-color: rgba(168, 85, 247, 0.2);
  border-color: rgba(168, 85, 247, 0.4);
  box-shadow: 0 0 15px rgba(168, 85, 247, 0.3);
}

/* Form Styles */
.form-container {
  background-color: rgba(255, 255, 255, 0.03);
  padding: 2rem;
  border-radius: 1rem;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  border: 1px solid rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
}

.form-group {
  margin-bottom: 1.5rem;
}

label {
  display: block;
  font-size: 0.875rem;
  font-weight: 500;
  color: #9ca3af;
  margin-bottom: 0.5rem;
}

input, textarea {
  width: 100%;
  padding: 0.75rem;
  background-color: rgba(255, 255, 255, 0.05);
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 0.5rem;
  color: #fff;
  transition: all 0.3s ease;
}

input:focus, textarea:focus {
  outline: none;
  border-color: #a855f7;
  box-shadow: 0 0 0 3px rgba(168, 85, 247, 0.2);
  background-color: rgba(255, 255, 255, 0.08);
}

input::placeholder, textarea::placeholder {
  color: #6b7280;
}

textarea {
  resize: vertical;
  min-height: 100px;
}

button {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  background: linear-gradient(135deg, #a855f7 0%, #7928ca 100%);
  color: white;
  border: none;
  border-radius: 0.5rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(168, 85, 247, 0.3);
}

button:hover:not(:disabled) {
  transform: translateY(-2px);
  box-shadow: 0 6px 20px rgba(168, 85, 247, 0.4);
}

button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}

.send-icon {
  width: 1.25rem;
  height: 1.25rem;
}

/* Animations */
@keyframes fade-in-down {
  0% {
    opacity: 0;
    transform: translateY(-20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slide-in-left {
  0% {
    opacity: 0;
    transform: translateX(-100px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes slide-in-right {
  0% {
    opacity: 0;
    transform: translateX(100px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.animate-fade-in-down {
  animation: fade-in-down 0.7s ease-out;
}

.animate-slide-in-left {
  animation: slide-in-left 0.7s ease-out;
}

.animate-slide-in-right {
  animation: slide-in-right 0.7s ease-out;
}
</style>