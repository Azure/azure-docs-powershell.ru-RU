---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/update-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Update-AzSapMonitor.md
ms.openlocfilehash: 9d87cfff428a5c3c176bea4deff95d0c652dc45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247389"
---
# <span data-ttu-id="c6b40-101">Update-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="c6b40-101">Update-AzSapMonitor</span></span>

## <span data-ttu-id="c6b40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6b40-102">SYNOPSIS</span></span>
<span data-ttu-id="c6b40-103">Пакеты исправлений. в поле «Теги» монитора SAP для указанной подписки, группы ресурсов и имени монитора.</span><span class="sxs-lookup"><span data-stu-id="c6b40-103">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="c6b40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6b40-104">SYNTAX</span></span>

### <span data-ttu-id="c6b40-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6b40-105">UpdateExpanded (Default)</span></span>
```
Update-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c6b40-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c6b40-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6b40-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6b40-107">DESCRIPTION</span></span>
<span data-ttu-id="c6b40-108">Пакеты исправлений. в поле «Теги» монитора SAP для указанной подписки, группы ресурсов и имени монитора.</span><span class="sxs-lookup"><span data-stu-id="c6b40-108">Patches the Tags field of a SAP monitor for the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="c6b40-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6b40-109">EXAMPLES</span></span>

### <span data-ttu-id="c6b40-110">Пример 1: обновление монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="c6b40-110">Example 1: Update a SAP monitor by name</span></span>
```powershell
PS C:\> Update-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-spamonitor-t01 -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-spamonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="c6b40-111">Эта команда обновляет монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="c6b40-111">This commands updates a SAP monitor by name.</span></span>

### <span data-ttu-id="c6b40-112">Пример 2: обновление монитора SAP по объекту</span><span class="sxs-lookup"><span data-stu-id="c6b40-112">Example 2: Update a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Update-AzSapMonitor -InputObject $sap -Tag @{'key'=1;'key2'=2; 'key3'=3}

Location Name              Type
-------- ----              ----
westus2  ps-sapmonitor-t01 Microsoft.HanaOnAzure/sapMonitors
```

<span data-ttu-id="c6b40-113">Эта команда обновляет монитор SAP по объектам.</span><span class="sxs-lookup"><span data-stu-id="c6b40-113">This commands updates a SAP monitor by object.</span></span>

## <span data-ttu-id="c6b40-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6b40-114">PARAMETERS</span></span>

### <span data-ttu-id="c6b40-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6b40-115">-DefaultProfile</span></span>
<span data-ttu-id="c6b40-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b40-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6b40-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6b40-117">-InputObject</span></span>
<span data-ttu-id="c6b40-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="c6b40-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6b40-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6b40-119">-Name</span></span>
<span data-ttu-id="c6b40-120">Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="c6b40-120">Name of the SAP monitor resource.</span></span>

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

### <span data-ttu-id="c6b40-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6b40-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6b40-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6b40-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="c6b40-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6b40-123">-SubscriptionId</span></span>
<span data-ttu-id="c6b40-124">Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b40-124">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6b40-125">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c6b40-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c6b40-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="c6b40-126">-Tag</span></span>
<span data-ttu-id="c6b40-127">Поле «Теги» ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6b40-127">Tags field of the resource.</span></span>

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

### <span data-ttu-id="c6b40-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6b40-128">-Confirm</span></span>
<span data-ttu-id="c6b40-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6b40-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6b40-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6b40-130">-WhatIf</span></span>
<span data-ttu-id="c6b40-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6b40-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6b40-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6b40-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6b40-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6b40-133">CommonParameters</span></span>
<span data-ttu-id="c6b40-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6b40-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6b40-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6b40-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6b40-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6b40-136">INPUTS</span></span>

### <span data-ttu-id="c6b40-137">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="c6b40-137">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="c6b40-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6b40-138">OUTPUTS</span></span>

### <span data-ttu-id="c6b40-139">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. Api20200207Preview. ISapMonitor</span><span class="sxs-lookup"><span data-stu-id="c6b40-139">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.Api20200207Preview.ISapMonitor</span></span>

## <span data-ttu-id="c6b40-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6b40-140">NOTES</span></span>

<span data-ttu-id="c6b40-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c6b40-141">ALIASES</span></span>

<span data-ttu-id="c6b40-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="c6b40-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6b40-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c6b40-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6b40-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c6b40-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6b40-145">INPUTOBJECT <IHanaOnAzureIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="c6b40-145">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6b40-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="c6b40-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6b40-147">`[Location <String>]`: Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="c6b40-147">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="c6b40-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Имя операции</span><span class="sxs-lookup"><span data-stu-id="c6b40-148">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="c6b40-149">`[ProviderInstanceName <String>]`: Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="c6b40-149">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="c6b40-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6b40-150">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c6b40-151">`[ResourceName <String>]`: Имя ресурса идентификации.</span><span class="sxs-lookup"><span data-stu-id="c6b40-151">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="c6b40-152">`[SapMonitorName <String>]`: Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="c6b40-152">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="c6b40-153">`[Scope <String>]`: Область поставщика ресурсов ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6b40-153">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="c6b40-154">Родительский ресурс, который расширяется управляемыми идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="c6b40-154">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="c6b40-155">`[SubscriptionId <String>]`: Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c6b40-155">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c6b40-156">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c6b40-156">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c6b40-157">`[VaultName <String>]`: Имя хранилища</span><span class="sxs-lookup"><span data-stu-id="c6b40-157">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="c6b40-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6b40-158">RELATED LINKS</span></span>

