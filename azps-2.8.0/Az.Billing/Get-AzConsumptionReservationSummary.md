---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: 3b59aaf537c544a53a1e1cccbb09c1964f6662fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727661"
---
# <span data-ttu-id="a54d7-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="a54d7-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="a54d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a54d7-102">SYNOPSIS</span></span>
<span data-ttu-id="a54d7-103">Получение сводки по резервированию для ежедневного или ежемесячного детализации.</span><span class="sxs-lookup"><span data-stu-id="a54d7-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="a54d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a54d7-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a54d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a54d7-105">DESCRIPTION</span></span>
<span data-ttu-id="a54d7-106">Командлет **Get-AzConsumptionReservationSummary** получает сведения о резервировании для ежедневного или ежемесячного гранка.</span><span class="sxs-lookup"><span data-stu-id="a54d7-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="a54d7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a54d7-107">EXAMPLES</span></span>

### <span data-ttu-id="a54d7-108">Пример 1: получение итогов по резервированию с помощью идентификатора заказа на резервирование для ежемесячного детализации</span><span class="sxs-lookup"><span data-stu-id="a54d7-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="a54d7-109">Пример 2: получение сводок резервирования с ИД заказа на резервирование и идентификатором резервирования для ежемесячного детализации</span><span class="sxs-lookup"><span data-stu-id="a54d7-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain monthly -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20170901
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20170901
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  288
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  9/1/2017 12:00:00 AM
UsedHour:  288
```

### <span data-ttu-id="a54d7-110">Пример 3: получение итогов по резервированию с помощью идентификатора заказа на резервирование для ежедневного интервала в указанном диапазоне дат</span><span class="sxs-lookup"><span data-stu-id="a54d7-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="a54d7-111">Пример 4: получение сводок резервирования с ИД заказа на резервирование и идентификатором резервирования для ежедневного интервала в указанном диапазоне дат</span><span class="sxs-lookup"><span data-stu-id="a54d7-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationSummary -Grain daily -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
AvgUtilizationPercentage:  100
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640/providers/Microsoft.Consumption/reservationSummaries/20171101
MaxUtilizationPercentage:  100
MinUtilizationPercentage:  100
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171101
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
Type:  Microsoft.Consumption/reservationSummaries
UsageDate:  11/1/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="a54d7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a54d7-112">PARAMETERS</span></span>

### <span data-ttu-id="a54d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a54d7-113">-DefaultProfile</span></span>
<span data-ttu-id="a54d7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a54d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a54d7-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a54d7-115">-EndDate</span></span>
<span data-ttu-id="a54d7-116">Конечные данные (гггг-мм-дд в формате UTC) сводки резервирований, которые требуются только для ежедневного детализации.</span><span class="sxs-lookup"><span data-stu-id="a54d7-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54d7-117">-Зернистость</span><span class="sxs-lookup"><span data-stu-id="a54d7-117">-Grain</span></span>
<span data-ttu-id="a54d7-118">Временные Гранки сводки резервирования могут быть ежедневно или ежемесячными.</span><span class="sxs-lookup"><span data-stu-id="a54d7-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: daily, monthly

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54d7-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a54d7-119">-ReservationId</span></span>
<span data-ttu-id="a54d7-120">Идентификатор резервирования в заказе на резервирование.</span><span class="sxs-lookup"><span data-stu-id="a54d7-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="a54d7-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a54d7-121">-ReservationOrderId</span></span>
<span data-ttu-id="a54d7-122">Идентификатор покупки резервирования.</span><span class="sxs-lookup"><span data-stu-id="a54d7-122">The identifier of a reservation purchase.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54d7-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a54d7-123">-StartDate</span></span>
<span data-ttu-id="a54d7-124">Начальные данные (гггг-мм-дд в формате UTC) сводки резервирований, которые требуются только для ежедневного детализации.</span><span class="sxs-lookup"><span data-stu-id="a54d7-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a54d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54d7-125">CommonParameters</span></span>
<span data-ttu-id="a54d7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a54d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54d7-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a54d7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54d7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a54d7-128">INPUTS</span></span>

### <span data-ttu-id="a54d7-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="a54d7-129">None</span></span>

## <span data-ttu-id="a54d7-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a54d7-130">OUTPUTS</span></span>

### <span data-ttu-id="a54d7-131">Microsoft. Azure. Commands. потребление. Models. PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="a54d7-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="a54d7-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a54d7-132">NOTES</span></span>

## <span data-ttu-id="a54d7-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a54d7-133">RELATED LINKS</span></span>
