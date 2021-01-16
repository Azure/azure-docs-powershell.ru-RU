---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397303"
---
# <span data-ttu-id="3f16a-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="3f16a-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="3f16a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f16a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f16a-103">Получает сведения о потоках данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3f16a-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="3f16a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f16a-104">SYNTAX</span></span>

### <span data-ttu-id="3f16a-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f16a-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f16a-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="3f16a-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f16a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f16a-107">DESCRIPTION</span></span>
<span data-ttu-id="3f16a-108">Cmdlet **Get-AzSynapseDataFlow** получает сведения о потоках данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3f16a-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="3f16a-109">Если задать имя потока данных, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="3f16a-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="3f16a-110">Если имя не указано, этот cmdlet получает сведения обо всех потоках данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3f16a-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="3f16a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f16a-111">EXAMPLES</span></span>

### <span data-ttu-id="3f16a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f16a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3f16a-113">Эта команда получает сведения обо всех потоках данных в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3f16a-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3f16a-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f16a-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="3f16a-115">Эта команда получает сведения о потоке данных ContosoDataFlow в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3f16a-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3f16a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f16a-116">PARAMETERS</span></span>

### <span data-ttu-id="3f16a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f16a-117">-DefaultProfile</span></span>
<span data-ttu-id="3f16a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f16a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f16a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3f16a-119">-Name</span></span>
<span data-ttu-id="3f16a-120">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="3f16a-120">The data flow name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataFlowName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f16a-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f16a-121">-WorkspaceName</span></span>
<span data-ttu-id="3f16a-122">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="3f16a-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f16a-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f16a-123">-WorkspaceObject</span></span>
<span data-ttu-id="3f16a-124">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="3f16a-124">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f16a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f16a-125">CommonParameters</span></span>
<span data-ttu-id="3f16a-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f16a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f16a-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f16a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f16a-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f16a-128">INPUTS</span></span>

### <span data-ttu-id="3f16a-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f16a-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3f16a-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f16a-130">OUTPUTS</span></span>

### <span data-ttu-id="3f16a-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="3f16a-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="3f16a-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f16a-132">NOTES</span></span>

## <span data-ttu-id="3f16a-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f16a-133">RELATED LINKS</span></span>
