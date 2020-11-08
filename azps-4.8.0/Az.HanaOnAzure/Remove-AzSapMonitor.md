---
external help file: ''
Module Name: Az.HanaOnAzure
online version: https://docs.microsoft.com/en-us/powershell/module/az.hanaonazure/remove-azsapmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HanaOnAzure/help/Remove-AzSapMonitor.md
ms.openlocfilehash: bcba06d87bce2f9ccc8016afc9f08dff75e29b1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079613"
---
# <span data-ttu-id="12203-101">Remove-AzSapMonitor</span><span class="sxs-lookup"><span data-stu-id="12203-101">Remove-AzSapMonitor</span></span>

## <span data-ttu-id="12203-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12203-102">SYNOPSIS</span></span>
<span data-ttu-id="12203-103">Удаляет монитор SAP с указанной подпиской, группой ресурсов и именем монитора.</span><span class="sxs-lookup"><span data-stu-id="12203-103">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="12203-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12203-104">SYNTAX</span></span>

### <span data-ttu-id="12203-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="12203-105">Delete (Default)</span></span>
```
Remove-AzSapMonitor -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="12203-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="12203-106">DeleteViaIdentity</span></span>
```
Remove-AzSapMonitor -InputObject <IHanaOnAzureIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="12203-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12203-107">DESCRIPTION</span></span>
<span data-ttu-id="12203-108">Удаляет монитор SAP с указанной подпиской, группой ресурсов и именем монитора.</span><span class="sxs-lookup"><span data-stu-id="12203-108">Deletes a SAP monitor with the specified subscription, resource group, and monitor name.</span></span>

## <span data-ttu-id="12203-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12203-109">EXAMPLES</span></span>

### <span data-ttu-id="12203-110">Пример 1: удаление монитора SAP по имени</span><span class="sxs-lookup"><span data-stu-id="12203-110">Example 1: Remove a SAP monitor by name</span></span>
```powershell
PS C:\> Remove-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t02

```

<span data-ttu-id="12203-111">Эта команда удаляет монитор SAP по имени.</span><span class="sxs-lookup"><span data-stu-id="12203-111">This command removes a SAP monitor by name.</span></span>

### <span data-ttu-id="12203-112">Пример 2: удаление монитора SAP по объекту</span><span class="sxs-lookup"><span data-stu-id="12203-112">Example 2: Remove a SAP monitor by object</span></span>
```powershell
PS C:\> $sap = Get-AzSapMonitor -ResourceGroupName nancyc-hn1 -Name ps-sapmonitor-t01
PS C:\> Remove-AzSapMonitor -InputObject $sap

```

<span data-ttu-id="12203-113">Эта команда удаляет монитор SAP по объекту.</span><span class="sxs-lookup"><span data-stu-id="12203-113">This command removes a SAP monitor by object.</span></span>

## <span data-ttu-id="12203-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12203-114">PARAMETERS</span></span>

### <span data-ttu-id="12203-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12203-115">-AsJob</span></span>
<span data-ttu-id="12203-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="12203-116">Run the command as a job</span></span>

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

### <span data-ttu-id="12203-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12203-117">-DefaultProfile</span></span>
<span data-ttu-id="12203-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12203-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12203-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12203-119">-InputObject</span></span>
<span data-ttu-id="12203-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="12203-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="12203-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12203-121">-Name</span></span>
<span data-ttu-id="12203-122">Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="12203-122">Name of the SAP monitor resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SapMonitorName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12203-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="12203-123">-NoWait</span></span>
<span data-ttu-id="12203-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="12203-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="12203-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12203-125">-PassThru</span></span>
<span data-ttu-id="12203-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="12203-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="12203-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12203-127">-ResourceGroupName</span></span>
<span data-ttu-id="12203-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12203-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="12203-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="12203-129">-SubscriptionId</span></span>
<span data-ttu-id="12203-130">Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12203-130">Subscription ID which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="12203-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="12203-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="12203-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12203-132">-Confirm</span></span>
<span data-ttu-id="12203-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12203-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12203-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12203-134">-WhatIf</span></span>
<span data-ttu-id="12203-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12203-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12203-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12203-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12203-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12203-137">CommonParameters</span></span>
<span data-ttu-id="12203-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12203-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12203-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12203-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12203-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12203-140">INPUTS</span></span>

### <span data-ttu-id="12203-141">Microsoft. Azure. PowerShell. командлеты. HanaOnAzure. Models. IHanaOnAzureIdentity</span><span class="sxs-lookup"><span data-stu-id="12203-141">Microsoft.Azure.PowerShell.Cmdlets.HanaOnAzure.Models.IHanaOnAzureIdentity</span></span>

## <span data-ttu-id="12203-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12203-142">OUTPUTS</span></span>

### <span data-ttu-id="12203-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12203-143">System.Boolean</span></span>

## <span data-ttu-id="12203-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="12203-144">NOTES</span></span>

<span data-ttu-id="12203-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="12203-145">ALIASES</span></span>

<span data-ttu-id="12203-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="12203-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="12203-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="12203-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="12203-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="12203-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="12203-149">INPUTOBJECT <IHanaOnAzureIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="12203-149">INPUTOBJECT <IHanaOnAzureIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="12203-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="12203-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="12203-151">`[Location <String>]`: Расположение удаленного хранилища.</span><span class="sxs-lookup"><span data-stu-id="12203-151">`[Location <String>]`: The location of the deleted vault.</span></span>
  - <span data-ttu-id="12203-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Имя операции</span><span class="sxs-lookup"><span data-stu-id="12203-152">`[OperationKind <AccessPolicyUpdateKind?>]`: Name of the operation</span></span>
  - <span data-ttu-id="12203-153">`[ProviderInstanceName <String>]`: Имя экземпляра поставщика.</span><span class="sxs-lookup"><span data-stu-id="12203-153">`[ProviderInstanceName <String>]`: Name of the provider instance.</span></span>
  - <span data-ttu-id="12203-154">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12203-154">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="12203-155">`[ResourceName <String>]`: Имя ресурса идентификации.</span><span class="sxs-lookup"><span data-stu-id="12203-155">`[ResourceName <String>]`: The name of the identity resource.</span></span>
  - <span data-ttu-id="12203-156">`[SapMonitorName <String>]`: Имя ресурса монитора SAP.</span><span class="sxs-lookup"><span data-stu-id="12203-156">`[SapMonitorName <String>]`: Name of the SAP monitor resource.</span></span>
  - <span data-ttu-id="12203-157">`[Scope <String>]`: Область поставщика ресурсов ресурса.</span><span class="sxs-lookup"><span data-stu-id="12203-157">`[Scope <String>]`: The resource provider scope of the resource.</span></span> <span data-ttu-id="12203-158">Родительский ресурс, который расширяется управляемыми идентификаторами.</span><span class="sxs-lookup"><span data-stu-id="12203-158">Parent resource being extended by Managed Identities.</span></span>
  - <span data-ttu-id="12203-159">`[SubscriptionId <String>]`: Идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="12203-159">`[SubscriptionId <String>]`: Subscription ID which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="12203-160">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="12203-160">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="12203-161">`[VaultName <String>]`: Имя хранилища</span><span class="sxs-lookup"><span data-stu-id="12203-161">`[VaultName <String>]`: Name of the vault</span></span>

## <span data-ttu-id="12203-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12203-162">RELATED LINKS</span></span>

