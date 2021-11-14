# Kalman-filtering
ADC Kalman filtering

تابع میانگین گیری ADC  به روش کالمن توسط معادله یک جمله ای بسیار دقیق با تغییر مقدار  K میتوان لختی خروجی را تغییر داد . 
uint32_t average_Adc(void)
{  
       int K;
       value=adc_value[0];
       NEW=value;
       value=K*OLD+(1-K)*NEW;
       OLD=NEW;
       return value;
}
