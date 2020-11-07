---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: 1345978ac502d0c7d576b56f720bd16ca704e062
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905661"
---
# <span data-ttu-id="349c8-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="349c8-101">Split-AzReservation</span></span>

## <span data-ttu-id="349c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="349c8-102">SYNOPSIS</span></span>
<span data-ttu-id="349c8-103">Разделение а `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="349c8-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="349c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="349c8-104">SYNTAX</span></span>

### <span data-ttu-id="349c8-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="349c8-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="349c8-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="349c8-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="349c8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="349c8-107">DESCRIPTION</span></span>
<span data-ttu-id="349c8-108">Разделите элемент на `Reservation` две `Reservation` s с указанным распределением количества.</span><span class="sxs-lookup"><span data-stu-id="349c8-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="349c8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="349c8-109">EXAMPLES</span></span>

### <span data-ttu-id="349c8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="349c8-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="349c8-111">Разделение заданной `Reservation` `Reservation` величины на две с помощью соответствующих количеств</span><span class="sxs-lookup"><span data-stu-id="349c8-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="349c8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="349c8-112">PARAMETERS</span></span>

### <span data-ttu-id="349c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="349c8-113">-DefaultProfile</span></span>
<span data-ttu-id="349c8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="349c8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="349c8-115">-Количество</span><span class="sxs-lookup"><span data-stu-id="349c8-115">-Quantity</span></span>
<span data-ttu-id="349c8-116">Целые числа, разделенные запятыми, в поле количества двух `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="349c8-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

```yaml
Type: System.Int32[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c8-117">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="349c8-117">-Reservation</span></span>
<span data-ttu-id="349c8-118">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="349c8-118">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="349c8-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="349c8-119">-ReservationId</span></span>
<span data-ttu-id="349c8-120">Идентификатор `Reservation` для разделения</span><span class="sxs-lookup"><span data-stu-id="349c8-120">Id of the `Reservation` to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c8-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="349c8-121">-ReservationOrderId</span></span>
<span data-ttu-id="349c8-122">Идентификатор элемента, `ReservationOrder` содержащего сведения о том `Reservation` , что пользователь хочет разделить</span><span class="sxs-lookup"><span data-stu-id="349c8-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

```yaml
Type: System.Guid
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="349c8-123">-Confirm</span></span>
<span data-ttu-id="349c8-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="349c8-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="349c8-125">-WhatIf</span></span>
<span data-ttu-id="349c8-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="349c8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="349c8-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="349c8-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="349c8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="349c8-128">CommonParameters</span></span>
<span data-ttu-id="349c8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="349c8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="349c8-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="349c8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="349c8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="349c8-131">INPUTS</span></span>

### <span data-ttu-id="349c8-132">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="349c8-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="349c8-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="349c8-133">OUTPUTS</span></span>

### <span data-ttu-id="349c8-134">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="349c8-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="349c8-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="349c8-135">NOTES</span></span>

## <span data-ttu-id="349c8-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="349c8-136">RELATED LINKS</span></span>
