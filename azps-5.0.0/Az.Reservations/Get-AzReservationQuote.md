---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Reservations.dll-Help.xml
Module Name: Az.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/az.reservations/get-azreservationquote
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Reservations/Reservations/help/Get-AzReservationQuote.md
ms.openlocfilehash: 844e67f7491825fe0484a60d55cb254988cfb5c9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246363"
---
# <span data-ttu-id="2027f-101">Get-AzReservationQuote</span><span class="sxs-lookup"><span data-stu-id="2027f-101">Get-AzReservationQuote</span></span>

## <span data-ttu-id="2027f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2027f-102">SYNOPSIS</span></span>
<span data-ttu-id="2027f-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="2027f-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="2027f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2027f-104">SYNTAX</span></span>

```
Get-AzReservationQuote -ReservedResourceType <String> -Sku <String> [-Location <String>]
 -BillingScopeId <String> -Term <String> [-BillingPlan <String>] -Quantity <Int32> -DisplayName <String>
 -AppliedScopeType <String> [-AppliedScope <String>] [-Renew <Boolean>] [-InstanceFlexibility <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2027f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2027f-105">DESCRIPTION</span></span>
<span data-ttu-id="2027f-106">Рассчитайте цену за размещение заказа на резервирование.</span><span class="sxs-lookup"><span data-stu-id="2027f-106">Calculate price for placing a reservation order.</span></span>

## <span data-ttu-id="2027f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2027f-107">EXAMPLES</span></span>

### <span data-ttu-id="2027f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2027f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzReservationQuote -ReservedResourceType "VirtualMachines" [-Sku "standard b1"] -Location "centralus"
-BillingScopeId "/subscriptions/79c182d9-9af7-4fd5-b136-b71f0a69a1d0" -Term "P1Y" [-BillingPlan "Monthly"] -Quantity 2 [-DisplayName "demo"] -AppliedScopeType "Shared" [-AppliedScopes ""]
```

<span data-ttu-id="2027f-109">После того как вы получите доступ к каталогу, клиент может получить и другие продукты на основе местоположения.</span><span class="sxs-lookup"><span data-stu-id="2027f-109">After get catalog, customer can get the differe product based on location.</span></span> <span data-ttu-id="2027f-110">С помощью этих сведений проверьте правильность цены.</span><span class="sxs-lookup"><span data-stu-id="2027f-110">By using those infomation, check the price properly</span></span>

## <span data-ttu-id="2027f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2027f-111">PARAMETERS</span></span>

### <span data-ttu-id="2027f-112">-AppliedScope</span><span class="sxs-lookup"><span data-stu-id="2027f-112">-AppliedScope</span></span>
<span data-ttu-id="2027f-113">Подписка на то, что эта льгота будет применена.</span><span class="sxs-lookup"><span data-stu-id="2027f-113">Subscription that the benefit will be applied.</span></span> <span data-ttu-id="2027f-114">Обязательно, если для типа с областью применения задано Single.</span><span class="sxs-lookup"><span data-stu-id="2027f-114">Required if --applied-scope-type is Single.</span></span> <span data-ttu-id="2027f-115">Не указывайте Shared в качестве типа с областью применения.</span><span class="sxs-lookup"><span data-stu-id="2027f-115">Do not specify if --applied-scope-type is Shared.</span></span>

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

### <span data-ttu-id="2027f-116">-AppliedScopeType</span><span class="sxs-lookup"><span data-stu-id="2027f-116">-AppliedScopeType</span></span>
<span data-ttu-id="2027f-117">Тип примененной области для обновления резервирования с помощью "Single" или "Shared"</span><span class="sxs-lookup"><span data-stu-id="2027f-117">Type of the Applied Scope to update the reservation with "Single" or "Shared"</span></span>

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

### <span data-ttu-id="2027f-118">-BillingPlan</span><span class="sxs-lookup"><span data-stu-id="2027f-118">-BillingPlan</span></span>
<span data-ttu-id="2027f-119">Параметры плана выставления счетов, доступные для этого SKU.</span><span class="sxs-lookup"><span data-stu-id="2027f-119">The billing plan options available for this SKU.</span></span> <span data-ttu-id="2027f-120">"Ежемесячно" или "передний план"</span><span class="sxs-lookup"><span data-stu-id="2027f-120">"Monthly" or "Upfront"</span></span>

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

