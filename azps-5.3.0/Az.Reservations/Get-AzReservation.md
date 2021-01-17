---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservation.md
ms.openlocfilehash: 2970abdcce0be707e5b6ef407adee5261a0620de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421063"
---
# <span data-ttu-id="720be-101">Get-AzReservation</span><span class="sxs-lookup"><span data-stu-id="720be-101">Get-AzReservation</span></span>

## <span data-ttu-id="720be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="720be-102">SYNOPSIS</span></span>
<span data-ttu-id="720be-103">Получите `Reservation` заданный заказ на резервирование</span><span class="sxs-lookup"><span data-stu-id="720be-103">Get `Reservation`s in a given reservation Order</span></span>

## <span data-ttu-id="720be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="720be-104">SYNTAX</span></span>

### <span data-ttu-id="720be-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="720be-105">CommandLine (Default)</span></span>
```
Get-AzReservation -ReservationOrderId <Guid> [-ReservationId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="720be-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="720be-106">PipeObject</span></span>
```
Get-AzReservation [-ReservationOrder <PSReservationOrder>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="720be-107">PagePipeObject</span><span class="sxs-lookup"><span data-stu-id="720be-107">PagePipeObject</span></span>
```
Get-AzReservation [-ReservationOrderPage <PSReservationOrderPage>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="720be-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="720be-108">DESCRIPTION</span></span>
<span data-ttu-id="720be-109">Список `Reservation` находится в пределах `ReservationOrder` одного.</span><span class="sxs-lookup"><span data-stu-id="720be-109">List `Reservation`s within a single `ReservationOrder`.</span></span>

## <span data-ttu-id="720be-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="720be-110">EXAMPLES</span></span>

### <span data-ttu-id="720be-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="720be-111">Example 1</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="720be-112">Список `Reservation` в пределах `ReservationOrder` указанного.</span><span class="sxs-lookup"><span data-stu-id="720be-112">List `Reservation`s within the specified `ReservationOrder`.</span></span>

### <span data-ttu-id="720be-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="720be-113">Example 2</span></span>
```
PS C:\> Get-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

<span data-ttu-id="720be-114">Получите подробные `Reservation` сведения.</span><span class="sxs-lookup"><span data-stu-id="720be-114">Get specific `Reservation` details.</span></span>

## <span data-ttu-id="720be-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="720be-115">PARAMETERS</span></span>

### <span data-ttu-id="720be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="720be-116">-DefaultProfile</span></span>
<span data-ttu-id="720be-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="720be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="720be-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="720be-118">-ReservationId</span></span>
<span data-ttu-id="720be-119">Id of the `Reservation` look at</span><span class="sxs-lookup"><span data-stu-id="720be-119">Id of the `Reservation` to look at</span></span>

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

### <span data-ttu-id="720be-120">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="720be-120">-ReservationOrder</span></span>
<span data-ttu-id="720be-121">Параметр "Pipe object for" (Объект-труба) для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="720be-121">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="720be-122">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="720be-122">-ReservationOrderId</span></span>
<span data-ttu-id="720be-123">ИД `ReservationOrder` того, который содержит `Reservation`</span><span class="sxs-lookup"><span data-stu-id="720be-123">Id of the `ReservationOrder` that contains the `Reservation`.</span></span> <span data-ttu-id="720be-124">Обязательно.</span><span class="sxs-lookup"><span data-stu-id="720be-124">Required.</span></span>

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

### <span data-ttu-id="720be-125">-ReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="720be-125">-ReservationOrderPage</span></span>
<span data-ttu-id="720be-126">Параметр "Pipe object for" (Объект-труба) для `ReservationOrder`</span><span class="sxs-lookup"><span data-stu-id="720be-126">Pipe object parameter for `ReservationOrder`</span></span>

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

### <span data-ttu-id="720be-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="720be-127">CommonParameters</span></span>
<span data-ttu-id="720be-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="720be-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="720be-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="720be-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="720be-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="720be-130">INPUTS</span></span>

### <span data-ttu-id="720be-131">System.Guid</span><span class="sxs-lookup"><span data-stu-id="720be-131">System.Guid</span></span>

### <span data-ttu-id="720be-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span><span class="sxs-lookup"><span data-stu-id="720be-132">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrder</span></span>

### <span data-ttu-id="720be-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span><span class="sxs-lookup"><span data-stu-id="720be-133">Microsoft.Azure.Commands.Reservations.Models.PSReservationOrderPage</span></span>

## <span data-ttu-id="720be-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="720be-134">OUTPUTS</span></span>

### <span data-ttu-id="720be-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span><span class="sxs-lookup"><span data-stu-id="720be-135">Microsoft.Azure.Commands.Reservations.Models.PSReservationPage</span></span>

### <span data-ttu-id="720be-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="720be-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="720be-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="720be-137">NOTES</span></span>

## <span data-ttu-id="720be-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="720be-138">RELATED LINKS</span></span>
