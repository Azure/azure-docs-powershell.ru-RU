---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316467"
---
# <span data-ttu-id="c6106-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="c6106-101">Split-AzReservation</span></span>

## <span data-ttu-id="c6106-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6106-102">SYNOPSIS</span></span>
<span data-ttu-id="c6106-103">Разделение а `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="c6106-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="c6106-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6106-104">SYNTAX</span></span>

### <span data-ttu-id="c6106-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6106-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6106-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="c6106-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6106-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6106-107">DESCRIPTION</span></span>
<span data-ttu-id="c6106-108">Разделите элемент на `Reservation` две `Reservation` s с указанным распределением количества.</span><span class="sxs-lookup"><span data-stu-id="c6106-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="c6106-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6106-109">EXAMPLES</span></span>

### <span data-ttu-id="c6106-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6106-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="c6106-111">Разделение заданной `Reservation` `Reservation` величины на две с помощью соответствующих количеств</span><span class="sxs-lookup"><span data-stu-id="c6106-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="c6106-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6106-112">PARAMETERS</span></span>

### <span data-ttu-id="c6106-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6106-113">-DefaultProfile</span></span>
<span data-ttu-id="c6106-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6106-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6106-115">-Количество</span><span class="sxs-lookup"><span data-stu-id="c6106-115">-Quantity</span></span>
<span data-ttu-id="c6106-116">Целые числа, разделенные запятыми, в поле количества двух `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="c6106-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="c6106-117">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="c6106-117">-Reservation</span></span>
<span data-ttu-id="c6106-118">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="c6106-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="c6106-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="c6106-119">-ReservationId</span></span>
<span data-ttu-id="c6106-120">Идентификатор `Reservation` для разделения</span><span class="sxs-lookup"><span data-stu-id="c6106-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="c6106-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c6106-121">-ReservationOrderId</span></span>
<span data-ttu-id="c6106-122">Идентификатор элемента, `ReservationOrder` содержащего сведения о том `Reservation` , что пользователь хочет разделить</span><span class="sxs-lookup"><span data-stu-id="c6106-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="c6106-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6106-123">-Confirm</span></span>
<span data-ttu-id="c6106-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6106-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6106-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6106-125">-WhatIf</span></span>
<span data-ttu-id="c6106-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6106-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6106-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6106-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6106-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6106-128">CommonParameters</span></span>
<span data-ttu-id="c6106-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6106-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6106-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6106-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6106-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6106-131">INPUTS</span></span>

### <span data-ttu-id="c6106-132">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c6106-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c6106-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6106-133">OUTPUTS</span></span>

### <span data-ttu-id="c6106-134">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="c6106-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="c6106-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6106-135">NOTES</span></span>

## <span data-ttu-id="c6106-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6106-136">RELATED LINKS</span></span>
