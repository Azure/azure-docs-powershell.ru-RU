---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 12b44d2045574b1d787dd0b2bdb70ec44b616ae5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993236"
---
# <span data-ttu-id="56e3a-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="56e3a-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="56e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="56e3a-103">Возвращает состояние операций с базой данных.</span><span class="sxs-lookup"><span data-stu-id="56e3a-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="56e3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56e3a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56e3a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56e3a-105">DESCRIPTION</span></span>
<span data-ttu-id="56e3a-106">Cmdlet **Get-AzSqlDatabaseActivity** получает состояние операций базы данных в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="56e3a-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="56e3a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56e3a-107">EXAMPLES</span></span>

### <span data-ttu-id="56e3a-108">Пример 1. Просмотр состояния для всех экземпляров SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="56e3a-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="56e3a-109">Эта команда возвращает состояние всех экземпляров базы данных SQL в эластичном пуле под названием "ЭластичнаяPool01".</span><span class="sxs-lookup"><span data-stu-id="56e3a-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="56e3a-110">Пример 2. Просмотр состояния для всех операций SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="56e3a-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="56e3a-111">Эта команда возвращает состояние всех операций SQL базы данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="56e3a-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="56e3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56e3a-112">PARAMETERS</span></span>

### <span data-ttu-id="56e3a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="56e3a-113">-DatabaseName</span></span>
<span data-ttu-id="56e3a-114">Имя базы данных, для которой этот cmdlet получает состояние.</span><span class="sxs-lookup"><span data-stu-id="56e3a-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="56e3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e3a-115">-DefaultProfile</span></span>
<span data-ttu-id="56e3a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56e3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56e3a-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="56e3a-117">-ElasticPoolName</span></span>
<span data-ttu-id="56e3a-118">Имя эластичного пула баз данных, для которого этот cmdlet получает состояние.</span><span class="sxs-lookup"><span data-stu-id="56e3a-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="56e3a-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="56e3a-119">-OperationId</span></span>
<span data-ttu-id="56e3a-120">Определяет код операции, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e3a-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="56e3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="56e3a-122">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="56e3a-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="56e3a-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56e3a-123">-ServerName</span></span>
<span data-ttu-id="56e3a-124">Указывает имя базы данных Microsoft SQL Server в которой размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="56e3a-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="56e3a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56e3a-125">-Confirm</span></span>
<span data-ttu-id="56e3a-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e3a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56e3a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56e3a-127">-WhatIf</span></span>
<span data-ttu-id="56e3a-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e3a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56e3a-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56e3a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56e3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e3a-130">CommonParameters</span></span>
<span data-ttu-id="56e3a-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e3a-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56e3a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e3a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56e3a-133">INPUTS</span></span>

### <span data-ttu-id="56e3a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="56e3a-134">System.String</span></span>

### <span data-ttu-id="56e3a-135">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="56e3a-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="56e3a-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56e3a-136">OUTPUTS</span></span>

### <span data-ttu-id="56e3a-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="56e3a-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="56e3a-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56e3a-138">NOTES</span></span>

## <span data-ttu-id="56e3a-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56e3a-139">RELATED LINKS</span></span>
