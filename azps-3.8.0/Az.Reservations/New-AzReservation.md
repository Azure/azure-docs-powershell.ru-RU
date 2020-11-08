---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/new-azreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/New-AzReservation.md
ms.openlocfilehash: 60de1572afda000c8c1a99f53df1344b9b0fbfda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072759"
---
# <span data-ttu-id="c7b23-101">New-AzReservation</span><span class="sxs-lookup"><span data-stu-id="c7b23-101">New-AzReservation</span></span>

## <span data-ttu-id="c7b23-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7b23-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b23-103">Приобретите резервирование</span><span class="sxs-lookup"><span data-stu-id="c7b23-103">Purchase a reservation</span></span>

## <span data-ttu-id="c7b23-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7b23-104">SYNTAX</span></span>

```
New-AzReservation -ReservationOrderId <String> -ReservedResourceType <String> -Sku <String>
 [-Location <String>] -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32>
 -DisplayName <String> -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>]
 [-InstanceFlexibility <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7b23-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b23-105">DESCRIPTION</span></span>
<span data-ttu-id="c7b23-106">Приобретите экземпляр резервирования и получите преимущество</span><span class="sxs-lookup"><span data-stu-id="c7b23-106">Purchase a reservation Instance and get benefit</span></span>

## <span data-ttu-id="c7b23-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7b23-107">EXAMPLES</span></span>

### <span data-ttu-id="c7b23-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7b23-108">Example 1</span></span>
```powershell
PS C:\> New-AzReservation -ReservationOrderId "112382d9-9af7-4fd5-b136-b71f0a69a1d0" -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="c7b23-109">После расчета цены клиент может purcahse эту RI с помощью calculatePrice</span><span class="sxs-lookup"><span data-stu-id="c7b23-109">After calculate price, customer could purcahse that RI provide by calculatePrice</span></span>

## <span data-ttu-id="c7b23-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7b23-110">PARAMETERS</span></span>

### <span data-ttu-id="c7b23-111">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="c7b23-111">-AppliedScope</span></span>
<span data-ttu-id="c7b23-112">Подписка на то, что эта льгота будет применена.</span><span class="sxs-lookup"><span data-stu-id="c7b23-112">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="c7b23-113">Обязательно, если для типа с областью применения задано Single.</span><span class="sxs-lookup"><span data-stu-id="c7b23-113">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="c7b23-114">Не указывайте Shared в качестве типа с областью применения.</span><span class="sxs-lookup"><span data-stu-id="c7b23-114">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="c7b23-115">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="c7b23-115">-AppliedScopeType</span></span>
<span data-ttu-id="c7b23-116">Тип примененной области для обновления резервирования с помощью "Single" или "Shared"</span><span class="sxs-lookup"><span data-stu-id="c7b23-116">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="c7b23-117">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="c7b23-117">-BillingPlan</span></span>
<span data-ttu-id="c7b23-118">Параметры плана выставления счетов, доступные для этого SKU.</span><span class="sxs-lookup"><span data-stu-id="c7b23-118">The billing plan options available for this SKU.</span></span> <span data-ttu-id="c7b23-119">"Ежемесячно" или "передний план"</span><span class="sxs-lookup"><span data-stu-id="c7b23-119">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="c7b23-120">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="c7b23-120">-BillingScopeId</span></span>
<span data-ttu-id="c7b23-121">Подписка на план, который будет оплачиваться за закупок.</span><span class="sxs-lookup"><span data-stu-id="c7b23-121">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="c7b23-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b23-122">-DefaultProfile</span></span>
<span data-ttu-id="c7b23-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b23-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7b23-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c7b23-124">-DisplayName</span></span>
<span data-ttu-id="c7b23-125">Понятное имя пользователя, которое легко идентифицировать резервирование.</span><span class="sxs-lookup"><span data-stu-id="c7b23-125">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="c7b23-126">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="c7b23-126">-InstanceFlexibility</span></span>
<span data-ttu-id="c7b23-127">{{Fill InstanceFlexibility Description}}</span><span class="sxs-lookup"><span data-stu-id="c7b23-127">{{ Fill InstanceFlexibility Description }}</span></span>

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

### <span data-ttu-id="c7b23-128">-Location</span><span class="sxs-lookup"><span data-stu-id="c7b23-128">-Location</span></span>
<span data-ttu-id="c7b23-129">Расположение, которое доступно для SKU.</span><span class="sxs-lookup"><span data-stu-id="c7b23-129">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="c7b23-130">-Количество</span><span class="sxs-lookup"><span data-stu-id="c7b23-130">-Quantity</span></span>
<span data-ttu-id="c7b23-131">Количество продуктов для расчета цен или покупок.</span><span class="sxs-lookup"><span data-stu-id="c7b23-131">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="c7b23-132">-Продление подписки</span><span class="sxs-lookup"><span data-stu-id="c7b23-132">-Renew</span></span>
<span data-ttu-id="c7b23-133">Если установить для этого значения значение истина, Дата окончания срока действия будет автоматически присвоена новому резервированию.</span><span class="sxs-lookup"><span data-stu-id="c7b23-133">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="c7b23-134">-ReservationOrderId</span><span class="sxs-lookup"><span data-stu-id="c7b23-134">-ReservationOrderId</span></span>
<span data-ttu-id="c7b23-135">Код заказа на резервирование для покупки, создание с резервированием для резервирования за AZ.</span><span class="sxs-lookup"><span data-stu-id="c7b23-135">Id of reservation order to purchase, generate by az reservations reservation-order calculate.</span></span>

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

### <span data-ttu-id="c7b23-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="c7b23-136">-ReservedResourceType</span></span>
<span data-ttu-id="c7b23-137">Тип ресурса, для которого необходимо предоставить SKU.</span><span class="sxs-lookup"><span data-stu-id="c7b23-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="c7b23-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="c7b23-138">-Sku</span></span>
<span data-ttu-id="c7b23-139">Название SKU</span><span class="sxs-lookup"><span data-stu-id="c7b23-139">Sku name</span></span>

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

### <span data-ttu-id="c7b23-140">-Term</span><span class="sxs-lookup"><span data-stu-id="c7b23-140">-Term</span></span>
<span data-ttu-id="c7b23-141">Доступные условия резервирования для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="c7b23-141">Available reservation terms for this resource.</span></span>


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

### <span data-ttu-id="c7b23-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7b23-142">-Confirm</span></span>
<span data-ttu-id="c7b23-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7b23-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7b23-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7b23-144">-WhatIf</span></span>
<span data-ttu-id="c7b23-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7b23-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7b23-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7b23-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7b23-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b23-147">CommonParameters</span></span>
<span data-ttu-id="c7b23-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7b23-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b23-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7b23-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b23-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7b23-150">INPUTS</span></span>

### <span data-ttu-id="c7b23-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="c7b23-151">None</span></span>

## <span data-ttu-id="c7b23-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b23-152">OUTPUTS</span></span>

### <span data-ttu-id="c7b23-153">Microsoft. Azure. Management. резервирования. Models. ReservationOrderResponse</span><span class="sxs-lookup"><span data-stu-id="c7b23-153">Microsoft.Azure.Management.Reservations.Models.ReservationOrderResponse</span></span>

## <span data-ttu-id="c7b23-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7b23-154">NOTES</span></span>

## <span data-ttu-id="c7b23-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7b23-155">RELATED LINKS</span></span>
