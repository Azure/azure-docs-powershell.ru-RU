---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/get-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Get-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 55ca24a7213dea4e9d0743689c080ebbb439430a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426135"
---
# <span data-ttu-id="46a8f-101">Get-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="46a8f-101">Get-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="46a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="46a8f-103">Свойства экземпляра поставщика для указанной подписки, группы ресурсов, имени sapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="46a8f-103">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="46a8f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46a8f-104">SYNTAX</span></span>

### <span data-ttu-id="46a8f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46a8f-105">List (Default)</span></span>
```
Get-AzSapMonitorProviderInstance -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="46a8f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="46a8f-106">Get</span></span>
```
Get-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="46a8f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46a8f-107">GetViaIdentity</span></span>
```
Get-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="46a8f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46a8f-108">DESCRIPTION</span></span>
<span data-ttu-id="46a8f-109">Свойства экземпляра поставщика для указанной подписки, группы ресурсов, имени sapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="46a8f-109">Gets properties of a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="46a8f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46a8f-110">EXAMPLES</span></span>

### <span data-ttu-id="46a8f-111">Пример 1. Все экземпляры, которые находятся под монитором SAP</span><span class="sxs-lookup"><span data-stu-id="46a8f-111">Example 1: Get all instances under a SAP monitor</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01

Name                 Type
----                 ----
ps-sapmonitorins-t01 Microsoft.HanaOnAzure/sapMonitors/providerInstances
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="46a8f-112">Эта команда получает все экземпляры под мониторОМ SAP.</span><span class="sxs-lookup"><span data-stu-id="46a8f-112">This command gets all instances under a SAP monitor.</span></span>

### <span data-ttu-id="46a8f-113">Пример 2. Просмотр экземпляров монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="46a8f-113">Example 2: Get an instances of SAP monitor by name</span></span>
```powershell
PS C:\> Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="46a8f-114">Эта команда получает экземпляры монитора SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="46a8f-114">This command gets an instances of SAP monitor by name.</span></span>

### <span data-ttu-id="46a8f-115">Пример 3. Просмотр экземпляров монитора SAP для объекта</span><span class="sxs-lookup"><span data-stu-id="46a8f-115">Example 3: Get an instances of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02
PS C:\> Get-AzSapMonitorProviderInstance -InputObject $sapIns

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="46a8f-116">Эта команда получает экземпляры монитора SAP для объекта.</span><span class="sxs-lookup"><span data-stu-id="46a8f-116">This command gets an instances of SAP monitor by object.</span></span>

### <span data-ttu-id="46a8f-117">Пример 4. Просмотр экземпляров монитора SAP для конвейера</span><span class="sxs-lookup"><span data-stu-id="46a8f-117">Example 4: Get an instances of SAP monitor by pipeline</span></span>
```powershell
PS C:\> @{Id = "/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/nancyc-hn1/providers/Microsoft.HanaOnAzure/sapMonitors/ps-spamonitor-t01/providerInstances/ps-sapmonitorins-t02"} | Get-AzSapMonitorProviderInstance

Name                 Type
----                 ----
ps-sapmonitorins-t02 Microsoft.HanaOnAzure/sapMonitors/providerInstances
```

<span data-ttu-id="46a8f-118">Эта команда получает экземпляры монитора SAP в конвейере.</span><span class="sxs-lookup"><span data-stu-id="46a8f-118">This command gets an instances of SAP monitor by pipeline.</span></span>

## <span data-ttu-id="46a8f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46a8f-119">PARAMETERS</span></span>

### <span data-ttu-id="46a8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46a8f-120">-DefaultProfile</span></span>
<span data-ttu-id="46a8f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46a8f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46a8f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46a8f-122">-InputObject</span></span>
<span data-ttu-id="46a8f-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="46a8f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46a8f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="46a8f-124">-Name</span></span>
<span data-ttu-id="46a8f-125">Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="46a8f-125">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46a8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="46a8f-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46a8f-127">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a8f-128">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="46a8f-128">-SapMonitorName</span></span>
<span data-ttu-id="46a8f-129">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="46a8f-129">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a8f-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46a8f-130">-SubscriptionId</span></span>
<span data-ttu-id="46a8f-131">Идентификация подписки, однозначно определяемая подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46a8f-131">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46a8f-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="46a8f-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46a8f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46a8f-133">CommonParameters</span></span>
<span data-ttu-id="46a8f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46a8f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46a8f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46a8f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46a8f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46a8f-136">INPUTS</span></span>

### <span data-ttu-id="46a8f-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="46a8f-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="46a8f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46a8f-138">OUTPUTS</span></span>

### <span data-ttu-id="46a8f-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span><span class="sxs-lookup"><span data-stu-id="46a8f-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.IProviderInstance</span></span>

## <span data-ttu-id="46a8f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46a8f-140">NOTES</span></span>

<span data-ttu-id="46a8f-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="46a8f-141">ALIASES</span></span>

<span data-ttu-id="46a8f-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="46a8f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46a8f-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="46a8f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46a8f-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46a8f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46a8f-145">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="46a8f-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46a8f-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="46a8f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46a8f-147">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="46a8f-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="46a8f-148">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="46a8f-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="46a8f-149">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="46a8f-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="46a8f-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46a8f-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="46a8f-151">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="46a8f-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="46a8f-152">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="46a8f-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="46a8f-153">`[Scope <String>]`Область поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46a8f-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="46a8f-154">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="46a8f-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="46a8f-155">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46a8f-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="46a8f-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="46a8f-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="46a8f-157">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="46a8f-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="46a8f-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46a8f-158">RELATED LINKS</span></span>

