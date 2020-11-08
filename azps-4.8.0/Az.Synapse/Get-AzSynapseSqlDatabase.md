---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlDatabase.md
ms.openlocfilehash: c203e9c80978f50bd7879627b733de2ec0c6cf7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235194"
---
# <span data-ttu-id="44058-101">Get-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="44058-101">Get-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="44058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44058-102">SYNOPSIS</span></span>
<span data-ttu-id="44058-103">Возвращает базу данных SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="44058-103">Gets a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="44058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44058-104">SYNTAX</span></span>

### <span data-ttu-id="44058-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44058-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44058-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44058-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlDatabase [-Name <String>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44058-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44058-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlDatabase -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44058-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44058-108">DESCRIPTION</span></span>
<span data-ttu-id="44058-109">[Эта функция доступна только для некоторых подписок (Предварительная версия). Командлет **Get-AzSynapseSqlDatabase** получает сведения о базе данных Azure SYNAPSE Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="44058-109">[This feature is in a limited preview, initially accessible only to certain subscriptions.] The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="44058-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44058-110">EXAMPLES</span></span>

### <span data-ttu-id="44058-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44058-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="44058-112">Эта команда получает все базы данных SQL в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="44058-112">This command gets all SQL databases under a workspace.</span></span>

### <span data-ttu-id="44058-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="44058-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="44058-114">Эта команда получает базу данных SQL в разделе Рабочая область ContosoWorkspace с именем ContosoSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="44058-114">This command gets the SQL database under workspace ContosoWorkspace with name ContosoSqlDatabase.</span></span>

### <span data-ttu-id="44058-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="44058-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlDatabase
```

<span data-ttu-id="44058-116">Эта команда получает все базы данных SQL в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="44058-116">This command gets all the SQL databases under a workspace through pipeline.</span></span>

### <span data-ttu-id="44058-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="44058-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlDatabase -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase"
```

<span data-ttu-id="44058-118">Эта команда получает базу данных SQL с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="44058-118">This command gets the SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="44058-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44058-119">PARAMETERS</span></span>

### <span data-ttu-id="44058-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44058-120">-DefaultProfile</span></span>
<span data-ttu-id="44058-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44058-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44058-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44058-122">-Name</span></span>
<span data-ttu-id="44058-123">Имя базы данных SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="44058-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="44058-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44058-124">-ResourceGroupName</span></span>
<span data-ttu-id="44058-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44058-125">Resource group name.</span></span>

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

### <span data-ttu-id="44058-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44058-126">-ResourceId</span></span>
<span data-ttu-id="44058-127">Идентификатор ресурса Synapse базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="44058-127">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="44058-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44058-128">-WorkspaceName</span></span>
<span data-ttu-id="44058-129">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="44058-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="44058-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="44058-130">-WorkspaceObject</span></span>
<span data-ttu-id="44058-131">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="44058-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="44058-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44058-132">CommonParameters</span></span>
<span data-ttu-id="44058-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44058-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44058-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44058-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44058-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44058-135">INPUTS</span></span>

### <span data-ttu-id="44058-136">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="44058-136">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="44058-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44058-137">OUTPUTS</span></span>

### <span data-ttu-id="44058-138">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="44058-138">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="44058-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="44058-139">NOTES</span></span>

## <span data-ttu-id="44058-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44058-140">RELATED LINKS</span></span>
