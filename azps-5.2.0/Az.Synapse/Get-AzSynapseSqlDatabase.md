---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410436"
---
# <span data-ttu-id="8f69d-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f69d-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="8f69d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f69d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f69d-103">Получает базу данных Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="8f69d-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="8f69d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f69d-104">SYNTAX</span></span>

### <span data-ttu-id="8f69d-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f69d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f69d-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f69d-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8f69d-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f69d-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f69d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f69d-108">DESCRIPTION</span></span>
<span data-ttu-id="8f69d-109">[Эта функция доступна в ограниченном режиме предварительного просмотра и изначально доступна только для определенных подписок.] Чтобы получить сведения о базе данных Azure Synapse Analytics, можно получить сведения о SQL **Get-AzSynapseSqlDatabase.**</span><span class="sxs-lookup"><span data-stu-id="8f69d-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="8f69d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f69d-110">EXAMPLES</span></span>

### <span data-ttu-id="8f69d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f69d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8f69d-112">Эта команда возвращает все SQL под рабочей областью.</span><span class="sxs-lookup"><span data-stu-id="8f69d-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="8f69d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8f69d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="8f69d-114">Эта команда возвращает базу SQL рабочей области ContosoWorkspace с именем ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="8f69d-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="8f69d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8f69d-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="8f69d-116">Эта команда передает все базы SQL под рабочей областью через канал.</span><span class="sxs-lookup"><span data-stu-id="8f69d-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="8f69d-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="8f69d-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="8f69d-118">Эта команда возвращает SQL с указанным ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="8f69d-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="8f69d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f69d-119">PARAMETERS</span></span>

### <span data-ttu-id="8f69d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f69d-120">-DefaultProfile</span></span>
<span data-ttu-id="8f69d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f69d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f69d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8f69d-122">-Name</span></span>
<span data-ttu-id="8f69d-123">Имя базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="8f69d-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="8f69d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f69d-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f69d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f69d-125">Resource group name.</span></span>

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

### <span data-ttu-id="8f69d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f69d-126">-ResourceId</span></span>
<span data-ttu-id="8f69d-127">Идентификатор ресурса базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="8f69d-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="8f69d-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8f69d-128">-WorkspaceName</span></span>
<span data-ttu-id="8f69d-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8f69d-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8f69d-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8f69d-130">-WorkspaceObject</span></span>
<span data-ttu-id="8f69d-131">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="8f69d-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8f69d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f69d-132">CommonParameters</span></span>
<span data-ttu-id="8f69d-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f69d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f69d-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8f69d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f69d-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f69d-135">INPUTS</span></span>

### <span data-ttu-id="8f69d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8f69d-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8f69d-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f69d-137">OUTPUTS</span></span>

### <span data-ttu-id="8f69d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f69d-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="8f69d-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f69d-139">NOTES</span></span>

## <span data-ttu-id="8f69d-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f69d-140">RELATED LINKS</span></span>