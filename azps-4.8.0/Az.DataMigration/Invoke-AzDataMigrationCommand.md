---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: ebfc974fdf268225c6c572756f7c5567b691ec04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236764"
---
# <span data-ttu-id="c9b8f-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="c9b8f-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="c9b8f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b8f-103">Создает новую команду для выполнения в существующей задаче DMS.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="c9b8f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9b8f-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="c9b8f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b8f-106">Командлет Invoke-AzDataMigrationCommand создает новую задачу команды для выполнения в существующей задаче миграции.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="c9b8f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b8f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9b8f-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="c9b8f-109">В приведенных выше примерах для создания команды для существующей службы, проекта и задачи используется командлет Invoke-AzDataMigrationCommand.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="c9b8f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b8f-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="c9b8f-111">-CommandType</span></span>
<span data-ttu-id="c9b8f-112">Тип команды.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-112">Command Type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.CommandTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: CompleteSqlDBSync, CancelMongoDB, RestartMongoDB, FinishMongoDB, CompleteSqlMiSync

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9b8f-113">-DefaultProfile</span></span>
<span data-ttu-id="c9b8f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b8f-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="c9b8f-115">-ProjectName</span></span>
<span data-ttu-id="c9b8f-116">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-116">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b8f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b8f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9b8f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b8f-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c9b8f-119">-ServiceName</span></span>
<span data-ttu-id="c9b8f-120">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-120">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9b8f-121">-Имя_задания</span><span class="sxs-lookup"><span data-stu-id="c9b8f-121">-TaskName</span></span>
<span data-ttu-id="c9b8f-122">Имя задачи, на которой выполняется команда.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="c9b8f-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="c9b8f-123">-ObjectName</span></span>
<span data-ttu-id="c9b8f-124">Имя объекта базы данных, для которого будет выполняться команда.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="c9b8f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c9b8f-125">-Confirm</span></span>
<span data-ttu-id="c9b8f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9b8f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b8f-127">-WhatIf</span></span>
<span data-ttu-id="c9b8f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b8f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9b8f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b8f-130">CommonParameters</span></span>
<span data-ttu-id="c9b8f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9b8f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b8f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9b8f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b8f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9b8f-133">INPUTS</span></span>

### <span data-ttu-id="c9b8f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c9b8f-134">System.String</span></span>

## <span data-ttu-id="c9b8f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9b8f-135">OUTPUTS</span></span>

### <span data-ttu-id="c9b8f-136">Microsoft. Azure. Management. Migration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="c9b8f-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="c9b8f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9b8f-137">NOTES</span></span>

## <span data-ttu-id="c9b8f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9b8f-138">RELATED LINKS</span></span>
