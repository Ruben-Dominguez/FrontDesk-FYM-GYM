<template>
  <div class="gym-body">
    
    <div class="gym-container container">
      <b-row>
        <b-col class="gym-col padding-0">
          <div class="btn-group btn-group-justified">
            <h1>Membresias</h1>
            <div class="form-container" id="new-gym-button">
              <b-button class="new-gym" variant="light" @click="show">Nueva membresía</b-button>
            </div>
          </div>

          <div class="cajahijo2">
            <div class="cajahijo3">
              <div class="cajahijo4">
              <b-card-text class="text-center">
                    <b-row>
                      <b-col>
                        <h6>Membresía mensual</h6>
                      </b-col>
                      <b-col>
                        <p>Tipo de usuario:socio</p>
                      </b-col>
                      <b-col>
                        <p>Fecha de corte</p>
                      </b-col>
                    </b-row>
                  </b-card-text>
              </div>
            </div>
            
          </div>

          
        </b-col>
      </b-row>
    </div>
  </div>

  <div id="myModal" class="modal"  style="overflow-y: scroll;">
    <div class="modal-content">
      <div class="close-div">
        <div class="close">&times;</div>
      </div>
      <h3 class="agregar-titulo">Agregar nueva membresía</h3>
      <b-form class="agregar-form" @submit="onSubmitAgregar">
        <b-form-group id="input-group-agregar">
          <b-container class="bv-example-row">
            <b-row>
              <b-col>
                <label >Nombre</label>
                <b-form-input
                  id="input-3"
                  v-model="nombreMembresia"
                  type="text"
                  placeholder="Ingresa el nombre"
                  required
                ></b-form-input>

                <label >Porcentaje de descuento</label>
                <b-form-input
                  id="input-3"
                  v-model="PorcentajeMembresia"
                  type="text"
                  placeholder="Ingresa el porcentaje de descuento"
                  required
                ></b-form-input>

                <label >Periodicidad</label>
                <b-form-input
                  id="input-3"
                  v-model="PeriodicidadMembresia"
                  type="text"
                  placeholder="Ingresa la periodicidad"
                  required
                ></b-form-input>

              </b-col>
              
            </b-row>
          </b-container>
        </b-form-group>
        <b-button class="restablecer-button" type="submit" variant="primary">Agregar</b-button>
      </b-form>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          password: ''
        },
        emailNuevo: ''
      }
    },
    mounted() {
      var modal = document.getElementById("myModal");
      var span = document.getElementsByClassName("close")[0];

      span.onclick = function() {
        modal.style.display = "none";
      }
      window.onclick = function(event) {
        if (event.target == modal) {
          modal.style.display = "none";
        }
      }

    },
    methods: {
      onSubmit(event) {
        event.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onSubmitAgregar(event) {
        event.preventDefault()
        alert(JSON.stringify(this.emailNuevo))
      },
      show(event) {
        event.preventDefault()
        var modal = document.getElementById("myModal");
        modal.style.display = "block";
      }
    }
  }
</script>

<style scoped>
  * {
    padding: 0;
    margin: 0;
    font-family: 'Roboto', sans-serif;
    color: black;
  }

  .padding-0{
    padding-right:0;
    padding-left:0;
}

  .gym-body {
    background-color: #ECDFF4;
    height: 100vh;
  }

  .gym-container {
    border-radius: 20px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }

  .gym-col {
    background-color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    border-radius: 20px 20px 20px 20px;
  }

  .form-container{
    width: 100%;
  }

  h1 {
    text-align: left;
    font-size: 2rem;
    font-weight: 600;
    width: 100%;
    padding: 1rem 0 1rem 1rem;
  }

  .new-gym {
    width: 30%;
    float: right;
    background-color: white;
    border-color: lightgrey;
    color: blueviolet;
  }

  .new-gym:hover {
    background-color: lightgrey;
    border-color: lightgrey;
    color: blueviolet;
  } 

  #new-gym-button{
    padding: 1rem 1rem 0 1rem;
  }

  label {
    text-align: left !important;
    width: 100%;
    padding: .5rem 0 .5rem 0;
  }

  input {
    height: 4rem;
    color: rgb(102, 102, 102)
  }

  .restablecer-button {
    width: 30%;
  }

  .restablecer-button,
  .login-button {
    background-color: #8D2BC0;
    border-color: #8D2BC0;
    color: white;
  }

  .restablecer-button:hover,
  .login-button:hover {
    background-color: #560b7d;
    border-color: #560b7d;
  }

  

  .modal {
    display: none; 
    position: fixed; 
    z-index: 1; 
    left: 0;
    top: 0;
    width: 100%; 
    height: 100%;
    overflow: hidden;
    background-color: rgb(0,0,0); 
    background-color: rgba(0,0,0,0.4);
  }

  .modal-content {
    display: flex;
    background-color: #ffffff;
    margin: 15% auto; 
    padding: 20px;
    border: 1px solid #888;
    width: 40%; 
    border-radius: 16px;
  }

  .close-div {
    display: flex;
    justify-content: right;
    width: 100%;
  }

  .close {
    color: #aaa;
    font-size: 28px;
    font-weight: bold;
    width: auto;
    height: auto;
    padding: .5rem 1rem;
  }

  .close:hover,
  .close:focus {
    color: black;
    text-decoration: none;
    cursor: pointer;
  }

  .restablecer-titulo {
    padding: .5rem 0 2.5rem 0;
  }

  .restablecer-form {
    width: 72%;
    margin: 0 0 4rem 0;
  }

  #input-3 {
    width: 100%;
  }

  #gimnasios{
    width: 80%;
    background-color: #fefefe;
    padding: .5rem .5rem .5rem .5rem;
  }

  .cajahijo1 {
  display: flex;
  padding: 3rem;
  justify-content: space-around;
}

.cajahijo2 {
  background-color: #D2A3DA;
  border-radius: 30px;
  height: auto;
  margin-left: 10%;
  margin-right: 10%;
  padding: 2rem;
}

.cajahijo3 {
  background-color: white;
  border-radius: 20px;
  height: auto;
  margin: 2rem;
  display: flex;
  align-items: center;
  padding: 0 0 0 3rem;
}

.cajahijo4 {
  display: flex;
  flex-direction: column;
  padding:1rem;
}

</style>