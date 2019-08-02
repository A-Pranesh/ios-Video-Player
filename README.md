# ios-Video-Player
import React from 'react';
import { StyleSheet, View, Text, Image, ImageBackground } from 'react-native';
 
 export default class VideoPlayer extends React.Component {
 	render() {
 		const playIcon = require('./images/play.png');
		const volumeIcon = require('./images/sound.png');
		const hdIcon = require('./images/hd-sign.png');
		const fullScreenIcon = require('./images/full-screen.png');
		const remoteImage = {
  			url: `https://farm5.staticflickr.com/4702/24825836327_bb2e0fc39b_b.jpg`};
  		return (
  				<View style = {styles.appContainer}>
  					<ImageBackground source = {remoteImage} style = {styles.videoContainer} 
  					resizeMode = 'contain' >
  						<View style = {styles.controlsContainer}>
  							<Image source = {playIcon} style = {styles.icon}  />
  							<Image source  = {volumeIcon} style = {styles.icon}  />
  							<View style = {styles.progress}>
  								<View style = {styles.progressBar} />
  							</View>
  							<Image source = {hdIcon} style = {styles.icon}  />
  							<Image source = {fullScreenIcon} style = {styles.icon}  />
  						</View>
  					</ImageBackground>
  				</View>
  			);
 	}
 }


 const styles = StyleSheet.create({
 	appContainer: {
 		flex: 2,
 	},
 	videoContainer: {
 		flex: 1,
 		justifyContent: 'center',
 		alignItems: 'center',
 		flexDirection: 'row',
 		backgroundColor: 'black',
 	},
 	controlsContainer: {
 		flex: 1,
 		flexDirection: 'row',
 		padding: 5,
 		backgroundColor: 'grey',
 		marginTop: 180,
 	},
 	icons: {
 		height: 15,
 		width: 15,
 		marginLeft: 5,
 		marginRight: 5,
 	},
 	progress: {
 		backgroundColor: 'black',
 		borderRadius: 7,
 		height: 15,
 		margin: 5,
 		flex: 1,
 	},
 	progressBar: {
 		backgroundColor: 'red',
 		borderRadius: 5,
 		margin: 3,
 		height: 10,
 		width: 150,
 	},
 });
