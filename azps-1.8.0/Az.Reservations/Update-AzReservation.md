---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 7e7b32322d6c6a131ee906c56b0c4fbdd0a5d63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729467"
---
# <span data-ttu-id="5d56f-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="5d56f-101">Update-AzReservation</span></span>

## <span data-ttu-id="5d56f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d56f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d56f-103">Обновление `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5d56f-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="5d56f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d56f-104">SYNTAX</span></span>

### <span data-ttu-id="5d56f-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d56f-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d56f-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="5d56f-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d56f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d56f-107">DESCRIPTION</span></span>
<span data-ttu-id="5d56f-108">Обновляет примененные области `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5d56f-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="5d56f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d56f-109">EXAMPLES</span></span>

### <span data-ttu-id="5d56f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d56f-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="5d56f-111">Обновляет AppliedScopeType с заданным `Reservation` значение Single и InstanceFlexibility на on.</span><span class="sxs-lookup"><span data-stu-id="5d56f-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="5d56f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5d56f-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="5d56f-113">Обновляет AppliedScopeType указанного элемента `Reservation` в Shared и InstanceFlexibility на OFF.</span><span class="sxs-lookup"><span data-stu-id="5d56f-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="5d56f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d56f-114">PARAMETERS</span></span>

### <span data-ttu-id="5d56f-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="5d56f-115">-AppliedScope</span></span>
<span data-ttu-id="5d56f-116">SubscriptionId для `Reservation` применения</span><span class="sxs-lookup"><span data-stu-id="5d56f-116">SubscriptionId for this `Reservation` to be applied</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="5d56f-117">-AppliedScopeType</span></span>
<span data-ttu-id="5d56f-118">Тип применяемой области</span><span class="sxs-lookup"><span data-stu-id="5d56f-118">Type of the Applied Scope</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d56f-119">-DefaultProfile</span></span>
<span data-ttu-id="5d56f-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d56f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d56f-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="5d56f-121">-InstanceFlexibility</span></span>
<span data-ttu-id="5d56f-122">При наличии обновите значение InstanceFlexibility для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="5d56f-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="5d56f-123">Если не указано, существующее значение остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="5d56f-123">If not specified, the existing value remains unchanged.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d56f-124">-Name</span></span>
<span data-ttu-id="5d56f-125">Имя резервирования</span><span class="sxs-lookup"><span data-stu-id="5d56f-125">Name of Reservation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-126">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="5d56f-126">-Reservation</span></span>
<span data-ttu-id="5d56f-127">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="5d56f-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="5d56f-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="5d56f-128">-ReservationId</span></span>
<span data-ttu-id="5d56f-129">Идентификатор элемента `Reservation` для обновления.</span><span class="sxs-lookup"><span data-stu-id="5d56f-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="5d56f-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="5d56f-130">-ReservationOrderId</span></span>
<span data-ttu-id="5d56f-131">Идентификатор элемента `ReservationOrder` для обновления.</span><span class="sxs-lookup"><span data-stu-id="5d56f-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="5d56f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d56f-132">-Confirm</span></span>
<span data-ttu-id="5d56f-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d56f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d56f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d56f-134">-WhatIf</span></span>
<span data-ttu-id="5d56f-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d56f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d56f-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d56f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d56f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d56f-137">CommonParameters</span></span>
<span data-ttu-id="5d56f-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d56f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d56f-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d56f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d56f-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d56f-140">INPUTS</span></span>

### <span data-ttu-id="5d56f-141">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5d56f-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5d56f-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d56f-142">OUTPUTS</span></span>

### <span data-ttu-id="5d56f-143">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="5d56f-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="5d56f-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d56f-144">NOTES</span></span>

## <span data-ttu-id="5d56f-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d56f-145">RELATED LINKS</span></span>
