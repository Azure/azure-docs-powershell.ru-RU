---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: d7eab73fbe6bed4a51df7c5056a0dc52787de845
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904153"
---
# <span data-ttu-id="6d3af-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="6d3af-101">Get-AzReservation</span></span>

## <span data-ttu-id="6d3af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d3af-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3af-103">Получить `Reservation` s в заданном заказе на резервирование</span><span class="sxs-lookup"><span data-stu-id="6d3af-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="6d3af-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d3af-104">SYNTAX</span></span>

### <span data-ttu-id="6d3af-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d3af-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d3af-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="6d3af-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6d3af-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="6d3af-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6d3af-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d3af-108">DESCRIPTION</span></span>
<span data-ttu-id="6d3af-109">Список `Reservation` s в одном `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="6d3af-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="6d3af-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d3af-110">EXAMPLES</span></span>

### <span data-ttu-id="6d3af-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d3af-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="6d3af-112">Список `Reservation` s в указанном диапазоне `ReservationOrder` .</span><span class="sxs-lookup"><span data-stu-id="6d3af-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="6d3af-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6d3af-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="6d3af-114">Получить определенные `Reservation` сведения.</span><span class="sxs-lookup"><span data-stu-id="6d3af-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="6d3af-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d3af-115">PARAMETERS</span></span>

### <span data-ttu-id="6d3af-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3af-116">-DefaultProfile</span></span>
<span data-ttu-id="6d3af-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d3af-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d3af-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6d3af-118">-ReservationId</span></span>
<span data-ttu-id="6d3af-119">Идентификатор `Reservation` поиска</span><span class="sxs-lookup"><span data-stu-id="6d3af-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="6d3af-120">-ReservationOrder</span><span class="sxs-lookup"><span data-stu-id="6d3af-120">-ReservationOrder</span></span>
<span data-ttu-id="6d3af-121">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="6d3af-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="6d3af-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6d3af-122">-ReservationOrderId</span></span>
<span data-ttu-id="6d3af-123">Идентификатор элемента `ReservationOrder` , содержащего `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6d3af-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="6d3af-124">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="6d3af-124">Required.</span></span>

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

### <span data-ttu-id="6d3af-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="6d3af-125">-ReservationOrderPage</span></span>
<span data-ttu-id="6d3af-126">Параметр объекта pipe для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="6d3af-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="6d3af-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3af-127">CommonParameters</span></span>
<span data-ttu-id="6d3af-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d3af-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3af-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d3af-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3af-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d3af-130">INPUTS</span></span>

### <span data-ttu-id="6d3af-131">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6d3af-131">System.Guid</span></span>

### <span data-ttu-id="6d3af-132">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="6d3af-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="6d3af-133">Microsoft. Azure. Commands. резервирования. Models. PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="6d3af-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="6d3af-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d3af-134">OUTPUTS</span></span>

### <span data-ttu-id="6d3af-135">Microsoft. Azure. Commands. резервирования. Models. PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="6d3af-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="6d3af-136">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6d3af-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6d3af-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d3af-137">NOTES</span></span>

## <span data-ttu-id="6d3af-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d3af-138">RELATED LINKS</span></span>
