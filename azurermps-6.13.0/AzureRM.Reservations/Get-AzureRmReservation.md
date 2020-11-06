---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 1003dcf38815be8daba8b0e218dbca430a89f9e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558308"
---
# <span data-ttu-id="6b874-101">Get-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="6b874-101">Get-AzureRmReservation</span></span>

## <span data-ttu-id="6b874-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b874-102">SYNOPSIS</span></span>
<span data-ttu-id="6b874-103">Получить `Reservation` s в заданном заказе на резервирование</span><span class="sxs-lookup"><span data-stu-id="6b874-103">Get `Reservation`s in a given reservation Order</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b874-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b874-104">SYNTAX</span></span>

### <span data-ttu-id="6b874-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6b874-105">CommandLine (Default)</span></span>
```
Get-AzureRmReservation -ReservationOrderId <Guid> [-ReservationId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b874-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="6b874-106">PipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b874-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="6b874-107">PagePipeObject</span></span>
```
Get-AzureRmReservation [-ReservationOrderPage <PSReservationOrderPage>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b874-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b874-108">DESCRIPTION</span></span>
<span data-ttu-id="6b874-109">Список `Reservation` s в одном `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="6b874-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="6b874-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b874-110">EXAMPLES</span></span>

### <span data-ttu-id="6b874-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b874-111">Example 1</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="6b874-112">Список `Reservation` s в указанном диапазоне `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="6b874-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="6b874-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6b874-113">Example 2</span></span>
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="6b874-114">Получить определенные `Reservation` сведения.</span><span class="sxs-lookup"><span data-stu-id="6b874-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="6b874-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b874-115">PARAMETERS</span></span>

### <span data-ttu-id="6b874-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b874-116">-DefaultProfile</span></span>
<span data-ttu-id="6b874-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b874-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b874-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6b874-118">-ReservationId</span></span>
<span data-ttu-id="6b874-119">Идентификатор `Reservation` поиска</span><span class="sxs-lookup"><span data-stu-id="6b874-119">Id of the `Reservation` to look at</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b874-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="6b874-120">-ReservationOrder</span></span>
<span data-ttu-id="6b874-121">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="6b874-121">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder
Parameter Sets: PipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b874-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6b874-122">-ReservationOrderId</span></span>
<span data-ttu-id="6b874-123">Идентификатор элемента `ReservationOrder` , содержащего `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6b874-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="6b874-124">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="6b874-124">Required.</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b874-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="6b874-125">-ReservationOrderPage</span></span>
<span data-ttu-id="6b874-126">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="6b874-126">Pipe object parameter for `ReservationOrder`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage
Parameter Sets: PagePipeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6b874-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b874-127">CommonParameters</span></span>
<span data-ttu-id="6b874-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b874-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b874-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b874-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b874-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b874-130">INPUTS</span></span>

### <span data-ttu-id="6b874-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6b874-131">System.Guid</span></span>

### <span data-ttu-id="6b874-132">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="6b874-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>
<span data-ttu-id="6b874-133">Параметры: ReservationOrder (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b874-133">Parameters: ReservationOrder (ByValue)</span></span>

### <span data-ttu-id="6b874-134">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="6b874-134">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>
<span data-ttu-id="6b874-135">Параметры: ReservationOrderPage (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6b874-135">Parameters: ReservationOrderPage (ByValue)</span></span>

## <span data-ttu-id="6b874-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b874-136">OUTPUTS</span></span>

### <span data-ttu-id="6b874-137">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="6b874-137">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="6b874-138">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6b874-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6b874-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b874-139">NOTES</span></span>

## <span data-ttu-id="6b874-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b874-140">RELATED LINKS</span></span>
