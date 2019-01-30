metadata {
 	definition (name: "webCoRE Traffic Info", namespace: "SmartThings", author: "Brian Roy") {
    capability "Carbon Dioxide Measurement"
    capability "Battery"
    attribute "carbonDioxide","number"
    attribute "battery","number"
    command "setCommuteTime"
    command "setBatteryLevel"
     }
 	tiles {
 		valueTile("carbonDioxide", "device.carbonDioxide", width: 3, height: 1, canChangeBackground: true) {
 			state "default", label:'${currentValue}'
 		}
 		valueTile("battery", "device.battery", width: 3, height: 1) {
 			state "default", label:'${currentValue}'
 		}
 		main(["carbonDioxide"])
 		details(["carbonDioxide","battery"])
 	}
 }

def setBatteryLevel(newLevel) {
	log.debug "Executing 'setBatteryLevel'"
	sendEvent(name: "battery", value: newLevel, isStateChange: true)
}
 def setCommuteTime (param1) {
    sendEvent("name":"carbonDioxide", "value":param1)
}
