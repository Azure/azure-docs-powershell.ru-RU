---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionpricesheet
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionPriceSheet.md
ms.openlocfilehash: e52c096d1c5cf2c012952a89a922b7d3719c3f20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727669"
---
# Get-AzConsumptionPriceSheet

## КРАТКИй обзор
Получение прайс – листов для подписки.

## Максимальное

```
Get-AzConsumptionPriceSheet [-BillingPeriodName <String>] [-ExpandMeterDetail] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## NОПИСАНИЕ
Командлет **Get-AzConsumptionPriceSheet** получает листы цен для подписки.

## ИЛЛЮСТРИРУЮТ

### Пример 1: получение прайс – листов
```powershell
PS C:\> Get-AzConsumptionPriceSheet
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### Пример 2: получение прайс – листов с развернутым MeterDetails
```powershell
PS C:\> Get-AzConsumptionPriceSheet -ExpandMeterDetail
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterDetails:  MeterCategory:  Virtual Machines
                             MeterLocation:  US North Central
                             MeterName:  Compute Hours
                             MeterSubCategory:  Standard_D11_v2 VM_Promo (Windows)
                             Unit:  Hours
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

### Пример 3: получение прайс – листов для BillingPeriodName
```powershell
PS C:\> Get-AzConsumptionPriceSheet -BillingPeriodName 201712
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  46367D67-1E4C-4ED4-8267-4477083F581C
              PartNumber:  AAA-53590
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.37
```

### Пример 4: получение первых 5 записей прайс – листов
```powershell
PS C:\> Get-AzConsumptionPriceSheet -Top 5
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601/providers/Microsoft.Consumption/pricesheets/default
Name:  default
Type:  Microsoft.Consumption/pricesheets
Pricesheets:  BillingPeriodId:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Billing/billingPeriods/20180601
              CurrencyCode:  USD
              IncludedQuantity:  0
              MeterId:  BACDDD36-2C2C-46BB-8CFA-D13C15EE4A7E
              PartNumber:  AAA-49135
              UnitOfMeasure:  10 Hours
              UnitPrice:  1.33
```

## ПАРАМЕТРЫ

### -BillingPeriodName
Название определенного расчетного периода, чтобы получить прайс-листы, связанные с.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpandMeterDetail
Разворачивать прайсные листы, основываясь на MeterDetails.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Top
Определение максимального числа возвращаемых записей.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction. Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ВХОДНЫЕ данные

### Ничего

## НАПРЯЖЕНИЕ

### Microsoft. Azure. Commands. потребление. Models. PSPriceSheet

## Пуск

## ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ
