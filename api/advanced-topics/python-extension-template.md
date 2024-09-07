
import React from 'react';
import { createAppContainer } from 'react-navigation';
import { createStackNavigator } from 'react-navigation-stack';
import HomeScreen from '../screens/HomeScreen';
import DetailsScreen from '../screens/DetailsScreen';

const AppNavigator = createStackNavigator(
  {
      Home: HomeScreen,
          Details: DetailsScreen,
            },
              {
                  initialRouteName: 'Home',
                    }
                    );

                    export default createAppContainer(AppNavigator);
                    import React from 'react';
                    import { View, Text, Button, StyleSheet } from 'react-native';
                    import { Video } from 'react-native-video';

                    const HomeScreen = ({ navigation }) => {
                      return (
                          <View style={styles.container}>
                                <Text style={styles.title}>Bienvenido a Mundo Yamila Travel</Text>
                                      <Video
                                              source={{ uri: 'URL_DEL_VIDEO' }}
                                                      style={styles.backgroundVideo}
                                                              controls
                                                                    />
                                                                          <Button
                                                                                  title="Ver detalles"
                                                                                          onPress={() => navigation.navigate('Details')}
                                                                                                />
                                                                                                    </View>
                                                                                                      );
                                                                                                      };

                                                                                                      const styles = StyleSheet.create({
                                                                                                        container: {
                                                                                                            flex: 1,
                                                                                                                justifyContent: 'center',
                                                                                                                    alignItems: 'center',
                                                                                                                      },
                                                                                                                        title: {
                                                                                                                            fontSize: 20,
                                                                                                                                fontWeight: 'bold',
                                                                                                                                  },
                                                                                                                                    backgroundVideo: {
                                                                                                                                        width: '100%',
                                                                                                                                            height: 200,
                                                                                                                                              },
                                                                                                                                              });

                                                                                                                                              export default HomeScreen;
                                                                                                                                              import React from 'react';
                                                                                                                                              import { View, Text, StyleSheet } from 'react-native';
                                                                                                                                              import MapView from 'react-native-maps';

                                                                                                                                              const DetailsScreen = () => {
                                                                                                                                                return (
                                                                                                                                                    <View style={styles.container}>
                                                                                                                                                          <Text style={styles.title}>Detalles del Viaje</Text>
                                                                                                                                                                <MapView
                                                                                                                                                                        style={styles.map}
                                                                                                                                                                                initialRegion={{
                                                                                                                                                                                          latitude: 21.17,
                                                                                                                                                                                                    longitude: -86.85,
                                                                                                                                                                                                              latitudeDelta: 0.0922,
                                                                                                                                                                                                                        longitudeDelta: 0.0421,
                                                                                                                                                                                                                                }}
                                                                                                                                                                                                                                      />
                                                                                                                                                                                                                                          </View>
                                                                                                                                                                                                                                            );
                                                                                                                                                                                                                                            };

                                                                                                                                                                                                                                            const styles = StyleSheet.create({
                                                                                                                                                                                                                                              container: {
                                                                                                                                                                                                                                                  flex: 1,
                                                                                                                                                                                                                                                      justifyContent: 'center',
                                                                                                                                                                                                                                                          alignItems: 'center',
                                                                                                                                                                                                                                                            },
                                                                                                                                                                                                                                                              title: {
                                                                                                                                                                                                                                                                  fontSize: 20,
                                                                                                                                                                                                                                                                      fontWeight: 'bold',
                                                                                                                                                                                                                                                                        },
                                                                                                                                                                                                                                                                          map: {
                                                                                                                                                                                                                                                                              width: '100%',
                                                                                                                                                                                                                                                                                  height: '100%',
                                                                                                                                                                                                                                                                                    },
                                                                                                                                                                                                                                                                                    });

                                                                                                                                                                                                                                                                                    export default DetailsScreen;
                                                                                                                                                                                                                                                                                    import React from 'react';
                                                                                                                                                                                                                                                                                    import AppNavigator from './src/navigation/AppNavigator';

                                                                                                                                                                                                                                                                                    const App = () => {
                                                                                                                                                                                                                                                                                      return <AppNavigator />;
                                                                                                                                                                                                                                                                                      };

                                                                                                                                                                                                                                                                                      export default App;
