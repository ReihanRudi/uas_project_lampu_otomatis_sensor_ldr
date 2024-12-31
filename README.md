# Project Lampu Otomatis Sensor Ldr
# Deskripsi
Lampu otomatis yang menggunakan sensor cahaya, khususnya Light Dependent Resistor (LDR), dirancang untuk mengatur pencahayaan secara otomatis berdasarkan intensitas cahaya di sekitarnya. Dengan teknologi ini, lampu otomatis berbasis sensor LDR memberikan solusi efisien dan praktis untuk pencahayaan modern
# Komponen (Alat & Bahan):
• Arduino uno r3 dip = 1 Unit •Sensor ldr = 1 Unit • Led 5mm merah = 1 Unit • Power suppy = 1 Unit 
• Resistor = 1 Unit • Relay = 1 Unit  • Lampu AC = 1 Unit
# Skema Sirkuit:
![gambar skema sirkuit ardiouno](https://github.com/user-attachments/assets/c0aa20a5-f198-4e6c-a623-5d1262c6b7ba)
# Code Program
``` int ldr = A0;
int led = 6;
int nilai;

void setup() {
  pinMode(led, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  nilai = analogRead(ldr);
  Serial.print("Nilai LDR: ");
  Serial.println(nilai);

  if (nilai < 700) {
    digitalWrite(led, LOW);
  }
  else {
    digitalWrite(led, HIGH);
  }

 }
