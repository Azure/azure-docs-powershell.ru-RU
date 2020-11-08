---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: f80f67270652d9c9edef38c9eb793074acd95a27
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074389"
---
# <span data-ttu-id="99aa7-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="99aa7-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="99aa7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="99aa7-103">Получает единицу обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-103">Gets the service unit.</span></span>

## <span data-ttu-id="99aa7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99aa7-104">SYNTAX</span></span>

### <span data-ttu-id="99aa7-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99aa7-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99aa7-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="99aa7-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99aa7-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="99aa7-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99aa7-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="99aa7-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99aa7-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="99aa7-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99aa7-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="99aa7-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99aa7-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="99aa7-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99aa7-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99aa7-112">DESCRIPTION</span></span>
<span data-ttu-id="99aa7-113">Командлет **Get-AzDeploymentManagerServiceUnit** получает модуль обслуживания в службе.</span><span class="sxs-lookup"><span data-stu-id="99aa7-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="99aa7-114">Укажите модуль обслуживания по ее имени, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99aa7-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="99aa7-115">Кроме того, можно предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="99aa7-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="99aa7-116">Вы можете локально изменить этот объект, а затем применить изменения к единице обслуживания с помощью командлета Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="99aa7-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="99aa7-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99aa7-117">EXAMPLES</span></span>

### <span data-ttu-id="99aa7-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99aa7-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="99aa7-119">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="99aa7-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="99aa7-120">Пример 2: получение единицы обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="99aa7-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="99aa7-121">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="99aa7-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="99aa7-122">Пример 3: получение единиц измерения обслуживания с помощью объекта Service Unit.</span><span class="sxs-lookup"><span data-stu-id="99aa7-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="99aa7-123">Эта команда возвращает единицу измерения, имя которой, имя службы, имя топологии службы и ResourceGroup совпадают со свойствами Name, ServiceName, ServiceTopologyName и ResourceGroupName для $serviceUnitObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="99aa7-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="99aa7-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99aa7-124">PARAMETERS</span></span>

### <span data-ttu-id="99aa7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99aa7-125">-DefaultProfile</span></span>
<span data-ttu-id="99aa7-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99aa7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99aa7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99aa7-127">-InputObject</span></span>
<span data-ttu-id="99aa7-128">Объект ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-128">Service unit resource object.</span></span>

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

### <span data-ttu-id="99aa7-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99aa7-129">-Name</span></span>
<span data-ttu-id="99aa7-130">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-130">The name of the service unit.</span></span>

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

### <span data-ttu-id="99aa7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99aa7-131">-ResourceGroupName</span></span>
<span data-ttu-id="99aa7-132">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99aa7-132">The resource group.</span></span>

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

### <span data-ttu-id="99aa7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99aa7-133">-ResourceId</span></span>
<span data-ttu-id="99aa7-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="99aa7-134">The resource identifier.</span></span>

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

### <span data-ttu-id="99aa7-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="99aa7-135">-ServiceName</span></span>
<span data-ttu-id="99aa7-136">Имя службы, частью которой является модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-136">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="99aa7-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="99aa7-137">-ServiceObject</span></span>
<span data-ttu-id="99aa7-138">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-138">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99aa7-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="99aa7-139">-ServiceResourceId</span></span>
<span data-ttu-id="99aa7-140">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-140">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99aa7-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="99aa7-141">-ServiceTopologyName</span></span>
<span data-ttu-id="99aa7-142">Имя топологии службы, частью которой является единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="99aa7-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="99aa7-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="99aa7-144">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-144">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99aa7-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="99aa7-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="99aa7-146">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="99aa7-146">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="99aa7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99aa7-147">CommonParameters</span></span>
<span data-ttu-id="99aa7-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99aa7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99aa7-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99aa7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99aa7-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99aa7-150">INPUTS</span></span>

### <span data-ttu-id="99aa7-151">System. String</span><span class="sxs-lookup"><span data-stu-id="99aa7-151">System.String</span></span>

### <span data-ttu-id="99aa7-152">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="99aa7-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="99aa7-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99aa7-153">OUTPUTS</span></span>

### <span data-ttu-id="99aa7-154">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="99aa7-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="99aa7-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="99aa7-155">NOTES</span></span>

## <span data-ttu-id="99aa7-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99aa7-156">RELATED LINKS</span></span>
