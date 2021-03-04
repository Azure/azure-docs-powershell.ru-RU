---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/test-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlPool.md
ms.openlocfilehash: d932a875957f1649976966a9f2e115e93dfea351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011235"
---
# <span data-ttu-id="1ebd2-101">Test-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1ebd2-101">Test-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1ebd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ebd2-102">SYNOPSIS</span></span>
<span data-ttu-id="1ebd2-103">Проверяет наличие пула средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-103">Checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1ebd2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ebd2-104">SYNTAX</span></span>

### <span data-ttu-id="1ebd2-105">TestByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ebd2-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ebd2-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ebd2-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ebd2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ebd2-107">DESCRIPTION</span></span>
<span data-ttu-id="1ebd2-108">Cmdlet **Test-AzSynapseSqlPool** проверяет наличие пула аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-108">The **Test-AzSynapseSqlPool** cmdlet checks for the existence of a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1ebd2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ebd2-109">EXAMPLES</span></span>

### <span data-ttu-id="1ebd2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1ebd2-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1ebd2-111">Эта команда проверяет наличие указанного SQL пула.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-111">This command checks the existence of the specified SQL pool.</span></span>

## <span data-ttu-id="1ebd2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ebd2-112">PARAMETERS</span></span>

### <span data-ttu-id="1ebd2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ebd2-113">-DefaultProfile</span></span>
<span data-ttu-id="1ebd2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ebd2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1ebd2-115">-Name</span></span>
<span data-ttu-id="1ebd2-116">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-116">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebd2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ebd2-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ebd2-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebd2-119">-Version</span><span class="sxs-lookup"><span data-stu-id="1ebd2-119">-Version</span></span>
<span data-ttu-id="1ebd2-120">Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-120">Version of Synapse SQL pool.</span></span> <span data-ttu-id="1ebd2-121">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-121">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebd2-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1ebd2-122">-WorkspaceName</span></span>
<span data-ttu-id="1ebd2-123">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-123">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ebd2-124">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1ebd2-124">-WorkspaceObject</span></span>
<span data-ttu-id="1ebd2-125">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-125">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ebd2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ebd2-126">CommonParameters</span></span>
<span data-ttu-id="1ebd2-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ebd2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ebd2-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ebd2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ebd2-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ebd2-129">INPUTS</span></span>

### <span data-ttu-id="1ebd2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1ebd2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1ebd2-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ebd2-131">OUTPUTS</span></span>

### <span data-ttu-id="1ebd2-132">System.Object</span><span class="sxs-lookup"><span data-stu-id="1ebd2-132">System.Object</span></span>
## <span data-ttu-id="1ebd2-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ebd2-133">NOTES</span></span>

## <span data-ttu-id="1ebd2-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ebd2-134">RELATED LINKS</span></span>
