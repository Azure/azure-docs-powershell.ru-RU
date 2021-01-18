---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationsummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationSummary.md
ms.openlocfilehash: a76254f1aeb369e6f93ed8edccfd6f74ff79ceb0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519770"
---
# <span data-ttu-id="ec813-101">Get-AzConsumptionReservationSummary</span><span class="sxs-lookup"><span data-stu-id="ec813-101">Get-AzConsumptionReservationSummary</span></span>

## <span data-ttu-id="ec813-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec813-102">SYNOPSIS</span></span>
<span data-ttu-id="ec813-103">Получать сводки по резервированиям за день или за каждый месяц.</span><span class="sxs-lookup"><span data-stu-id="ec813-103">Get reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="ec813-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec813-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationSummary -Grain <String> -ReservationOrderId <String> [-ReservationId <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec813-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec813-105">DESCRIPTION</span></span>
<span data-ttu-id="ec813-106">Cmdlet **Get-AzConsumptionReservationSummary** получает сводки резервирования для суточного или ежемесячного зерна.</span><span class="sxs-lookup"><span data-stu-id="ec813-106">The **Get-AzConsumptionReservationSummary** cmdlet gets reservation summaries for daily or monthly grain.</span></span>

## <span data-ttu-id="ec813-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec813-107">EXAMPLES</span></span>

### <span data-ttu-id="ec813-108">Пример 1. Получить сводки по резервированиям с ид заказа на резервирование для ежемесячного зерна</span><span class="sxs-lookup"><span data-stu-id="ec813-108">Example 1: Get reservation summaries with reservation order Id for monthly grain</span></span>
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

### <span data-ttu-id="ec813-109">Пример 2. Получите сводки по резервированиям с ИД заказа на резервирование и ид резервирования для ежемесячного зерна</span><span class="sxs-lookup"><span data-stu-id="ec813-109">Example 2: Get reservation summaries with reservation order Id and reservation Id for monthly grain</span></span>
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

### <span data-ttu-id="ec813-110">Пример 3. Получить сводки по резервированию с ид заказа на резервирование для суточного диапазона дат</span><span class="sxs-lookup"><span data-stu-id="ec813-110">Example 3: Get reservation summaries with reservation order Id for daily grain provided date range</span></span>
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

### <span data-ttu-id="ec813-111">Пример 4. Получите сводки по резервированию с помощью ИД заказа на резервирование и ИД резервирования для ежедневного зернистого диапазона дат</span><span class="sxs-lookup"><span data-stu-id="ec813-111">Example 4: Get reservation summaries with reservation order Id and reservation Id for daily grain provided date range</span></span>
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

## <span data-ttu-id="ec813-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec813-112">PARAMETERS</span></span>

### <span data-ttu-id="ec813-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec813-113">-DefaultProfile</span></span>
<span data-ttu-id="ec813-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec813-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec813-115">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ec813-115">-EndDate</span></span>
<span data-ttu-id="ec813-116">Конечные данные сводки по резервированиям (ДДГ-ММ-ММ в UTC), необходимые только для ежедневного зерна.</span><span class="sxs-lookup"><span data-stu-id="ec813-116">The end data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="ec813-117">-Grain</span><span class="sxs-lookup"><span data-stu-id="ec813-117">-Grain</span></span>
<span data-ttu-id="ec813-118">Время, определенное в сводке резервирования, может быть ежедневно или ежемесячно.</span><span class="sxs-lookup"><span data-stu-id="ec813-118">The time grain of the reservation summary, can be daily or monthly.</span></span>

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

### <span data-ttu-id="ec813-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="ec813-119">-ReservationId</span></span>
<span data-ttu-id="ec813-120">Идентификатор резервирования в заказе резервирования.</span><span class="sxs-lookup"><span data-stu-id="ec813-120">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="ec813-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="ec813-121">-ReservationOrderId</span></span>
<span data-ttu-id="ec813-122">Идентификатор приобретенного резервирования.</span><span class="sxs-lookup"><span data-stu-id="ec813-122">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="ec813-123">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ec813-123">-StartDate</span></span>
<span data-ttu-id="ec813-124">Начальные данные (ММ-ММ-ДД в UTC) сводки резервирования, необходимые только для ежедневного анализа.</span><span class="sxs-lookup"><span data-stu-id="ec813-124">The start data (YYYY-MM-DD in UTC) of the reservation summary, required only for daily grain.</span></span>

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

### <span data-ttu-id="ec813-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec813-125">CommonParameters</span></span>
<span data-ttu-id="ec813-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec813-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec813-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec813-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec813-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec813-128">INPUTS</span></span>

### <span data-ttu-id="ec813-129">Нет</span><span class="sxs-lookup"><span data-stu-id="ec813-129">None</span></span>

## <span data-ttu-id="ec813-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec813-130">OUTPUTS</span></span>

### <span data-ttu-id="ec813-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span><span class="sxs-lookup"><span data-stu-id="ec813-131">Microsoft.Azure.Commands.Consumption.Models.PSReservationSummary</span></span>

## <span data-ttu-id="ec813-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec813-132">NOTES</span></span>

## <span data-ttu-id="ec813-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec813-133">RELATED LINKS</span></span>
