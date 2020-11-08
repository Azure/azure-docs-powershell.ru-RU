---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPool.md
ms.openlocfilehash: d37012ee5188b6dea15968aee8659387e06a87f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246610"
---
# <span data-ttu-id="d5d62-101">Get-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d5d62-101">Get-AzSynapseSqlPool</span></span>

## <span data-ttu-id="d5d62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5d62-102">SYNOPSIS</span></span>
<span data-ttu-id="d5d62-103">Получение пула SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="d5d62-103">Gets a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d5d62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5d62-104">SYNTAX</span></span>

### <span data-ttu-id="d5d62-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5d62-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> [-Name <String>] [-Version <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d62-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d62-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Name <String>] [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5d62-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5d62-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5d62-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d62-108">DESCRIPTION</span></span>
<span data-ttu-id="d5d62-109">Командлет **Get-AzSynapseSqlPool** получает сведения о пуле SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d5d62-109">The **Get-AzSynapseSqlPool** cmdlet gets information about an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d5d62-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5d62-110">EXAMPLES</span></span>

### <span data-ttu-id="d5d62-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5d62-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="d5d62-112">Эта команда получает все пулы SQL в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d5d62-112">This command gets all SQL pools under a workspace.</span></span>

### <span data-ttu-id="d5d62-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d5d62-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="d5d62-114">Эта команда получает пул SQL в разделе Рабочая область ContosoWorkspace с именем ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="d5d62-114">This command gets the SQL pool under workspace ContosoWorkspace with name ContosoSqlPool.</span></span>

### <span data-ttu-id="d5d62-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d5d62-115">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseSqlPool
```

<span data-ttu-id="d5d62-116">Эта команда получает доступ ко всем пулам SQL в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5d62-116">This command gets all the SQL pools under a workspace through pipeline.</span></span>

### <span data-ttu-id="d5d62-117">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d5d62-117">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceId "/subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool"
```

<span data-ttu-id="d5d62-118">Эта команда получает пул SQL с указанным ИДЕНТИФИКАТОРом ресурса.</span><span class="sxs-lookup"><span data-stu-id="d5d62-118">This command gets the SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="d5d62-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5d62-119">PARAMETERS</span></span>

### <span data-ttu-id="d5d62-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5d62-120">-DefaultProfile</span></span>
<span data-ttu-id="d5d62-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5d62-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5d62-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5d62-122">-Name</span></span>
<span data-ttu-id="d5d62-123">Имя пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d5d62-123">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="d5d62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5d62-124">-ResourceGroupName</span></span>
<span data-ttu-id="d5d62-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5d62-125">Resource group name.</span></span>

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

### <span data-ttu-id="d5d62-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5d62-126">-ResourceId</span></span>
<span data-ttu-id="d5d62-127">Идентификатор ресурса пула SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d5d62-127">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="d5d62-128">-Version</span><span class="sxs-lookup"><span data-stu-id="d5d62-128">-Version</span></span>
<span data-ttu-id="d5d62-129">[Эта функция доступна только для некоторых подписок (Предварительная версия). Версия пула Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="d5d62-129">[This feature is in a limited preview, initially accessible only to certain subscriptions.] Version of Synapse SQL pool.</span></span> <span data-ttu-id="d5d62-130">Например, 2 или 3.</span><span class="sxs-lookup"><span data-stu-id="d5d62-130">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="d5d62-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5d62-131">-WorkspaceName</span></span>
<span data-ttu-id="d5d62-132">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d5d62-132">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d5d62-133">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d5d62-133">-WorkspaceObject</span></span>
<span data-ttu-id="d5d62-134">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d5d62-134">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d5d62-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5d62-135">CommonParameters</span></span>
<span data-ttu-id="d5d62-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5d62-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5d62-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5d62-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5d62-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5d62-138">INPUTS</span></span>

### <span data-ttu-id="d5d62-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d5d62-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d5d62-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5d62-140">OUTPUTS</span></span>

### <span data-ttu-id="d5d62-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d5d62-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d5d62-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5d62-142">NOTES</span></span>

## <span data-ttu-id="d5d62-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5d62-143">RELATED LINKS</span></span>
