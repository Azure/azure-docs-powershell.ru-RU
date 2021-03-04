---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 7d586af76115ddf7cada5a443dd10d51463fe576
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981843"
---
# <span data-ttu-id="cbe62-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="cbe62-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="cbe62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbe62-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe62-103">Возвращает сведения об наборе данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cbe62-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="cbe62-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cbe62-104">SYNTAX</span></span>

### <span data-ttu-id="cbe62-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cbe62-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbe62-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="cbe62-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbe62-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbe62-107">DESCRIPTION</span></span>
<span data-ttu-id="cbe62-108">Для получения сведений об наборе данных в рабочей области возвращается набор данных **Get-AzSynapseDataset.**</span><span class="sxs-lookup"><span data-stu-id="cbe62-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="cbe62-109">Если указать имя для наборов данных, этот cmdlet получит сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="cbe62-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="cbe62-110">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cbe62-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="cbe62-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cbe62-111">EXAMPLES</span></span>

### <span data-ttu-id="cbe62-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cbe62-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="cbe62-113">Эта команда получает сведения обо всех наборах данных в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbe62-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cbe62-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cbe62-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="cbe62-115">Эта команда получает сведения о наборе данных ContosoDataset в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbe62-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="cbe62-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbe62-116">PARAMETERS</span></span>

### <span data-ttu-id="cbe62-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe62-117">-DefaultProfile</span></span>
<span data-ttu-id="cbe62-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe62-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbe62-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cbe62-119">-Name</span></span>
<span data-ttu-id="cbe62-120">Имя наборов данных.</span><span class="sxs-lookup"><span data-stu-id="cbe62-120">The dataset name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatasetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe62-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbe62-121">-WorkspaceName</span></span>
<span data-ttu-id="cbe62-122">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="cbe62-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cbe62-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cbe62-123">-WorkspaceObject</span></span>
<span data-ttu-id="cbe62-124">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cbe62-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cbe62-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe62-125">CommonParameters</span></span>
<span data-ttu-id="cbe62-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe62-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe62-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbe62-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe62-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cbe62-128">INPUTS</span></span>

### <span data-ttu-id="cbe62-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cbe62-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cbe62-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cbe62-130">OUTPUTS</span></span>

### <span data-ttu-id="cbe62-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="cbe62-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="cbe62-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cbe62-132">NOTES</span></span>

## <span data-ttu-id="cbe62-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbe62-133">RELATED LINKS</span></span>
