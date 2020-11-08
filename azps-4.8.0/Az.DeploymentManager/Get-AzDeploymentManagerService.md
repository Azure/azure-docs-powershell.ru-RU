---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078329"
---
# <span data-ttu-id="1bb65-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="1bb65-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="1bb65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1bb65-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb65-103">Возвращает службу.</span><span class="sxs-lookup"><span data-stu-id="1bb65-103">Gets the service.</span></span>

## <span data-ttu-id="1bb65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1bb65-104">SYNTAX</span></span>

### <span data-ttu-id="1bb65-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1bb65-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bb65-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1bb65-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1bb65-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb65-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bb65-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb65-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1bb65-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="1bb65-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bb65-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bb65-110">DESCRIPTION</span></span>
<span data-ttu-id="1bb65-111">Командлет **Get-AzDeploymentManagerService** Получает службу в рамках топологии службы и возвращает объект, представляющий эту службу.</span><span class="sxs-lookup"><span data-stu-id="1bb65-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="1bb65-112">Укажите службу, указав ее имя, топологию службы и имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1bb65-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="1bb65-113">Кроме того, можно предоставить объект обслуживания или ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="1bb65-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="1bb65-114">Вы можете локально изменить этот объект, а затем применить изменения к службе с помощью командлета Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="1bb65-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="1bb65-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1bb65-115">EXAMPLES</span></span>

### <span data-ttu-id="1bb65-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1bb65-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="1bb65-117">Эта команда получает службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1bb65-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1bb65-118">Пример 2: получение службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="1bb65-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="1bb65-119">Эта команда получает службу с именем ContosoService1 в топологии службы с именем ContosoServiceTopology в ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1bb65-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1bb65-120">Пример 3: получение службы с помощью объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1bb65-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="1bb65-121">Эта команда возвращает службу, имя и название топологии обслуживания и ResourceGroup которой соответствуют свойствам Name, ServiceTopologyName и ResourceGroupName для $serviceObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="1bb65-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="1bb65-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1bb65-122">PARAMETERS</span></span>

### <span data-ttu-id="1bb65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb65-123">-DefaultProfile</span></span>
<span data-ttu-id="1bb65-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bb65-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bb65-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1bb65-125">-InputObject</span></span>
<span data-ttu-id="1bb65-126">Объект обслуживания.</span><span class="sxs-lookup"><span data-stu-id="1bb65-126">Service object.</span></span>

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

### <span data-ttu-id="1bb65-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1bb65-127">-Name</span></span>
<span data-ttu-id="1bb65-128">Имя службы.</span><span class="sxs-lookup"><span data-stu-id="1bb65-128">The name of the service.</span></span>

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

### <span data-ttu-id="1bb65-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb65-129">-ResourceGroupName</span></span>
<span data-ttu-id="1bb65-130">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1bb65-130">The resource group.</span></span>

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

### <span data-ttu-id="1bb65-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb65-131">-ResourceId</span></span>
<span data-ttu-id="1bb65-132">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="1bb65-132">The resource identifier.</span></span>

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

### <span data-ttu-id="1bb65-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="1bb65-133">-ServiceTopologyName</span></span>
<span data-ttu-id="1bb65-134">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="1bb65-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="1bb65-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="1bb65-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="1bb65-136">Объект Topology (топология службы), в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="1bb65-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="1bb65-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="1bb65-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="1bb65-138">Идентификатор ресурса топологии обслуживания, в котором должна быть создана служба.</span><span class="sxs-lookup"><span data-stu-id="1bb65-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="1bb65-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb65-139">CommonParameters</span></span>
<span data-ttu-id="1bb65-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1bb65-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb65-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1bb65-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb65-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1bb65-142">INPUTS</span></span>

### <span data-ttu-id="1bb65-143">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb65-143">System.String</span></span>

### <span data-ttu-id="1bb65-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="1bb65-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="1bb65-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bb65-145">OUTPUTS</span></span>

### <span data-ttu-id="1bb65-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="1bb65-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="1bb65-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="1bb65-147">NOTES</span></span>

## <span data-ttu-id="1bb65-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bb65-148">RELATED LINKS</span></span>