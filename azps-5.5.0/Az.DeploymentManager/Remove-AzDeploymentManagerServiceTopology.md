---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238103"
---
# <span data-ttu-id="10728-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="10728-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="10728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10728-102">SYNOPSIS</span></span>
<span data-ttu-id="10728-103">Удаляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="10728-103">Deletes the service topology.</span></span> <span data-ttu-id="10728-104">Перед удалением топологии службы необходимо удалить все службы, созданные в топологии службы.</span><span class="sxs-lookup"><span data-stu-id="10728-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="10728-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10728-105">SYNTAX</span></span>

### <span data-ttu-id="10728-106">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="10728-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10728-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="10728-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10728-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="10728-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10728-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10728-109">DESCRIPTION</span></span>
<span data-ttu-id="10728-110">Для **удаления топологии службы** будет удалена топология службы.</span><span class="sxs-lookup"><span data-stu-id="10728-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="10728-111">Укажите топологию службы по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10728-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="10728-112">Кроме того, у вас может быть объект ServiceTopology или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="10728-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="10728-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10728-113">EXAMPLES</span></span>

### <span data-ttu-id="10728-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10728-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="10728-115">Эта команда удаляет топологию службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="10728-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="10728-116">Пример 2. Удаление топологии службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="10728-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="10728-117">Эта команда удаляет топологию службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="10728-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="10728-118">Пример 3. Удаление топологии службы с помощью объекта топологии службы.</span><span class="sxs-lookup"><span data-stu-id="10728-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="10728-119">Эта команда удаляет топологию службы, имя и группа ресурсов которой соответствуют свойствам Name и ResourceGroupName соответствующего $serviceTopologyObject службы.</span><span class="sxs-lookup"><span data-stu-id="10728-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="10728-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10728-120">PARAMETERS</span></span>

### <span data-ttu-id="10728-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10728-121">-DefaultProfile</span></span>
<span data-ttu-id="10728-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10728-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10728-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10728-123">-InputObject</span></span>
<span data-ttu-id="10728-124">Удаляемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="10728-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="10728-125">-Name</span><span class="sxs-lookup"><span data-stu-id="10728-125">-Name</span></span>
<span data-ttu-id="10728-126">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="10728-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="10728-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10728-127">-PassThru</span></span>
<span data-ttu-id="10728-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="10728-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="10728-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10728-129">-ResourceGroupName</span></span>
<span data-ttu-id="10728-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10728-130">The resource group.</span></span>

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

### <span data-ttu-id="10728-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10728-131">-ResourceId</span></span>
<span data-ttu-id="10728-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="10728-132">The resource identifier.</span></span>

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

### <span data-ttu-id="10728-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10728-133">-Confirm</span></span>
<span data-ttu-id="10728-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10728-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10728-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10728-135">-WhatIf</span></span>
<span data-ttu-id="10728-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10728-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10728-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="10728-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10728-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10728-138">CommonParameters</span></span>
<span data-ttu-id="10728-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10728-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10728-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10728-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10728-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10728-141">INPUTS</span></span>

### <span data-ttu-id="10728-142">System.String</span><span class="sxs-lookup"><span data-stu-id="10728-142">System.String</span></span>

### <span data-ttu-id="10728-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="10728-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="10728-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10728-144">OUTPUTS</span></span>

### <span data-ttu-id="10728-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10728-145">System.Boolean</span></span>

## <span data-ttu-id="10728-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10728-146">NOTES</span></span>

## <span data-ttu-id="10728-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10728-147">RELATED LINKS</span></span>
