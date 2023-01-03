# estufa-hortalicas
Projeto eletrônico da Estufa de Hortaliças - Desafio DIO

Circuito disponível em:

https://www.tinkercad.com/things/fCKRJu7rRL7-fantastic-albar/editel?tenant=circuits

***
// Estufa de hortaliças

int pinTMP = 0;
int pinVent = 7;
int pinLed = 8;

int valorTMP = 0;

void setup()
{
  pinMode(pinTMP, OUTPUT);
  pinMode(pinVent, OUTPUT);
}

void loop()
{
  valorTMP = analogRead(pinTMP);
  
  if (valorTMP >= 300) {
  	digitalWrite(pinVent, HIGH);  
  } else {
    digitalWrite(pinVent, LOW); 
  }
  
  if (valorTMP > 500) {
  	digitalWrite(pinLed, HIGH); 
  } else {
    digitalWrite(pinLed, LOW);
  }
  
  delay(1000);
}
