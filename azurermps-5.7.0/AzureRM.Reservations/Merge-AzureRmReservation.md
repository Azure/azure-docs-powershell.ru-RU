---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/merge-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Merge-AzureRmReservation.md
ms.openlocfilehash: 1f5b0c6a743c9ed26864144cf8df21917bc2ac45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563344"
---
# <span data-ttu-id="57cc1-101">Merge-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="57cc1-101">Merge-AzureRmReservation</span></span>

## <span data-ttu-id="57cc1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="57cc1-103">Объединение двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="57cc1-103">Merges two `Reservation`s.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="57cc1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57cc1-104">SYNTAX</span></span>

### <span data-ttu-id="57cc1-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57cc1-105">CommandLine (Default)</span></span>
```
Merge-AzureRmReservation -ReservationOrderId <String> -ReservationId <String[]> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57cc1-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="57cc1-106">PipeObject</span></span>
```
Merge-AzureRmReservation -Reservation <PSReservation[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57cc1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57cc1-107">DESCRIPTION</span></span>
<span data-ttu-id="57cc1-108">Объединить указанные `Reservation` s в новый `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="57cc1-108">Merge the specified `Reservation`s into a new `Reservation`.</span></span> <span data-ttu-id="57cc1-109">Два из `Reservation` объединяемых слияний должны иметь одинаковые свойства.</span><span class="sxs-lookup"><span data-stu-id="57cc1-109">The two `Reservation`s being merged must have same properties.</span></span>

## <span data-ttu-id="57cc1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="57cc1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57cc1-111">Example 1</span></span>
```
PS C:\> Merge-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111","11111111-0000-0000-0000-1111111111"
```

<span data-ttu-id="57cc1-112">Объединение двух заданных `Reservation` s в один `Reservation`</span><span class="sxs-lookup"><span data-stu-id="57cc1-112">Merge the two specified `Reservation`s into one `Reservation`</span></span>

## <span data-ttu-id="57cc1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57cc1-113">PARAMETERS</span></span>

### <span data-ttu-id="57cc1-114">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="57cc1-114">-Reservation</span></span>
<span data-ttu-id="57cc1-115">Строки двух ReservationIds, разделенные запятыми, для слияния</span><span class="sxs-lookup"><span data-stu-id="57cc1-115">Comma-separated strings of two ReservationIds to merge</span></span>

```yaml
Type: PSReservation[]
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57cc1-116">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="57cc1-116">-ReservationId</span></span>
<span data-ttu-id="57cc1-117">ReservationOrderId для того `ReservationOrder` , который состоит из двух `Reservation` s.</span><span class="sxs-lookup"><span data-stu-id="57cc1-117">ReservationOrderId for the `ReservationOrder` that contains the two `Reservation`s</span></span>

```yaml
Type: String[]
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cc1-118">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="57cc1-118">-ReservationOrderId</span></span>
<span data-ttu-id="57cc1-119">{{Fill ReservationOrderId Description}}</span><span class="sxs-lookup"><span data-stu-id="57cc1-119">{{Fill ReservationOrderId Description}}</span></span>

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cc1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57cc1-120">-Confirm</span></span>
<span data-ttu-id="57cc1-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="57cc1-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cc1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57cc1-122">-WhatIf</span></span>
<span data-ttu-id="57cc1-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="57cc1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57cc1-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="57cc1-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57cc1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57cc1-125">CommonParameters</span></span>
<span data-ttu-id="57cc1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57cc1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57cc1-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57cc1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57cc1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57cc1-128">INPUTS</span></span>

### <span data-ttu-id="57cc1-129">Microsoft. Azure. Commands. резервирования. Models. PSReservation []</span><span class="sxs-lookup"><span data-stu-id="57cc1-129">Microsoft.Azure.Commands.Reservations.Models.PSReservation[]</span></span>

## <span data-ttu-id="57cc1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57cc1-130">OUTPUTS</span></span>

### <span data-ttu-id="57cc1-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. резервирования. Models. PSReservation, Microsoft. Azure. Commands. резервирования, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="57cc1-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Reservations.Models.PSReservation, Microsoft.Azure.Commands.Reservations, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="57cc1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="57cc1-132">NOTES</span></span>

## <span data-ttu-id="57cc1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57cc1-133">RELATED LINKS</span></span>

