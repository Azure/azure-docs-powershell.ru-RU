---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataset.md
ms.openlocfilehash: 8919c554fb32a102991b9c40236e897662709ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246500"
---
# <span data-ttu-id="4930c-101">Get-AzSynapseDataset</span><span class="sxs-lookup"><span data-stu-id="4930c-101">Get-AzSynapseDataset</span></span>

## <span data-ttu-id="4930c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4930c-102">SYNOPSIS</span></span>
<span data-ttu-id="4930c-103">Получение сведений о наборах данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4930c-103">Gets information about datasets in workspace.</span></span>

## <span data-ttu-id="4930c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4930c-104">SYNTAX</span></span>

### <span data-ttu-id="4930c-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4930c-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataset -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4930c-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="4930c-106">GetByObject</span></span>
```
Get-AzSynapseDataset -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4930c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4930c-107">DESCRIPTION</span></span>
<span data-ttu-id="4930c-108">Командлет **Get-AzSynapseDataset** получает сведения о наборах данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4930c-108">The **Get-AzSynapseDataset** cmdlet gets information about datasets in workspace.</span></span>
<span data-ttu-id="4930c-109">Если вы задаете имя набора данных, этот командлет получает сведения об этом наборе данных.</span><span class="sxs-lookup"><span data-stu-id="4930c-109">If you specify the name of a dataset, this cmdlet gets information about that dataset.</span></span>
<span data-ttu-id="4930c-110">Если имя не задано, этот командлет получает сведения обо всех наборах данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4930c-110">If you do not specify a name, this cmdlet gets information about all the datasets in the workspace.</span></span>

## <span data-ttu-id="4930c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4930c-111">EXAMPLES</span></span>

### <span data-ttu-id="4930c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4930c-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="4930c-113">Эта команда получает сведения обо всех наборах данных в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4930c-113">This command gets information about all datasets in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="4930c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4930c-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataset -WorkspaceName ContosoWorkspace -Name ContosoDataset
```

<span data-ttu-id="4930c-115">Эта команда получает сведения о наборе данных с именем ContosoDataset в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4930c-115">This command gets information about the dataset named ContosoDataset in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4930c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4930c-116">PARAMETERS</span></span>

### <span data-ttu-id="4930c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4930c-117">-DefaultProfile</span></span>
<span data-ttu-id="4930c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4930c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4930c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4930c-119">-Name</span></span>
<span data-ttu-id="4930c-120">Имя набора данных.</span><span class="sxs-lookup"><span data-stu-id="4930c-120">The dataset name.</span></span>

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

### <span data-ttu-id="4930c-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4930c-121">-WorkspaceName</span></span>
<span data-ttu-id="4930c-122">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="4930c-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4930c-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4930c-123">-WorkspaceObject</span></span>
<span data-ttu-id="4930c-124">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="4930c-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4930c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4930c-125">CommonParameters</span></span>
<span data-ttu-id="4930c-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4930c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4930c-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4930c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4930c-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4930c-128">INPUTS</span></span>

### <span data-ttu-id="4930c-129">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4930c-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="4930c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4930c-130">OUTPUTS</span></span>

### <span data-ttu-id="4930c-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span><span class="sxs-lookup"><span data-stu-id="4930c-131">Microsoft.Azure.Commands.Synapse.Models.PSDatasetResource</span></span>

## <span data-ttu-id="4930c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="4930c-132">NOTES</span></span>

## <span data-ttu-id="4930c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4930c-133">RELATED LINKS</span></span>
