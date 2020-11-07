---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/merge-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Merge-AzReservation.md
ms.openlocfilehash: 8974a8a0bf8230b630a848e922527bc0b08bdb02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904129"
---
# <span data-ttu-id="15261-101">Merge-AzReservation</span><span class="sxs-lookup"><span data-stu-id="15261-101">Merge-AzReservation</span></span>

## <span data-ttu-id="15261-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15261-102">SYNOPSIS</span></span>
<span data-ttu-id="15261-103">Объединение двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="15261-103">Merges two `Reservation`s.</span></span>

## <span data-ttu-id="15261-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15261-104">SYNTAX</span></span>

### <span data-ttu-id="15261-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15261-105">CommandLine (Default)</span></span>
```
Merge-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15261-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="15261-106">PipeObject</span></span>
```
Merge-AzReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15261-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15261-107">DESCRIPTION</span></span>
<span data-ttu-id="15261-108">Объединить указанные `Reservation` s в новый `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="15261-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="15261-109">Два из `Reservation` объединяемых слияний должны иметь одинаковые свойства.</span><span class="sxs-lookup"><span data-stu-id="15261-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="15261-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15261-110">EXAMPLES</span></span>

### <span data-ttu-id="15261-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15261-111">Example 1</span></span>
```
PS C:\> Merge-AzReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="15261-112">Объединение двух заданных `Reservation` s в один `Reservation`</span><span class="sxs-lookup"><span data-stu-id="15261-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="15261-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15261-113">PARAMETERS</span></span>

### <span data-ttu-id="15261-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15261-114">-DefaultProfile</span></span>
<span data-ttu-id="15261-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15261-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15261-116">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="15261-116">-Reservation</span></span>
<span data-ttu-id="15261-117">Строки двух ReservationIds, разделенные запятыми, для слияния</span><span class="sxs-lookup"><span data-stu-id="15261-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="15261-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="15261-118">-ReservationId</span></span>
<span data-ttu-id="15261-119">ReservationOrderId для того `ReservationOrder` , который состоит из двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="15261-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="15261-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="15261-120">-ReservationOrderId</span></span>
<span data-ttu-id="15261-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="15261-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="15261-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15261-122">-Confirm</span></span>
<span data-ttu-id="15261-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15261-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15261-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15261-124">-WhatIf</span></span>
<span data-ttu-id="15261-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15261-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15261-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15261-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15261-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15261-127">CommonParameters</span></span>
<span data-ttu-id="15261-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15261-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15261-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15261-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15261-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15261-130">INPUTS</span></span>

### <span data-ttu-id="15261-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="15261-131">None</span></span>

## <span data-ttu-id="15261-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15261-132">OUTPUTS</span></span>

### <span data-ttu-id="15261-133">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="15261-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="15261-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="15261-134">NOTES</span></span>

## <span data-ttu-id="15261-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15261-135">RELATED LINKS</span></span>
