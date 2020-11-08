---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlDatabase.md
ms.openlocfilehash: 16f2df5900fcc522f0ff3afb7b9f5b14ea5f0b64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078562"
---
# <span data-ttu-id="96b1b-101">New-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96b1b-101">New-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="96b1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="96b1b-103">Создает базу данных SQL Analytics Synapse.</span><span class="sxs-lookup"><span data-stu-id="96b1b-103">Creates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="96b1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96b1b-104">SYNTAX</span></span>

### <span data-ttu-id="96b1b-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96b1b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96b1b-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="96b1b-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlDatabase -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-Collation <String>] [-MaxSizeInBytes <Int64>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96b1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="96b1b-108">Командлет **Get-AzSynapseSqlDatabase** получает сведения о базе данных Azure SYNAPSE Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="96b1b-108">The **Get-AzSynapseSqlDatabase** cmdlet gets information about an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="96b1b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96b1b-109">EXAMPLES</span></span>

### <span data-ttu-id="96b1b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96b1b-110">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase 
```

<span data-ttu-id="96b1b-111">Эта команда создает базу данных SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="96b1b-111">This command creates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="96b1b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96b1b-112">PARAMETERS</span></span>

### <span data-ttu-id="96b1b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96b1b-113">-AsJob</span></span>
<span data-ttu-id="96b1b-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="96b1b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96b1b-115">-Параметры сортировки</span><span class="sxs-lookup"><span data-stu-id="96b1b-115">-Collation</span></span>
<span data-ttu-id="96b1b-116">Параметры сортировки определяют правила, которые сортируют и сравнивают данные, и их нельзя изменить после создания пула SQL.</span><span class="sxs-lookup"><span data-stu-id="96b1b-116">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="96b1b-117">Параметры сортировки по умолчанию SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="96b1b-117">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

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

### <span data-ttu-id="96b1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96b1b-118">-DefaultProfile</span></span>
<span data-ttu-id="96b1b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96b1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96b1b-120">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="96b1b-120">-MaxSizeInBytes</span></span>
<span data-ttu-id="96b1b-121">Указывает максимальный размер базы данных в байтах.</span><span class="sxs-lookup"><span data-stu-id="96b1b-121">Specifies the maximum size of the database in bytes.</span></span>

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

### <span data-ttu-id="96b1b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96b1b-122">-Name</span></span>
<span data-ttu-id="96b1b-123">Имя базы данных SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="96b1b-123">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="96b1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96b1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="96b1b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96b1b-125">Resource group name.</span></span>

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

### <span data-ttu-id="96b1b-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="96b1b-126">-Tag</span></span>
<span data-ttu-id="96b1b-127">Строковый словарь тегов, связанных с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="96b1b-127">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="96b1b-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="96b1b-128">-WorkspaceName</span></span>
<span data-ttu-id="96b1b-129">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="96b1b-129">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="96b1b-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="96b1b-130">-WorkspaceObject</span></span>
<span data-ttu-id="96b1b-131">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="96b1b-131">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="96b1b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96b1b-132">-Confirm</span></span>
<span data-ttu-id="96b1b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96b1b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96b1b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96b1b-134">-WhatIf</span></span>
<span data-ttu-id="96b1b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96b1b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96b1b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96b1b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96b1b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96b1b-137">CommonParameters</span></span>
<span data-ttu-id="96b1b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96b1b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96b1b-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96b1b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96b1b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96b1b-140">INPUTS</span></span>

### <span data-ttu-id="96b1b-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="96b1b-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="96b1b-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96b1b-142">OUTPUTS</span></span>

### <span data-ttu-id="96b1b-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96b1b-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="96b1b-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="96b1b-144">NOTES</span></span>

## <span data-ttu-id="96b1b-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96b1b-145">RELATED LINKS</span></span>
