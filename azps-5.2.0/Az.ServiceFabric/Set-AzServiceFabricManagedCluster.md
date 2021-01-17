---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricManagedCluster.md
ms.openlocfilehash: 4636dc8f8c8efdf9dae5f7d2094fd3432528f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397684"
---
# <span data-ttu-id="73236-101">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="73236-101">Set-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="73236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73236-102">SYNOPSIS</span></span>
<span data-ttu-id="73236-103">Настройка свойств ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-103">Set cluster resource properties.</span></span>

## <span data-ttu-id="73236-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73236-104">SYNTAX</span></span>

### <span data-ttu-id="73236-105">ByObj (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73236-105">ByObj (Default)</span></span>
```
Set-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73236-106">WithPramsByName</span><span class="sxs-lookup"><span data-stu-id="73236-106">WithPramsByName</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String>
 [-UpgradeMode <ClusterUpgradeMode>] [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>]
 [-ClientConnectionPort <Int32>] [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73236-107">ByNameById</span><span class="sxs-lookup"><span data-stu-id="73236-107">ByNameById</span></span>
```
Set-AzServiceFabricManagedCluster [-ResourceId] <String> [-UpgradeMode <ClusterUpgradeMode>]
 [-CodeVersion <String>] [-HttpGatewayConnectionPort <Int32>] [-ClientConnectionPort <Int32>]
 [-DnsName <String>] [-ReverseProxyEndpointPort <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73236-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73236-108">DESCRIPTION</span></span>
<span data-ttu-id="73236-109">Настройка свойств ресурсов кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-109">Set cluster resource properties.</span></span>

## <span data-ttu-id="73236-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73236-110">EXAMPLES</span></span>

### <span data-ttu-id="73236-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="73236-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Update-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName -DnsName testnewdns -ClientConnectionPort 50000 -Verbose
```

<span data-ttu-id="73236-112">Обновив имя dns и порт клиентского подключения для кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-112">Update dns name and client connection port for the cluster.</span></span>

### <span data-ttu-id="73236-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="73236-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster.DnsName = "testnewdns"
$cluster.ClientConnectionPort = 50000
$cluster | Set-AzServiceFabricManagedCluster
```

<span data-ttu-id="73236-114">Обновив имя dns и порт клиентского подключения для кластера, перенастройку.</span><span class="sxs-lookup"><span data-stu-id="73236-114">Update dns name and client connection port for the cluster, with piping.</span></span>

## <span data-ttu-id="73236-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73236-115">PARAMETERS</span></span>

### <span data-ttu-id="73236-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73236-116">-AsJob</span></span>
<span data-ttu-id="73236-117">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="73236-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="73236-118">-ClientConnectionPort</span><span class="sxs-lookup"><span data-stu-id="73236-118">-ClientConnectionPort</span></span>
<span data-ttu-id="73236-119">Порт, используемый для клиентских подключений к кластеру.</span><span class="sxs-lookup"><span data-stu-id="73236-119">Port used for client connections to the cluster.</span></span> <span data-ttu-id="73236-120">Значение по умолчанию: 19 000.</span><span class="sxs-lookup"><span data-stu-id="73236-120">Default: 19000.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-121">-CodeVersion</span><span class="sxs-lookup"><span data-stu-id="73236-121">-CodeVersion</span></span>
<span data-ttu-id="73236-122">Версия кода кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-122">Cluster code version.</span></span> <span data-ttu-id="73236-123">Используется только в режиме обновления вручную.</span><span class="sxs-lookup"><span data-stu-id="73236-123">Only use if upgrade mode is Manual.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73236-124">-DefaultProfile</span></span>
<span data-ttu-id="73236-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73236-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-126">-DnsName</span><span class="sxs-lookup"><span data-stu-id="73236-126">-DnsName</span></span>
<span data-ttu-id="73236-127">Имя DNS кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-127">Cluster's dns name.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-128">-HttpGatewayConnectionPort</span><span class="sxs-lookup"><span data-stu-id="73236-128">-HttpGatewayConnectionPort</span></span>
<span data-ttu-id="73236-129">Порт, используемый для http-подключений к кластеру.</span><span class="sxs-lookup"><span data-stu-id="73236-129">Port used for http connections to the cluster.</span></span> <span data-ttu-id="73236-130">Значение по умолчанию: 19080.</span><span class="sxs-lookup"><span data-stu-id="73236-130">Default: 19080.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73236-131">-InputObject</span></span>
<span data-ttu-id="73236-132">Управляемый ресурс кластера</span><span class="sxs-lookup"><span data-stu-id="73236-132">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73236-133">-Name</span><span class="sxs-lookup"><span data-stu-id="73236-133">-Name</span></span>
<span data-ttu-id="73236-134">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-134">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73236-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73236-135">-ResourceGroupName</span></span>
<span data-ttu-id="73236-136">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73236-136">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: WithPramsByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73236-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73236-137">-ResourceId</span></span>
<span data-ttu-id="73236-138">Управляемый ид ресурсов кластера</span><span class="sxs-lookup"><span data-stu-id="73236-138">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73236-139">-ReverseProxyEndpointPort</span><span class="sxs-lookup"><span data-stu-id="73236-139">-ReverseProxyEndpointPort</span></span>
<span data-ttu-id="73236-140">Конечная точка, используемая обратным прокси-сервером.</span><span class="sxs-lookup"><span data-stu-id="73236-140">Endpoint used by reverse proxy.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: WithPramsByName, ByNameById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-141">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="73236-141">-UpgradeMode</span></span>
<span data-ttu-id="73236-142">Режим обновления версии кода кластера.</span><span class="sxs-lookup"><span data-stu-id="73236-142">Cluster code version upgrade mode.</span></span> <span data-ttu-id="73236-143">Автоматически или вручную.</span><span class="sxs-lookup"><span data-stu-id="73236-143">Automatic or Manual.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode]
Parameter Sets: WithPramsByName, ByNameById
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73236-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73236-144">-Confirm</span></span>
<span data-ttu-id="73236-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="73236-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73236-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73236-146">-WhatIf</span></span>
<span data-ttu-id="73236-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73236-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73236-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73236-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73236-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73236-149">CommonParameters</span></span>
<span data-ttu-id="73236-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73236-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73236-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73236-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73236-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73236-152">INPUTS</span></span>

### <span data-ttu-id="73236-153">System.String</span><span class="sxs-lookup"><span data-stu-id="73236-153">System.String</span></span>

## <span data-ttu-id="73236-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73236-154">OUTPUTS</span></span>

### <span data-ttu-id="73236-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span><span class="sxs-lookup"><span data-stu-id="73236-155">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster</span></span>

## <span data-ttu-id="73236-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73236-156">NOTES</span></span>

## <span data-ttu-id="73236-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73236-157">RELATED LINKS</span></span>
