#png('plot1.png', width = 480, height = 480)
hist(rawData$GlobalActivePower, col = 'red',
     main = 'Global Active Power',
     xlab = 'Global Active Power (kilowatts)')# Project-


     #png('plot2.png', width = 480, height = 480)
plot(x = rawData$DateTime, y = rawData$GlobalActivePower, 
     type = 'l', xlab = NA, ylab = 'Global Active Power (kilowatts)')

     #png('plot3.png', width = 480, height = 480)
plot(x = rawData$DateTime, y = rawData$SubMetering1, type = 'l',
     xlab = NA, ylab = 'Energy sub metering')
lines(x = rawData$DateTime, y = rawData$SubMetering2, col = 'red')
lines(x = rawData$DateTime, y = rawData$SubMetering3, col = 'blue')
legend('topright', 
       legend = c('Sub_metering_1', 'Sub_metering_2', 'Sub_metering_3'),
       col = c('black', 'red', 'blue'),
       lwd = 1)


       #png('plot4.png', width = 480, height = 480)
par(mfrow = c(2, 2)) 
  #plots from left to right, top to bottom (since you used mfrow vs mfcol)

#plot 4a = plot 1
plot(x = rawData$DateTime, y = rawData$GlobalActivePower, 
     type = 'l', xlab = NA, ylab = 'Global Active Power')

#plot 4b
plot(x = rawData$DateTime, y = rawData$Voltage, 
     type = 'l', xlab = 'datetime', ylab = 'Voltage')

#plot 4c = plot 3
plot(x = rawData$DateTime, y = rawData$SubMetering1, type = 'l',
     xlab = NA, ylab = 'Energy sub metering')
lines(x = rawData$DateTime, y = rawData$SubMetering2, col = 'red')
lines(x = rawData$DateTime, y = rawData$SubMetering3, col = 'blue')
legend('topright', 
       legend = c('Sub_metering_1', 'Sub_metering_2', 'Sub_metering_3'),
       col = c('black', 'red', 'blue'),
       lwd = 1, bty = 'n')

#plot 4d
plot(x = rawData$DateTime, y = rawData$GlobalReactivePower, type = 'l',
     xlab = 'datetime', ylab = 'Global_reactive_power')
