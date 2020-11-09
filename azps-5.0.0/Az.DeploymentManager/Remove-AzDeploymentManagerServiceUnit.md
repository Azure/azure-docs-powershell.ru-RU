---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312671"
---
# <span data-ttu-id="a47cb-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a47cb-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a47cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a47cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a47cb-103">Удаление единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-103">Deletes the service unit.</span></span>

## <span data-ttu-id="a47cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a47cb-104">SYNTAX</span></span>

### <span data-ttu-id="a47cb-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a47cb-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47cb-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a47cb-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47cb-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a47cb-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47cb-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="a47cb-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47cb-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a47cb-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47cb-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a47cb-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a47cb-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="a47cb-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a47cb-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a47cb-112">DESCRIPTION</span></span>
<span data-ttu-id="a47cb-113">Командлет **Remove-AzDeploymentManagerServiceUnit** удаляет модуль службы в службе.</span><span class="sxs-lookup"><span data-stu-id="a47cb-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="a47cb-114">Укажите модуль обслуживания по ее имени, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a47cb-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="a47cb-115">Кроме того, можно предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a47cb-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="a47cb-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a47cb-116">EXAMPLES</span></span>

### <span data-ttu-id="a47cb-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a47cb-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="a47cb-118">Эта команда удаляет модуль служб с именем ContosoService1Storage в службе ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a47cb-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a47cb-119">Пример 2: удаление единицы обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="a47cb-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="a47cb-120">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a47cb-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a47cb-121">Пример 3: удаление единицы обслуживания с помощью объекта сервисного модуля.</span><span class="sxs-lookup"><span data-stu-id="a47cb-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="a47cb-122">Эта команда удаляет сервисный модуль с именем, именем службы, именем и $serviceUnitObject свойством ResourceGroup для службы Name, ServiceName, ServiceTopologyName и ResourceGroupName, соответственно.</span><span class="sxs-lookup"><span data-stu-id="a47cb-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="a47cb-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a47cb-123">PARAMETERS</span></span>

### <span data-ttu-id="a47cb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47cb-124">-DefaultProfile</span></span>
<span data-ttu-id="a47cb-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a47cb-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a47cb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a47cb-126">-InputObject</span></span>
<span data-ttu-id="a47cb-127">Объект ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a47cb-128">-Name</span></span>
<span data-ttu-id="a47cb-129">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a47cb-130">-PassThru</span></span>
<span data-ttu-id="a47cb-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="a47cb-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a47cb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47cb-132">-ResourceGroupName</span></span>
<span data-ttu-id="a47cb-133">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a47cb-133">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a47cb-134">-ResourceId</span></span>
<span data-ttu-id="a47cb-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="a47cb-135">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a47cb-136">-ServiceName</span></span>
<span data-ttu-id="a47cb-137">Имя службы, частью которой является модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="a47cb-138">-ServiceObject</span></span>
<span data-ttu-id="a47cb-139">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a47cb-140">-ServiceResourceId</span></span>
<span data-ttu-id="a47cb-141">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="a47cb-142">-ServiceTopologyName</span></span>
<span data-ttu-id="a47cb-143">Имя топологии службы, частью которой является единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-143">The name of the service topology the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="a47cb-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="a47cb-145">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a47cb-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a47cb-147">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="a47cb-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47cb-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a47cb-148">-Confirm</span></span>
<span data-ttu-id="a47cb-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a47cb-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a47cb-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a47cb-150">-WhatIf</span></span>
<span data-ttu-id="a47cb-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a47cb-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a47cb-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a47cb-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a47cb-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47cb-153">CommonParameters</span></span>
<span data-ttu-id="a47cb-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a47cb-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47cb-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a47cb-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47cb-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a47cb-156">INPUTS</span></span>

### <span data-ttu-id="a47cb-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a47cb-157">System.String</span></span>

### <span data-ttu-id="a47cb-158">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a47cb-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a47cb-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a47cb-159">OUTPUTS</span></span>

### <span data-ttu-id="a47cb-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a47cb-160">System.Boolean</span></span>

## <span data-ttu-id="a47cb-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="a47cb-161">NOTES</span></span>

## <span data-ttu-id="a47cb-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a47cb-162">RELATED LINKS</span></span>
