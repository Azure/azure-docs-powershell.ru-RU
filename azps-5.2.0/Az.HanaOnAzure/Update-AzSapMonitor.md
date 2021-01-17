---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399215"
---
# <span data-ttu-id="d5d48-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d48-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="d5d48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5d48-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d48-103">Исправление поля "Теги" на мониторе SAP для указанной подписки, группы ресурсов и имени монитора.</span><span class="sxs-lookup"><span data-stu-id="d5d48-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="d5d48-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5d48-104">SYNTAX</span></span>

### <span data-ttu-id="d5d48-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5d48-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d5d48-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d5d48-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d5d48-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d48-107">DESCRIPTION</span></span>
<span data-ttu-id="d5d48-108">Исправление поля "Теги" на мониторе SAP для указанной подписки, группы ресурсов и имени монитора.</span><span class="sxs-lookup"><span data-stu-id="d5d48-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="d5d48-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5d48-109">EXAMPLES</span></span>

### <span data-ttu-id="d5d48-110">Пример 1. Обновление монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="d5d48-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d5d48-111">Эта команда обновляет монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="d5d48-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="d5d48-112">Пример 2. Обновление монитора SAP по объектам</span><span class="sxs-lookup"><span data-stu-id="d5d48-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="d5d48-113">Эта команда обновляет монитор SAP по объекту.</span><span class="sxs-lookup"><span data-stu-id="d5d48-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="d5d48-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5d48-114">PARAMETERS</span></span>

### <span data-ttu-id="d5d48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d48-115">-DefaultProfile</span></span>
<span data-ttu-id="d5d48-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d48-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5d48-117">-InputObject</span></span>
<span data-ttu-id="d5d48-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d5d48-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d5d48-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d5d48-119">-Name</span></span>
<span data-ttu-id="d5d48-120">Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="d5d48-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="d5d48-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d48-121">-ResourceGroupName</span></span>
<span data-ttu-id="d5d48-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5d48-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="d5d48-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d5d48-123">-SubscriptionId</span></span>
<span data-ttu-id="d5d48-124">Идентификация подписки, однозначно определяемая подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d48-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d5d48-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d5d48-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d5d48-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="d5d48-126">-Tag</span></span>
<span data-ttu-id="d5d48-127">Поле "Теги" для ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5d48-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="d5d48-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5d48-128">-Confirm</span></span>
<span data-ttu-id="d5d48-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5d48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5d48-130">-WhatIf</span></span>
<span data-ttu-id="d5d48-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5d48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5d48-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d5d48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5d48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d48-133">CommonParameters</span></span>
<span data-ttu-id="d5d48-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5d48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d48-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5d48-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d48-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5d48-136">INPUTS</span></span>

### <span data-ttu-id="d5d48-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="d5d48-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="d5d48-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5d48-138">OUTPUTS</span></span>

### <span data-ttu-id="d5d48-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="d5d48-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="d5d48-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5d48-140">NOTES</span></span>

<span data-ttu-id="d5d48-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d5d48-141">ALIASES</span></span>

<span data-ttu-id="d5d48-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d5d48-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d5d48-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d5d48-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d5d48-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d5d48-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d5d48-145">INPUTOBJECT <IHanaOnAzureIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d5d48-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d5d48-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d5d48-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d5d48-147">`[Location <String>]`: расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="d5d48-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="d5d48-148">`[OperationKind <AccessPolicyUpdateKind?>]`: название операции</span><span class="sxs-lookup"><span data-stu-id="d5d48-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="d5d48-149">`[ProviderInstanceName <String>]`: имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="d5d48-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="d5d48-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5d48-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="d5d48-151">`[ResourceName <String>]`: Имя ресурса удостоверения.</span><span class="sxs-lookup"><span data-stu-id="d5d48-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="d5d48-152">`[SapMonitorName <String>]`. Имя ресурса sap monitor.</span><span class="sxs-lookup"><span data-stu-id="d5d48-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="d5d48-153">`[Scope <String>]`Область поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5d48-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="d5d48-154">Родительский ресурс, который расширяется с помощью управляемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="d5d48-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="d5d48-155">`[SubscriptionId <String>]`: ИД подписки, однозначно определяемой подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d48-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d5d48-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d5d48-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d5d48-157">`[VaultName <String>]`: имя сейфа</span><span class="sxs-lookup"><span data-stu-id="d5d48-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="d5d48-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5d48-158">RELATED LINKS</span></span>