### <span data-ttu-id="2027f-121">-BillingScopeId</span><span class="sxs-lookup"><span data-stu-id="2027f-121">-BillingScopeId</span></span>
<span data-ttu-id="2027f-122">Подписка на план, который будет оплачиваться за закупок.</span><span class="sxs-lookup"><span data-stu-id="2027f-122">Subscription that will be charged for purchasing Reservation.</span></span>

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

### <span data-ttu-id="2027f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2027f-123">-DefaultProfile</span></span>
<span data-ttu-id="2027f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2027f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2027f-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2027f-125">-DisplayName</span></span>
<span data-ttu-id="2027f-126">Понятное имя пользователя, которое легко идентифицировать резервирование.</span><span class="sxs-lookup"><span data-stu-id="2027f-126">Friendly name for user to easily identified the reservation.</span></span>

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

### <span data-ttu-id="2027f-127">-InstanceFlexibility</span><span class="sxs-lookup"><span data-stu-id="2027f-127">-InstanceFlexibility</span></span>
<span data-ttu-id="2027f-128">Тип гибкости экземпляра, с которым можно обновить резервирование.</span><span class="sxs-lookup"><span data-stu-id="2027f-128">Type of the Instance Flexibility to update the reservation with.</span></span>

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

### <span data-ttu-id="2027f-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2027f-129">-Location</span></span>
<span data-ttu-id="2027f-130">Расположение, которое доступно для SKU.</span><span class="sxs-lookup"><span data-stu-id="2027f-130">Location that the SKU is available.</span></span>

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

### <span data-ttu-id="2027f-131">-Количество</span><span class="sxs-lookup"><span data-stu-id="2027f-131">-Quantity</span></span>
<span data-ttu-id="2027f-132">Количество продуктов для расчета цен или покупок.</span><span class="sxs-lookup"><span data-stu-id="2027f-132">Quantity of product for calculating price or purchasing.</span></span>

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

### <span data-ttu-id="2027f-133">-Продление подписки</span><span class="sxs-lookup"><span data-stu-id="2027f-133">-Renew</span></span>
<span data-ttu-id="2027f-134">Если установить для этого значения значение истина, Дата окончания срока действия будет автоматически присвоена новому резервированию.</span><span class="sxs-lookup"><span data-stu-id="2027f-134">Set this to true will automatically purchase a new reservation on the expiration date time.</span></span>

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

### <span data-ttu-id="2027f-135">-ReservedResourceType</span><span class="sxs-lookup"><span data-stu-id="2027f-135">-ReservedResourceType</span></span>
<span data-ttu-id="2027f-136">Тип ресурса, для которого необходимо предоставить SKU.</span><span class="sxs-lookup"><span data-stu-id="2027f-136">Type of the resource for which the skus should be provided.</span></span>

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

### <span data-ttu-id="2027f-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="2027f-137">-Sku</span></span>
<span data-ttu-id="2027f-138">Название SKU, получение списка SKU с помощью команды "резервирование", "Показать каталог"</span><span class="sxs-lookup"><span data-stu-id="2027f-138">Sku name, get the sku list by using command az reservations catalog show</span></span>

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

### <span data-ttu-id="2027f-139">-Term</span><span class="sxs-lookup"><span data-stu-id="2027f-139">-Term</span></span>
<span data-ttu-id="2027f-140">Доступные условия резервирования для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="2027f-140">Available reservation terms for this resource.</span></span>

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

### <span data-ttu-id="2027f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2027f-141">CommonParameters</span></span>
<span data-ttu-id="2027f-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2027f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2027f-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2027f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2027f-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2027f-144">INPUTS</span></span>

### <span data-ttu-id="2027f-145">Ничего</span><span class="sxs-lookup"><span data-stu-id="2027f-145">None</span></span>

## <span data-ttu-id="2027f-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2027f-146">OUTPUTS</span></span>

### <span data-ttu-id="2027f-147">Microsoft. Azure. Management. резервирования. Models. CalculatePriceResponse</span><span class="sxs-lookup"><span data-stu-id="2027f-147">Microsoft.Azure.Management.Reservations.Models.CalculatePriceResponse</span></span>

## <span data-ttu-id="2027f-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2027f-148">NOTES</span></span>

## <span data-ttu-id="2027f-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2027f-149">RELATED LINKS</span></span>
