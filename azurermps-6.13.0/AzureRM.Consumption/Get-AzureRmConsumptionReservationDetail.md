---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionreservationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionReservationDetail.md
ms.openlocfilehash: a7a4b50198a63329b0d45986f2bce60edb927777
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732113"
---
# <span data-ttu-id="6eb7f-101">Get-AzureRmConsumptionReservationDetail</span><span class="sxs-lookup"><span data-stu-id="6eb7f-101">Get-AzureRmConsumptionReservationDetail</span></span>

## <span data-ttu-id="6eb7f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6eb7f-102">SYNOPSIS</span></span>
<span data-ttu-id="6eb7f-103">Получение сведений о резервированиях для указанного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-103">Get reservations details for provided date range.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eb7f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6eb7f-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionReservationDetail -StartDate <DateTime> -EndDate <DateTime> -ReservationOrderId <String>
 [-ReservationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6eb7f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eb7f-105">DESCRIPTION</span></span>
<span data-ttu-id="6eb7f-106">Командлет **Get-AzureRmConsumptionReservationDetail** получает сведения о резервированиях для указанного диапазона дат.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-106">The **Get-AzureRmConsumptionReservationDetail** cmdlet gets reservations details for provided date range.</span></span>

## <span data-ttu-id="6eb7f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6eb7f-107">EXAMPLES</span></span>

### <span data-ttu-id="6eb7f-108">Пример 1: получение сведений о резервировании с ИД заказа на резервирование для указанного диапазона дат</span><span class="sxs-lookup"><span data-stu-id="6eb7f-108">Example 1: Get reservation details with reservation order Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -StartDate 2017-10-01 -EndDate 2017-12-07
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

### <span data-ttu-id="6eb7f-109">Пример 2: получение сведений о резервировании с ИД заказа на резервирование и идентификатором резервирования для указанного диапазона дат</span><span class="sxs-lookup"><span data-stu-id="6eb7f-109">Example 2: Get reservation details with reservation order Id and reservation Id for provided date range</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionReservationDetail -ReservationOrderId ca69259e-bd4f-45c3-bf28-3f353f9cce9b -ReservationId f37f4b70-52ba-4344-a8bd-28abfd21d640 -StartDate 2017-10-01 -EndDate 2017-12-07
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

## <span data-ttu-id="6eb7f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6eb7f-110">PARAMETERS</span></span>

### <span data-ttu-id="6eb7f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eb7f-111">-DefaultProfile</span></span>
<span data-ttu-id="6eb7f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eb7f-113">-EndDate</span><span class="sxs-lookup"><span data-stu-id="6eb7f-113">-EndDate</span></span>
<span data-ttu-id="6eb7f-114">Конечные данные (гггг-мм-дд в формате UTC) сведений о резервировании.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-114">The end data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="6eb7f-115">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6eb7f-115">-ReservationId</span></span>
<span data-ttu-id="6eb7f-116">Идентификатор резервирования в заказе на резервирование.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-116">The identifier of a reservation within a reservation order.</span></span>

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

### <span data-ttu-id="6eb7f-117">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6eb7f-117">-ReservationOrderId</span></span>
<span data-ttu-id="6eb7f-118">Идентификатор покупки резервирования.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-118">The identifier of a reservation purchase.</span></span>

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

### <span data-ttu-id="6eb7f-119">-StartDate</span><span class="sxs-lookup"><span data-stu-id="6eb7f-119">-StartDate</span></span>
<span data-ttu-id="6eb7f-120">Начальные данные (гггг-мм-дд в формате UTC) сведений о резервировании.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-120">The start data (YYYY-MM-DD in UTC) of the reservation detail.</span></span>

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

### <span data-ttu-id="6eb7f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eb7f-121">CommonParameters</span></span>
<span data-ttu-id="6eb7f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6eb7f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eb7f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eb7f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eb7f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6eb7f-124">INPUTS</span></span>

### <span data-ttu-id="6eb7f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="6eb7f-125">None</span></span>

## <span data-ttu-id="6eb7f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6eb7f-126">OUTPUTS</span></span>

### <span data-ttu-id="6eb7f-127">Microsoft. Azure. Commands. потребление. Models. PSReservationDetail</span><span class="sxs-lookup"><span data-stu-id="6eb7f-127">Microsoft.Azure.Commands.Consumption.Models.PSReservationDetail</span></span>

## <span data-ttu-id="6eb7f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="6eb7f-128">NOTES</span></span>

## <span data-ttu-id="6eb7f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6eb7f-129">RELATED LINKS</span></span>
