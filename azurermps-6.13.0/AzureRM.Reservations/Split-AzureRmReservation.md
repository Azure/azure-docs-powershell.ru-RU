---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/split-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Split-AzureRmReservation.md
ms.openlocfilehash: bc1fba5c7fa7e01a3c2461907a214809e175f3ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558299"
---
# <span data-ttu-id="6ff9e-101">Split-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="6ff9e-101">Split-AzureRmReservation</span></span>

## <span data-ttu-id="6ff9e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ff9e-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff9e-103">Разделение а `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="6ff9e-103">Split a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ff9e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ff9e-104">SYNTAX</span></span>

### <span data-ttu-id="6ff9e-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ff9e-105">CommandLine (Default)</span></span>
```
Split-AzureRmReservation -ReservationOrderId <Guid> -ReservationId <Guid> -Quantity <Int32[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff9e-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="6ff9e-106">PipeObject</span></span>
```
Split-AzureRmReservation -Quantity <Int32[]> -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff9e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ff9e-107">DESCRIPTION</span></span>
<span data-ttu-id="6ff9e-108">Разделите элемент на `Reservation` две `Reservation` s с указанным распределением количества.</span><span class="sxs-lookup"><span data-stu-id="6ff9e-108">Split a `Reservation` into two `Reservation`s with specified quantity distribution.</span></span>

## <span data-ttu-id="6ff9e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ff9e-109">EXAMPLES</span></span>

### <span data-ttu-id="6ff9e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ff9e-110">Example 1</span></span>
```
PS C:\> Split-AzureRmReservation -ReservationOrderId "00000000-ffff-ffff-0000-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111" -Quantities 2,3
```

<span data-ttu-id="6ff9e-111">Разделение заданной `Reservation` `Reservation` величины на две с помощью соответствующих количеств</span><span class="sxs-lookup"><span data-stu-id="6ff9e-111">Split the specified `Reservation` into two `Reservation`s with the corresponding quantities</span></span>

## <span data-ttu-id="6ff9e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ff9e-112">PARAMETERS</span></span>

### <span data-ttu-id="6ff9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff9e-113">-DefaultProfile</span></span>
<span data-ttu-id="6ff9e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff9e-115">-Количество</span><span class="sxs-lookup"><span data-stu-id="6ff9e-115">-Quantity</span></span>
<span data-ttu-id="6ff9e-116">Целые числа, разделенные запятыми, в поле количества двух `Reservation` s</span><span class="sxs-lookup"><span data-stu-id="6ff9e-116">Comma-separated integers for quantity field of the two `Reservation`s</span></span>

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

### <span data-ttu-id="6ff9e-117">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="6ff9e-117">-Reservation</span></span>
<span data-ttu-id="6ff9e-118">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="6ff9e-118">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="6ff9e-119">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="6ff9e-119">-ReservationId</span></span>
<span data-ttu-id="6ff9e-120">Идентификатор `Reservation` для разделения</span><span class="sxs-lookup"><span data-stu-id="6ff9e-120">Id of the `Reservation` to split</span></span>

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

### <span data-ttu-id="6ff9e-121">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="6ff9e-121">-ReservationOrderId</span></span>
<span data-ttu-id="6ff9e-122">Идентификатор элемента, `ReservationOrder` содержащего сведения о том `Reservation` , что пользователь хочет разделить</span><span class="sxs-lookup"><span data-stu-id="6ff9e-122">Id of the `ReservationOrder` that contains the `Reservation` that user wants to split</span></span>

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

### <span data-ttu-id="6ff9e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ff9e-123">-Confirm</span></span>
<span data-ttu-id="6ff9e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ff9e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff9e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff9e-125">-WhatIf</span></span>
<span data-ttu-id="6ff9e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ff9e-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ff9e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ff9e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff9e-128">CommonParameters</span></span>
<span data-ttu-id="6ff9e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ff9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff9e-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff9e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff9e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ff9e-131">INPUTS</span></span>

### <span data-ttu-id="6ff9e-132">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6ff9e-132">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>
<span data-ttu-id="6ff9e-133">Параметры: резервирование (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6ff9e-133">Parameters: Reservation (ByValue)</span></span>

## <span data-ttu-id="6ff9e-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ff9e-134">OUTPUTS</span></span>

### <span data-ttu-id="6ff9e-135">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="6ff9e-135">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="6ff9e-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ff9e-136">NOTES</span></span>

## <span data-ttu-id="6ff9e-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ff9e-137">RELATED LINKS</span></span>
