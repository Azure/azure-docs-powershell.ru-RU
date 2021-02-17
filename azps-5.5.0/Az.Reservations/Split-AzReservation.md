---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/split-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Split-AzReservation.md
ms.openlocfilehash: b879b5b47c752a331f0c2d70a6d37e57b113d816
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210505"
---
# <span data-ttu-id="a5986-101">Split-AzReservation</span><span class="sxs-lookup"><span data-stu-id="a5986-101">Split-AzReservation</span></span>

## <span data-ttu-id="a5986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5986-102">SYNOPSIS</span></span>
<span data-ttu-id="a5986-103">Разделение `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="a5986-103">Split a `Reservation`.</span></span>

## <span data-ttu-id="a5986-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a5986-104">SYNTAX</span></span>

### <span data-ttu-id="a5986-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a5986-105">CommandLine (Default)</span></span>
```
Split-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5986-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="a5986-106">PipeObject</span></span>
```
Split-AzReservation -Quantity <Int32[]> -Reservation <PSReservation> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5986-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5986-107">DESCRIPTION</span></span>
<span data-ttu-id="a5986-108">Разделить `Reservation` 1 на два `Reservation` с помощью указанного распределения количества.</span><span class="sxs-lookup"><span data-stu-id="a5986-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="a5986-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a5986-109">EXAMPLES</span></span>

### <span data-ttu-id="a5986-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5986-110">Example 1</span></span>
```
PS C:\> Split-AzReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="a5986-111">Разделение указанного количества `Reservation` на два с соответствующим `Reservation` количеством</span><span class="sxs-lookup"><span data-stu-id="a5986-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="a5986-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5986-112">PARAMETERS</span></span>

### <span data-ttu-id="a5986-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5986-113">-DefaultProfile</span></span>
<span data-ttu-id="a5986-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5986-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5986-115">-Quantity</span><span class="sxs-lookup"><span data-stu-id="a5986-115">-Quantity</span></span>
<span data-ttu-id="a5986-116">С разделителем — запятые для поля "Количество" двух `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a5986-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="a5986-117">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="a5986-117">-Reservation</span></span>
<span data-ttu-id="a5986-118">Параметр "Pipe object for" (Объект-труба) для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="a5986-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="a5986-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="a5986-119">-ReservationId</span></span>
<span data-ttu-id="a5986-120">Id of the `Reservation` split</span><span class="sxs-lookup"><span data-stu-id="a5986-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="a5986-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="a5986-121">-ReservationOrderId</span></span>
<span data-ttu-id="a5986-122">Id of the `ReservationOrder` that contains the user wants to `Reservation` split</span><span class="sxs-lookup"><span data-stu-id="a5986-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="a5986-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5986-123">-Confirm</span></span>
<span data-ttu-id="a5986-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a5986-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5986-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5986-125">-WhatIf</span></span>
<span data-ttu-id="a5986-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5986-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5986-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a5986-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5986-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5986-128">CommonParameters</span></span>
<span data-ttu-id="a5986-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5986-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5986-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5986-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5986-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5986-131">INPUTS</span></span>

### <span data-ttu-id="a5986-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="a5986-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a5986-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a5986-133">OUTPUTS</span></span>

### <span data-ttu-id="a5986-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="a5986-134">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="a5986-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a5986-135">NOTES</span></span>

## <span data-ttu-id="a5986-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5986-136">RELATED LINKS</span></span>
