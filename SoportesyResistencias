//+------------------------------------------------------------------+
//|                                         soportesresistencias.mq4 |
//|                                  Copyright 2025, MetaQuotes Ltd. |
//|                                             https://www.mql5.com |
//+------------------------------------------------------------------+
#property copyright "Copyright 2025, MetaQuotes Ltd."
#property link      "https://www.mql5.com"
#property version   "1.00"
#property strict
//+------------------------------------------------------------------+
//| Script program start function                                    |
//+------------------------------------------------------------------+
void OnStart()
  {
//---
   
   Print("El precio más alto de los últimos 5 días es: "+ResistenciaUltimosDias());
   
   DibujarResistencia(ResistenciaUltimosDias());
  }
//+------------------------------------------------------------------+

double ResistenciaUltimosDias()
{
   int NumVelaPrecioMasAlto = iHighest(NULL,PERIOD_D1,MODE_HIGH,5,0);
   
   double PrecioMaximo = iClose(NULL,PERIOD_D1,NumVelaPrecioMasAlto);
   
   return PrecioMaximo;
}

void DibujarResistencia(double Precio)
{
   ObjectCreate(0,"ResistenciaDiaria",OBJ_HLINE,0,0,Precio);
