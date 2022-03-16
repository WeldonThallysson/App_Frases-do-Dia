import React from 'react';
import {Text,View,StyleSheet,TouchableOpacity,Image,Alert} from 'react-native';

//Essa const vai executar a logica das frases 
const Gera_Frase = () => {
    var numeroaleatorio = Math.random();

    numeroaleatorio = Math.floor(numeroaleatorio * 10);

    var frases = Array();
    frases[0] = 'Acorde Com Vontade de Viver';
    frases[1] = 'Você é Inteligente, por baixar esse App';
    frases[2] = 'Tem coisas que Você consegue e outras conquista';
    frases[3] = 'As Aves São tão Belas ja Parou para analisa-las como voão?';
    frases[4] = 'Você consegue ver Deus em Todas as Coisas,apenas queira enxergar'
    frases[5] = 'Não seja tão timido,as pessoas estão esperando Você se abrir para elas';
    frases[6] = 'Você e alguem no coração de Deus';
    frases[7] = 'tudo passará menos as palavras dele Jesus ';
    frases[8] = 'É tudo uma questão de Tempo, esse deserto vai passar'
    frases[9] = 'Se Deus é por Nos quem será contra nós?';
   
   var frase_Escolhida = frases[ numeroaleatorio ];

   Alert.alert(frase_Escolhida);
 }


// Essa const vai exibir tudo no aplicativo

const Aplicativo_Frases_do_Dia = () => {
   return(

       <View style={Estilo.ViewC}>
          <Image source={require('./imgs/logo.png')}/>

         <TouchableOpacity style={Estilo.Botao} onPress={Gera_Frase}>
            <Text style={Estilo.TextoBotao}>Nova Frase</Text>
         </TouchableOpacity>

       </View>

      )

};

export default Aplicativo_Frases_do_Dia;

const Estilo = StyleSheet.create({
    ViewC:{
      flex:1,
      backgroundColor:'white',
      justifyContent:'center',
      alignItems:'center'
    },

    Botao:{
      width: 140,
      padding:10,
      marginTop: 20,
      backgroundColor:'green',
      borderColor:'grey',
      borderWidth: 1,
      borderRadius: 3

    },
    TextoBotao:{
     color:'white',
     fontSize:15,
     fontWeight:"bold",
     textAlign:'center'

    },

});
