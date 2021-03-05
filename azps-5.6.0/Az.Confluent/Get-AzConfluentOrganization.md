---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/get-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Get-AzConfluentOrganization.md
ms.openlocfilehash: dcac6e7ce7e4c8daed2e2f8b43c44c2da82acd93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012595"
---
# <span data-ttu-id="91f38-101">Get-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="91f38-101">Get-AzConfluentOrganization</span></span>

## <span data-ttu-id="91f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91f38-102">SYNOPSIS</span></span>
<span data-ttu-id="91f38-103">Получите свойства определенного ресурса организации.</span><span class="sxs-lookup"><span data-stu-id="91f38-103">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="91f38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91f38-104">SYNTAX</span></span>

### <span data-ttu-id="91f38-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91f38-105">List (Default)</span></span>
```
Get-AzConfluentOrganization [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91f38-106">Получить</span><span class="sxs-lookup"><span data-stu-id="91f38-106">Get</span></span>
```
Get-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="91f38-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="91f38-107">GetViaIdentity</span></span>
```
Get-AzConfluentOrganization -InputObject <IConfluentIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="91f38-108">List1</span><span class="sxs-lookup"><span data-stu-id="91f38-108">List1</span></span>
```
Get-AzConfluentOrganization -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="91f38-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91f38-109">DESCRIPTION</span></span>
<span data-ttu-id="91f38-110">Получите свойства определенного ресурса организации.</span><span class="sxs-lookup"><span data-stu-id="91f38-110">Get the properties of a specific Organization resource.</span></span>

## <span data-ttu-id="91f38-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91f38-111">EXAMPLES</span></span>

### <span data-ttu-id="91f38-112">Пример 1. Список всех организаций с слиянием в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="91f38-112">Example 1: List all confluent organizations under a subscription</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization

Location      Name                     Type
--------      ----                     ----
westus2       RegionTestWestUS2        Microsoft.Confluent/organizations
westus2       RohitWUS2                Microsoft.Confluent/organizations
westus2       Rohit-Secret             Microsoft.Confluent/organizations
westus2       Rohit-Secret-2           Microsoft.Confluent/organizations
westus2       Rohit-Secret-WUS2-0      Microsoft.Confluent/organizations
westus2       RohitWus200              Microsoft.Confluent/organizations
westus2       RohitWUS300              Microsoft.Confluent/organizations
westus2       WestUS2-SSOTest          Microsoft.Confluent/organizations
westus2       dri-01-02-postman-stable Microsoft.Confluent/organizations
westus2       dri-02-02                Microsoft.Confluent/organizations
westcentralus RohitWCUS88              Microsoft.Confluent/organizations
```

<span data-ttu-id="91f38-113">Эта команда содержит список всех организаций, которые имеют подписку.</span><span class="sxs-lookup"><span data-stu-id="91f38-113">This command lists all confluent organizations under a subscription.</span></span>

### <span data-ttu-id="91f38-114">Пример 2. Список всех организаций, объединенных в группу ресурсов</span><span class="sxs-lookup"><span data-stu-id="91f38-114">Example 2: List all confluent organizations under a resource group</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test

Location    Name          Type
--------    ----          ----
eastus2euap ppe-metrics-2 Microsoft.Confluent/organizations
```

<span data-ttu-id="91f38-115">Эта команда содержит список всех организаций, объединенных в группу ресурсов.</span><span class="sxs-lookup"><span data-stu-id="91f38-115">This command lists all confluent organizations under a resource group.</span></span>

### <span data-ttu-id="91f38-116">Пример 3. Организация с слиянием по имени</span><span class="sxs-lookup"><span data-stu-id="91f38-116">Example 3: Get a confluent organization by name</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-01-portal

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-01-portal Microsoft.Confluent/organizations
```

<span data-ttu-id="91f38-117">Эта команда получает организацию по имени.</span><span class="sxs-lookup"><span data-stu-id="91f38-117">This command gets a confluent organization by name.</span></span>

### <span data-ttu-id="91f38-118">Пример 4. Организация с каналом слияния</span><span class="sxs-lookup"><span data-stu-id="91f38-118">Example 4: Get a confluent organization by pipeline</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" | Get-AzConfluentOrganization

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="91f38-119">Эта команда получает организацию в канале слияния.</span><span class="sxs-lookup"><span data-stu-id="91f38-119">This command gets a confluent organization by pipeline.</span></span>

## <span data-ttu-id="91f38-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91f38-120">PARAMETERS</span></span>

### <span data-ttu-id="91f38-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f38-121">-DefaultProfile</span></span>
<span data-ttu-id="91f38-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91f38-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f38-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91f38-123">-InputObject</span></span>
<span data-ttu-id="91f38-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="91f38-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91f38-125">-Name</span><span class="sxs-lookup"><span data-stu-id="91f38-125">-Name</span></span>
<span data-ttu-id="91f38-126">Название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="91f38-126">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f38-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91f38-127">-ResourceGroupName</span></span>
<span data-ttu-id="91f38-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="91f38-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f38-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="91f38-129">-SubscriptionId</span></span>
<span data-ttu-id="91f38-130">ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="91f38-130">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91f38-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f38-131">CommonParameters</span></span>
<span data-ttu-id="91f38-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f38-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f38-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91f38-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f38-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91f38-134">INPUTS</span></span>

### <span data-ttu-id="91f38-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="91f38-135">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="91f38-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91f38-136">OUTPUTS</span></span>

### <span data-ttu-id="91f38-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="91f38-137">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="91f38-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91f38-138">NOTES</span></span>

<span data-ttu-id="91f38-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="91f38-139">ALIASES</span></span>

<span data-ttu-id="91f38-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="91f38-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="91f38-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="91f38-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="91f38-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="91f38-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="91f38-143">INPUTOBJECT <IConfluentIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="91f38-143">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="91f38-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="91f38-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="91f38-145">`[OrganizationName <String>]`: название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="91f38-145">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="91f38-146">`[ResourceGroupName <String>]`: имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="91f38-146">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="91f38-147">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="91f38-147">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="91f38-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91f38-148">RELATED LINKS</span></span>

