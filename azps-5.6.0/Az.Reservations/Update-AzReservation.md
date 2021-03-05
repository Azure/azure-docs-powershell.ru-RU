---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/powershell/module/az.reservations/update-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Update-AzReservation.md
ms.openlocfilehash: b93dd1462bb019b12fe761e0bdd6cc4172c01b89
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000179"
---
# <span data-ttu-id="d2ce8-101">Update-AzReservation</span><span class="sxs-lookup"><span data-stu-id="d2ce8-101">Update-AzReservation</span></span>

## <span data-ttu-id="d2ce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ce8-103">Обновление `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d2ce8-103">Update a `Reservation`.</span></span>

## <span data-ttu-id="d2ce8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2ce8-104">SYNTAX</span></span>

### <span data-ttu-id="d2ce8-105">CommandLine (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2ce8-105">CommandLine (Default)</span></span>
```
Update-AzReservation -ReservationOrderId <Guid> -ReservationId <Guid> -AppliedScopeType <String>
 [-AppliedScope <String>] [-InstanceFlexibility <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2ce8-106">PipeObject</span><span class="sxs-lookup"><span data-stu-id="d2ce8-106">PipeObject</span></span>
```
Update-AzReservation -AppliedScopeType <String> [-AppliedScope <String>] [-InstanceFlexibility <String>]
 -Reservation <PSReservation> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2ce8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ce8-107">DESCRIPTION</span></span>
<span data-ttu-id="d2ce8-108">Обновляет примененные области `Reservation` действия.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-108">Updates the applied scopes of the `Reservation`.</span></span>

## <span data-ttu-id="d2ce8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2ce8-109">EXAMPLES</span></span>

### <span data-ttu-id="d2ce8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2ce8-110">Example 1</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedScopeType "Single" -appliedscope "/subscriptions/1111aaaa-b1b2-c0c2-d0d2-00000fffff" -InstanceFlexibility "On"
```

<span data-ttu-id="d2ce8-111">Обновляет AppliedScopeType указанного на Single и `Reservation` InstanceFlexibility to On.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-111">Updates the AppliedScopeType of the specified `Reservation` to Single and InstanceFlexibility to On.</span></span>

### <span data-ttu-id="d2ce8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d2ce8-112">Example 2</span></span>
```
PS C:\> Update-AzReservation -ReservationOrderId "11111111-1111-1111-1111-1111111111" -ReservationId "00000000-1111-1111-1111-0000000000" -appliedscopetype "Shared" -InstanceFlexibility "Off"
```

<span data-ttu-id="d2ce8-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-113">Updates the AppliedScopeType of the specified `Reservation` to Shared and InstanceFlexibility to Off.</span></span>

## <span data-ttu-id="d2ce8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2ce8-114">PARAMETERS</span></span>

### <span data-ttu-id="d2ce8-115">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="d2ce8-115">-AppliedScope</span></span>
<span data-ttu-id="d2ce8-116">SubscriptionId для `Reservation` этого действия</span><span class="sxs-lookup"><span data-stu-id="d2ce8-116">SubscriptionId for this `Reservation` to be applied</span></span>

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

### <span data-ttu-id="d2ce8-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="d2ce8-117">-AppliedScopeType</span></span>
<span data-ttu-id="d2ce8-118">Тип примененной области</span><span class="sxs-lookup"><span data-stu-id="d2ce8-118">Type of the Applied Scope</span></span>

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

### <span data-ttu-id="d2ce8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ce8-119">-DefaultProfile</span></span>
<span data-ttu-id="d2ce8-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2ce8-121">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="d2ce8-121">-InstanceFlexibility</span></span>
<span data-ttu-id="d2ce8-122">При этом обновляется значение висячивости экземпляра `Reservation` .</span><span class="sxs-lookup"><span data-stu-id="d2ce8-122">If present, updates the InstanceFlexibility value of the `Reservation`.</span></span> <span data-ttu-id="d2ce8-123">Если значение не задано, существующее значение не изменяется.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-123">If not specified, the existing value remains unchanged.</span></span>

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

### <span data-ttu-id="d2ce8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d2ce8-124">-Name</span></span>
<span data-ttu-id="d2ce8-125">Название резервирования</span><span class="sxs-lookup"><span data-stu-id="d2ce8-125">Name of Reservation</span></span>

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

### <span data-ttu-id="d2ce8-126">-Резервирование</span><span class="sxs-lookup"><span data-stu-id="d2ce8-126">-Reservation</span></span>
<span data-ttu-id="d2ce8-127">Параметр "Pipe object for" (Объект-труба) для `Reservation`</span><span class="sxs-lookup"><span data-stu-id="d2ce8-127">Pipe object parameter for `Reservation`</span></span>

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

### <span data-ttu-id="d2ce8-128">-ReservationId</span><span class="sxs-lookup"><span data-stu-id="d2ce8-128">-ReservationId</span></span>
<span data-ttu-id="d2ce8-129">ИД `Reservation` обновления</span><span class="sxs-lookup"><span data-stu-id="d2ce8-129">Id of the `Reservation` to update</span></span>

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

### <span data-ttu-id="d2ce8-130">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="d2ce8-130">-ReservationOrderId</span></span>
<span data-ttu-id="d2ce8-131">ИД `ReservationOrder` обновления</span><span class="sxs-lookup"><span data-stu-id="d2ce8-131">Id of the `ReservationOrder` to update</span></span>

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

### <span data-ttu-id="d2ce8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2ce8-132">-Confirm</span></span>
<span data-ttu-id="d2ce8-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2ce8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2ce8-134">-WhatIf</span></span>
<span data-ttu-id="d2ce8-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2ce8-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2ce8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ce8-137">CommonParameters</span></span>
<span data-ttu-id="d2ce8-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2ce8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ce8-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2ce8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ce8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2ce8-140">INPUTS</span></span>

### <span data-ttu-id="d2ce8-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="d2ce8-141">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d2ce8-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2ce8-142">OUTPUTS</span></span>

### <span data-ttu-id="d2ce8-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span><span class="sxs-lookup"><span data-stu-id="d2ce8-143">Microsoft.Azure.Commands.Reservations.Models.PSReservation</span></span>

## <span data-ttu-id="d2ce8-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2ce8-144">NOTES</span></span>

## <span data-ttu-id="d2ce8-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2ce8-145">RELATED LINKS</span></span>
