---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: b89feae28cee95c63184fd5c0e172a4cb005cac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216825"
---
# <span data-ttu-id="efa2f-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="efa2f-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="efa2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efa2f-102">SYNOPSIS</span></span>
<span data-ttu-id="efa2f-103">Создает базу данных Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="efa2f-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="efa2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="efa2f-104">SYNTAX</span></span>

### <span data-ttu-id="efa2f-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efa2f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efa2f-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="efa2f-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efa2f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efa2f-107">DESCRIPTION</span></span>
<span data-ttu-id="efa2f-108">Чтобы получить сведения о базе данных Azure Synapse Analytics, можно получить сведения о SQL **Get-AzSynapseSqlDatabase.**</span><span class="sxs-lookup"><span data-stu-id="efa2f-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="efa2f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="efa2f-109">EXAMPLES</span></span>

### <span data-ttu-id="efa2f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="efa2f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="efa2f-111">Эта команда создает базу данных Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="efa2f-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="efa2f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efa2f-112">PARAMETERS</span></span>

### <span data-ttu-id="efa2f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="efa2f-113">-AsJob</span></span>
<span data-ttu-id="efa2f-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="efa2f-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-115">-Collation</span><span class="sxs-lookup"><span data-stu-id="efa2f-115">-Collation</span></span>
<span data-ttu-id="efa2f-116">Сортировка определяет правила сортировки и сравнения данных, и их невозможно изменить SQL создания пула.</span><span class="sxs-lookup"><span data-stu-id="efa2f-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="efa2f-117">По умолчанию для этого SQL_latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="efa2f-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efa2f-118">-DefaultProfile</span></span>
<span data-ttu-id="efa2f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efa2f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efa2f-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="efa2f-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="efa2f-121">Максимальный размер базы данных в этихбайтах.</span><span class="sxs-lookup"><span data-stu-id="efa2f-121">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="efa2f-122">-Name</span></span>
<span data-ttu-id="efa2f-123">Имя базы данных Synapse SQL.</span><span class="sxs-lookup"><span data-stu-id="efa2f-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="efa2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efa2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="efa2f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="efa2f-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="efa2f-126">-Tag</span></span>
<span data-ttu-id="efa2f-127">Строковый строковый словарь тегов, связанный с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="efa2f-127">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="efa2f-128">-WorkspaceName</span></span>
<span data-ttu-id="efa2f-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="efa2f-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="efa2f-130">-WorkspaceObject</span></span>
<span data-ttu-id="efa2f-131">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="efa2f-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efa2f-132">-Confirm</span></span>
<span data-ttu-id="efa2f-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa2f-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efa2f-134">-WhatIf</span></span>
<span data-ttu-id="efa2f-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efa2f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efa2f-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="efa2f-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efa2f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efa2f-137">CommonParameters</span></span>
<span data-ttu-id="efa2f-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efa2f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efa2f-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efa2f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efa2f-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efa2f-140">INPUTS</span></span>

### <span data-ttu-id="efa2f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="efa2f-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="efa2f-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="efa2f-142">OUTPUTS</span></span>

### <span data-ttu-id="efa2f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="efa2f-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="efa2f-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="efa2f-144">NOTES</span></span>

## <span data-ttu-id="efa2f-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efa2f-145">RELATED LINKS</span></span>
