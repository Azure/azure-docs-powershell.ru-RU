---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 6428e4df850d2806939f5d9f8d4e115698e91fb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732289"
---
# <span data-ttu-id="5d0c4-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="5d0c4-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="5d0c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d0c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0c4-103">Объединение двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d0c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d0c4-104">SYNTAX</span></span>

### <span data-ttu-id="5d0c4-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d0c4-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d0c4-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="5d0c4-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d0c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d0c4-107">DESCRIPTION</span></span>
<span data-ttu-id="5d0c4-108">Объединить указанные `Reservation` s в новый `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5d0c4-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="5d0c4-109">Два из `Reservation` объединяемых слияний должны иметь одинаковые свойства.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="5d0c4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d0c4-110">EXAMPLES</span></span>

### <span data-ttu-id="5d0c4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d0c4-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="5d0c4-112">Объединение двух заданных `Reservation` s в один `Reservation`</span><span class="sxs-lookup"><span data-stu-id="5d0c4-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="5d0c4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d0c4-113">PARAMETERS</span></span>

### <span data-ttu-id="5d0c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0c4-114">-DefaultProfile</span></span>
<span data-ttu-id="5d0c4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d0c4-116">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="5d0c4-116">-Reservation</span></span>
<span data-ttu-id="5d0c4-117">Строки двух ReservationIds, разделенные запятыми, для слияния</span><span class="sxs-lookup"><span data-stu-id="5d0c4-117">Comma-separated strings of two ReservationIds to merge</span></span>

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

### <span data-ttu-id="5d0c4-118">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="5d0c4-118">-ReservationId</span></span>
<span data-ttu-id="5d0c4-119">ReservationOrderId для того `ReservationOrder` , который состоит из двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-119">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

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

### <span data-ttu-id="5d0c4-120">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5d0c4-120">-ReservationOrderId</span></span>
<span data-ttu-id="5d0c4-121">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="5d0c4-121">{{Fill ReservationOrderId Description}}</span></span>

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

### <span data-ttu-id="5d0c4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d0c4-122">-Confirm</span></span>
<span data-ttu-id="5d0c4-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d0c4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d0c4-124">-WhatIf</span></span>
<span data-ttu-id="5d0c4-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d0c4-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d0c4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0c4-127">CommonParameters</span></span>
<span data-ttu-id="5d0c4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d0c4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0c4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d0c4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0c4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d0c4-130">INPUTS</span></span>

### <span data-ttu-id="5d0c4-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="5d0c4-131">None</span></span>

## <span data-ttu-id="5d0c4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d0c4-132">OUTPUTS</span></span>

### <span data-ttu-id="5d0c4-133">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5d0c4-133">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5d0c4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d0c4-134">NOTES</span></span>

## <span data-ttu-id="5d0c4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d0c4-135">RELATED LINKS</span></span>
