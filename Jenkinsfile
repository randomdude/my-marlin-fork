node("arduino")
{
	checkout scm

	sh "arduino-cli core update-index"
	sh "arduino-cli core install arduino:avr"
	sh "arduino-cli lib install u8glib"
	sh "arduino-cli compile --verbose --fqbn arduino:avr:mega:cpu=atmega2560 Marlin/Marlin.ino"

	archiveArtifacts 'Marlin/build/arduino.avr.mega/*.hex' 
}