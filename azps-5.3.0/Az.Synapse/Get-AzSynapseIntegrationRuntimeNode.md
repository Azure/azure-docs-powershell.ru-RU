---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: 5df58da7ef5fa0829da27f4d6a46372f42bc9dc5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424524"
---
# <span data-ttu-id="67ec7-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="67ec7-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="67ec7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="67ec7-103">Возвращает сведения об узле для интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="67ec7-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="67ec7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67ec7-104">SYNTAX</span></span>

### <span data-ttu-id="67ec7-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67ec7-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67ec7-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ec7-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ec7-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ec7-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67ec7-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ec7-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ec7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67ec7-109">DESCRIPTION</span></span>
<span data-ttu-id="67ec7-110">Cmdlet **Get-AzSynapseIntegrationRuntimeNode** получает подробные сведения об узле интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="67ec7-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="67ec7-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67ec7-111">EXAMPLES</span></span>

### <span data-ttu-id="67ec7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="67ec7-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="67ec7-113">Командлет получает сведения узла Node_1 в режиме самостоятельной интеграции "test-selfhost-ir" в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="67ec7-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="67ec7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="67ec7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="67ec7-115">Он получает сведения узла Node_1 в режиме самостоятельной интеграции "test-selfhost-ir" в рабочей области "test-df-eu2", включая IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="67ec7-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="67ec7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ec7-116">PARAMETERS</span></span>

### <span data-ttu-id="67ec7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ec7-117">-DefaultProfile</span></span>
<span data-ttu-id="67ec7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67ec7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ec7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ec7-119">-InputObject</span></span>
<span data-ttu-id="67ec7-120">Объект интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="67ec7-120">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="67ec7-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="67ec7-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="67ec7-122">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="67ec7-123">-IpAddress</span></span>
<span data-ttu-id="67ec7-124">IP-адрес узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="67ec7-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="67ec7-125">-Name</span><span class="sxs-lookup"><span data-stu-id="67ec7-125">-Name</span></span>
<span data-ttu-id="67ec7-126">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="67ec7-126">The integration runtime node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ec7-127">-ResourceGroupName</span></span>
<span data-ttu-id="67ec7-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67ec7-128">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ec7-129">-ResourceId</span></span>
<span data-ttu-id="67ec7-130">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="67ec7-130">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="67ec7-131">-WorkspaceName</span></span>
<span data-ttu-id="67ec7-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="67ec7-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="67ec7-133">-WorkspaceObject</span></span>
<span data-ttu-id="67ec7-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="67ec7-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ec7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ec7-135">CommonParameters</span></span>
<span data-ttu-id="67ec7-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ec7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ec7-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67ec7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ec7-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67ec7-138">INPUTS</span></span>

### <span data-ttu-id="67ec7-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="67ec7-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="67ec7-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="67ec7-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="67ec7-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67ec7-141">OUTPUTS</span></span>

### <span data-ttu-id="67ec7-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="67ec7-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="67ec7-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="67ec7-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="67ec7-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67ec7-144">NOTES</span></span>

## <span data-ttu-id="67ec7-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67ec7-145">RELATED LINKS</span></span>
