#include "usbd_cdc_if.h"
#include "adc.h"
#include <stdio.h>

extern USBD_HandleTypeDef hUsbDeviceFS;

void Send_ADC_Value_Over_USB(uint32_t adc_value)
{
  char buffer[10];
  snprintf(buffer, sizeof(buffer), "%lu\n", adc_value);  // Format value

  // Transmit via USB CDC
  CDC_Transmit_FS((uint8_t*)buffer, strlen(buffer));
}
