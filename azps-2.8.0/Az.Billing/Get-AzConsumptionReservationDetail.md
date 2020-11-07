---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionReservationDetail.md
ms.openlocfilehash: 0776e824d9463a0577f64f2b19f0d71ece29cfa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727668"
---
# <span data-ttu-id="f5298-101">Get-AzConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="f5298-101">Get-AzConsumptionReservationDetail</span></span>

## <span data-ttu-id="f5298-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f5298-102">SYNOPSIS</span></span>
<span data-ttu-id="f5298-103">Получение сведений о резервированиях для указанного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f5298-103">Get reservations details for provided date range.</span></span>

## <span data-ttu-id="f5298-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f5298-104">SYNTAX</span></span>

```
Get-AzConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5298-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5298-105">DESCRIPTION</span></span>
<span data-ttu-id="f5298-106">Командлет **Get-AzConsumptionReservationDetail** получает сведения о резервированиях для указанного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="f5298-106">The **Get-AzConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="f5298-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f5298-107">EXAMPLES</span></span>

### <span data-ttu-id="f5298-108">Пример 1: получение сведений о резервировании с ИД заказа на резервирование для указанного диапазона дат</span><span class="sxs-lookup"><span data-stu-id="f5298-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

### <span data-ttu-id="f5298-109">Пример 2: получение сведений о резервировании с ИД заказа на резервирование и идентификатором резервирования для указанного диапазона дат</span><span class="sxs-lookup"><span data-stu-id="f5298-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
Id:  providers/Microsoft.Capacity/reservationOrders/ca69259e-bd4f-45c3-bf28-3f353f9cce9b/reservations/f37f4b70-52ba-4344-a8bd-28abfd21d640providers/Microsoft.Consumption/reservationDetails/20171007
InstanceId:  subscriptions/a98d6dc5-eb8f-46cf-8938-f1fb08f03706/resourcegroups/testrg/providers/microsoft.compute/virtualmachines/std2swindows
Name:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b_f37f4b70-52ba-4344-a8bd-28abfd21d640_20171007
ReservationId:  f37f4b70-52ba-4344-a8bd-28abfd21d640
ReservationOrderId:  ca69259e-bd4f-45c3-bf28-3f353f9cce9b
ReservedHour:  24
SkuName:  Standard_DS2_v2
TotalReservedQuantity:  1
Type:  Microsoft.Consumption/reservationDetails
UsageDate:  10/7/2017 12:00:00 AM
UsedHour:  24
```

## <span data-ttu-id="f5298-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f5298-110">PARAMETERS</span></span>

### <span data-ttu-id="f5298-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5298-111">-DefaultProfile</span></span>
<span data-ttu-id="f5298-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5298-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5298-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f5298-113">-EndDate</span></span>
<span data-ttu-id="f5298-114">Конечные данные (гггг-мм-дд в формате UTC) сведений о резервировании.</span><span class="sxs-lookup"><span data-stu-id="f5298-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5298-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="f5298-115">-ReservationId</span></span>
<span data-ttu-id="f5298-116">Идентификатор резервирования в заказе на резервирование.</span><span class="sxs-lookup"><span data-stu-id="f5298-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="f5298-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="f5298-117">-ReservationOrderId</span></span>
<span data-ttu-id="f5298-118">Идентификатор покупки резервирования.</span><span class="sxs-lookup"><span data-stu-id="f5298-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="f5298-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="f5298-119">-StartDate</span></span>
<span data-ttu-id="f5298-120">Начальные данные (гггг-мм-дд в формате UTC) сведений о резервировании.</span><span class="sxs-lookup"><span data-stu-id="f5298-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5298-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5298-121">CommonParameters</span></span>
<span data-ttu-id="f5298-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f5298-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5298-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5298-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5298-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f5298-124">INPUTS</span></span>

### <span data-ttu-id="f5298-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="f5298-125">None</span></span>

## <span data-ttu-id="f5298-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5298-126">OUTPUTS</span></span>

### <span data-ttu-id="f5298-127">Microsoft. Azure. Commands. потребление. Models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="f5298-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="f5298-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f5298-128">NOTES</span></span>

## <span data-ttu-id="f5298-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5298-129">RELATED LINKS</span></span>
