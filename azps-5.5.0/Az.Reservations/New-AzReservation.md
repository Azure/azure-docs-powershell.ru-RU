---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210497"
---
# <span data-ttu-id="fe864-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="fe864-101">New-AzReservation</span></span>

## <span data-ttu-id="fe864-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe864-102">SYNOPSIS</span></span>
<span data-ttu-id="fe864-103">Приобретение резервирования</span><span class="sxs-lookup"><span data-stu-id="fe864-103">Purchase a reservation</span></span>

## <span data-ttu-id="fe864-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe864-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe864-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe864-105">DESCRIPTION</span></span>
<span data-ttu-id="fe864-106">Приобрести экземпляр резервирования и получить преимущество</span><span class="sxs-lookup"><span data-stu-id="fe864-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="fe864-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe864-107">EXAMPLES</span></span>

### <span data-ttu-id="fe864-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe864-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="fe864-109">После вычисления цены клиент мог очистить данные RI по calculatePrice</span><span class="sxs-lookup"><span data-stu-id="fe864-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="fe864-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe864-110">PARAMETERS</span></span>

### <span data-ttu-id="fe864-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="fe864-111">-AppliedScope</span></span>
<span data-ttu-id="fe864-112">Подписка, к которую будет применено это преимущество.</span><span class="sxs-lookup"><span data-stu-id="fe864-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="fe864-113">Требуется, если --applied-scope-type is Single.</span><span class="sxs-lookup"><span data-stu-id="fe864-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="fe864-114">Не укажите, является ли тип "Общий" --applied-scope-type общим.</span><span class="sxs-lookup"><span data-stu-id="fe864-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="fe864-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="fe864-115">-AppliedScopeType</span></span>
<span data-ttu-id="fe864-116">Тип применяемой области, чтобы обновить резервирование на "Один" или "Общий"</span><span class="sxs-lookup"><span data-stu-id="fe864-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="fe864-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="fe864-117">-BillingPlan</span></span>
<span data-ttu-id="fe864-118">Варианты плана вы счета, доступные для этого SKU.</span><span class="sxs-lookup"><span data-stu-id="fe864-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="fe864-119">"Monthly" или "Upfront"</span><span class="sxs-lookup"><span data-stu-id="fe864-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="fe864-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="fe864-120">-BillingScopeId</span></span>
<span data-ttu-id="fe864-121">Подписка, с которую взимается плата за резервирование.</span><span class="sxs-lookup"><span data-stu-id="fe864-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="fe864-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe864-122">-DefaultProfile</span></span>
<span data-ttu-id="fe864-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe864-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe864-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fe864-124">-DisplayName</span></span>
<span data-ttu-id="fe864-125">Имя, которое легко определить для резервирования.</span><span class="sxs-lookup"><span data-stu-id="fe864-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="fe864-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="fe864-126">-InstanceFlexibility</span></span>
<span data-ttu-id="fe864-127">{{ Fill InstanceFlexibility Description }}</span><span class="sxs-lookup"><span data-stu-id="fe864-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="fe864-128">-Location</span><span class="sxs-lookup"><span data-stu-id="fe864-128">-Location</span></span>
<span data-ttu-id="fe864-129">Расположение, где находится SKU.</span><span class="sxs-lookup"><span data-stu-id="fe864-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="fe864-130">-Quantity</span><span class="sxs-lookup"><span data-stu-id="fe864-130">-Quantity</span></span>
<span data-ttu-id="fe864-131">Количество продукта для расчета цены или приобретения.</span><span class="sxs-lookup"><span data-stu-id="fe864-131">Quantity of product for calculating price or purchasing.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe864-132">-Продлить</span><span class="sxs-lookup"><span data-stu-id="fe864-132">-Renew</span></span>
<span data-ttu-id="fe864-133">При этом будет автоматически приобретено новое резервирование в срок действия.</span><span class="sxs-lookup"><span data-stu-id="fe864-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe864-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="fe864-134">-ReservationOrderId</span></span>
<span data-ttu-id="fe864-135">Id of reservation order to purchase, generate by az reservations-order-order calculate.</span><span class="sxs-lookup"><span data-stu-id="fe864-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="fe864-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="fe864-136">-ReservedResourceType</span></span>
<span data-ttu-id="fe864-137">Тип ресурса, для которого должны быть предоставлены skus.</span><span class="sxs-lookup"><span data-stu-id="fe864-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="fe864-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe864-138">-Sku</span></span>
<span data-ttu-id="fe864-139">Имя SKU</span><span class="sxs-lookup"><span data-stu-id="fe864-139">Sku name</span></span>

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

### <span data-ttu-id="fe864-140">-Term</span><span class="sxs-lookup"><span data-stu-id="fe864-140">-Term</span></span>
<span data-ttu-id="fe864-141">Доступные условия резервирования для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe864-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="fe864-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe864-142">-Confirm</span></span>
<span data-ttu-id="fe864-143">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe864-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe864-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe864-144">-WhatIf</span></span>
<span data-ttu-id="fe864-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe864-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe864-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fe864-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe864-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe864-147">CommonParameters</span></span>
<span data-ttu-id="fe864-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe864-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe864-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe864-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe864-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe864-150">INPUTS</span></span>

### <span data-ttu-id="fe864-151">Нет</span><span class="sxs-lookup"><span data-stu-id="fe864-151">None</span></span>

## <span data-ttu-id="fe864-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe864-152">OUTPUTS</span></span>

### <span data-ttu-id="fe864-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="fe864-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="fe864-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe864-154">NOTES</span></span>

## <span data-ttu-id="fe864-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe864-155">RELATED LINKS</span></span>
