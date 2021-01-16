---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseDataFlow.md
ms.openlocfilehash: 4147343b01e53050f88429424ca7a9c70aa445c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507953"
---
# <span data-ttu-id="7a032-101">Set-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="7a032-101">Set-AzSynapseDataFlow</span></span>

## <span data-ttu-id="7a032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a032-102">SYNOPSIS</span></span>
<span data-ttu-id="7a032-103">Создает или обновляет поток данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7a032-103">Creates or updates a data flow in workspace.</span></span>

## <span data-ttu-id="7a032-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7a032-104">SYNTAX</span></span>

### <span data-ttu-id="7a032-105">SetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7a032-105">SetByName (Default)</span></span>
```
Set-AzSynapseDataFlow -WorkspaceName <String> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a032-106">SetByObject</span><span class="sxs-lookup"><span data-stu-id="7a032-106">SetByObject</span></span>
```
Set-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> -Name <String> -DefinitionFile <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a032-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7a032-107">DESCRIPTION</span></span>
<span data-ttu-id="7a032-108">Cmdlet **Set-AzSynapseDataFlow** создает поток данных или обновляет существующий поток данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7a032-108">The **Set-AzSynapseDataFlow** cmdlet creates a data flow or updates an existing data flow in workspace.</span></span>

## <span data-ttu-id="7a032-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7a032-109">EXAMPLES</span></span>

### <span data-ttu-id="7a032-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7a032-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow -DefinitionFile "C:\\samples\\DataFlow.json"
```

<span data-ttu-id="7a032-111">Эта команда создает поток данных ContosoDataFlow в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7a032-111">This command creates a data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>
<span data-ttu-id="7a032-112">Эта команда будет базой данных, которая будет DataFlow.jsфайле.</span><span class="sxs-lookup"><span data-stu-id="7a032-112">The command bases the data flow on information in the DataFlow.json file.</span></span>

## <span data-ttu-id="7a032-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a032-113">PARAMETERS</span></span>

### <span data-ttu-id="7a032-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a032-114">-AsJob</span></span>
<span data-ttu-id="7a032-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7a032-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a032-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a032-116">-DefaultProfile</span></span>
<span data-ttu-id="7a032-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7a032-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a032-118">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="7a032-118">-DefinitionFile</span></span>
<span data-ttu-id="7a032-119">Путь к файлу JSON.</span><span class="sxs-lookup"><span data-stu-id="7a032-119">The JSON file path.</span></span>

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

### <span data-ttu-id="7a032-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7a032-120">-Name</span></span>
<span data-ttu-id="7a032-121">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="7a032-121">The data flow name.</span></span>

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

### <span data-ttu-id="7a032-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7a032-122">-WorkspaceName</span></span>
<span data-ttu-id="7a032-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="7a032-123">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7a032-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7a032-124">-WorkspaceObject</span></span>
<span data-ttu-id="7a032-125">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="7a032-125">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="7a032-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a032-126">-Confirm</span></span>
<span data-ttu-id="7a032-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7a032-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a032-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a032-128">-WhatIf</span></span>
<span data-ttu-id="7a032-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a032-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a032-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7a032-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a032-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a032-131">CommonParameters</span></span>
<span data-ttu-id="7a032-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a032-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a032-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a032-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a032-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a032-134">INPUTS</span></span>

### <span data-ttu-id="7a032-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7a032-135">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="7a032-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7a032-136">OUTPUTS</span></span>

### <span data-ttu-id="7a032-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="7a032-137">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="7a032-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7a032-138">NOTES</span></span>

## <span data-ttu-id="7a032-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7a032-139">RELATED LINKS</span></span>
