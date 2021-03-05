---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/update-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/Update-AzConfluentOrganization.md
ms.openlocfilehash: 7332d3154e87da2d9249dc16e3986efd636b737a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012563"
---
# <span data-ttu-id="23b31-101">Update-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="23b31-101">Update-AzConfluentOrganization</span></span>

## <span data-ttu-id="23b31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b31-102">SYNOPSIS</span></span>
<span data-ttu-id="23b31-103">Обновление ресурса организации</span><span class="sxs-lookup"><span data-stu-id="23b31-103">Update Organization resource</span></span>

## <span data-ttu-id="23b31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23b31-104">SYNTAX</span></span>

### <span data-ttu-id="23b31-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23b31-105">UpdateExpanded (Default)</span></span>
```
Update-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="23b31-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="23b31-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConfluentOrganization -InputObject <IConfluentIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23b31-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23b31-107">DESCRIPTION</span></span>
<span data-ttu-id="23b31-108">Обновление ресурса организации</span><span class="sxs-lookup"><span data-stu-id="23b31-108">Update Organization resource</span></span>

## <span data-ttu-id="23b31-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23b31-109">EXAMPLES</span></span>

### <span data-ttu-id="23b31-110">Пример 1. Обновление организации по имени</span><span class="sxs-lookup"><span data-stu-id="23b31-110">Example 1: Update a confluent organization by name</span></span>
```powershell
PS C:\> pdate-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Tag @{"key01" = "value01"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="23b31-111">Эта команда обновляет организацию по имени.</span><span class="sxs-lookup"><span data-stu-id="23b31-111">This command updates a confluent organization by name.</span></span>

### <span data-ttu-id="23b31-112">Пример 2. Обновление организации с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="23b31-112">Example 2: Update a confluent organization by pipeline</span></span>
```powershell
PS C:\> Get-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh | Update-AzConfluentOrganization -Tag @{"key01" = "value01"; "key02"="value02"}

Location Name                 Type
-------- ----                 ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="23b31-113">Эта команда обновляет объединенные организации по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="23b31-113">This command updates a confluent organization by pipeline.</span></span>

## <span data-ttu-id="23b31-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23b31-114">PARAMETERS</span></span>

### <span data-ttu-id="23b31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b31-115">-DefaultProfile</span></span>
<span data-ttu-id="23b31-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23b31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b31-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23b31-117">-InputObject</span></span>
<span data-ttu-id="23b31-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="23b31-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-119">-Name</span><span class="sxs-lookup"><span data-stu-id="23b31-119">-Name</span></span>
<span data-ttu-id="23b31-120">Название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="23b31-120">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b31-121">-ResourceGroupName</span></span>
<span data-ttu-id="23b31-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="23b31-122">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23b31-123">-SubscriptionId</span></span>
<span data-ttu-id="23b31-124">ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="23b31-124">Microsoft Azure subscription id</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b31-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="23b31-125">-Tag</span></span>
<span data-ttu-id="23b31-126">ARM тегов ресурсов</span><span class="sxs-lookup"><span data-stu-id="23b31-126">ARM resource tags</span></span>

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

### <span data-ttu-id="23b31-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23b31-127">-Confirm</span></span>
<span data-ttu-id="23b31-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b31-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23b31-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b31-129">-WhatIf</span></span>
<span data-ttu-id="23b31-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b31-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23b31-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23b31-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23b31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b31-132">CommonParameters</span></span>
<span data-ttu-id="23b31-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b31-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23b31-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b31-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23b31-135">INPUTS</span></span>

### <span data-ttu-id="23b31-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span><span class="sxs-lookup"><span data-stu-id="23b31-136">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.IConfluentIdentity</span></span>

## <span data-ttu-id="23b31-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23b31-137">OUTPUTS</span></span>

### <span data-ttu-id="23b31-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="23b31-138">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="23b31-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23b31-139">NOTES</span></span>

<span data-ttu-id="23b31-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="23b31-140">ALIASES</span></span>

<span data-ttu-id="23b31-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="23b31-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23b31-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="23b31-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23b31-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="23b31-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23b31-144">INPUTOBJECT <IConfluentIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="23b31-144">INPUTOBJECT <IConfluentIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="23b31-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="23b31-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="23b31-146">`[OrganizationName <String>]`: название ресурса организации</span><span class="sxs-lookup"><span data-stu-id="23b31-146">`[OrganizationName <String>]`: Organization resource name</span></span>
  - <span data-ttu-id="23b31-147">`[ResourceGroupName <String>]`: название группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="23b31-147">`[ResourceGroupName <String>]`: Resource group name</span></span>
  - <span data-ttu-id="23b31-148">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="23b31-148">`[SubscriptionId <String>]`: Microsoft Azure subscription id</span></span>

## <span data-ttu-id="23b31-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23b31-149">RELATED LINKS</span></span>

