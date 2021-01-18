---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507242"
---
# <span data-ttu-id="ec965-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="ec965-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="ec965-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec965-102">SYNOPSIS</span></span>
<span data-ttu-id="ec965-103">Исправление поля "Теги" на мониторе SAP для указанной подписки, группы ресурсов и имени монитора.</span><span class="sxs-lookup"><span data-stu-id="ec965-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ec965-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec965-104">SYNTAX</span></span>

### <span data-ttu-id="ec965-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec965-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ec965-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ec965-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ec965-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec965-107">DESCRIPTION</span></span>
<span data-ttu-id="ec965-108">Исправление поля "Теги" на мониторе SAP для указанной подписки, группы ресурсов и имени монитора.</span><span class="sxs-lookup"><span data-stu-id="ec965-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="ec965-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec965-109">EXAMPLES</span></span>

### <span data-ttu-id="ec965-110">Пример 1. Обновление монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="ec965-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ec965-111">Эта команда обновляет монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="ec965-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="ec965-112">Пример 2. Обновление монитора SAP по объектам</span><span class="sxs-lookup"><span data-stu-id="ec965-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="ec965-113">Эта команда обновляет монитор SAP по объектам.</span><span class="sxs-lookup"><span data-stu-id="ec965-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="ec965-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec965-114">PARAMETERS</span></span>

### <span data-ttu-id="ec965-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec965-115">-DefaultProfile</span></span>
<span data-ttu-id="ec965-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec965-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec965-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec965-117">-InputObject</span></span>
<span data-ttu-id="ec965-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ec965-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec965-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ec965-119">-Name</span></span>
<span data-ttu-id="ec965-120">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="ec965-120">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec965-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec965-121">-ResourceGroupName</span></span>
<span data-ttu-id="ec965-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec965-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="ec965-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ec965-123">-SubscriptionId</span></span>
<span data-ttu-id="ec965-124">Идентификация подписки, однозначно определяемая подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec965-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ec965-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ec965-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ec965-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec965-126">-Tag</span></span>
<span data-ttu-id="ec965-127">Поле тегов ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec965-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="ec965-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec965-128">-Confirm</span></span>
<span data-ttu-id="ec965-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec965-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec965-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec965-130">-WhatIf</span></span>
<span data-ttu-id="ec965-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec965-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec965-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ec965-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec965-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec965-133">CommonParameters</span></span>
<span data-ttu-id="ec965-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec965-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec965-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec965-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec965-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec965-136">INPUTS</span></span>

### <span data-ttu-id="ec965-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="ec965-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="ec965-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec965-138">OUTPUTS</span></span>

### <span data-ttu-id="ec965-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="ec965-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="ec965-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec965-140">NOTES</span></span>

<span data-ttu-id="ec965-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ec965-141">ALIASES</span></span>

<span data-ttu-id="ec965-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ec965-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ec965-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ec965-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ec965-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ec965-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ec965-145">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ec965-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ec965-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ec965-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ec965-147">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="ec965-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="ec965-148">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="ec965-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="ec965-149">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="ec965-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="ec965-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec965-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ec965-151">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="ec965-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="ec965-152">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="ec965-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="ec965-153">`[Scope <String>]`. Область поставщика ресурсов для ресурса.</span><span class="sxs-lookup"><span data-stu-id="ec965-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="ec965-154">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="ec965-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="ec965-155">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ec965-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ec965-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ec965-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ec965-157">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="ec965-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="ec965-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec965-158">RELATED LINKS</span></span>

