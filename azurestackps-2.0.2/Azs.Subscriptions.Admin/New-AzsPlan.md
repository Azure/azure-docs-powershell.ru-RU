---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsplan
schema: 2.0.0
ms.openlocfilehash: 213ae5a86675f6aea43377d298d339a00b37856d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94077084"
---
# <span data-ttu-id="15c52-101">New-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="15c52-101">New-AzsPlan</span></span>

## <span data-ttu-id="15c52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15c52-102">SYNOPSIS</span></span>
<span data-ttu-id="15c52-103">Создайте или обновите план.</span><span class="sxs-lookup"><span data-stu-id="15c52-103">Create or update the plan.</span></span>

## <span data-ttu-id="15c52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15c52-104">SYNTAX</span></span>

### <span data-ttu-id="15c52-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15c52-105">CreateExpanded (Default)</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -QuotaIds <String[]> [-SubscriptionId <String>]
 [-Description <String>] [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-PropertiesName <String>] [-SkuIds <String[]>] [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="15c52-106">Заново</span><span class="sxs-lookup"><span data-stu-id="15c52-106">Create</span></span>
```
New-AzsPlan -Name <String> -ResourceGroupName <String> -PlanDefinition <IPlan> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="15c52-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15c52-107">DESCRIPTION</span></span>
<span data-ttu-id="15c52-108">Создайте или обновите план.</span><span class="sxs-lookup"><span data-stu-id="15c52-108">Create or update the plan.</span></span>

## <span data-ttu-id="15c52-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15c52-109">EXAMPLES</span></span>

### <span data-ttu-id="15c52-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15c52-110">Example 1</span></span>
```powershell
PS C:\> New-AzsPlan -Name "testplan" -ResourceGroupName "testrg" -QuotaIds "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota" -Description "testplan"

Description         : testplan
DisplayName         : testplan
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan
Location            : redmond
Name                : testplan
PropertiesName      : testplan
QuotaIds            : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/locations/redmond/quotas/delegatedProviderQuota}
SkuIds              : 
SubscriptionCount   : 0
Tags                : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                : Microsoft.Subscriptions.Admin/plans
```

<span data-ttu-id="15c52-111">Создание нового плана</span><span class="sxs-lookup"><span data-stu-id="15c52-111">Creates a new plan</span></span>

## <span data-ttu-id="15c52-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15c52-112">PARAMETERS</span></span>

### <span data-ttu-id="15c52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15c52-113">-DefaultProfile</span></span>
<span data-ttu-id="15c52-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15c52-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15c52-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="15c52-115">-Description</span></span>
<span data-ttu-id="15c52-116">Описание плана.</span><span class="sxs-lookup"><span data-stu-id="15c52-116">Description of the plan.</span></span>

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

### <span data-ttu-id="15c52-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15c52-117">-DisplayName</span></span>
<span data-ttu-id="15c52-118">Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="15c52-118">Display name.</span></span>

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

### <span data-ttu-id="15c52-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="15c52-119">-ExternalReferenceId</span></span>
<span data-ttu-id="15c52-120">Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="15c52-120">External reference identifier.</span></span>

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

### <span data-ttu-id="15c52-121">-Location</span><span class="sxs-lookup"><span data-stu-id="15c52-121">-Location</span></span>
<span data-ttu-id="15c52-122">Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="15c52-122">Location of the resource</span></span>

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

### <span data-ttu-id="15c52-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15c52-123">-Name</span></span>
<span data-ttu-id="15c52-124">Название плана.</span><span class="sxs-lookup"><span data-stu-id="15c52-124">Name of the plan.</span></span>

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

### <span data-ttu-id="15c52-125">-PlanDefinition</span><span class="sxs-lookup"><span data-stu-id="15c52-125">-PlanDefinition</span></span>
<span data-ttu-id="15c52-126">План представляет пакет квот и возможностей, которые предлагаются клиентам.</span><span class="sxs-lookup"><span data-stu-id="15c52-126">A plan represents a package of quotas and capabilities that are offered tenants.</span></span>
<span data-ttu-id="15c52-127">Клиент может получить этот план посредством предложения по обновлению доступа к основным облачным службам.</span><span class="sxs-lookup"><span data-stu-id="15c52-127">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
<span data-ttu-id="15c52-128">Для конструирования ознакомьтесь с разделом "Заметки" для свойств PLANDEFINITION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="15c52-128">To construct, see NOTES section for PLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="15c52-129">-PropertiesName</span><span class="sxs-lookup"><span data-stu-id="15c52-129">-PropertiesName</span></span>
<span data-ttu-id="15c52-130">Название плана.</span><span class="sxs-lookup"><span data-stu-id="15c52-130">Name of the plan.</span></span>

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

### <span data-ttu-id="15c52-131">-QuotaIds</span><span class="sxs-lookup"><span data-stu-id="15c52-131">-QuotaIds</span></span>
<span data-ttu-id="15c52-132">Идентификаторы квот в плане.</span><span class="sxs-lookup"><span data-stu-id="15c52-132">Quota identifiers under the plan.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="15c52-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15c52-133">-ResourceGroupName</span></span>
<span data-ttu-id="15c52-134">Группа ресурсов, в которой находится ресурс.</span><span class="sxs-lookup"><span data-stu-id="15c52-134">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="15c52-135">-SkuIds</span><span class="sxs-lookup"><span data-stu-id="15c52-135">-SkuIds</span></span>
<span data-ttu-id="15c52-136">Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="15c52-136">SKU identifiers.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="15c52-137">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="15c52-137">-SubscriptionCount</span></span>
<span data-ttu-id="15c52-138">Число подписок.</span><span class="sxs-lookup"><span data-stu-id="15c52-138">Subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="15c52-139">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15c52-139">-SubscriptionId</span></span>
<span data-ttu-id="15c52-140">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure. Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="15c52-140">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="15c52-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15c52-141">-Confirm</span></span>
<span data-ttu-id="15c52-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15c52-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15c52-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15c52-143">-WhatIf</span></span>
<span data-ttu-id="15c52-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15c52-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15c52-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15c52-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15c52-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15c52-146">CommonParameters</span></span>
<span data-ttu-id="15c52-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15c52-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15c52-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15c52-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15c52-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15c52-149">INPUTS</span></span>

### <span data-ttu-id="15c52-150">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="15c52-150">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

## <span data-ttu-id="15c52-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15c52-151">OUTPUTS</span></span>

### <span data-ttu-id="15c52-152">Microsoft. Azure. PowerShell. командлеты. SubscriptionsAdmin. Models. Api20151101. IPlan</span><span class="sxs-lookup"><span data-stu-id="15c52-152">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlan</span></span>

<span data-ttu-id="15c52-153">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="15c52-153">ALIASES</span></span>

## <span data-ttu-id="15c52-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="15c52-154">NOTES</span></span>

<span data-ttu-id="15c52-155">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15c52-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15c52-156">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15c52-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="15c52-157">PLANDEFINITION <IPlan> : план представляет пакет квот и возможностей, которые предлагаются клиентам.</span><span class="sxs-lookup"><span data-stu-id="15c52-157">PLANDEFINITION <IPlan>: A plan represents a package of quotas and capabilities that are offered tenants.</span></span> <span data-ttu-id="15c52-158">Клиент может получить этот план посредством предложения по обновлению доступа к основным облачным службам.</span><span class="sxs-lookup"><span data-stu-id="15c52-158">A tenant can acquire this plan through an offer to upgrade his access to underlying cloud services.</span></span>
  - <span data-ttu-id="15c52-159">`[Location <String>]`: Расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="15c52-159">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="15c52-160">`[Description <String>]`: Описание плана.</span><span class="sxs-lookup"><span data-stu-id="15c52-160">`[Description <String>]`: Description of the plan.</span></span>
  - <span data-ttu-id="15c52-161">`[DisplayName <String>]`: Отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="15c52-161">`[DisplayName <String>]`: Display name.</span></span>
  - <span data-ttu-id="15c52-162">`[ExternalReferenceId <String>]`: Идентификатор внешней ссылки.</span><span class="sxs-lookup"><span data-stu-id="15c52-162">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="15c52-163">`[PropertiesName <String>]`: Имя плана.</span><span class="sxs-lookup"><span data-stu-id="15c52-163">`[PropertiesName <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="15c52-164">`[QuotaIds <String[]>]`: Идентификаторы квоты в плане.</span><span class="sxs-lookup"><span data-stu-id="15c52-164">`[QuotaIds <String[]>]`: Quota identifiers under the plan.</span></span>
  - <span data-ttu-id="15c52-165">`[SkuIds <String[]>]`: Идентификаторы SKU.</span><span class="sxs-lookup"><span data-stu-id="15c52-165">`[SkuIds <String[]>]`: SKU identifiers.</span></span>
  - <span data-ttu-id="15c52-166">`[SubscriptionCount <Int32?>]`: Количество подписок.</span><span class="sxs-lookup"><span data-stu-id="15c52-166">`[SubscriptionCount <Int32?>]`: Subscription count.</span></span>

## <span data-ttu-id="15c52-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15c52-167">RELATED LINKS</span></span>
