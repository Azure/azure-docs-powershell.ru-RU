---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseActivity.md
ms.openlocfilehash: f6beaa0651e406d94e1718bb1b1fdea6ef1c3507
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212369"
---
# <span data-ttu-id="952c0-101">Stop-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="952c0-101">Stop-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="952c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="952c0-102">SYNOPSIS</span></span>
<span data-ttu-id="952c0-103">Отменяет операцию асинхронного обновления базы данных.</span><span class="sxs-lookup"><span data-stu-id="952c0-103">Cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="952c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="952c0-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="952c0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="952c0-105">DESCRIPTION</span></span>
<span data-ttu-id="952c0-106">Cmdlet **Stop-AzSqlDatabaseActivity** отменяет операцию асинхронного обновления базы данных.</span><span class="sxs-lookup"><span data-stu-id="952c0-106">The **Stop-AzSqlDatabaseActivity** cmdlet cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="952c0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="952c0-107">EXAMPLES</span></span>

### <span data-ttu-id="952c0-108">Пример 1. Отмена асинхронного обновления базы данных</span><span class="sxs-lookup"><span data-stu-id="952c0-108">Example 1: Cancel the asynchronous updates operation on the database</span></span>
```
PS C:\>Stop-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : Database01
State           : CANCELLED
Operation       : UpdateLogicalDatabase
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
Properties      : Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel+DatabaseState
```

<span data-ttu-id="952c0-109">Эта команда отменяет операцию асинхронного обновления базы данных.</span><span class="sxs-lookup"><span data-stu-id="952c0-109">This command cancels the asynchronous updates operation on the database.</span></span>

## <span data-ttu-id="952c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="952c0-110">PARAMETERS</span></span>

### <span data-ttu-id="952c0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="952c0-111">-DatabaseName</span></span>
<span data-ttu-id="952c0-112">Указывает имя базы данных, для которой этот cmdlet получает состояние.</span><span class="sxs-lookup"><span data-stu-id="952c0-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="952c0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952c0-113">-DefaultProfile</span></span>
<span data-ttu-id="952c0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="952c0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="952c0-115">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="952c0-115">-ElasticPoolName</span></span>
<span data-ttu-id="952c0-116">Имя эластичного пула Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="952c0-116">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="952c0-117">-OperationId</span><span class="sxs-lookup"><span data-stu-id="952c0-117">-OperationId</span></span>
<span data-ttu-id="952c0-118">Определяет код операции, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="952c0-118">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="952c0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="952c0-119">-ResourceGroupName</span></span>
<span data-ttu-id="952c0-120">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="952c0-120">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="952c0-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="952c0-121">-ServerName</span></span>
<span data-ttu-id="952c0-122">Указывает имя базы данных Microsoft SQL Server в которой размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="952c0-122">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="952c0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="952c0-123">-Confirm</span></span>
<span data-ttu-id="952c0-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="952c0-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952c0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952c0-125">-WhatIf</span></span>
<span data-ttu-id="952c0-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="952c0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952c0-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="952c0-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952c0-128">CommonParameters</span></span>
<span data-ttu-id="952c0-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952c0-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="952c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952c0-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="952c0-131">INPUTS</span></span>

### <span data-ttu-id="952c0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="952c0-132">System.String</span></span>

### <span data-ttu-id="952c0-133">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="952c0-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="952c0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="952c0-134">OUTPUTS</span></span>

### <span data-ttu-id="952c0-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="952c0-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="952c0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="952c0-136">NOTES</span></span>

## <span data-ttu-id="952c0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="952c0-137">RELATED LINKS</span></span>
