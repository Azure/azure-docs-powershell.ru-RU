---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: 532246d6e672c4e1770802ab2a0fb01af03455b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015683"
---
# <span data-ttu-id="1cb6a-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1cb6a-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1cb6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cb6a-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb6a-103">Получает пул средств аналитики Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1cb6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cb6a-104">SYNTAX</span></span>

### <span data-ttu-id="1cb6a-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cb6a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cb6a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb6a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cb6a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cb6a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cb6a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb6a-108">DESCRIPTION</span></span>
<span data-ttu-id="1cb6a-109">Чтобы получить сведения о пуле аналитики Azure Synapse Analytics, можно получить SQL **Get-AzSynapseSqlPool.**</span><span class="sxs-lookup"><span data-stu-id="1cb6a-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1cb6a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cb6a-110">EXAMPLES</span></span>

### <span data-ttu-id="1cb6a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cb6a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1cb6a-112">Эта команда возвращает все SQL под рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="1cb6a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1cb6a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1cb6a-114">Эта команда возвращает пул SQL в рабочей области ContosoWorkspace с именем ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="1cb6a-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="1cb6a-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="1cb6a-116">Эта команда получает все пулы SQL под рабочей областью через канал.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="1cb6a-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="1cb6a-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="1cb6a-118">Эта команда возвращает пул SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="1cb6a-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cb6a-119">PARAMETERS</span></span>

### <span data-ttu-id="1cb6a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb6a-120">-DefaultProfile</span></span>
<span data-ttu-id="1cb6a-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cb6a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1cb6a-122">-Name</span></span>
<span data-ttu-id="1cb6a-123">Имя SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-123">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: SqlPoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb6a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cb6a-124">-ResourceGroupName</span></span>
<span data-ttu-id="1cb6a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-125">Resource group name.</span></span>

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

### <span data-ttu-id="1cb6a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cb6a-126">-ResourceId</span></span>
<span data-ttu-id="1cb6a-127">Идентификатор ресурса для SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="1cb6a-128">-Version</span><span class="sxs-lookup"><span data-stu-id="1cb6a-128">-Version</span></span>
<span data-ttu-id="1cb6a-129">[Эта функция доступна в ограниченном доступе только для определенных подписок.] Версия SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="1cb6a-130">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="1cb6a-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1cb6a-131">-WorkspaceName</span></span>
<span data-ttu-id="1cb6a-132">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1cb6a-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1cb6a-133">-WorkspaceObject</span></span>
<span data-ttu-id="1cb6a-134">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1cb6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb6a-135">CommonParameters</span></span>
<span data-ttu-id="1cb6a-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cb6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb6a-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cb6a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb6a-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cb6a-138">INPUTS</span></span>

### <span data-ttu-id="1cb6a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1cb6a-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1cb6a-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cb6a-140">OUTPUTS</span></span>

### <span data-ttu-id="1cb6a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1cb6a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1cb6a-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cb6a-142">NOTES</span></span>

## <span data-ttu-id="1cb6a-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cb6a-143">RELATED LINKS</span></span>
