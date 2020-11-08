---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitorproviderinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitorProviderInstance.md
ms.openlocfilehash: 53f251b001b4e2f6319840079e9db3111c00b006
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247390"
---
# <span data-ttu-id="dd475-101">Remove-AzSapMonitorProviderInstance</span><span class="sxs-lookup"><span data-stu-id="dd475-101">Remove-AzSapMonitorProviderInstance</span></span>

## <span data-ttu-id="dd475-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dd475-102">SYNOPSIS</span></span>
<span data-ttu-id="dd475-103">Удаляет экземпляр поставщика для указанной подписки, группы ресурсов, имени SapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd475-103">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="dd475-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dd475-104">SYNTAX</span></span>

### <span data-ttu-id="dd475-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dd475-105">Delete (Default)</span></span>
```
Remove-AzSapMonitorProviderInstance -Name <String> -ResourceGroupName <String> -SapMonitorName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="dd475-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dd475-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitorProviderInstance -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dd475-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd475-107">DESCRIPTION</span></span>
<span data-ttu-id="dd475-108">Удаляет экземпляр поставщика для указанной подписки, группы ресурсов, имени SapMonitor и имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd475-108">Deletes a provider instance for the specified subscription, resource group, SapMonitor name, and resource name.</span></span>

## <span data-ttu-id="dd475-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dd475-109">EXAMPLES</span></span>

### <span data-ttu-id="dd475-110">Пример 1: удаление экземпляра монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="dd475-110">Example 1: Remove instance of SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t02

```

<span data-ttu-id="dd475-111">Эта команда удаляет экземпляр монитора SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="dd475-111">This command removes instance of SAP monitor by name.</span></span>

### <span data-ttu-id="dd475-112">Пример 2: удаление экземпляра монитора SAP по объекту</span><span class="sxs-lookup"><span data-stu-id="dd475-112">Example 2: Remove instance of SAP monitor by object</span></span>
```powershell
PS C:\> $sapIns = Get-AzSapMonitorProviderInstance -ResourceGroupName nancyc-hn1 -SapMonitorName ps-spamonitor-t01 -Name ps-sapmonitorins-t01
PS C:\> Remove-AzSapMonitorProviderInstance -InputObject $sapIns

```

<span data-ttu-id="dd475-113">Эта команда удаляет экземпляр монитора SAP по объекту.</span><span class="sxs-lookup"><span data-stu-id="dd475-113">This command removes instance of SAP monitor by object.</span></span>

## <span data-ttu-id="dd475-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dd475-114">PARAMETERS</span></span>

### <span data-ttu-id="dd475-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd475-115">-AsJob</span></span>
<span data-ttu-id="dd475-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="dd475-116">Run the command as a job</span></span>

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

### <span data-ttu-id="dd475-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd475-117">-DefaultProfile</span></span>
<span data-ttu-id="dd475-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd475-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd475-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd475-119">-InputObject</span></span>
<span data-ttu-id="dd475-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="dd475-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd475-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dd475-121">-Name</span></span>
<span data-ttu-id="dd475-122">Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="dd475-122">Name of the provider instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ProviderInstanceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd475-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="dd475-123">-NoWait</span></span>
<span data-ttu-id="dd475-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="dd475-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dd475-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd475-125">-PassThru</span></span>
<span data-ttu-id="dd475-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dd475-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dd475-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd475-127">-ResourceGroupName</span></span>
<span data-ttu-id="dd475-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd475-128">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd475-129">-SapMonitorName</span><span class="sxs-lookup"><span data-stu-id="dd475-129">-SapMonitorName</span></span>
<span data-ttu-id="dd475-130">Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="dd475-130">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd475-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dd475-131">-SubscriptionId</span></span>
<span data-ttu-id="dd475-132">Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd475-132">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dd475-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="dd475-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd475-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd475-134">-Confirm</span></span>
<span data-ttu-id="dd475-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dd475-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd475-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd475-136">-WhatIf</span></span>
<span data-ttu-id="dd475-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dd475-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd475-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dd475-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd475-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd475-139">CommonParameters</span></span>
<span data-ttu-id="dd475-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dd475-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd475-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd475-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd475-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dd475-142">INPUTS</span></span>

### <span data-ttu-id="dd475-143">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="dd475-143">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="dd475-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd475-144">OUTPUTS</span></span>

### <span data-ttu-id="dd475-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd475-145">System.Boolean</span></span>

## <span data-ttu-id="dd475-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="dd475-146">NOTES</span></span>

<span data-ttu-id="dd475-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="dd475-147">ALIASES</span></span>

<span data-ttu-id="dd475-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dd475-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dd475-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dd475-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dd475-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dd475-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dd475-151">INPUTOBJECT <IHanaOnAzureIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="dd475-151">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dd475-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="dd475-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dd475-153">`[Location <String>]`: Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="dd475-153">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="dd475-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Имя операции</span><span class="sxs-lookup"><span data-stu-id="dd475-154">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="dd475-155">`[ProviderInstanceName <String>]`: Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="dd475-155">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="dd475-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd475-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dd475-157">`[ResourceName <String>]`: Имя ресурса идентификации.</span><span class="sxs-lookup"><span data-stu-id="dd475-157">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="dd475-158">`[SapMonitorName <String>]`: Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="dd475-158">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="dd475-159">`[Scope <String>]`: Область поставщика ресурсов ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd475-159">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="dd475-160">Родительский ресурс, который расширяется управляемыми идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="dd475-160">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="dd475-161">`[SubscriptionId <String>]`: Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dd475-161">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dd475-162">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="dd475-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dd475-163">`[VaultName <String>]`: Имя хранилища</span><span class="sxs-lookup"><span data-stu-id="dd475-163">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="dd475-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd475-164">RELATED LINKS</span></span>

