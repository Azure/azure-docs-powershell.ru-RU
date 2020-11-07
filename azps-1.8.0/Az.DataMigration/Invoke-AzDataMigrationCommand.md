---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: f00c1499e7f7e8a5a6d6b14bcbd8289b35ae2ced
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900702"
---
# <span data-ttu-id="5ba0c-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="5ba0c-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="5ba0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba0c-103">Создает новую команду для выполнения в существующей задаче DMS.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="5ba0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ba0c-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="5ba0c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ba0c-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba0c-106">Командлет Invoke-AzDataMigrationCommand создает новую задачу команды для выполнения в существующей задаче миграции.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="5ba0c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ba0c-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba0c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5ba0c-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="5ba0c-109">В приведенных выше примерах для создания команды для существующей службы, проекта и задачи используется командлет Invoke-AzDataMigrationCommand.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="5ba0c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ba0c-110">PARAMETERS</span></span>

### <span data-ttu-id="5ba0c-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="5ba0c-111">-CommandType</span></span>
<span data-ttu-id="5ba0c-112">Тип команды.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-112">Command Type.</span></span>

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

### <span data-ttu-id="5ba0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba0c-113">-DefaultProfile</span></span>
<span data-ttu-id="5ba0c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ba0c-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="5ba0c-115">-ProjectName</span></span>
<span data-ttu-id="5ba0c-116">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-116">The name of the project.</span></span>

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

### <span data-ttu-id="5ba0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ba0c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="5ba0c-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5ba0c-119">-ServiceName</span></span>
<span data-ttu-id="5ba0c-120">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="5ba0c-121">-Имя_задания</span><span class="sxs-lookup"><span data-stu-id="5ba0c-121">-TaskName</span></span>
<span data-ttu-id="5ba0c-122">Имя задачи, на которой выполняется команда.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="5ba0c-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="5ba0c-123">-ObjectName</span></span>
<span data-ttu-id="5ba0c-124">Имя объекта базы данных, для которого будет выполняться команда.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="5ba0c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ba0c-125">-Confirm</span></span>
<span data-ttu-id="5ba0c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba0c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba0c-127">-WhatIf</span></span>
<span data-ttu-id="5ba0c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba0c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ba0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba0c-130">CommonParameters</span></span>
<span data-ttu-id="5ba0c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ba0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba0c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba0c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba0c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ba0c-133">INPUTS</span></span>

### <span data-ttu-id="5ba0c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba0c-134">System.String</span></span>

## <span data-ttu-id="5ba0c-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ba0c-135">OUTPUTS</span></span>

### <span data-ttu-id="5ba0c-136">Microsoft. Azure. Management. Migration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="5ba0c-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="5ba0c-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ba0c-137">NOTES</span></span>

## <span data-ttu-id="5ba0c-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ba0c-138">RELATED LINKS</span></span>
