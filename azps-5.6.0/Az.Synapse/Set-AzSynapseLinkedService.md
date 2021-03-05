---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapselinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseLinkedService.md
ms.openlocfilehash: 1e05754245b4179d02c144538473fa586531f95c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007480"
---
# <span data-ttu-id="7e08f-101">Set-AzSynapseLinkedService</span><span class="sxs-lookup"><span data-stu-id="7e08f-101">Set-AzSynapseLinkedService</span></span>

## <span data-ttu-id="7e08f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e08f-102">SYNOPSIS</span></span>
<span data-ttu-id="7e08f-103">Связывает хранилище данных или облачную службу с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="7e08f-103">Links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="7e08f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7e08f-104">SYNTAX</span></span>

### <span data-ttu-id="7e08f-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e08f-105">SetByName (Default)</span></span>
```
Set-AzSynapseLinkedService -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e08f-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7e08f-106">SetByObject</span></span>
```
Set-AzSynapseLinkedService -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e08f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e08f-107">DESCRIPTION</span></span>
<span data-ttu-id="7e08f-108">Cmdlet **Set-AzSynapseLinkedService** связывает хранилище данных или облачную службу с рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="7e08f-108">The **Set-AzSynapseLinkedService** cmdlet links a data store or a cloud service to workspace.</span></span>

## <span data-ttu-id="7e08f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7e08f-109">EXAMPLES</span></span>

### <span data-ttu-id="7e08f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e08f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseLinkedService -WorkspaceName ContosoWorkspace -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="7e08f-111">Эта команда создает связанную службу с именем ContosoLinkedService в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7e08f-111">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7e08f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7e08f-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Set-AzSynapseLinkedService -Name ContosoLinkedService -DefinitionFile "C:\\samples\\LinkedService.json"
```

<span data-ttu-id="7e08f-113">Эта команда создает связанную службу с именем ContosoLinkedService в рабочей области ContosoWorkspace через канал.</span><span class="sxs-lookup"><span data-stu-id="7e08f-113">This command creates a linked service named ContosoLinkedService in the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="7e08f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e08f-114">PARAMETERS</span></span>

### <span data-ttu-id="7e08f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e08f-115">-AsJob</span></span>
<span data-ttu-id="7e08f-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7e08f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e08f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e08f-117">-DefaultProfile</span></span>
<span data-ttu-id="7e08f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e08f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e08f-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7e08f-119">-DefinitionFile</span></span>
<span data-ttu-id="7e08f-120">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="7e08f-120">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e08f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7e08f-121">-Name</span></span>
<span data-ttu-id="7e08f-122">Имя связанной службы.</span><span class="sxs-lookup"><span data-stu-id="7e08f-122">The linked service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e08f-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7e08f-123">-WorkspaceName</span></span>
<span data-ttu-id="7e08f-124">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7e08f-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e08f-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7e08f-125">-WorkspaceObject</span></span>
<span data-ttu-id="7e08f-126">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="7e08f-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e08f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e08f-127">-Confirm</span></span>
<span data-ttu-id="7e08f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7e08f-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e08f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e08f-129">-WhatIf</span></span>
<span data-ttu-id="7e08f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e08f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e08f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7e08f-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e08f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e08f-132">CommonParameters</span></span>
<span data-ttu-id="7e08f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e08f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e08f-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e08f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e08f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e08f-135">INPUTS</span></span>

### <span data-ttu-id="7e08f-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e08f-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7e08f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e08f-137">OUTPUTS</span></span>

### <span data-ttu-id="7e08f-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span><span class="sxs-lookup"><span data-stu-id="7e08f-138">Microsoft.Azure.Commands.Synapse.Models.PSLinkedServiceResource</span></span>

## <span data-ttu-id="7e08f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7e08f-139">NOTES</span></span>

## <span data-ttu-id="7e08f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e08f-140">RELATED LINKS</span></span>
