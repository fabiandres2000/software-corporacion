<template lang="">
    <v-container fluid class="down-top-padding">
      <v-row>
        <v-col cols="12" lg="12">
          <v-card>
            <v-card-text class="text-left p-5">
                <h2 style="color: #2c4a73; font-weight: bold">Test Vocacional</h2>
                <br>
                <div class="row">
                    <div class="col-9">
                        <h3><span span class="theme_color">Bienvenido(a): {{estudiante.nombre}}</span></h3>
                    </div>
                    <div class="col-3" style="text-align: right">
                    
                    </div>
                </div>
                <hr>
                <div class="row">
                    <div class="col-12">
                        <h5 style="font-size: 21px; text-align: justify;">Lee atentamente cada pregunta y responde a cada una de ellas con toda sinceridad sin omitir ninguna.</h5>
                        <h5 style="font-size: 21px; text-align: justify;">Recuerda que no hay respuestas buenas o malas, ya que cada persona tiene gustos diferentes</h5>
                    </div>
                </div>
                <div class="row">
                    <div class="col-lg-12" v-if="paso == 1">
                    <form ref="form_paso_1" @submit.prevent="guardar_respuesta_vocacional('form_paso_1')">
                        <div class="row">
                            <div class="col-md-12">
                                <div class="tab_menu">
                                    <div class="container">
                                        <table id="customers">
                                            <thead>
                                                <tr>
                                                    <th>Pregunta</th>
                                                    <th>Si</th>
                                                    <th>No</th>
                                                </tr>
                                            </thead>
                                            <tbody>
                                                <tr>
                                                    <td>1.	¿Aceptarías trabajar escribiendo artículos en la sección económica de un diario? </td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_1" name="preg_1"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_1" name="preg_1"></td>
                                                </tr>
                                                <tr>
                                                    <td>2.	¿Te ofrecerías para organizar la despedida de soltero de uno de tus amigos?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_2" name="preg_2"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_2" name="preg_2"></td>
                                                </tr>
                                                <tr>
                                                    <td>3.	¿Te gustaría dirigir un proyecto para diseñar barrios en tu provincia?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_3" name="preg_3"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_3" name="preg_3"></td>
                                                </tr>
                                                <tr>
                                                    <td>4.	¿Ante una frustración siempre opones un pensamiento positivo?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_4" name="preg_4"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_4" name="preg_4"></td>
                                                </tr>
                                                <tr>
                                                    <td>5.	¿Te dedicarías a ayudar a personas accidentadas o atacadas por asaltantes?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_5" name="preg_5"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_5" name="preg_5"></td>
                                                </tr>
                                                <tr>
                                                    <td>6.	¿Cuando eras chico, te interesaba saber cómo estaban construidos tus juguetes?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_6" name="preg_6"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_6" name="preg_6"></td>
                                                </tr>
                                                <tr>
                                                    <td>7.	¿Te interesan más los misterios de la naturaleza que los secretos de la tecnología?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_7" name="preg_7"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_7" name="preg_7"></td>
                                                </tr>
                                                <tr>
                                                    <td>8.	¿Escuchas atentamente los problemas que te plantean tus amigos?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_8" name="preg_8"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_8" name="preg_8"></td>
                                                </tr>
                                                <tr>
                                                    <td>9.	¿Te ofrecerías para explicar a tus compañeros un determinado tema que ellos no entendieron?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_9" name="preg_9"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_9" name="preg_9"></td>
                                                </tr>
                                                <tr>
                                                    <td>10.	 ¿Sos exigente y crítico con tu equipo de trabajo?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_10" name="preg_10"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_10" name="preg_10"></td>
                                                </tr>
                                                <tr>
                                                    <td>11.	¿Te atrae armar rompecabezas o puzzles?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_11" name="preg_11"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_11" name="preg_11"></td>
                                                </tr>
                                                <tr>
                                                    <td>12.	¿Puedes establecer la diferencia conceptual entre macroeconomía y microeconomía?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_12" name="preg_12"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_12" name="preg_12"></td>
                                                </tr>
                                                <tr>
                                                    <td>13.	¿Usar uniforme te hace sentir distinto, importante?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_13" name="preg_13"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_13" name="preg_13"></td>
                                                </tr>
                                                <tr>
                                                    <td>14. ¿Participarías de una investigación sobre la violencia en el fútbol?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_14" name="preg_14"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_14" name="preg_14"></td>
                                                </tr>
                                                <tr>
                                                    <td>15. ¿Organizas tu dinero de manera que te alcance hasta el próximo cobro?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_15" name="preg_15"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_15" name="preg_15"></td>
                                                </tr>
                                                <tr>
                                                    <td>16.	¿Convences fácilmente a otras personas sobre la validez de tus argumentos?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_16" name="preg_16"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_16" name="preg_16"></td>
                                                </tr>
                                                <tr>
                                                    <td>17.	¿Estás informado sobre los nuevos descubrimientos que se están realizando sobre la Teoría del Big Bang?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_17" name="preg_17"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_17" name="preg_17"></td>
                                                </tr>
                                                <tr>
                                                    <td>18. Ante una situación de emergencia, ¿actuás rápidamente?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_18" name="preg_18"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_18" name="preg_18"></td>
                                                </tr>
                                                <tr>
                                                    <td>19.	¿Cuando tenés que resolver un problema matemático, perseverás hasta encontrar la solución?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_19" name="preg_19"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_19" name="preg_19"></td>
                                                </tr>
                                                <tr>
                                                    <td>20.	¿Si te convocara tu club preferido para dirigir un campo de deportes, aceptarías?</td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="si" id="preg_20" name="preg_20"></td>
                                                    <td style="text-align: center"><input type="radio" class="form_control" value="no" id="preg_20" name="preg_20"></td>
                                                </tr>
                                            </tbody>
                                        </table>
                                        <div class="row" style="margin-top: 30px">			
                                            <div class="col-3"></div>
                                            <div class="col-6" style="text-align:center" >
                                                <button style="width: 100%; color: white" type="submit"  class="btn btn-success">Siguiente</button>
                                            </div>
                                            <div class="col-3"></div>	
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </form>
                </div>
            </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
