---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012568"
---
# <span data-ttu-id="ca431-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="ca431-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="ca431-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca431-102">SYNOPSIS</span></span>
<span data-ttu-id="ca431-103">Создание ресурса организации</span><span class="sxs-lookup"><span data-stu-id="ca431-103">Create Organization resource</span></span>

## <span data-ttu-id="ca431-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca431-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ca431-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca431-105">DESCRIPTION</span></span>
<span data-ttu-id="ca431-106">Создание ресурса организации</span><span class="sxs-lookup"><span data-stu-id="ca431-106">Create Organization resource</span></span>

## <span data-ttu-id="ca431-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca431-107">EXAMPLES</span></span>

### <span data-ttu-id="ca431-108">Пример 1. Создание организации с слияниями</span><span class="sxs-lookup"><span data-stu-id="ca431-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="ca431-109">Эта команда создает организацию с слиянием.</span><span class="sxs-lookup"><span data-stu-id="ca431-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="ca431-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca431-110">PARAMETERS</span></span>

### <span data-ttu-id="ca431-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca431-111">-AsJob</span></span>
<span data-ttu-id="ca431-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ca431-112">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca431-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca431-113">-DefaultProfile</span></span>
<span data-ttu-id="ca431-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca431-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca431-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ca431-115">-Location</span></span>
<span data-ttu-id="ca431-116">Расположение ресурса организации</span><span class="sxs-lookup"><span data-stu-id="ca431-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="ca431-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ca431-117">-Name</span></span>
<span data-ttu-id="ca431-118">Название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="ca431-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca431-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ca431-119">-NoWait</span></span>
<span data-ttu-id="ca431-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ca431-120">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca431-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="ca431-121">-OfferDetailId</span></span>
<span data-ttu-id="ca431-122">ИД предложения</span><span class="sxs-lookup"><span data-stu-id="ca431-122">Offer Id</span></span>

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

### <span data-ttu-id="ca431-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="ca431-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="ca431-124">ИД плана предложения</span><span class="sxs-lookup"><span data-stu-id="ca431-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="ca431-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="ca431-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="ca431-126">Название плана предложения</span><span class="sxs-lookup"><span data-stu-id="ca431-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="ca431-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="ca431-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="ca431-128">ИД Издателя</span><span class="sxs-lookup"><span data-stu-id="ca431-128">Publisher Id</span></span>

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

### <span data-ttu-id="ca431-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="ca431-129">-OfferDetailStatus</span></span>
<span data-ttu-id="ca431-130">Состояние предложения SaaS</span><span class="sxs-lookup"><span data-stu-id="ca431-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca431-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="ca431-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="ca431-132">Единица срока действия плана предложения</span><span class="sxs-lookup"><span data-stu-id="ca431-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="ca431-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca431-133">-ResourceGroupName</span></span>
<span data-ttu-id="ca431-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ca431-134">Resource group name</span></span>

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

### <span data-ttu-id="ca431-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca431-135">-SubscriptionId</span></span>
<span data-ttu-id="ca431-136">ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="ca431-136">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="ca431-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca431-137">-Tag</span></span>
<span data-ttu-id="ca431-138">Теги ресурсов организации</span><span class="sxs-lookup"><span data-stu-id="ca431-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca431-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca431-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="ca431-140">Адрес электронной почты</span><span class="sxs-lookup"><span data-stu-id="ca431-140">Email address</span></span>

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

### <span data-ttu-id="ca431-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="ca431-141">-UserDetailFirstName</span></span>
<span data-ttu-id="ca431-142">Имя</span><span class="sxs-lookup"><span data-stu-id="ca431-142">First name</span></span>

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

### <span data-ttu-id="ca431-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="ca431-143">-UserDetailLastName</span></span>
<span data-ttu-id="ca431-144">Фамилия</span><span class="sxs-lookup"><span data-stu-id="ca431-144">Last name</span></span>

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

### <span data-ttu-id="ca431-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca431-145">-Confirm</span></span>
<span data-ttu-id="ca431-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ca431-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca431-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca431-147">-WhatIf</span></span>
<span data-ttu-id="ca431-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca431-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca431-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ca431-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca431-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca431-150">CommonParameters</span></span>
<span data-ttu-id="ca431-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca431-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca431-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca431-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca431-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca431-153">INPUTS</span></span>

## <span data-ttu-id="ca431-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca431-154">OUTPUTS</span></span>

### <span data-ttu-id="ca431-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="ca431-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="ca431-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca431-156">NOTES</span></span>

<span data-ttu-id="ca431-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ca431-157">ALIASES</span></span>

## <span data-ttu-id="ca431-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca431-158">RELATED LINKS</span></span>

