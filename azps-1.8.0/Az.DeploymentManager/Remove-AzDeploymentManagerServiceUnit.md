---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730983"
---
# <span data-ttu-id="867bc-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="867bc-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="867bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="867bc-102">SYNOPSIS</span></span>
<span data-ttu-id="867bc-103">Удаление единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-103">Deletes the service unit.</span></span>

## <span data-ttu-id="867bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="867bc-104">SYNTAX</span></span>

### <span data-ttu-id="867bc-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="867bc-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867bc-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="867bc-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867bc-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="867bc-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867bc-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="867bc-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867bc-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="867bc-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867bc-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="867bc-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="867bc-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="867bc-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="867bc-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="867bc-112">DESCRIPTION</span></span>
<span data-ttu-id="867bc-113">Командлет **Remove-AzDeploymentManagerServiceUnit** удаляет модуль службы в службе.</span><span class="sxs-lookup"><span data-stu-id="867bc-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="867bc-114">Укажите модуль обслуживания по ее имени, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="867bc-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="867bc-115">Кроме того, можно предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="867bc-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="867bc-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="867bc-116">EXAMPLES</span></span>

### <span data-ttu-id="867bc-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="867bc-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="867bc-118">Эта команда удаляет модуль служб с именем ContosoService1Storage в службе ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="867bc-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="867bc-119">Пример 2: удаление единицы обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="867bc-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="867bc-120">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="867bc-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="867bc-121">Пример 3: удаление единицы обслуживания с помощью объекта сервисного модуля.</span><span class="sxs-lookup"><span data-stu-id="867bc-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="867bc-122">Эта команда удаляет сервисный модуль с именем, именем службы, именем и $serviceUnitObject свойством ResourceGroup для службы Name, ServiceName, ServiceTopologyName и ResourceGroupName, соответственно.</span><span class="sxs-lookup"><span data-stu-id="867bc-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="867bc-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="867bc-123">PARAMETERS</span></span>

### <span data-ttu-id="867bc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="867bc-124">-DefaultProfile</span></span>
<span data-ttu-id="867bc-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="867bc-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="867bc-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="867bc-126">-InputObject</span></span>
<span data-ttu-id="867bc-127">Объект ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="867bc-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="867bc-128">-Name</span></span>
<span data-ttu-id="867bc-129">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="867bc-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="867bc-130">-PassThru</span></span>
<span data-ttu-id="867bc-131">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="867bc-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="867bc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="867bc-132">-ResourceGroupName</span></span>
<span data-ttu-id="867bc-133">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="867bc-133">The resource group.</span></span>

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

### <span data-ttu-id="867bc-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="867bc-134">-ResourceId</span></span>
<span data-ttu-id="867bc-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="867bc-135">The resource identifier.</span></span>

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

### <span data-ttu-id="867bc-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="867bc-136">-ServiceName</span></span>
<span data-ttu-id="867bc-137">Имя службы, частью которой является модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="867bc-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="867bc-138">-ServiceObject</span></span>
<span data-ttu-id="867bc-139">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="867bc-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="867bc-140">-ServiceResourceId</span></span>
<span data-ttu-id="867bc-141">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="867bc-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="867bc-142">-ServiceTopologyName</span></span>
<span data-ttu-id="867bc-143">Имя топологии службы, частью которой является единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="867bc-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="867bc-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="867bc-145">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="867bc-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="867bc-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="867bc-147">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="867bc-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="867bc-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="867bc-148">-Confirm</span></span>
<span data-ttu-id="867bc-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="867bc-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="867bc-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="867bc-150">-WhatIf</span></span>
<span data-ttu-id="867bc-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="867bc-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="867bc-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="867bc-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="867bc-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="867bc-153">CommonParameters</span></span>
<span data-ttu-id="867bc-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="867bc-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="867bc-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="867bc-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="867bc-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="867bc-156">INPUTS</span></span>

### <span data-ttu-id="867bc-157">System. String</span><span class="sxs-lookup"><span data-stu-id="867bc-157">System.String</span></span>

### <span data-ttu-id="867bc-158">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="867bc-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="867bc-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="867bc-159">OUTPUTS</span></span>

### <span data-ttu-id="867bc-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="867bc-160">System.Boolean</span></span>

## <span data-ttu-id="867bc-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="867bc-161">NOTES</span></span>

## <span data-ttu-id="867bc-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="867bc-162">RELATED LINKS</span></span>
