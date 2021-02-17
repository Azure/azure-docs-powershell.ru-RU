---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210513"
---
# <span data-ttu-id="534bd-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="534bd-101">Merge-AzReservation</span></span>

## <span data-ttu-id="534bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="534bd-102">SYNOPSIS</span></span>
<span data-ttu-id="534bd-103">Объединяет два `Reservation` из них.</span><span class="sxs-lookup"><span data-stu-id="534bd-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="534bd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="534bd-104">SYNTAX</span></span>

### <span data-ttu-id="534bd-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="534bd-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="534bd-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="534bd-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="534bd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="534bd-107">DESCRIPTION</span></span>
<span data-ttu-id="534bd-108">Объединение указанных `Reservation` s в `Reservation` новое.</span><span class="sxs-lookup"><span data-stu-id="534bd-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="534bd-109">У двух `Reservation` объединенных объектов должны быть одинаковые свойства.</span><span class="sxs-lookup"><span data-stu-id="534bd-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="534bd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="534bd-110">EXAMPLES</span></span>

### <span data-ttu-id="534bd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="534bd-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="534bd-112">Объединение двух указанных `Reservation` s в один `Reservation`</span><span class="sxs-lookup"><span data-stu-id="534bd-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="534bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="534bd-113">PARAMETERS</span></span>

### <span data-ttu-id="534bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="534bd-114">-DefaultProfile</span></span>
<span data-ttu-id="534bd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="534bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="534bd-116">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="534bd-116">-Reservation</span></span>
<span data-ttu-id="534bd-117">Строки двух условий резервирования, разделенные запятой</span><span class="sxs-lookup"><span data-stu-id="534bd-117">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: Microsoft.Azure.Commands.Reservations.Models.PSReservation[]
Parameter Sets: PipeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534bd-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="534bd-118">-ReservationId</span></span>
<span data-ttu-id="534bd-119">ReservationOrderId для `ReservationOrder` этих двух `Reservation`</span><span class="sxs-lookup"><span data-stu-id="534bd-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: CommandLine
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="534bd-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="534bd-120">-ReservationOrderId</span></span>
<span data-ttu-id="534bd-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="534bd-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="534bd-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="534bd-122">-Confirm</span></span>
<span data-ttu-id="534bd-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="534bd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="534bd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="534bd-124">-WhatIf</span></span>
<span data-ttu-id="534bd-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="534bd-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="534bd-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="534bd-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="534bd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="534bd-127">CommonParameters</span></span>
<span data-ttu-id="534bd-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="534bd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="534bd-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="534bd-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="534bd-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="534bd-130">INPUTS</span></span>

### <span data-ttu-id="534bd-131">Нет</span><span class="sxs-lookup"><span data-stu-id="534bd-131">None</span></span>

## <span data-ttu-id="534bd-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="534bd-132">OUTPUTS</span></span>

### <span data-ttu-id="534bd-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="534bd-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="534bd-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="534bd-134">NOTES</span></span>

## <span data-ttu-id="534bd-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="534bd-135">RELATED LINKS</span></span>
