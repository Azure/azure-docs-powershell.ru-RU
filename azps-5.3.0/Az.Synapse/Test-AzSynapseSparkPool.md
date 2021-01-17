---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423967"
---
# <span data-ttu-id="696dc-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="696dc-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="696dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696dc-102">SYNOPSIS</span></span>
<span data-ttu-id="696dc-103">Проверяет наличие пула спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="696dc-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="696dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="696dc-104">SYNTAX</span></span>

### <span data-ttu-id="696dc-105">TestByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="696dc-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="696dc-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="696dc-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="696dc-107">DESCRIPTION</span></span>
<span data-ttu-id="696dc-108">**Спарклет Test-AzSynapseSparkPool** проверяет наличие пула спарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="696dc-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="696dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="696dc-109">EXAMPLES</span></span>

### <span data-ttu-id="696dc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="696dc-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="696dc-111">Эта команда проверяет наличие указанного пула спарков.</span><span class="sxs-lookup"><span data-stu-id="696dc-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="696dc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696dc-112">PARAMETERS</span></span>

### <span data-ttu-id="696dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696dc-113">-DefaultProfile</span></span>
<span data-ttu-id="696dc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="696dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="696dc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="696dc-115">-Name</span></span>
<span data-ttu-id="696dc-116">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="696dc-116">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="696dc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696dc-117">-ResourceGroupName</span></span>
<span data-ttu-id="696dc-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="696dc-118">Resource group name.</span></span>

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

### <span data-ttu-id="696dc-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="696dc-119">-WorkspaceName</span></span>
<span data-ttu-id="696dc-120">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="696dc-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="696dc-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="696dc-121">-WorkspaceObject</span></span>
<span data-ttu-id="696dc-122">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="696dc-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="696dc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696dc-123">CommonParameters</span></span>
<span data-ttu-id="696dc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696dc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696dc-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="696dc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696dc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="696dc-126">INPUTS</span></span>

### <span data-ttu-id="696dc-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="696dc-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="696dc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="696dc-128">OUTPUTS</span></span>

### <span data-ttu-id="696dc-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="696dc-129">System.Object</span></span>
## <span data-ttu-id="696dc-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="696dc-130">NOTES</span></span>

## <span data-ttu-id="696dc-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="696dc-131">RELATED LINKS</span></span>
