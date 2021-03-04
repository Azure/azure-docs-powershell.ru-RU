---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/Invoke-AzDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Invoke-AzDataMigrationCommand.md
ms.openlocfilehash: e99e2e6a8c0b2c8a0fc0b2d2143d2b4301520ab0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952648"
---
# <span data-ttu-id="38506-101">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="38506-101">Invoke-AzDataMigrationCommand</span></span>

## <span data-ttu-id="38506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38506-102">SYNOPSIS</span></span>
<span data-ttu-id="38506-103">Создает новую команду, которая будет выполняться в существующей задаче DMS.</span><span class="sxs-lookup"><span data-stu-id="38506-103">Creates a new command to be executed on an existing DMS task.</span></span>

## <span data-ttu-id="38506-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="38506-104">SYNTAX</span></span>

```
Invoke-AzDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String> [-ObjectName <ObjectName>]
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] 
 [<CommonParameters>]
```

## <span data-ttu-id="38506-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38506-105">DESCRIPTION</span></span>
<span data-ttu-id="38506-106">Командлет Invoke-AzDataMigrationCommand создает новую задачу, которая будет запускаться для существующей задачи миграции.</span><span class="sxs-lookup"><span data-stu-id="38506-106">The Invoke-AzDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="38506-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="38506-107">EXAMPLES</span></span>

### <span data-ttu-id="38506-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="38506-108">Example 1</span></span>
```
PS C:\> $command = Invoke-AzDataMigrationCommand -CommandType CompleteSqlDBSync -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="38506-109">В примерах выше Invoke-AzDataMigrationCommand командлет для создания команды для существующей службы, проекта и задачи.</span><span class="sxs-lookup"><span data-stu-id="38506-109">The above examples uses the Invoke-AzDataMigrationCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="38506-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38506-110">PARAMETERS</span></span>

### <span data-ttu-id="38506-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="38506-111">-CommandType</span></span>
<span data-ttu-id="38506-112">Тип команды.</span><span class="sxs-lookup"><span data-stu-id="38506-112">Command Type.</span></span>

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

### <span data-ttu-id="38506-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38506-113">-DefaultProfile</span></span>
<span data-ttu-id="38506-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38506-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38506-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="38506-115">-ProjectName</span></span>
<span data-ttu-id="38506-116">Название проекта.</span><span class="sxs-lookup"><span data-stu-id="38506-116">The name of the project.</span></span>

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

### <span data-ttu-id="38506-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38506-117">-ResourceGroupName</span></span>
<span data-ttu-id="38506-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38506-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="38506-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="38506-119">-ServiceName</span></span>
<span data-ttu-id="38506-120">Имя службы миграции базы данных.</span><span class="sxs-lookup"><span data-stu-id="38506-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="38506-121">-TaskName</span><span class="sxs-lookup"><span data-stu-id="38506-121">-TaskName</span></span>
<span data-ttu-id="38506-122">Имя задачи, для которого будет выполниться команда.</span><span class="sxs-lookup"><span data-stu-id="38506-122">The name of the task the command is run on.</span></span>

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
### <span data-ttu-id="38506-123">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="38506-123">-ObjectName</span></span>
<span data-ttu-id="38506-124">Имя объекта базы данных, с которого будет запускаться команда.</span><span class="sxs-lookup"><span data-stu-id="38506-124">The name of the database object the command will run against.</span></span>

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

### <span data-ttu-id="38506-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38506-125">-Confirm</span></span>
<span data-ttu-id="38506-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38506-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38506-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38506-127">-WhatIf</span></span>
<span data-ttu-id="38506-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38506-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38506-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="38506-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38506-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38506-130">CommonParameters</span></span>
<span data-ttu-id="38506-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38506-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38506-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38506-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38506-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38506-133">INPUTS</span></span>

### <span data-ttu-id="38506-134">System.String</span><span class="sxs-lookup"><span data-stu-id="38506-134">System.String</span></span>

## <span data-ttu-id="38506-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="38506-135">OUTPUTS</span></span>

### <span data-ttu-id="38506-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span><span class="sxs-lookup"><span data-stu-id="38506-136">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="38506-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="38506-137">NOTES</span></span>

## <span data-ttu-id="38506-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38506-138">RELATED LINKS</span></span>
