---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/Invoke-AzureRmDataMigrationCommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/Invoke-AzureRmDataMigrationCommand.md
ms.openlocfilehash: 882d7eb0b005478850addda2d066c7266e6c2ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566474"
---
# <span data-ttu-id="e55c4-101">Invoke-AzureRmDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="e55c4-101">Invoke-AzureRmDataMigrationCommand</span></span>

## <span data-ttu-id="e55c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e55c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e55c4-103">Создает новую команду для выполнения в существующей задаче DMS.</span><span class="sxs-lookup"><span data-stu-id="e55c4-103">Creates a new command to be executed on an existing DMS task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e55c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e55c4-104">SYNTAX</span></span>

```
Invoke-AzureRmDataMigrationCommand -CommandType <String> -ResourceGroupName <String> -ServiceName <String>
 -ProjectName <String> -TaskName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e55c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e55c4-105">DESCRIPTION</span></span>
<span data-ttu-id="e55c4-106">Командлет New-AzureRmDataMigrationCommand создает новую задачу команды для выполнения в существующей задаче миграции.</span><span class="sxs-lookup"><span data-stu-id="e55c4-106">The New-AzureRmDataMigrationCommand cmdlet creates a new command task to be run on an existing migration task.</span></span>

## <span data-ttu-id="e55c4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e55c4-107">EXAMPLES</span></span>

### <span data-ttu-id="e55c4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e55c4-108">Example 1</span></span>
```
PS C:\> $command = New-AzureRmDmsCommand -CommandType Complete -ResourceGroupName $rg.ResourceGroupName -ServiceName $service.Name -ProjectName -TaskName $taskName -DatabaseName $output.DatabaseName
```

<span data-ttu-id="e55c4-109">В приведенных выше примерах для создания команды для существующей службы, проекта и задачи используется командлет New-AzureRmDmsCommand.</span><span class="sxs-lookup"><span data-stu-id="e55c4-109">The above examples uses the New-AzureRmDmsCommand cmdlet to create a command for an existing service, project, and task</span></span>

## <span data-ttu-id="e55c4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e55c4-110">PARAMETERS</span></span>

### <span data-ttu-id="e55c4-111">-CommandType</span><span class="sxs-lookup"><span data-stu-id="e55c4-111">-CommandType</span></span>
<span data-ttu-id="e55c4-112">Тип команды.</span><span class="sxs-lookup"><span data-stu-id="e55c4-112">Command Type.</span></span>

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

### <span data-ttu-id="e55c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55c4-113">-DefaultProfile</span></span>
<span data-ttu-id="e55c4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e55c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55c4-115">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="e55c4-115">-ProjectName</span></span>
<span data-ttu-id="e55c4-116">Имя проекта.</span><span class="sxs-lookup"><span data-stu-id="e55c4-116">The name of the project.</span></span>

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

### <span data-ttu-id="e55c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="e55c4-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e55c4-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="e55c4-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e55c4-119">-ServiceName</span></span>
<span data-ttu-id="e55c4-120">Имя службы миграции баз данных.</span><span class="sxs-lookup"><span data-stu-id="e55c4-120">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="e55c4-121">-Имя_задания</span><span class="sxs-lookup"><span data-stu-id="e55c4-121">-TaskName</span></span>
<span data-ttu-id="e55c4-122">Имя задачи, на которой выполняется команда.</span><span class="sxs-lookup"><span data-stu-id="e55c4-122">The name of the task the command is run on.</span></span>

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

### <span data-ttu-id="e55c4-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e55c4-123">-Confirm</span></span>
<span data-ttu-id="e55c4-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e55c4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55c4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55c4-125">-WhatIf</span></span>
<span data-ttu-id="e55c4-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e55c4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e55c4-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e55c4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55c4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55c4-128">CommonParameters</span></span>
<span data-ttu-id="e55c4-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e55c4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55c4-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e55c4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55c4-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e55c4-131">INPUTS</span></span>

### <span data-ttu-id="e55c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e55c4-132">System.String</span></span>

## <span data-ttu-id="e55c4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e55c4-133">OUTPUTS</span></span>

### <span data-ttu-id="e55c4-134">Microsoft. Azure. Management. Migration. Models. CommandProperties</span><span class="sxs-lookup"><span data-stu-id="e55c4-134">Microsoft.Azure.Management.DataMigration.Models.CommandProperties</span></span>

## <span data-ttu-id="e55c4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e55c4-135">NOTES</span></span>

## <span data-ttu-id="e55c4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e55c4-136">RELATED LINKS</span></span>
