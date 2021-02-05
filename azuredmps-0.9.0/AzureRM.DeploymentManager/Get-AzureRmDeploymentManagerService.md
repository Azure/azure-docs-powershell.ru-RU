---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572111"
---
# <span data-ttu-id="4f033-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="4f033-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="4f033-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f033-102">SYNOPSIS</span></span>
<span data-ttu-id="4f033-103">Возвращает службу в топологии службы.</span><span class="sxs-lookup"><span data-stu-id="4f033-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="4f033-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4f033-104">SYNTAX</span></span>

### <span data-ttu-id="4f033-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f033-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f033-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="4f033-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f033-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="4f033-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f033-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f033-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f033-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="4f033-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f033-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f033-110">DESCRIPTION</span></span>
<span data-ttu-id="4f033-111">**Cmdlet Get-AzureRmDeploymentManagerService** получает службу в топологии службы и возвращает объект, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="4f033-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="4f033-112">Укажите службу по имени, топологии службы и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f033-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="4f033-113">Кроме того, вы можете предоставить объект Service или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4f033-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="4f033-114">Вы можете изменить этот объект локально, а затем применить изменения к службе с помощью Set-AzureRmDeploymentManagerService-управления.</span><span class="sxs-lookup"><span data-stu-id="4f033-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="4f033-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4f033-115">EXAMPLES</span></span>

### <span data-ttu-id="4f033-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f033-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="4f033-117">Эта команда получает службу с именем ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4f033-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4f033-118">Пример 2. Получите службу, используя идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4f033-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="4f033-119">Эта команда получает службу с именем ContosoService1 в топологии службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4f033-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4f033-120">Пример 3. Получить службу с использованием объекта-службы.</span><span class="sxs-lookup"><span data-stu-id="4f033-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="4f033-121">Эта команда возвращает службу, имя которой, имя топологии службы и группа ресурсов соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="4f033-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="4f033-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f033-122">PARAMETERS</span></span>

### <span data-ttu-id="4f033-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f033-123">-DefaultProfile</span></span>
<span data-ttu-id="4f033-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f033-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f033-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4f033-125">-Name</span></span>
<span data-ttu-id="4f033-126">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="4f033-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f033-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f033-127">-ResourceGroupName</span></span>
<span data-ttu-id="4f033-128">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4f033-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f033-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f033-129">-ResourceId</span></span>
<span data-ttu-id="4f033-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4f033-130">The resource identifier.</span></span>

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

### <span data-ttu-id="4f033-131">-Service</span><span class="sxs-lookup"><span data-stu-id="4f033-131">-Service</span></span>
<span data-ttu-id="4f033-132">Сервисный объект.</span><span class="sxs-lookup"><span data-stu-id="4f033-132">Service object.</span></span>

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

### <span data-ttu-id="4f033-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="4f033-133">-ServiceTopology</span></span>
<span data-ttu-id="4f033-134">Объект топологии службы, в котором необходимо создать службу.</span><span class="sxs-lookup"><span data-stu-id="4f033-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="4f033-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="4f033-135">-ServiceTopologyName</span></span>
<span data-ttu-id="4f033-136">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="4f033-136">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f033-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="4f033-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="4f033-138">Идентификатор ресурса топологии службы, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="4f033-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="4f033-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f033-139">CommonParameters</span></span>
<span data-ttu-id="4f033-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f033-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f033-141">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f033-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f033-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f033-142">INPUTS</span></span>

### <span data-ttu-id="4f033-143">Нет</span><span class="sxs-lookup"><span data-stu-id="4f033-143">None</span></span>

## <span data-ttu-id="4f033-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f033-144">OUTPUTS</span></span>

### <span data-ttu-id="4f033-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="4f033-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="4f033-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4f033-146">NOTES</span></span>

## <span data-ttu-id="4f033-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f033-147">RELATED LINKS</span></span>

[<span data-ttu-id="4f033-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="4f033-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="4f033-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="4f033-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="4f033-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="4f033-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
