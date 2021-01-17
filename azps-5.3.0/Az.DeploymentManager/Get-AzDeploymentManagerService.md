---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98426476"
---
# <span data-ttu-id="d7bde-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d7bde-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="d7bde-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7bde-102">SYNOPSIS</span></span>
<span data-ttu-id="d7bde-103">Получает службу.</span><span class="sxs-lookup"><span data-stu-id="d7bde-103">Gets the service.</span></span>

## <span data-ttu-id="d7bde-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7bde-104">SYNTAX</span></span>

### <span data-ttu-id="d7bde-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7bde-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bde-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d7bde-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7bde-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bde-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7bde-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bde-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d7bde-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="d7bde-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7bde-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7bde-110">DESCRIPTION</span></span>
<span data-ttu-id="d7bde-111">**Cmdlet Get-AzDeploymentManagerService** получает службу в топологии службы и возвращает объект, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="d7bde-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="d7bde-112">Укажите службу по имени, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7bde-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="d7bde-113">Кроме того, вы можете предоставить объект Service или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d7bde-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="d7bde-114">Вы можете изменить этот объект локально, а затем применить изменения к службе с помощью Set-AzDeploymentManagerService-управления.</span><span class="sxs-lookup"><span data-stu-id="d7bde-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="d7bde-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7bde-115">EXAMPLES</span></span>

### <span data-ttu-id="d7bde-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7bde-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="d7bde-117">Эта команда получает службу с именем ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d7bde-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d7bde-118">Пример 2. Получить службу с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7bde-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="d7bde-119">Эта команда получает службу с именем ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d7bde-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d7bde-120">Пример 3. Получить службу с использованием объекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d7bde-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="d7bde-121">Эта команда возвращает службу, имя которой, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="d7bde-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="d7bde-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7bde-122">PARAMETERS</span></span>

### <span data-ttu-id="d7bde-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7bde-123">-DefaultProfile</span></span>
<span data-ttu-id="d7bde-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7bde-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7bde-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7bde-125">-InputObject</span></span>
<span data-ttu-id="d7bde-126">Сервисный объект.</span><span class="sxs-lookup"><span data-stu-id="d7bde-126">Service object.</span></span>

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

### <span data-ttu-id="d7bde-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d7bde-127">-Name</span></span>
<span data-ttu-id="d7bde-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="d7bde-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bde-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7bde-129">-ResourceGroupName</span></span>
<span data-ttu-id="d7bde-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7bde-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bde-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bde-131">-ResourceId</span></span>
<span data-ttu-id="d7bde-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="d7bde-132">The resource identifier.</span></span>

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

### <span data-ttu-id="d7bde-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="d7bde-133">-ServiceTopologyName</span></span>
<span data-ttu-id="d7bde-134">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="d7bde-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="d7bde-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d7bde-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="d7bde-136">Объект топологии службы, в котором необходимо создать службу.</span><span class="sxs-lookup"><span data-stu-id="d7bde-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bde-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d7bde-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="d7bde-138">Идентификатор ресурса топологии службы, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="d7bde-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7bde-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7bde-139">CommonParameters</span></span>
<span data-ttu-id="d7bde-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7bde-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7bde-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7bde-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7bde-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7bde-142">INPUTS</span></span>

### <span data-ttu-id="d7bde-143">System.String</span><span class="sxs-lookup"><span data-stu-id="d7bde-143">System.String</span></span>

### <span data-ttu-id="d7bde-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d7bde-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d7bde-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7bde-145">OUTPUTS</span></span>

### <span data-ttu-id="d7bde-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d7bde-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d7bde-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7bde-147">NOTES</span></span>

## <span data-ttu-id="d7bde-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7bde-148">RELATED LINKS</span></span>
