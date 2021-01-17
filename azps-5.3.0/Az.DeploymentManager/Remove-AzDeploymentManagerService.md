---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426412"
---
# <span data-ttu-id="9171f-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="9171f-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="9171f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9171f-102">SYNOPSIS</span></span>
<span data-ttu-id="9171f-103">Удаляет службу.</span><span class="sxs-lookup"><span data-stu-id="9171f-103">Deletes the service..</span></span> <span data-ttu-id="9171f-104">Перед удалением службы необходимо удалить все единицы обслуживания, созданные в службе.</span><span class="sxs-lookup"><span data-stu-id="9171f-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="9171f-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9171f-105">SYNTAX</span></span>

### <span data-ttu-id="9171f-106">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9171f-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9171f-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="9171f-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9171f-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9171f-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9171f-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9171f-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9171f-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="9171f-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9171f-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9171f-111">DESCRIPTION</span></span>
<span data-ttu-id="9171f-112">С **его учетом** удаляется служба в топологии службы.</span><span class="sxs-lookup"><span data-stu-id="9171f-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="9171f-113">Укажите службу по имени, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9171f-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="9171f-114">Кроме того, вы можете предоставить объект Service или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9171f-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="9171f-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9171f-115">EXAMPLES</span></span>

### <span data-ttu-id="9171f-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9171f-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="9171f-117">Эта команда удаляет службу с именем ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9171f-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9171f-118">Пример 2. Удаление службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="9171f-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="9171f-119">Эта команда удаляет службу с именем ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9171f-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9171f-120">Пример 3. Удаление службы с помощью объекта-службы.</span><span class="sxs-lookup"><span data-stu-id="9171f-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="9171f-121">Эта команда удаляет службу, имя которой, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="9171f-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="9171f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9171f-122">PARAMETERS</span></span>

### <span data-ttu-id="9171f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9171f-123">-DefaultProfile</span></span>
<span data-ttu-id="9171f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9171f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9171f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9171f-125">-InputObject</span></span>
<span data-ttu-id="9171f-126">Сервисный объект.</span><span class="sxs-lookup"><span data-stu-id="9171f-126">Service object.</span></span>

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

### <span data-ttu-id="9171f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="9171f-127">-Name</span></span>
<span data-ttu-id="9171f-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="9171f-128">The name of the service.</span></span>

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

### <span data-ttu-id="9171f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9171f-129">-PassThru</span></span>
<span data-ttu-id="9171f-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9171f-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9171f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9171f-131">-ResourceGroupName</span></span>
<span data-ttu-id="9171f-132">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9171f-132">The resource group.</span></span>

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

### <span data-ttu-id="9171f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9171f-133">-ResourceId</span></span>
<span data-ttu-id="9171f-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="9171f-134">The resource identifier.</span></span>

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

### <span data-ttu-id="9171f-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="9171f-135">-ServiceTopologyName</span></span>
<span data-ttu-id="9171f-136">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="9171f-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="9171f-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="9171f-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="9171f-138">Объект топологии службы, в котором необходимо создать службу.</span><span class="sxs-lookup"><span data-stu-id="9171f-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="9171f-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9171f-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="9171f-140">Идентификатор ресурса топологии службы, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="9171f-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="9171f-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9171f-141">-Confirm</span></span>
<span data-ttu-id="9171f-142">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9171f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9171f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9171f-143">-WhatIf</span></span>
<span data-ttu-id="9171f-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9171f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9171f-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9171f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9171f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9171f-146">CommonParameters</span></span>
<span data-ttu-id="9171f-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9171f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9171f-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9171f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9171f-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9171f-149">INPUTS</span></span>

### <span data-ttu-id="9171f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9171f-150">System.String</span></span>

### <span data-ttu-id="9171f-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="9171f-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="9171f-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9171f-152">OUTPUTS</span></span>

### <span data-ttu-id="9171f-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9171f-153">System.Boolean</span></span>

## <span data-ttu-id="9171f-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9171f-154">NOTES</span></span>

## <span data-ttu-id="9171f-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9171f-155">RELATED LINKS</span></span>
