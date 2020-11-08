---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: fc0b04049184334c59a38226e031342fc29207b2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065781"
---
# <span data-ttu-id="075d9-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="075d9-101">Merge-AzReservation</span></span>

## <span data-ttu-id="075d9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="075d9-102">SYNOPSIS</span></span>
<span data-ttu-id="075d9-103">Объединение двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="075d9-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="075d9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="075d9-104">SYNTAX</span></span>

### <span data-ttu-id="075d9-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="075d9-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="075d9-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="075d9-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="075d9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="075d9-107">DESCRIPTION</span></span>
<span data-ttu-id="075d9-108">Объединить указанные `Reservation` s в новый `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="075d9-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="075d9-109">Два из `Reservation` объединяемых слияний должны иметь одинаковые свойства.</span><span class="sxs-lookup"><span data-stu-id="075d9-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="075d9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="075d9-110">EXAMPLES</span></span>

### <span data-ttu-id="075d9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="075d9-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="075d9-112">Объединение двух заданных `Reservation` s в один `Reservation`</span><span class="sxs-lookup"><span data-stu-id="075d9-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="075d9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="075d9-113">PARAMETERS</span></span>

### <span data-ttu-id="075d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075d9-114">-DefaultProfile</span></span>
<span data-ttu-id="075d9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="075d9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="075d9-116">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="075d9-116">-Reservation</span></span>
<span data-ttu-id="075d9-117">Строки двух ReservationIds, разделенные запятыми, для слияния</span><span class="sxs-lookup"><span data-stu-id="075d9-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="075d9-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="075d9-118">-ReservationId</span></span>
<span data-ttu-id="075d9-119">ReservationOrderId для того `ReservationOrder` , который состоит из двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="075d9-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="075d9-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="075d9-120">-ReservationOrderId</span></span>
<span data-ttu-id="075d9-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="075d9-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="075d9-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="075d9-122">-Confirm</span></span>
<span data-ttu-id="075d9-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="075d9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="075d9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="075d9-124">-WhatIf</span></span>
<span data-ttu-id="075d9-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="075d9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="075d9-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="075d9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="075d9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075d9-127">CommonParameters</span></span>
<span data-ttu-id="075d9-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="075d9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075d9-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="075d9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075d9-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="075d9-130">INPUTS</span></span>

### <span data-ttu-id="075d9-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="075d9-131">None</span></span>

## <span data-ttu-id="075d9-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="075d9-132">OUTPUTS</span></span>

### <span data-ttu-id="075d9-133">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="075d9-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="075d9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="075d9-134">NOTES</span></span>

## <span data-ttu-id="075d9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="075d9-135">RELATED LINKS</span></span>
