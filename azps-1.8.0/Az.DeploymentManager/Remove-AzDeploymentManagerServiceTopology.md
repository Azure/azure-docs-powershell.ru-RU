---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730987"
---
# <span data-ttu-id="6184a-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6184a-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="6184a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6184a-102">SYNOPSIS</span></span>
<span data-ttu-id="6184a-103">Удаляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="6184a-103">Deletes the service topology.</span></span> <span data-ttu-id="6184a-104">Прежде чем удалять топологию службы, необходимо удалить все службы, созданные в рамках топологии службы.</span><span class="sxs-lookup"><span data-stu-id="6184a-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="6184a-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6184a-105">SYNTAX</span></span>

### <span data-ttu-id="6184a-106">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6184a-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6184a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6184a-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6184a-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="6184a-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6184a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6184a-109">DESCRIPTION</span></span>
<span data-ttu-id="6184a-110">Командлет **Remove-AzDeploymentManagerServiceTopology** удаляет топологию службы.</span><span class="sxs-lookup"><span data-stu-id="6184a-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="6184a-111">Укажите топологию службы по ее имени и названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6184a-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="6184a-112">Кроме того, можно предоставить объект ServiceTopology или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6184a-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="6184a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6184a-113">EXAMPLES</span></span>

### <span data-ttu-id="6184a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6184a-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="6184a-115">Эта команда удаляет из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="6184a-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6184a-116">Пример 2. Удалите топологию службы, используя идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6184a-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="6184a-117">Эта команда удаляет из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="6184a-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6184a-118">Пример 3: Удаление топологии служб с помощью объекта Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="6184a-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="6184a-119">Эта команда удаляет топологию службы, имя и название ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="6184a-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="6184a-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6184a-120">PARAMETERS</span></span>

### <span data-ttu-id="6184a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6184a-121">-DefaultProfile</span></span>
<span data-ttu-id="6184a-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6184a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6184a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6184a-123">-InputObject</span></span>
<span data-ttu-id="6184a-124">Ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6184a-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="6184a-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6184a-125">-Name</span></span>
<span data-ttu-id="6184a-126">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="6184a-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="6184a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6184a-127">-PassThru</span></span>
<span data-ttu-id="6184a-128">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="6184a-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6184a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6184a-129">-ResourceGroupName</span></span>
<span data-ttu-id="6184a-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6184a-130">The resource group.</span></span>

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

### <span data-ttu-id="6184a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6184a-131">-ResourceId</span></span>
<span data-ttu-id="6184a-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="6184a-132">The resource identifier.</span></span>

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

### <span data-ttu-id="6184a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6184a-133">-Confirm</span></span>
<span data-ttu-id="6184a-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6184a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6184a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6184a-135">-WhatIf</span></span>
<span data-ttu-id="6184a-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6184a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6184a-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6184a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6184a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6184a-138">CommonParameters</span></span>
<span data-ttu-id="6184a-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6184a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6184a-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6184a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6184a-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6184a-141">INPUTS</span></span>

### <span data-ttu-id="6184a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6184a-142">System.String</span></span>

### <span data-ttu-id="6184a-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="6184a-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="6184a-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6184a-144">OUTPUTS</span></span>

### <span data-ttu-id="6184a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6184a-145">System.Boolean</span></span>

## <span data-ttu-id="6184a-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="6184a-146">NOTES</span></span>

## <span data-ttu-id="6184a-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6184a-147">RELATED LINKS</span></span>
