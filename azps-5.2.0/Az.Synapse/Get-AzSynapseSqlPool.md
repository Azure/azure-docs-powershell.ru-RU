---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410431"
---
# <span data-ttu-id="99cc1-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="99cc1-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="99cc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99cc1-102">SYNOPSIS</span></span>
<span data-ttu-id="99cc1-103">Получает пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="99cc1-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="99cc1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="99cc1-104">SYNTAX</span></span>

### <span data-ttu-id="99cc1-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99cc1-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99cc1-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99cc1-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99cc1-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="99cc1-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="99cc1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99cc1-108">DESCRIPTION</span></span>
<span data-ttu-id="99cc1-109">Чтобы получить сведения о пуле аналитики Azure Synapse Analytics, можно получить SQL **Get-AzSynapseSqlPool.**</span><span class="sxs-lookup"><span data-stu-id="99cc1-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="99cc1-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="99cc1-110">EXAMPLES</span></span>

### <span data-ttu-id="99cc1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99cc1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="99cc1-112">Эта команда возвращает все SQL под рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="99cc1-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="99cc1-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="99cc1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="99cc1-114">Эта команда возвращает пул SQL в рабочей области ContosoWorkspace с именем ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="99cc1-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="99cc1-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="99cc1-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="99cc1-116">Эта команда получает все пулы SQL под рабочей областью через канал.</span><span class="sxs-lookup"><span data-stu-id="99cc1-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="99cc1-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="99cc1-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="99cc1-118">Эта команда возвращает пул SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="99cc1-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="99cc1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99cc1-119">PARAMETERS</span></span>

### <span data-ttu-id="99cc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99cc1-120">-DefaultProfile</span></span>
<span data-ttu-id="99cc1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99cc1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99cc1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="99cc1-122">-Name</span></span>
<span data-ttu-id="99cc1-123">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="99cc1-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99cc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="99cc1-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99cc1-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cc1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99cc1-126">-ResourceId</span></span>
<span data-ttu-id="99cc1-127">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="99cc1-127">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cc1-128">-Version</span><span class="sxs-lookup"><span data-stu-id="99cc1-128">-Version</span></span>
<span data-ttu-id="99cc1-129">[Эта функция доступна в ограниченном доступе только для определенных подписок.] Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="99cc1-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="99cc1-130">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="99cc1-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="99cc1-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="99cc1-131">-WorkspaceName</span></span>
<span data-ttu-id="99cc1-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="99cc1-132">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99cc1-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="99cc1-133">-WorkspaceObject</span></span>
<span data-ttu-id="99cc1-134">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="99cc1-134">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99cc1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99cc1-135">CommonParameters</span></span>
<span data-ttu-id="99cc1-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99cc1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99cc1-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99cc1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99cc1-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99cc1-138">INPUTS</span></span>

### <span data-ttu-id="99cc1-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="99cc1-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="99cc1-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="99cc1-140">OUTPUTS</span></span>

### <span data-ttu-id="99cc1-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="99cc1-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="99cc1-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="99cc1-142">NOTES</span></span>

## <span data-ttu-id="99cc1-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99cc1-143">RELATED LINKS</span></span>
