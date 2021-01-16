---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397308"
---
# <span data-ttu-id="adb21-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="adb21-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="adb21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adb21-102">SYNOPSIS</span></span>
<span data-ttu-id="adb21-103">Получает сведения об наборе данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="adb21-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="adb21-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="adb21-104">SYNTAX</span></span>

### <span data-ttu-id="adb21-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adb21-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="adb21-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="adb21-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adb21-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="adb21-107">DESCRIPTION</span></span>
<span data-ttu-id="adb21-108">Для получения сведений об наборе данных в рабочей области возвращается набор данных **Get-AzSynapseDataset.**</span><span class="sxs-lookup"><span data-stu-id="adb21-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="adb21-109">Если указать имя для наборов данных, этот cmdlet получит сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="adb21-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="adb21-110">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="adb21-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="adb21-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="adb21-111">EXAMPLES</span></span>

### <span data-ttu-id="adb21-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="adb21-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="adb21-113">Эта команда получает сведения обо всех наборах данных в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="adb21-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="adb21-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="adb21-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="adb21-115">Эта команда получает сведения о наборе данных ContosoDataset в рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="adb21-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="adb21-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adb21-116">PARAMETERS</span></span>

### <span data-ttu-id="adb21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adb21-117">-DefaultProfile</span></span>
<span data-ttu-id="adb21-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="adb21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adb21-119">-Name</span><span class="sxs-lookup"><span data-stu-id="adb21-119">-Name</span></span>
<span data-ttu-id="adb21-120">Имя наборов данных.</span><span class="sxs-lookup"><span data-stu-id="adb21-120">The dataset name.</span></span>

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

### <span data-ttu-id="adb21-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="adb21-121">-WorkspaceName</span></span>
<span data-ttu-id="adb21-122">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="adb21-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="adb21-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="adb21-123">-WorkspaceObject</span></span>
<span data-ttu-id="adb21-124">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="adb21-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="adb21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adb21-125">CommonParameters</span></span>
<span data-ttu-id="adb21-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adb21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adb21-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adb21-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adb21-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="adb21-128">INPUTS</span></span>

### <span data-ttu-id="adb21-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="adb21-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="adb21-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="adb21-130">OUTPUTS</span></span>

### <span data-ttu-id="adb21-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="adb21-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="adb21-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="adb21-132">NOTES</span></span>

## <span data-ttu-id="adb21-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="adb21-133">RELATED LINKS</span></span>
