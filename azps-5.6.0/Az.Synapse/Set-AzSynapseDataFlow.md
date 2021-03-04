---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4254a301e599dac542a099b9c4f2ebace8929ab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952979"
---
# <span data-ttu-id="74b80-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="74b80-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="74b80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b80-102">SYNOPSIS</span></span>
<span data-ttu-id="74b80-103">Создает или обновляет поток данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="74b80-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="74b80-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="74b80-104">SYNTAX</span></span>

### <span data-ttu-id="74b80-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74b80-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74b80-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="74b80-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74b80-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74b80-107">DESCRIPTION</span></span>
<span data-ttu-id="74b80-108">Cmdlet **Set-AzSynapseDataFlow** создает поток данных или обновляет существующий поток данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="74b80-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="74b80-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="74b80-109">EXAMPLES</span></span>

### <span data-ttu-id="74b80-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74b80-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="74b80-111">Эта команда создает поток данных ContosoDataFlow в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="74b80-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="74b80-112">Эта команда будет базой данных, которая будет DataFlow.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="74b80-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="74b80-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74b80-113">PARAMETERS</span></span>

### <span data-ttu-id="74b80-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74b80-114">-AsJob</span></span>
<span data-ttu-id="74b80-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="74b80-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="74b80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b80-116">-DefaultProfile</span></span>
<span data-ttu-id="74b80-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74b80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b80-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="74b80-118">-DefinitionFile</span></span>
<span data-ttu-id="74b80-119">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="74b80-119">The JSON file path.</span></span>

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

### <span data-ttu-id="74b80-120">-Name</span><span class="sxs-lookup"><span data-stu-id="74b80-120">-Name</span></span>
<span data-ttu-id="74b80-121">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="74b80-121">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74b80-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="74b80-122">-WorkspaceName</span></span>
<span data-ttu-id="74b80-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="74b80-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="74b80-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="74b80-124">-WorkspaceObject</span></span>
<span data-ttu-id="74b80-125">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="74b80-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="74b80-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74b80-126">-Confirm</span></span>
<span data-ttu-id="74b80-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74b80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b80-128">-WhatIf</span></span>
<span data-ttu-id="74b80-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74b80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b80-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="74b80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b80-131">CommonParameters</span></span>
<span data-ttu-id="74b80-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b80-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74b80-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b80-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74b80-134">INPUTS</span></span>

### <span data-ttu-id="74b80-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="74b80-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="74b80-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="74b80-136">OUTPUTS</span></span>

### <span data-ttu-id="74b80-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="74b80-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="74b80-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="74b80-138">NOTES</span></span>

## <span data-ttu-id="74b80-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74b80-139">RELATED LINKS</span></span>
