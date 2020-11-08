---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: 4d4228ebcdf007485e35b45b93ea738c828c9c4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064871"
---
# <span data-ttu-id="42bf8-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="42bf8-101">Update-AzReservation</span></span>

## <span data-ttu-id="42bf8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="42bf8-103">Обновление `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="42bf8-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="42bf8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42bf8-104">SYNTAX</span></span>

### <span data-ttu-id="42bf8-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42bf8-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42bf8-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="42bf8-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="42bf8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42bf8-107">DESCRIPTION</span></span>
<span data-ttu-id="42bf8-108">Обновляет примененные области `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="42bf8-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="42bf8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42bf8-109">EXAMPLES</span></span>

### <span data-ttu-id="42bf8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42bf8-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="42bf8-111">Обновляет AppliedScopeType с заданным `Reservation` значение Single и InstanceFlexibility на on.</span><span class="sxs-lookup"><span data-stu-id="42bf8-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="42bf8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42bf8-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="42bf8-113">Обновляет AppliedScopeType указанного элемента `Reservation` в Shared и InstanceFlexibility на OFF.</span><span class="sxs-lookup"><span data-stu-id="42bf8-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="42bf8-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42bf8-114">PARAMETERS</span></span>

### <span data-ttu-id="42bf8-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="42bf8-115">-AppliedScope</span></span>
<span data-ttu-id="42bf8-116">SubscriptionId для `Reservation` применения</span><span class="sxs-lookup"><span data-stu-id="42bf8-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="42bf8-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="42bf8-117">-AppliedScopeType</span></span>
<span data-ttu-id="42bf8-118">Тип применяемой области</span><span class="sxs-lookup"><span data-stu-id="42bf8-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="42bf8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42bf8-119">-DefaultProfile</span></span>
<span data-ttu-id="42bf8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42bf8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42bf8-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="42bf8-121">-InstanceFlexibility</span></span>
<span data-ttu-id="42bf8-122">При наличии обновите значение InstanceFlexibility для `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="42bf8-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="42bf8-123">Если не указано, существующее значение остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="42bf8-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="42bf8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42bf8-124">-Name</span></span>
<span data-ttu-id="42bf8-125">Имя резервирования</span><span class="sxs-lookup"><span data-stu-id="42bf8-125">Name of Reservation</span></span>

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

### <span data-ttu-id="42bf8-126">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="42bf8-126">-Reservation</span></span>
<span data-ttu-id="42bf8-127">Параметр объекта pipe для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="42bf8-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="42bf8-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="42bf8-128">-ReservationId</span></span>
<span data-ttu-id="42bf8-129">Идентификатор элемента `Reservation` для обновления.</span><span class="sxs-lookup"><span data-stu-id="42bf8-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="42bf8-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="42bf8-130">-ReservationOrderId</span></span>
<span data-ttu-id="42bf8-131">Идентификатор элемента `ReservationOrder` для обновления.</span><span class="sxs-lookup"><span data-stu-id="42bf8-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="42bf8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42bf8-132">-Confirm</span></span>
<span data-ttu-id="42bf8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42bf8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42bf8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42bf8-134">-WhatIf</span></span>
<span data-ttu-id="42bf8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42bf8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42bf8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42bf8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42bf8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42bf8-137">CommonParameters</span></span>
<span data-ttu-id="42bf8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42bf8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42bf8-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42bf8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42bf8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42bf8-140">INPUTS</span></span>

### <span data-ttu-id="42bf8-141">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="42bf8-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="42bf8-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42bf8-142">OUTPUTS</span></span>

### <span data-ttu-id="42bf8-143">Microsoft. Azure. Commands. резервирования. Models. PSReservation</span><span class="sxs-lookup"><span data-stu-id="42bf8-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="42bf8-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="42bf8-144">NOTES</span></span>

## <span data-ttu-id="42bf8-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42bf8-145">RELATED LINKS</span></span>
