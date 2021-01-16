---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSqlDatabase.md
ms.openlocfilehash: e97c10359d00fefa30c783e67c7a3bc64c16a214
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507905"
---
# <span data-ttu-id="29d8a-101">Test-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="29d8a-101">Test-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="29d8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29d8a-102">SYNOPSIS</span></span>
<span data-ttu-id="29d8a-103">Проверяет наличие базы данных Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="29d8a-103">Checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="29d8a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="29d8a-104">SYNTAX</span></span>

### <span data-ttu-id="29d8a-105">TestByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29d8a-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29d8a-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29d8a-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29d8a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29d8a-107">DESCRIPTION</span></span>
<span data-ttu-id="29d8a-108">Cmdlet **Test-AzSynapseSqlDatabase** проверяет наличие базы данных Synapse Analytics SQL данных.</span><span class="sxs-lookup"><span data-stu-id="29d8a-108">The **Test-AzSynapseSqlDatabase** cmdlet checks for the existence of a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="29d8a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="29d8a-109">EXAMPLES</span></span>

### <span data-ttu-id="29d8a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29d8a-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="29d8a-111">Эта команда проверяет наличие указанной SQL данных.</span><span class="sxs-lookup"><span data-stu-id="29d8a-111">This command checks the existence of the specified SQL database.</span></span>

## <span data-ttu-id="29d8a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29d8a-112">PARAMETERS</span></span>

### <span data-ttu-id="29d8a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29d8a-113">-DefaultProfile</span></span>
<span data-ttu-id="29d8a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29d8a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29d8a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="29d8a-115">-Name</span></span>
<span data-ttu-id="29d8a-116">Имя базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="29d8a-116">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="29d8a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29d8a-117">-ResourceGroupName</span></span>
<span data-ttu-id="29d8a-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29d8a-118">Resource group name.</span></span>

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

### <span data-ttu-id="29d8a-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="29d8a-119">-WorkspaceName</span></span>
<span data-ttu-id="29d8a-120">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="29d8a-120">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="29d8a-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="29d8a-121">-WorkspaceObject</span></span>
<span data-ttu-id="29d8a-122">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="29d8a-122">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="29d8a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29d8a-123">CommonParameters</span></span>
<span data-ttu-id="29d8a-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29d8a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29d8a-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29d8a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29d8a-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="29d8a-126">INPUTS</span></span>

### <span data-ttu-id="29d8a-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="29d8a-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="29d8a-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="29d8a-128">OUTPUTS</span></span>

### <span data-ttu-id="29d8a-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="29d8a-129">System.Boolean</span></span>

## <span data-ttu-id="29d8a-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="29d8a-130">NOTES</span></span>

## <span data-ttu-id="29d8a-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29d8a-131">RELATED LINKS</span></span>
