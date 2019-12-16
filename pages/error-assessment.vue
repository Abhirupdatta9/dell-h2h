<template>  
    <v-row class="mx-auto my-12">
        <v-col cols="12" >
            <v-row><p class=" mt-12 display-1 font-weight-light" >WELCOME TO OUR SYSTEM ASSESSMENT</p></v-row>
            <v-row class="mb-12">
            <v-col cols="12" class="mb-12">
            <v-card height="50vh" width="80vw" class="mb-12">
                <v-card-title>System Error Assessment</v-card-title>
                <v-form
                    ref="form"
                    v-model="valid"
                    lazy-validation
                >
                    <v-stepper v-model="e1">
                        <v-stepper-header >
                        <v-stepper-step v-for="n in qno" :key="n" :complete="e1 > n" :step="n">Question {{n}}</v-stepper-step>

                        <v-divider></v-divider>

                        
                        </v-stepper-header>

                        <v-stepper-items v-for="question in questions" :key="question">
                        <v-stepper-content  :step="question.num">
                            <v-card
                            class="mx-12 my-6"
                            elevation="1"
                            height="250px"
                            width="70vw"
                            >
                                
                                <v-row
                                    align="center"
                                    justify="start"
                                    class="ml-12"
                                >
                                    <v-col cols="12">
                                    <p class="">{{question.num}}. &nbsp;&nbsp;&nbsp;&nbsp;{{question.ques}}</p>
                                    </v-col>
                                    
                                    <v-col cols="6">
                                    <v-select v-if="question.num == 1"
                                    :items="items"
                                    v-model="formData[question.num - 1]"
                                    label="Select product name"
                                    outlined
                                    ></v-select>
                                    
                                   
                                    <v-radio-group v-else
                                    v-model="formData[question.num - 1]"
                                    mandatory>
                                        <v-radio
                                        color="primary"
                                        
                                        v-for="n in 4"
                                        :key="n"
                                        :label="question.options[n-1]"
                                        :value="question.options[n-1]"
                                        ></v-radio>
                                        <br>
                                    </v-radio-group>
                                    </v-col>
                                </v-row>

                            </v-card>
                            <!-- {{formData}} -->
                            <v-btn
                            class="ml-12"
                            color="primary"
                            v-if="question.num < qno"
                            @click="e1 = question.num+1"
                            >
                            Continue
                            </v-btn>
                            <v-btn class="ml-12" to="/error-assessment-result" @click="submit" v-else color="primary">
                                Submit
                            </v-btn>

                            
                        </v-stepper-content>
                        </v-stepper-items>
                    </v-stepper>
                    
                </v-form>
            </v-card>
            </v-col>
            </v-row>
        </v-col>
        
    </v-row>
       

    
</template>

<script>
import { async } from 'q';
export default {
    data () {
        
        return {
            e1: 0,
            qno: 3,
            formData: [0,0],
            items: ["Faulty", "Slow", "Hang", "Not faulty"],
            questions: [
                {
                    num: 1,
                    ques: "Select your product name from the dropdown",
                    options: ["Faulty", "Slow", "Hang", "Not faulty"],
                },
                {
                    num: 2,
                    ques: "What kind of software problem are you facing?",
                    options: ["Faulty", "Slow", "Hang", "Not faulty"],
                },
                {
                    num: 3,
                    ques: "What kind of hardware problem are you facing?",
                    options: ["Broken", "Battery", "Configuration", "Not faulty"],
                },
                
            ],  
        }
    },
    async asyncData() {
        // items = await this.$axios.get('/order');
        // console.log(items);
    },
    methods: {
        submit() {
            
            // this.$axios.post('/issues',formData);
        }
    }
    
}    
</script>