//+------------------------------------------------------------------+
//|                                     SimpleAlgoV3Pro_Header.mqh     |
//+------------------------------------------------------------------+
#include <Trade/Trade.mqh>
CTrade trade;

// Stop Loss Types
enum ENUM_STOP_TYPE
{
    STOP_ATR,           // ATR
    STOP_FIXED,         // Fixed Percent
    STOP_DYNAMIC,       // Dynamic
    STOP_CHANDELIER,    // Chandelier
    STOP_SUPERTREND     // SuperTrend
};

// Exit Types
enum ENUM_EXIT_TYPE
{
    EXIT_TPS_ONLY,      // TPs Only
    EXIT_SIGNAL_ONLY,   // Next Signal Only
    EXIT_BOTH           // Both
};

// Global Variables
int ATRHandle;
int SMA8Handle;
int SMA9Handle;
int SMA13Handle;
bool TP1Reached = false;
bool TP2Reached = false;
bool TP3Reached = false;
double LastTP1, LastTP2, LastTP3, LastStop;