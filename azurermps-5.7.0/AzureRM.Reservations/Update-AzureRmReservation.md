---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/update-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Update-AzureRmReservation.md
ms.openlocfilehash: 76abdc2f7a7099529af87f69af8e37319685aea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563335"
---
# <span data-ttu-id="5a7ec-101">Update-AzureRmReservation</span><span class="sxs-lookup"><span data-stu-id="5a7ec-101">Update-AzureRmReservation</span></span>

## <span data-ttu-id="5a7ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a7ec-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7ec-103">Обновление `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5a7ec-103">Update a `Reservation`.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a7ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a7ec-104">SYNTAX</span></span>

### <span data-ttu-id="5a7ec-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a7ec-105">CommandLine (Default)</span></span>
```
Update-AzureRmReservation -ReservationOrderId <String> -ReservationId <String> -AppliedScopeType <String>
 [-AppliedScope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a7ec-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="5a7ec-106">PipeObject</span></span>
```
Update-AzureRmReservation -AppliedScopeType <String> [-AppliedScope <String>] -Reservation <PSReservation>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a7ec-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a7ec-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7ec-108">Обновляет примененные области `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5a7ec-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="5a7ec-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a7ec-109">EXAMPLES</span></span>

### <span data-ttu-id="5a7ec-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a7ec-110">Example 1</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

<span data-ttu-id="5a7ec-111">Обновляет AppliedScopeType указанного резервирования на Single</span><span class="sxs-lookup"><span data-stu-id="5a7ec-111">Updates the AppliedScopeType of the specified reservation to Single</span></span>

### <span data-ttu-id="5a7ec-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a7ec-112">Example 2</span></span>
```
PS C:\> Update-AzureRmReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared"
```

<span data-ttu-id="5a7ec-113">Обновляет AppliedScopeType указанного резервирования до Shared.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-113">Updates the AppliedScopeType of the specified reservation to Shared</span></span>

## <span data-ttu-id="5a7ec-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a7ec-114">PARAMETERS</span></span>

### <span data-ttu-id="5a7ec-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="5a7ec-115">-AppliedScope</span></span>
<span data-ttu-id="5a7ec-116">SubscriptionId для `Reservation` применения</span><span class="sxs-lookup"><span data-stu-id="5a7ec-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ec-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="5a7ec-117">-AppliedScopeType</span></span>
<span data-ttu-id="5a7ec-118">Тип `Reservation` обновляемого элемента</span><span class="sxs-lookup"><span data-stu-id="5a7ec-118">Type of the `Reservation` to be updated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Single, Shared

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7ec-119">-DefaultProfile</span></span>
<span data-ttu-id="5a7ec-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ec-121">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="5a7ec-121">-Reservation</span></span>
<span data-ttu-id="5a7ec-122">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="5a7ec-122">Pipe object parameter for `Reservation`</span></span>

```yaml
Type: PSReservation
Parameter Sets: PipeObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ec-123">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="5a7ec-123">-ReservationId</span></span>
<span data-ttu-id="5a7ec-124">Идентификатор элемента `Reservation` для обновления.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-124">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="5a7ec-125">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5a7ec-125">-ReservationOrderId</span></span>
<span data-ttu-id="5a7ec-126">Идентификатор элемента `ReservationOrder` для обновления.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-126">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="5a7ec-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a7ec-127">-Confirm</span></span>
<span data-ttu-id="5a7ec-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a7ec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a7ec-129">-WhatIf</span></span>
<span data-ttu-id="5a7ec-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a7ec-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a7ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7ec-132">CommonParameters</span></span>
<span data-ttu-id="5a7ec-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a7ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7ec-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a7ec-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7ec-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a7ec-135">INPUTS</span></span>

### <span data-ttu-id="5a7ec-136">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5a7ec-136">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5a7ec-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a7ec-137">OUTPUTS</span></span>

### <span data-ttu-id="5a7ec-138">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5a7ec-138">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5a7ec-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a7ec-139">NOTES</span></span>

## <span data-ttu-id="5a7ec-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a7ec-140">RELATED LINKS</span></span>

