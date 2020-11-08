---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 8a3797006bb5006b1b4e715b45c5e12763c49f32
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/22/2020
ms.locfileid: "94075097"
---
# <span data-ttu-id="4d802-101">New-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4d802-101">New-AzsOfferDelegation</span></span>

## <span data-ttu-id="4d802-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4d802-102">SYNOPSIS</span></span>
<span data-ttu-id="4d802-103">Создание или обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="4d802-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="4d802-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4d802-104">SYNTAX</span></span>

### <span data-ttu-id="4d802-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d802-105">CreateExpanded (Default)</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-TargetSubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4d802-106">Заново</span><span class="sxs-lookup"><span data-stu-id="4d802-106">Create</span></span>
```
New-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4d802-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d802-107">DESCRIPTION</span></span>
<span data-ttu-id="4d802-108">Создание или обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="4d802-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="4d802-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4d802-109">EXAMPLES</span></span>

### <span data-ttu-id="4d802-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d802-110">Example 1</span></span>
```powershell
PS C:\> New-AzsOfferDelegation -Name "testofferdelegation" -OfferName "testoffer" -ResourceGroupName "testrg" -TargetSubscriptionId "dbc27112-f67a-4690-ba12-730f71cba018"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer/offerDelegations/testofferdel
                 egation
Location       : redmond
Name           : testoffer/testofferdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cba018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="4d802-111">Создание нового делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="4d802-111">Create a new offer delegation.</span></span>

## <span data-ttu-id="4d802-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4d802-112">PARAMETERS</span></span>

### <span data-ttu-id="4d802-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d802-113">-DefaultProfile</span></span>
<span data-ttu-id="4d802-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d802-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4d802-115">-Location</span><span class="sxs-lookup"><span data-stu-id="4d802-115">-Location</span></span>
<span data-ttu-id="4d802-116">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="4d802-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4d802-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4d802-117">-Name</span></span>
<span data-ttu-id="4d802-118">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="4d802-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="4d802-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="4d802-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="4d802-120">Делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="4d802-120">Offer delegation.</span></span>
<span data-ttu-id="4d802-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств OFFERDELEGATIONDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4d802-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4d802-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="4d802-122">-OfferName</span></span>
<span data-ttu-id="4d802-123">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="4d802-123">Name of an offer.</span></span>

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

### <span data-ttu-id="4d802-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d802-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d802-125">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="4d802-125">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4d802-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d802-126">-SubscriptionId</span></span>
<span data-ttu-id="4d802-127">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4d802-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4d802-128">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d802-128">-TargetSubscriptionId</span></span>
<span data-ttu-id="4d802-129">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="4d802-129">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4d802-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d802-130">-Confirm</span></span>
<span data-ttu-id="4d802-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4d802-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d802-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d802-132">-WhatIf</span></span>
<span data-ttu-id="4d802-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4d802-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d802-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4d802-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d802-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d802-135">CommonParameters</span></span>
<span data-ttu-id="4d802-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4d802-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d802-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d802-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d802-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4d802-138">INPUTS</span></span>

### <span data-ttu-id="4d802-139">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4d802-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="4d802-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d802-140">OUTPUTS</span></span>

### <span data-ttu-id="4d802-141">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="4d802-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="4d802-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4d802-142">ALIASES</span></span>

## <span data-ttu-id="4d802-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4d802-143">NOTES</span></span>

<span data-ttu-id="4d802-144">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4d802-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4d802-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4d802-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4d802-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="4d802-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="4d802-147">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="4d802-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="4d802-148">`[SubscriptionId <String>]`: Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="4d802-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="4d802-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d802-149">RELATED LINKS</span></span>

