---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c02a88cdb550e1ec9cb343b286d3211045873820
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980728"
---
# <span data-ttu-id="2566b-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="2566b-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="2566b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2566b-102">SYNOPSIS</span></span>
<span data-ttu-id="2566b-103">Возвращает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="2566b-103">Gets the service topology.</span></span>

## <span data-ttu-id="2566b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2566b-104">SYNTAX</span></span>

### <span data-ttu-id="2566b-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2566b-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2566b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2566b-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2566b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2566b-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2566b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2566b-108">DESCRIPTION</span></span>
<span data-ttu-id="2566b-109">Топология **службы возвращается cmdlet Get-AzDeploymentManagerServiceTopology.**</span><span class="sxs-lookup"><span data-stu-id="2566b-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="2566b-110">Вы можете изменить этот объект локально, а затем применить изменения к топологии с помощью Set-AzDeploymentManagerServiceTopology..</span><span class="sxs-lookup"><span data-stu-id="2566b-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="2566b-111">Укажите топологию службы по имени и имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2566b-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="2566b-112">Кроме того, у вас может быть объект ServiceTopology или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2566b-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="2566b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2566b-113">EXAMPLES</span></span>

### <span data-ttu-id="2566b-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2566b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="2566b-115">Эта команда получает топологию службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2566b-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2566b-116">Пример 2. Получите топологию службы с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="2566b-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="2566b-117">Эта команда получает топологию службы ContosoServiceTopology в contosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2566b-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2566b-118">Пример 3. Получить топологию службы с помощью объекта топологии службы.</span><span class="sxs-lookup"><span data-stu-id="2566b-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="2566b-119">Эта команда возвращает топологию службы, имя и группа ресурсов которой соответствуют свойствам Name и ResourceGroupName соответствующего $serviceTopologyObject службы.</span><span class="sxs-lookup"><span data-stu-id="2566b-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="2566b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2566b-120">PARAMETERS</span></span>

### <span data-ttu-id="2566b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2566b-121">-DefaultProfile</span></span>
<span data-ttu-id="2566b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2566b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2566b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2566b-123">-InputObject</span></span>
<span data-ttu-id="2566b-124">Объект ресурса топологии службы.</span><span class="sxs-lookup"><span data-stu-id="2566b-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="2566b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="2566b-125">-Name</span></span>
<span data-ttu-id="2566b-126">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="2566b-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2566b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2566b-127">-ResourceGroupName</span></span>
<span data-ttu-id="2566b-128">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2566b-128">The resource group.</span></span>

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

### <span data-ttu-id="2566b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2566b-129">-ResourceId</span></span>
<span data-ttu-id="2566b-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="2566b-130">The resource identifier.</span></span>

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

### <span data-ttu-id="2566b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2566b-131">CommonParameters</span></span>
<span data-ttu-id="2566b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2566b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2566b-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2566b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2566b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2566b-134">INPUTS</span></span>

### <span data-ttu-id="2566b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2566b-135">System.String</span></span>

### <span data-ttu-id="2566b-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="2566b-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="2566b-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2566b-137">OUTPUTS</span></span>

### <span data-ttu-id="2566b-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="2566b-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="2566b-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2566b-139">NOTES</span></span>

## <span data-ttu-id="2566b-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2566b-140">RELATED LINKS</span></span>
