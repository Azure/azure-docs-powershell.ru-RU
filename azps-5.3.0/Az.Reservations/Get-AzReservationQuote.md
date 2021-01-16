---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 073a059063198e91a1bbcc67814c01c1b786e7c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506726"
---
# <span data-ttu-id="f87a4-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="f87a4-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="f87a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f87a4-102">SYNOPSIS</span></span>
<span data-ttu-id="f87a4-103">Получите кавычка для резервирования.</span><span class="sxs-lookup"><span data-stu-id="f87a4-103">Get a quote for the reservation.</span></span> <span data-ttu-id="f87a4-104">Это передается для `New-AzReservation` покупки.</span><span class="sxs-lookup"><span data-stu-id="f87a4-104">This is passed to `New-AzReservation` to purchase.</span></span>

## <span data-ttu-id="f87a4-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f87a4-105">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f87a4-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f87a4-106">DESCRIPTION</span></span>
<span data-ttu-id="f87a4-107">Расчет цены для размещения заказа на резервирование.</span><span class="sxs-lookup"><span data-stu-id="f87a4-107">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="f87a4-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f87a4-108">EXAMPLES</span></span>

### <span data-ttu-id="f87a4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f87a4-109">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="f87a4-110">После получения каталога клиент может получить продукт в зависимости от расположения.</span><span class="sxs-lookup"><span data-stu-id="f87a4-110">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="f87a4-111">Используя эти сведения, проверьте правильное</span><span class="sxs-lookup"><span data-stu-id="f87a4-111">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="f87a4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f87a4-112">PARAMETERS</span></span>

### <span data-ttu-id="f87a4-113">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="f87a4-113">-AppliedScope</span></span>
<span data-ttu-id="f87a4-114">Подписка, в которую будет применено это преимущество.</span><span class="sxs-lookup"><span data-stu-id="f87a4-114">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="f87a4-115">Требуется, если --applied-scope-type is Single.</span><span class="sxs-lookup"><span data-stu-id="f87a4-115">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="f87a4-116">Не укажите, является ли тип "Общий" --applied-scope-type общим.</span><span class="sxs-lookup"><span data-stu-id="f87a4-116">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="f87a4-117">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="f87a4-117">-AppliedScopeType</span></span>
<span data-ttu-id="f87a4-118">Тип применяемой области, чтобы обновить резервирование на "Один" или "Общий"</span><span class="sxs-lookup"><span data-stu-id="f87a4-118">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="f87a4-119">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="f87a4-119">-BillingPlan</span></span>
<span data-ttu-id="f87a4-120">Варианты вы счета, доступные для этого SKU.</span><span class="sxs-lookup"><span data-stu-id="f87a4-120">The billing plan options available for this SKU.</span></span> <span data-ttu-id="f87a4-121">"Monthly" или "Upfront"</span><span class="sxs-lookup"><span data-stu-id="f87a4-121">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="f87a4-122">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="f87a4-122">-BillingScopeId</span></span>
<span data-ttu-id="f87a4-123">Подписка, с которую взимается плата за резервирование для покупки.</span><span class="sxs-lookup"><span data-stu-id="f87a4-123">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="f87a4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87a4-124">-DefaultProfile</span></span>
<span data-ttu-id="f87a4-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f87a4-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f87a4-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f87a4-126">-DisplayName</span></span>
<span data-ttu-id="f87a4-127">Имя, которое легко определить для резервирования.</span><span class="sxs-lookup"><span data-stu-id="f87a4-127">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="f87a4-128">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="f87a4-128">-InstanceFlexibility</span></span>
<span data-ttu-id="f87a4-129">Тип гибкости экземпляра для обновления резервирования.</span><span class="sxs-lookup"><span data-stu-id="f87a4-129">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="f87a4-130">-Location</span><span class="sxs-lookup"><span data-stu-id="f87a4-130">-Location</span></span>
<span data-ttu-id="f87a4-131">Расположение, где находится SKU.</span><span class="sxs-lookup"><span data-stu-id="f87a4-131">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="f87a4-132">-Quantity</span><span class="sxs-lookup"><span data-stu-id="f87a4-132">-Quantity</span></span>
<span data-ttu-id="f87a4-133">Количество продукта для расчета цены или приобретения.</span><span class="sxs-lookup"><span data-stu-id="f87a4-133">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="f87a4-134">-Renew</span><span class="sxs-lookup"><span data-stu-id="f87a4-134">-Renew</span></span>
<span data-ttu-id="f87a4-135">При этом будет автоматически приобретено новое резервирование в срок действия.</span><span class="sxs-lookup"><span data-stu-id="f87a4-135">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="f87a4-136">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="f87a4-136">-ReservedResourceType</span></span>
<span data-ttu-id="f87a4-137">Тип ресурса, для которого должны быть предоставлены skus.</span><span class="sxs-lookup"><span data-stu-id="f87a4-137">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="f87a4-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="f87a4-138">-Sku</span></span>
<span data-ttu-id="f87a4-139">Имя SKU, получить список SKU с помощью каталога резервирования az команды</span><span class="sxs-lookup"><span data-stu-id="f87a4-139">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="f87a4-140">-Term</span><span class="sxs-lookup"><span data-stu-id="f87a4-140">-Term</span></span>
<span data-ttu-id="f87a4-141">Доступные условия резервирования для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f87a4-141">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="f87a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87a4-142">CommonParameters</span></span>
<span data-ttu-id="f87a4-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87a4-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f87a4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87a4-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f87a4-145">INPUTS</span></span>

### <span data-ttu-id="f87a4-146">Нет</span><span class="sxs-lookup"><span data-stu-id="f87a4-146">None</span></span>

## <span data-ttu-id="f87a4-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f87a4-147">OUTPUTS</span></span>

### <span data-ttu-id="f87a4-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="f87a4-148">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="f87a4-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f87a4-149">NOTES</span></span>

## <span data-ttu-id="f87a4-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f87a4-150">RELATED LINKS</span></span>
