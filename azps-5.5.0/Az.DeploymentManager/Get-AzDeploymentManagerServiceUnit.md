---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228612"
---
# <span data-ttu-id="45acb-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="45acb-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="45acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45acb-102">SYNOPSIS</span></span>
<span data-ttu-id="45acb-103">Получает единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-103">Gets the service unit.</span></span>

## <span data-ttu-id="45acb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45acb-104">SYNTAX</span></span>

### <span data-ttu-id="45acb-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45acb-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45acb-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="45acb-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45acb-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="45acb-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45acb-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="45acb-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45acb-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="45acb-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45acb-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="45acb-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45acb-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="45acb-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45acb-112">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45acb-112">DESCRIPTION</span></span>
<span data-ttu-id="45acb-113">**Cmdlet Get-AzDeploymentManagerServiceUnit** получает единицу обслуживания в службе.</span><span class="sxs-lookup"><span data-stu-id="45acb-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="45acb-114">Укажите единицу обслуживания по названию, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45acb-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="45acb-115">Кроме того, вы можете предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="45acb-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="45acb-116">Вы можете изменить этот объект локально, а затем применить изменения к единице обслуживания с помощью Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="45acb-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="45acb-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45acb-117">EXAMPLES</span></span>

### <span data-ttu-id="45acb-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45acb-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="45acb-119">Эта команда получает службу с именем ContosoService1Storage службы ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45acb-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="45acb-120">Пример 2. Получить единицу обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="45acb-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="45acb-121">Эта команда получает службу с именем ContosoService1Storage службы ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="45acb-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="45acb-122">Пример 3. Получить единицу обслуживания с помощью объекта единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="45acb-123">Эта команда возвращает единицу службы, имя которой, имя службы, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceName, ServiceTopologyName и ResourceGroupName $serviceUnitObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="45acb-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="45acb-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45acb-124">PARAMETERS</span></span>

### <span data-ttu-id="45acb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45acb-125">-DefaultProfile</span></span>
<span data-ttu-id="45acb-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45acb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45acb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45acb-127">-InputObject</span></span>
<span data-ttu-id="45acb-128">Объект ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="45acb-129">-Name</span><span class="sxs-lookup"><span data-stu-id="45acb-129">-Name</span></span>
<span data-ttu-id="45acb-130">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45acb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45acb-131">-ResourceGroupName</span></span>
<span data-ttu-id="45acb-132">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45acb-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45acb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45acb-133">-ResourceId</span></span>
<span data-ttu-id="45acb-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="45acb-134">The resource identifier.</span></span>

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

### <span data-ttu-id="45acb-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="45acb-135">-ServiceName</span></span>
<span data-ttu-id="45acb-136">Название службы, в состав которого входит единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="45acb-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="45acb-137">-ServiceObject</span></span>
<span data-ttu-id="45acb-138">Объект-служба, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="45acb-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="45acb-139">-ServiceResourceId</span></span>
<span data-ttu-id="45acb-140">Идентификатор ресурса службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="45acb-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="45acb-141">-ServiceTopologyName</span></span>
<span data-ttu-id="45acb-142">Имя топологии службы, в состав которого входит единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="45acb-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="45acb-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="45acb-144">Объект топологии службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="45acb-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="45acb-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="45acb-146">Идентификатор ресурса топологии службы, в котором нужно создать единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="45acb-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="45acb-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45acb-147">CommonParameters</span></span>
<span data-ttu-id="45acb-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45acb-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45acb-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45acb-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45acb-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45acb-150">INPUTS</span></span>

### <span data-ttu-id="45acb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="45acb-151">System.String</span></span>

### <span data-ttu-id="45acb-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="45acb-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="45acb-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45acb-153">OUTPUTS</span></span>

### <span data-ttu-id="45acb-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="45acb-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="45acb-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45acb-155">NOTES</span></span>

## <span data-ttu-id="45acb-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45acb-156">RELATED LINKS</span></span>
