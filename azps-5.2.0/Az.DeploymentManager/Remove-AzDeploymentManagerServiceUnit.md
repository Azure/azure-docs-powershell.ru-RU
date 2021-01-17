---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397807"
---
# <span data-ttu-id="9a895-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="9a895-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="9a895-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a895-102">SYNOPSIS</span></span>
<span data-ttu-id="9a895-103">Удаляет единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-103">Deletes the service unit.</span></span>

## <span data-ttu-id="9a895-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9a895-104">SYNTAX</span></span>

### <span data-ttu-id="9a895-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a895-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="9a895-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="9a895-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="9a895-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="9a895-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a895-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a895-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="9a895-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a895-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a895-112">DESCRIPTION</span></span>
<span data-ttu-id="9a895-113">**Cmdlet Remove-AzDeploymentManagerServiceUnit** удаляет единицу обслуживания в службе.</span><span class="sxs-lookup"><span data-stu-id="9a895-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="9a895-114">Укажите единицу обслуживания по названию, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a895-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="9a895-115">Кроме того, вы можете предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9a895-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="9a895-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9a895-116">EXAMPLES</span></span>

### <span data-ttu-id="9a895-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a895-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="9a895-118">Эта команда удаляет службу с именем ContosoService1Storage службы ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9a895-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9a895-119">Пример 2. Удаление единицы обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="9a895-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="9a895-120">Эта команда получает службу с именем ContosoService1Storage службы ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9a895-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9a895-121">Пример 3. Удаление единицы обслуживания с помощью объекта единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="9a895-122">Эта команда удаляет единицу службы, имя которой, имя службы, имя топологии службы и группа ресурсов соответствуют свойствам "Имя Службы", "НазваниеПолуки" и "ИмяГруппы Ресурсов" $serviceUnitObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="9a895-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="9a895-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a895-123">PARAMETERS</span></span>

### <span data-ttu-id="9a895-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a895-124">-DefaultProfile</span></span>
<span data-ttu-id="9a895-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a895-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a895-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a895-126">-InputObject</span></span>
<span data-ttu-id="9a895-127">Объект ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="9a895-128">-Name</span><span class="sxs-lookup"><span data-stu-id="9a895-128">-Name</span></span>
<span data-ttu-id="9a895-129">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-129">The name of the service unit.</span></span>

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

### <span data-ttu-id="9a895-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a895-130">-PassThru</span></span>
<span data-ttu-id="9a895-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9a895-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9a895-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a895-132">-ResourceGroupName</span></span>
<span data-ttu-id="9a895-133">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9a895-133">The resource group.</span></span>

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

### <span data-ttu-id="9a895-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a895-134">-ResourceId</span></span>
<span data-ttu-id="9a895-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9a895-135">The resource identifier.</span></span>

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

### <span data-ttu-id="9a895-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9a895-136">-ServiceName</span></span>
<span data-ttu-id="9a895-137">Название службы, в состав которого входит единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="9a895-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="9a895-138">-ServiceObject</span></span>
<span data-ttu-id="9a895-139">Объект-служба, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="9a895-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="9a895-140">-ServiceResourceId</span></span>
<span data-ttu-id="9a895-141">Идентификатор ресурса службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="9a895-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="9a895-142">-ServiceTopologyName</span></span>
<span data-ttu-id="9a895-143">Имя топологии службы, в состав которого входит единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="9a895-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="9a895-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="9a895-145">Объект топологии службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="9a895-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9a895-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="9a895-147">Идентификатор ресурса топологии службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9a895-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="9a895-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a895-148">-Confirm</span></span>
<span data-ttu-id="9a895-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9a895-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a895-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a895-150">-WhatIf</span></span>
<span data-ttu-id="9a895-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a895-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a895-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9a895-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a895-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a895-153">CommonParameters</span></span>
<span data-ttu-id="9a895-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a895-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a895-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a895-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a895-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9a895-156">INPUTS</span></span>

### <span data-ttu-id="9a895-157">System.String</span><span class="sxs-lookup"><span data-stu-id="9a895-157">System.String</span></span>

### <span data-ttu-id="9a895-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="9a895-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="9a895-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9a895-159">OUTPUTS</span></span>

### <span data-ttu-id="9a895-160">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a895-160">System.Boolean</span></span>

## <span data-ttu-id="9a895-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9a895-161">NOTES</span></span>

## <span data-ttu-id="9a895-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a895-162">RELATED LINKS</span></span>
