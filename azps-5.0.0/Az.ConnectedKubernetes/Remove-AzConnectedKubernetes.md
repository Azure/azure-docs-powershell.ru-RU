---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246751"
---
# <span data-ttu-id="0678c-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="0678c-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="0678c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0678c-102">SYNOPSIS</span></span>
<span data-ttu-id="0678c-103">Удаление подключенного кластера и удаление отслеживаемого ресурса в диспетчере ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="0678c-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="0678c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0678c-104">SYNTAX</span></span>

### <span data-ttu-id="0678c-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0678c-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0678c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0678c-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0678c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0678c-107">DESCRIPTION</span></span>
<span data-ttu-id="0678c-108">Удаление подключенного кластера и удаление отслеживаемого ресурса в диспетчере ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="0678c-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="0678c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0678c-109">EXAMPLES</span></span>

### <span data-ttu-id="0678c-110">Пример 1: удаление подключенного kubernetes</span><span class="sxs-lookup"><span data-stu-id="0678c-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="0678c-111">Эта команда удаляет подключенный kubernetes</span><span class="sxs-lookup"><span data-stu-id="0678c-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="0678c-112">Пример 2: удаление подключенного kubernetes по объекту</span><span class="sxs-lookup"><span data-stu-id="0678c-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="0678c-113">Эта команда удаляет подключенный kubernetes по объекту.</span><span class="sxs-lookup"><span data-stu-id="0678c-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="0678c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0678c-114">PARAMETERS</span></span>

### <span data-ttu-id="0678c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0678c-115">-AsJob</span></span>
<span data-ttu-id="0678c-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0678c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0678c-117">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="0678c-117">-ClusterName</span></span>
<span data-ttu-id="0678c-118">Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="0678c-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0678c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0678c-119">-DefaultProfile</span></span>
<span data-ttu-id="0678c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0678c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0678c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0678c-121">-InputObject</span></span>
<span data-ttu-id="0678c-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0678c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0678c-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="0678c-123">-KubeConfig</span></span>
<span data-ttu-id="0678c-124">Путь к файлу конфигурации KUBE</span><span class="sxs-lookup"><span data-stu-id="0678c-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="0678c-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="0678c-125">-KubeContext</span></span>
<span data-ttu-id="0678c-126">Контекст Kubconfig с текущего компьютера</span><span class="sxs-lookup"><span data-stu-id="0678c-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="0678c-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="0678c-127">-NoWait</span></span>
<span data-ttu-id="0678c-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="0678c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0678c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0678c-129">-PassThru</span></span>
<span data-ttu-id="0678c-130">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0678c-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0678c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0678c-131">-ResourceGroupName</span></span>
<span data-ttu-id="0678c-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0678c-132">The name of the resource group.</span></span>
<span data-ttu-id="0678c-133">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0678c-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0678c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0678c-134">-SubscriptionId</span></span>
<span data-ttu-id="0678c-135">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0678c-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0678c-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0678c-136">-Confirm</span></span>
<span data-ttu-id="0678c-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0678c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0678c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0678c-138">-WhatIf</span></span>
<span data-ttu-id="0678c-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0678c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0678c-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0678c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0678c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0678c-141">CommonParameters</span></span>
<span data-ttu-id="0678c-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0678c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0678c-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0678c-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0678c-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0678c-144">INPUTS</span></span>

### <span data-ttu-id="0678c-145">Microsoft. Azure. PowerShell. командлеты. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="0678c-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="0678c-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0678c-146">OUTPUTS</span></span>

### <span data-ttu-id="0678c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0678c-147">System.Boolean</span></span>

## <span data-ttu-id="0678c-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="0678c-148">NOTES</span></span>

<span data-ttu-id="0678c-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0678c-149">ALIASES</span></span>

<span data-ttu-id="0678c-150">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0678c-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0678c-151">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0678c-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0678c-152">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0678c-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0678c-153">INPUTOBJECT <IConnectedKubernetesIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0678c-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0678c-154">`[ClusterName <String>]`: Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="0678c-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="0678c-155">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0678c-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0678c-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0678c-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0678c-157">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="0678c-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="0678c-158">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0678c-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="0678c-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0678c-159">RELATED LINKS</span></span>

