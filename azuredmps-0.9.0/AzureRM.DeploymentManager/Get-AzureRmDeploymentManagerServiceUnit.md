---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731705"
---
# <span data-ttu-id="ae655-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ae655-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="ae655-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae655-102">SYNOPSIS</span></span>
<span data-ttu-id="ae655-103">Возвращает единицу измерения обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-103">Gets a service unit.</span></span>

## <span data-ttu-id="ae655-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae655-104">SYNTAX</span></span>

### <span data-ttu-id="ae655-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae655-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae655-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="ae655-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae655-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ae655-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae655-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ae655-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae655-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="ae655-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae655-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae655-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae655-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae655-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae655-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae655-112">DESCRIPTION</span></span>
<span data-ttu-id="ae655-113">Командлет **Get-AzureRmDeploymentManagerServiceUnit** получает модуль обслуживания в службе.</span><span class="sxs-lookup"><span data-stu-id="ae655-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="ae655-114">Укажите модуль обслуживания по ее имени, службе, в которой она была определена, имя топологии службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae655-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="ae655-115">Кроме того, можно предоставить объект ServiceUnit или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ae655-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="ae655-116">Вы можете локально изменить этот объект, а затем применить изменения к единице обслуживания с помощью командлета Set-AzureRmDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="ae655-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="ae655-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae655-117">EXAMPLES</span></span>

### <span data-ttu-id="ae655-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae655-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="ae655-119">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ae655-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ae655-120">Пример 2: получение единицы обслуживания с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae655-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="ae655-121">Эта команда получает единицу службы с именем ContosoService1Storage под службой ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ae655-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ae655-122">Пример 3: получение единиц измерения обслуживания с помощью объекта Service Unit.</span><span class="sxs-lookup"><span data-stu-id="ae655-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="ae655-123">Эта команда возвращает единицу измерения, имя которой, имя службы, имя топологии службы и ResourceGroup совпадают со свойствами Name, ServiceName, ServiceTopologyName и ResourceGroupName для $serviceUnitObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="ae655-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="ae655-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae655-124">PARAMETERS</span></span>

### <span data-ttu-id="ae655-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae655-125">-DefaultProfile</span></span>
<span data-ttu-id="ae655-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae655-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae655-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae655-127">-Name</span></span>
<span data-ttu-id="ae655-128">Название единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae655-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae655-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae655-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae655-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae655-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae655-131">-ResourceId</span></span>
<span data-ttu-id="ae655-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="ae655-132">The resource identifier.</span></span>

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

### <span data-ttu-id="ae655-133">-Служба</span><span class="sxs-lookup"><span data-stu-id="ae655-133">-Service</span></span>
<span data-ttu-id="ae655-134">Объект обслуживания, для которого необходимо создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-134">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ae655-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae655-135">-ServiceName</span></span>
<span data-ttu-id="ae655-136">Имя службы, частью которой является модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae655-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="ae655-137">-ServiceResourceId</span></span>
<span data-ttu-id="ae655-138">Идентификатор ресурса службы, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ae655-139">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ae655-139">-ServiceTopology</span></span>
<span data-ttu-id="ae655-140">Объект Topology (топология службы), в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ae655-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="ae655-141">-ServiceTopologyName</span></span>
<span data-ttu-id="ae655-142">Имя топологии службы, частью которой является единица обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="ae655-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="ae655-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="ae655-144">Идентификатор ресурса топологии служб, в котором нужно создать модуль обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="ae655-145">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ae655-145">-ServiceUnit</span></span>
<span data-ttu-id="ae655-146">Объект ресурса единицы обслуживания.</span><span class="sxs-lookup"><span data-stu-id="ae655-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="ae655-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae655-147">CommonParameters</span></span>
<span data-ttu-id="ae655-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae655-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae655-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae655-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae655-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae655-150">INPUTS</span></span>

### <span data-ttu-id="ae655-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="ae655-151">None</span></span>

## <span data-ttu-id="ae655-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae655-152">OUTPUTS</span></span>

### <span data-ttu-id="ae655-153">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="ae655-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="ae655-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae655-154">NOTES</span></span>

## <span data-ttu-id="ae655-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae655-155">RELATED LINKS</span></span>

[<span data-ttu-id="ae655-156">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ae655-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="ae655-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ae655-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="ae655-158">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="ae655-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)