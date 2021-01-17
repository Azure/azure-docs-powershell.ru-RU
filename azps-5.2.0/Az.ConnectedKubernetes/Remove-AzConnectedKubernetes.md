---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323696"
---
# <span data-ttu-id="ade55-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="ade55-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="ade55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade55-102">SYNOPSIS</span></span>
<span data-ttu-id="ade55-103">Удалите подключенный кластер, удалите отслеживаемый ресурс в Диспетчере ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="ade55-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="ade55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ade55-104">SYNTAX</span></span>

### <span data-ttu-id="ade55-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ade55-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ade55-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ade55-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ade55-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ade55-107">DESCRIPTION</span></span>
<span data-ttu-id="ade55-108">Удалите подключенный кластер, удалите отслеживаемый ресурс в Диспетчере ресурсов Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="ade55-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="ade55-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ade55-109">EXAMPLES</span></span>

### <span data-ttu-id="ade55-110">Пример 1. Удаление подключенных куберсетей</span><span class="sxs-lookup"><span data-stu-id="ade55-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="ade55-111">Эта команда удаляет подключенные куберсети</span><span class="sxs-lookup"><span data-stu-id="ade55-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="ade55-112">Пример 2. Удаление подключенных куберсетей с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="ade55-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="ade55-113">Эта команда удаляет подключенные к объекту куберсети</span><span class="sxs-lookup"><span data-stu-id="ade55-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="ade55-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade55-114">PARAMETERS</span></span>

### <span data-ttu-id="ade55-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ade55-115">-AsJob</span></span>
<span data-ttu-id="ade55-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ade55-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ade55-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ade55-117">-ClusterName</span></span>
<span data-ttu-id="ade55-118">Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="ade55-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="ade55-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade55-119">-DefaultProfile</span></span>
<span data-ttu-id="ade55-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ade55-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ade55-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ade55-121">-InputObject</span></span>
<span data-ttu-id="ade55-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ade55-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ade55-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="ade55-123">-KubeConfig</span></span>
<span data-ttu-id="ade55-124">Путь к файлу config в kube</span><span class="sxs-lookup"><span data-stu-id="ade55-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="ade55-125">-KubeContext</span><span class="sxs-lookup"><span data-stu-id="ade55-125">-KubeContext</span></span>
<span data-ttu-id="ade55-126">Контекст Kubconfig с текущего компьютера</span><span class="sxs-lookup"><span data-stu-id="ade55-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="ade55-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ade55-127">-NoWait</span></span>
<span data-ttu-id="ade55-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ade55-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ade55-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ade55-129">-PassThru</span></span>
<span data-ttu-id="ade55-130">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="ade55-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ade55-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade55-131">-ResourceGroupName</span></span>
<span data-ttu-id="ade55-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade55-132">The name of the resource group.</span></span>
<span data-ttu-id="ade55-133">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ade55-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ade55-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ade55-134">-SubscriptionId</span></span>
<span data-ttu-id="ade55-135">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ade55-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ade55-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ade55-136">-Confirm</span></span>
<span data-ttu-id="ade55-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ade55-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade55-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade55-138">-WhatIf</span></span>
<span data-ttu-id="ade55-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ade55-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade55-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ade55-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade55-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade55-141">CommonParameters</span></span>
<span data-ttu-id="ade55-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ade55-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade55-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ade55-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade55-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ade55-144">INPUTS</span></span>

### <span data-ttu-id="ade55-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="ade55-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="ade55-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ade55-146">OUTPUTS</span></span>

### <span data-ttu-id="ade55-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ade55-147">System.Boolean</span></span>

## <span data-ttu-id="ade55-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ade55-148">NOTES</span></span>

<span data-ttu-id="ade55-149">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ade55-149">ALIASES</span></span>

<span data-ttu-id="ade55-150">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ade55-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ade55-151">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ade55-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ade55-152">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ade55-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ade55-153">INPUTOBJECT <IConnectedKubernetesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ade55-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ade55-154">`[ClusterName <String>]`Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="ade55-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="ade55-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ade55-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ade55-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade55-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ade55-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="ade55-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="ade55-158">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="ade55-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="ade55-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ade55-159">RELATED LINKS</span></span>

