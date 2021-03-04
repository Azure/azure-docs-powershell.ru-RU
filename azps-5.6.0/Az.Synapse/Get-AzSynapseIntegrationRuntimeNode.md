---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapseintegrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseIntegrationRuntimeNode.md
ms.openlocfilehash: dbd791b3ab77889e8c78279b576b614c4d86b4b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994734"
---
# <span data-ttu-id="ec15b-101">Get-AzSynapseIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ec15b-101">Get-AzSynapseIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ec15b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec15b-102">SYNOPSIS</span></span>
<span data-ttu-id="ec15b-103">Возвращает сведения об узле узла для интеграции со временем запуска.</span><span class="sxs-lookup"><span data-stu-id="ec15b-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="ec15b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ec15b-104">SYNTAX</span></span>

### <span data-ttu-id="ec15b-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ec15b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseIntegrationRuntimeNode [-ResourceGroupName <String>] -WorkspaceName <String>
 -IntegrationRuntimeName <String> -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec15b-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec15b-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -IntegrationRuntimeName <String> -WorkspaceObject <PSSynapseWorkspace>
 -Name <String> [-IpAddress] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec15b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec15b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -ResourceId <String> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec15b-108">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec15b-108">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseIntegrationRuntimeNode -InputObject <PSIntegrationRuntime> -Name <String> [-IpAddress]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec15b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec15b-109">DESCRIPTION</span></span>
<span data-ttu-id="ec15b-110">Cmdlet **Get-AzSynapseIntegrationRuntimeNode** получает подробные сведения об узле интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="ec15b-110">The **Get-AzSynapseIntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="ec15b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ec15b-111">EXAMPLES</span></span>

### <span data-ttu-id="ec15b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ec15b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'
```

<span data-ttu-id="ec15b-113">Командлет получает сведения узла Node_1 в режиме самостоятельной интеграции "test-selfhost-ir" в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ec15b-113">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace ContosoWorkspace.</span></span>

### <span data-ttu-id="ec15b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ec15b-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseIntegrationRuntimeNode -WorkspaceName ContosoWorkspace -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress
```

<span data-ttu-id="ec15b-115">Он получает в рабочей области сведения узла Node_1 в режиме самостоятельной интеграции "test-selfhost-ir" в рабочей области test-df-eu2, включая IP-адрес.</span><span class="sxs-lookup"><span data-stu-id="ec15b-115">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in workspace 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="ec15b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec15b-116">PARAMETERS</span></span>

### <span data-ttu-id="ec15b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec15b-117">-DefaultProfile</span></span>
<span data-ttu-id="ec15b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec15b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec15b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec15b-119">-InputObject</span></span>
<span data-ttu-id="ec15b-120">Объект runtime интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec15b-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="ec15b-121">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ec15b-121">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ec15b-122">Имя времени запуска интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec15b-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="ec15b-123">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="ec15b-123">-IpAddress</span></span>
<span data-ttu-id="ec15b-124">IP-адрес узла интеграции runtime.</span><span class="sxs-lookup"><span data-stu-id="ec15b-124">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="ec15b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ec15b-125">-Name</span></span>
<span data-ttu-id="ec15b-126">Имя узла времени интеграции.</span><span class="sxs-lookup"><span data-stu-id="ec15b-126">The integration runtime node name.</span></span>

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

### <span data-ttu-id="ec15b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec15b-127">-ResourceGroupName</span></span>
<span data-ttu-id="ec15b-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ec15b-128">Resource group name.</span></span>

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

### <span data-ttu-id="ec15b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec15b-129">-ResourceId</span></span>
<span data-ttu-id="ec15b-130">Идентификатор ресурса времени запуска интеграции Synapse.</span><span class="sxs-lookup"><span data-stu-id="ec15b-130">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="ec15b-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ec15b-131">-WorkspaceName</span></span>
<span data-ttu-id="ec15b-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="ec15b-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ec15b-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ec15b-133">-WorkspaceObject</span></span>
<span data-ttu-id="ec15b-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="ec15b-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ec15b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec15b-135">CommonParameters</span></span>
<span data-ttu-id="ec15b-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec15b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec15b-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ec15b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec15b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ec15b-138">INPUTS</span></span>

### <span data-ttu-id="ec15b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ec15b-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ec15b-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="ec15b-140">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="ec15b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ec15b-141">OUTPUTS</span></span>

### <span data-ttu-id="ec15b-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ec15b-142">Microsoft.Azure.Commands.Synapse.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="ec15b-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="ec15b-143">Microsoft.Azure.Commands.Synapse.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="ec15b-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ec15b-144">NOTES</span></span>

## <span data-ttu-id="ec15b-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec15b-145">RELATED LINKS</span></span>
