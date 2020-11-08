---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 59afc363d040724bbd525afc6e1f599a995cfdcb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/24/2020
ms.locfileid: "94075336"
---
# <span data-ttu-id="a2eb2-101">Set-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a2eb2-101">Set-AzsOfferDelegation</span></span>

## <span data-ttu-id="a2eb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2eb2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2eb2-103">Создание или обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-103">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a2eb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2eb2-104">SYNTAX</span></span>

### <span data-ttu-id="a2eb2-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Location <String>] [-PropertiesSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a2eb2-106">Обновление</span><span class="sxs-lookup"><span data-stu-id="a2eb2-106">Update</span></span>
```
Set-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 -OfferDelegationDefinition <IOfferDelegation> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2eb2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-107">DESCRIPTION</span></span>
<span data-ttu-id="a2eb2-108">Создание или обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-108">Create or update the offer delegation.</span></span>

## <span data-ttu-id="a2eb2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-109">EXAMPLES</span></span>

### <span data-ttu-id="a2eb2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2eb2-110">Example 1</span></span>
```powershell
PS C:\> Set-AzsOfferDelegation -Offer offer1 -ResourceGroupName rg1 -Name delegate1 -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946" -Location "local"

{{ Add output here }}
```

<span data-ttu-id="a2eb2-111">Обновление делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-111">Updates the offer delegation.</span></span>

## <span data-ttu-id="a2eb2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-112">PARAMETERS</span></span>

### <span data-ttu-id="a2eb2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2eb2-113">-DefaultProfile</span></span>
<span data-ttu-id="a2eb2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2eb2-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a2eb2-115">-Location</span></span>
<span data-ttu-id="a2eb2-116">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="a2eb2-116">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2eb2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a2eb2-117">-Name</span></span>
<span data-ttu-id="a2eb2-118">Имя делегирования предложения.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="a2eb2-119">-OfferDelegationDefinition</span><span class="sxs-lookup"><span data-stu-id="a2eb2-119">-OfferDelegationDefinition</span></span>
<span data-ttu-id="a2eb2-120">Делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-120">Offer delegation.</span></span>
<span data-ttu-id="a2eb2-121">Для конструирования ознакомьтесь с разделом "Заметки" для свойств OFFERDELEGATIONDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-121">To construct, see NOTES section for OFFERDELEGATIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a2eb2-122">-OfferName</span><span class="sxs-lookup"><span data-stu-id="a2eb2-122">-OfferName</span></span>
<span data-ttu-id="a2eb2-123">Название предложения.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-123">Name of an offer.</span></span>

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

### <span data-ttu-id="a2eb2-124">-PropertiesSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-124">-PropertiesSubscriptionId</span></span>
<span data-ttu-id="a2eb2-125">Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-125">Identifier of the subscription receiving the delegated offer.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a2eb2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2eb2-126">-ResourceGroupName</span></span>
<span data-ttu-id="a2eb2-127">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-127">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a2eb2-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2eb2-128">-SubscriptionId</span></span>
<span data-ttu-id="a2eb2-129">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-129">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a2eb2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2eb2-130">-Confirm</span></span>
<span data-ttu-id="a2eb2-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2eb2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2eb2-132">-WhatIf</span></span>
<span data-ttu-id="a2eb2-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2eb2-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2eb2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2eb2-135">CommonParameters</span></span>
<span data-ttu-id="a2eb2-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2eb2-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a2eb2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2eb2-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2eb2-138">INPUTS</span></span>

### <span data-ttu-id="a2eb2-139">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a2eb2-139">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

## <span data-ttu-id="a2eb2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-140">OUTPUTS</span></span>

### <span data-ttu-id="a2eb2-141">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="a2eb2-141">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="a2eb2-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-142">ALIASES</span></span>

## <span data-ttu-id="a2eb2-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2eb2-143">NOTES</span></span>

<span data-ttu-id="a2eb2-144">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-144">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2eb2-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a2eb2-146">OFFERDELEGATIONDEFINITION <IOfferDelegation> : делегирование предложений.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-146">OFFERDELEGATIONDEFINITION <IOfferDelegation>: Offer delegation.</span></span>
  - <span data-ttu-id="a2eb2-147">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="a2eb2-147">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="a2eb2-148">`[SubscriptionId <String>]`: Идентификатор подписки, получающей делегированное предложение.</span><span class="sxs-lookup"><span data-stu-id="a2eb2-148">`[SubscriptionId <String>]`: Identifier of the subscription receiving the delegated offer.</span></span>

## <span data-ttu-id="a2eb2-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2eb2-149">RELATED LINKS</span></span>

