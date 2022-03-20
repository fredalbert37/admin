<template>
  <div class="q-pa-md row justify-around items-center q-gutter-md">
    <div class="col-xs-12 col-sm-2 col-md-2 col-lg-2 col-xl-2 q-mt-md">
      <q-card class="my-card bg-purple text-dark flex justify-center">
        <q-card-section>
          <div class="text-h5 flex items-center justify-center">
            <q-icon color="primary" class="q-pa-xs rounded-borders" name="fas fa-user"></q-icon>
            <span  class="q-ml-sm"
            style="vertical-align: text-bottom;"
            >2600</span>
          </div>
          <div class="text-subtitle2 text-center">Nuevos Usuarios</div>
        </q-card-section>
        <q-card-section class="q-my-auto">
          <span style="color:#00C853">%35+</span>
          <q-icon class="q-ml-xs q-mb-xs" color="green" name="fas fa-arrow-up"></q-icon>
        </q-card-section>
      </q-card>
    </div>
    <div class="col-xs-12 col-sm-2 col-md-2 col-lg-2 col-xl-2 q-mt-md">
      <q-card class="my-card bg-purple text-dark flex justify-center">
        <q-card-section>
          <div class="text-h5 flex items-center justify-center">
            <q-icon color="primary" class="q-pa-xs rounded-borders" name="fas fa-shopping-bag"></q-icon>
            <span  class="q-ml-sm"
            style="vertical-align: text-bottom;"
            >500</span>
          </div>
          <div class="text-subtitle2 text-center">Compras del mes</div>
        </q-card-section>
        <q-card-section class="q-my-auto">
          <span style="color:#00C853">%2.1+</span>
          <q-icon class="q-ml-xs q-mb-xs" color="green" name="fas fa-arrow-up"></q-icon>
        </q-card-section>
      </q-card>
    </div>

    <div class="col-xs-12 col-sm-2 col-md-2 col-lg-2 col-xl-2 q-mt-md">
      <q-card class="my-card bg-purple text-dark flex justify-center">
        <q-card-section>
          <div class="text-h5 flex items-center justify-center">
            <q-icon color="primary" class="q-pa-xs rounded-borders" name="fas fa-eye"></q-icon>
            <span  class="q-ml-sm"
            style="vertical-align: text-bottom;"
            >16,000</span>
          </div>
          <div class="text-subtitle2 text-center">Visitas a la pagina</div>
        </q-card-section>
        <q-card-section class="q-my-auto">
          <span style="color:#F44336">%0.5+</span>
          <q-icon class="q-ml-xs q-mb-xs" color="red" name="fas fa-arrow-down"></q-icon>
        </q-card-section>
      </q-card>
    </div>

    <div class="col-xs-12 col-sm-2 col-md-2 col-lg-2 col-xl-2 q-mt-md">
      <q-card class="my-card bg-purple text-dark flex justify-center">
        <q-card-section>
          <div class="text-h5 flex items-center justify-center">
            <q-icon color="primary" class="q-pa-xs rounded-borders" name="fas fa-dollar-sign"></q-icon>
            <span  class="q-ml-sm"
            style="vertical-align: text-bottom;"
            >15,301</span>
          </div>
          <div class="text-subtitle2 text-center">Ingresos del mes</div>
        </q-card-section>
        <q-card-section class="q-my-auto">
          <span style="color:#00C853">%17.3+</span>
          <q-icon class="q-ml-xs q-mb-xs" color="green" name="fas fa-arrow-up"></q-icon>
        </q-card-section>
      </q-card>
    </div>
      
    
  </div> 
  
</template>

<script>

export default {
  name: 'Home',
  components: {
    
  }
}
</script>
