---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078327"
---
# <span data-ttu-id="c0336-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="c0336-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="c0336-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0336-102">SYNOPSIS</span></span>
<span data-ttu-id="c0336-103">Получает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="c0336-103">Gets the service topology.</span></span>

## <span data-ttu-id="c0336-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0336-104">SYNTAX</span></span>

### <span data-ttu-id="c0336-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0336-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0336-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0336-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0336-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="c0336-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0336-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0336-108">DESCRIPTION</span></span>
<span data-ttu-id="c0336-109">Командлет **Get-AzDeploymentManagerServiceTopology** получает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="c0336-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="c0336-110">Вы можете локально изменить этот объект, а затем применить изменения к топологии с помощью командлета Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c0336-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="c0336-111">Укажите топологию службы по ее имени и названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0336-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="c0336-112">Кроме того, можно предоставить объект ServiceTopology или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c0336-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="c0336-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0336-113">EXAMPLES</span></span>

### <span data-ttu-id="c0336-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0336-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="c0336-115">Эта команда получает из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c0336-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c0336-116">Пример 2: получение топологии служб с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="c0336-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="c0336-117">Эта команда получает из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="c0336-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c0336-118">Пример 3: получение топологии служб с помощью объекта Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="c0336-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="c0336-119">Эта команда возвращает топологию службы, имя и значение ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="c0336-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="c0336-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0336-120">PARAMETERS</span></span>

### <span data-ttu-id="c0336-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0336-121">-DefaultProfile</span></span>
<span data-ttu-id="c0336-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0336-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0336-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0336-123">-InputObject</span></span>
<span data-ttu-id="c0336-124">Объект ресурса "топология службы".</span><span class="sxs-lookup"><span data-stu-id="c0336-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="c0336-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0336-125">-Name</span></span>
<span data-ttu-id="c0336-126">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="c0336-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="c0336-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0336-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0336-128">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0336-128">The resource group.</span></span>

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

### <span data-ttu-id="c0336-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0336-129">-ResourceId</span></span>
<span data-ttu-id="c0336-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="c0336-130">The resource identifier.</span></span>

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

### <span data-ttu-id="c0336-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0336-131">CommonParameters</span></span>
<span data-ttu-id="c0336-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0336-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0336-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0336-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0336-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0336-134">INPUTS</span></span>

### <span data-ttu-id="c0336-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c0336-135">System.String</span></span>

### <span data-ttu-id="c0336-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c0336-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c0336-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0336-137">OUTPUTS</span></span>

### <span data-ttu-id="c0336-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="c0336-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="c0336-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0336-139">NOTES</span></span>

## <span data-ttu-id="c0336-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0336-140">RELATED LINKS</span></span>
