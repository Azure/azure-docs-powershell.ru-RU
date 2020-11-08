---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsedataflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDataFlow.md
ms.openlocfilehash: 87627738967a5c3174020932e5c9e7b996980ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235701"
---
# <span data-ttu-id="3b618-101">Get-AzSynapseDataFlow</span><span class="sxs-lookup"><span data-stu-id="3b618-101">Get-AzSynapseDataFlow</span></span>

## <span data-ttu-id="3b618-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b618-102">SYNOPSIS</span></span>
<span data-ttu-id="3b618-103">Возвращает сведения о потоках данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b618-103">Gets information about data flows in workspace.</span></span>

## <span data-ttu-id="3b618-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b618-104">SYNTAX</span></span>

### <span data-ttu-id="3b618-105">GetByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b618-105">GetByName (Default)</span></span>
```
Get-AzSynapseDataFlow -WorkspaceName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b618-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="3b618-106">GetByObject</span></span>
```
Get-AzSynapseDataFlow -WorkspaceObject <PSSynapseWorkspace> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b618-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b618-107">DESCRIPTION</span></span>
<span data-ttu-id="3b618-108">Командлет **Get-AzSynapseDataFlow** получает сведения о потоках данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b618-108">The **Get-AzSynapseDataFlow** cmdlet gets information about data flows in workspace.</span></span>
<span data-ttu-id="3b618-109">Если вы задаете имя потока данных, этот командлет получает сведения об этом потоке данных.</span><span class="sxs-lookup"><span data-stu-id="3b618-109">If you specify the name of a data flow, this cmdlet gets information about that data flow.</span></span>
<span data-ttu-id="3b618-110">Если имя не задано, этот командлет получает сведения обо всех потоках данных в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b618-110">If you do not specify a name, this cmdlet gets information about all the data flows in the workspace.</span></span>

## <span data-ttu-id="3b618-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b618-111">EXAMPLES</span></span>

### <span data-ttu-id="3b618-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b618-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="3b618-113">Эта команда получает сведения обо всех потоках данных в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3b618-113">This command gets information about all data flows in the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="3b618-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3b618-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseDataFlow -WorkspaceName ContosoWorkspace -Name ContosoDataFlow
```

<span data-ttu-id="3b618-115">Эта команда получает сведения о потоке данных с именем ContosoDataFlow в рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="3b618-115">This command gets information about the data flow named ContosoDataFlow in the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="3b618-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b618-116">PARAMETERS</span></span>

### <span data-ttu-id="3b618-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b618-117">-DefaultProfile</span></span>
<span data-ttu-id="3b618-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b618-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b618-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b618-119">-Name</span></span>
<span data-ttu-id="3b618-120">Имя потока данных.</span><span class="sxs-lookup"><span data-stu-id="3b618-120">The data flow name.</span></span>

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

### <span data-ttu-id="3b618-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3b618-121">-WorkspaceName</span></span>
<span data-ttu-id="3b618-122">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="3b618-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3b618-123">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3b618-123">-WorkspaceObject</span></span>
<span data-ttu-id="3b618-124">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3b618-124">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3b618-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b618-125">CommonParameters</span></span>
<span data-ttu-id="3b618-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b618-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b618-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b618-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b618-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b618-128">INPUTS</span></span>

### <span data-ttu-id="3b618-129">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="3b618-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3b618-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b618-130">OUTPUTS</span></span>

### <span data-ttu-id="3b618-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span><span class="sxs-lookup"><span data-stu-id="3b618-131">Microsoft.Azure.Commands.Synapse.Models.PSDataFlowResource</span></span>

## <span data-ttu-id="3b618-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b618-132">NOTES</span></span>

## <span data-ttu-id="3b618-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b618-133">RELATED LINKS</span></span>
