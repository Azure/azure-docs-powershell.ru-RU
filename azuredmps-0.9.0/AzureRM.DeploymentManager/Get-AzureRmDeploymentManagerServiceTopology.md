---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93556328"
---
# <span data-ttu-id="0ad10-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0ad10-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="0ad10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ad10-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad10-103">Возвращает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="0ad10-103">Gets a service topology.</span></span>

## <span data-ttu-id="0ad10-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ad10-104">SYNTAX</span></span>

### <span data-ttu-id="0ad10-105">Интерактивный (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ad10-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad10-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ad10-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ad10-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad10-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad10-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad10-108">DESCRIPTION</span></span>
<span data-ttu-id="0ad10-109">Командлет **Get-AzureRmDeploymentManagerServiceTopology** получает топологию службы.</span><span class="sxs-lookup"><span data-stu-id="0ad10-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="0ad10-110">Вы можете локально изменить этот объект, а затем применить изменения к топологии с помощью командлета Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="0ad10-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="0ad10-111">Укажите топологию службы по ее имени и названию группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ad10-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="0ad10-112">Кроме того, можно предоставить объект ServiceTopology или ResourceId.</span><span class="sxs-lookup"><span data-stu-id="0ad10-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="0ad10-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ad10-113">EXAMPLES</span></span>

### <span data-ttu-id="0ad10-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ad10-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="0ad10-115">Эта команда получает из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="0ad10-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0ad10-116">Пример 2: получение топологии служб с помощью идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad10-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="0ad10-117">Эта команда получает из ContosoResourceGroup топологию службы с именем ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="0ad10-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="0ad10-118">Пример 3: получение топологии служб с помощью объекта Topology (топология службы).</span><span class="sxs-lookup"><span data-stu-id="0ad10-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="0ad10-119">Эта команда возвращает топологию службы, имя и значение ResourceGroup которой соответствуют свойствам Name и ResourceGroupName для $serviceTopologyObject соответственно.</span><span class="sxs-lookup"><span data-stu-id="0ad10-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="0ad10-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ad10-120">PARAMETERS</span></span>

### <span data-ttu-id="0ad10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad10-121">-DefaultProfile</span></span>
<span data-ttu-id="0ad10-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad10-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad10-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ad10-123">-Name</span></span>
<span data-ttu-id="0ad10-124">Имя топологии службы.</span><span class="sxs-lookup"><span data-stu-id="0ad10-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="0ad10-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad10-125">-ResourceGroupName</span></span>
<span data-ttu-id="0ad10-126">Группа ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ad10-126">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad10-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ad10-127">-ResourceId</span></span>
<span data-ttu-id="0ad10-128">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="0ad10-128">The resource identifier.</span></span>

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

### <span data-ttu-id="0ad10-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0ad10-129">-ServiceTopology</span></span>
<span data-ttu-id="0ad10-130">Объект ресурса "топология службы".</span><span class="sxs-lookup"><span data-stu-id="0ad10-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="0ad10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad10-131">CommonParameters</span></span>
<span data-ttu-id="0ad10-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ad10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad10-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad10-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad10-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ad10-134">INPUTS</span></span>

### <span data-ttu-id="0ad10-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="0ad10-135">None</span></span>

## <span data-ttu-id="0ad10-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad10-136">OUTPUTS</span></span>

### <span data-ttu-id="0ad10-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="0ad10-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="0ad10-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ad10-138">NOTES</span></span>

## <span data-ttu-id="0ad10-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ad10-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ad10-140">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0ad10-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="0ad10-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0ad10-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="0ad10-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="0ad10-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)