</template>
<script>
import * as estudianteService from "../../servicios/estudiante_service"
//import * as practicasService from "../../servicios/practicas"
//import store from "../../store";
import $ from "jquery";
  
export default {
    name: "Vocacional",
    data: () => ({  
        id_estudiante: "",
        estudiante: {
            nombre: "",
        },
        paso: 1
    }),
    components: {},
    mounted() {
        this.id_estudiante = this.$session.get("id_estudiante");
        this.consultar_estudiante();
        this.verificar_paso_vocacional();
    },
    methods: {
        async consultar_estudiante(){
            await estudianteService.consultar_estudiante(this.id_estudiante).then(respuesta => {
                this.estudiante = respuesta.data.estudiante;
            });
        },
        async verificar_paso_vocacional(){
            await estudianteService.verificar_paso_vocacional(this.id_estudiante).then(respuesta => {
                this.paso = respuesta.data.paso;
                $('html, body').animate({scrollTop:400}, 1000); 
            });
        },
        async guardar_respuesta_vocacional(paso_form){
            const formData = new FormData(this.$refs[paso_form]); 
            const data = {};
            for (let [key, val] of formData.entries()) {
                Object.assign(data, { [key]: val })
            }
            
            Object.assign(data, { 'id_estudiante':  this.id_estudiante });
            Object.assign(data, { 'paso':  this.paso });

            await estudianteService.guardar_respuesta_vocacional(data).then(respuesta => {
                if(respuesta.data.success == 1){
                    for (let index = 1; index <= 20; index++) {
                        $('input[name=preg_'+index+']').prop('checked',false);
                    }
                    this.verificar_paso_vocacional();
                }else{
                    this.$swal('Error...', respuesta.data.respuesta, 'error');
                }
            });

            
        },
    }
  }
</script>
<style>
    label{
        color: #2c4a73;
        font-weight: bold;
    }

    #customers {
        font-family: Arial, Helvetica, sans-serif;
        border-collapse: collapse;
        width: 100%;
    }

    #customers td, #customers th {
        border: 1px solid #ddd;
        padding: 8px;
    }

    #customers tr:nth-child(even){background-color: #f2f2f2;}

    #customers tr:hover {background-color: #ddd;}

    #customers th {
        padding-top: 12px;
        padding-bottom: 12px;
        text-align: center;
        background-color: #2C4A73;
        color: white;
    }

    .cen {
        text-align: center;
    }

    input[type=radio] {
        border: 0px;
        height: 1em;
    }
</style>