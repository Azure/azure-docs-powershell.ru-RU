---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 284e568e1748c8bf6da3c5d43c27acb046be6172
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980691"
---
# <span data-ttu-id="62a7c-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="62a7c-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="62a7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="62a7c-103">Удаляет службу.</span><span class="sxs-lookup"><span data-stu-id="62a7c-103">Deletes the service..</span></span> <span data-ttu-id="62a7c-104">Перед удалением службы необходимо удалить все единицы обслуживания, созданные в службе.</span><span class="sxs-lookup"><span data-stu-id="62a7c-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="62a7c-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62a7c-105">SYNTAX</span></span>

### <span data-ttu-id="62a7c-106">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="62a7c-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="62a7c-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="62a7c-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a7c-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="62a7c-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a7c-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="62a7c-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62a7c-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="62a7c-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62a7c-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62a7c-111">DESCRIPTION</span></span>
<span data-ttu-id="62a7c-112">Для удаления службы в топологии службы будет удалена **cmdlet Remove-AzDeploymentManagerService.**</span><span class="sxs-lookup"><span data-stu-id="62a7c-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="62a7c-113">Укажите службу по имени, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62a7c-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="62a7c-114">Кроме того, вы можете предоставить объект Service или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="62a7c-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="62a7c-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62a7c-115">EXAMPLES</span></span>

### <span data-ttu-id="62a7c-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62a7c-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="62a7c-117">Эта команда удаляет службу с именем ContosoService1 в топологии службы ContosoServiceTopology в группе ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62a7c-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="62a7c-118">Пример 2. Удаление службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="62a7c-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="62a7c-119">Эта команда удаляет службу с именем ContosoService1 в топологии службы ContosoServiceTopology в группе ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="62a7c-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="62a7c-120">Пример 3. Удаление службы с помощью объекта-службы.</span><span class="sxs-lookup"><span data-stu-id="62a7c-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="62a7c-121">Эта команда удаляет службу, имя которой, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="62a7c-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="62a7c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62a7c-122">PARAMETERS</span></span>

### <span data-ttu-id="62a7c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a7c-123">-DefaultProfile</span></span>
<span data-ttu-id="62a7c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62a7c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a7c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62a7c-125">-InputObject</span></span>
<span data-ttu-id="62a7c-126">Сервисный объект.</span><span class="sxs-lookup"><span data-stu-id="62a7c-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62a7c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="62a7c-127">-Name</span></span>
<span data-ttu-id="62a7c-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="62a7c-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a7c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62a7c-129">-PassThru</span></span>
<span data-ttu-id="62a7c-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="62a7c-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="62a7c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a7c-131">-ResourceGroupName</span></span>
<span data-ttu-id="62a7c-132">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="62a7c-132">The resource group.</span></span>

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

### <span data-ttu-id="62a7c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62a7c-133">-ResourceId</span></span>
<span data-ttu-id="62a7c-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="62a7c-134">The resource identifier.</span></span>

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

### <span data-ttu-id="62a7c-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="62a7c-135">-ServiceTopologyName</span></span>
<span data-ttu-id="62a7c-136">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="62a7c-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="62a7c-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="62a7c-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="62a7c-138">Объект топологии службы, в котором необходимо создать службу.</span><span class="sxs-lookup"><span data-stu-id="62a7c-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a7c-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="62a7c-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="62a7c-140">Идентификатор ресурса топологии службы, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="62a7c-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62a7c-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62a7c-141">-Confirm</span></span>
<span data-ttu-id="62a7c-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="62a7c-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62a7c-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62a7c-143">-WhatIf</span></span>
<span data-ttu-id="62a7c-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62a7c-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62a7c-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62a7c-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62a7c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a7c-146">CommonParameters</span></span>
<span data-ttu-id="62a7c-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a7c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a7c-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62a7c-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a7c-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62a7c-149">INPUTS</span></span>

### <span data-ttu-id="62a7c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="62a7c-150">System.String</span></span>

### <span data-ttu-id="62a7c-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="62a7c-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="62a7c-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62a7c-152">OUTPUTS</span></span>

### <span data-ttu-id="62a7c-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62a7c-153">System.Boolean</span></span>

## <span data-ttu-id="62a7c-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62a7c-154">NOTES</span></span>

## <span data-ttu-id="62a7c-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62a7c-155">RELATED LINKS</span></span>
