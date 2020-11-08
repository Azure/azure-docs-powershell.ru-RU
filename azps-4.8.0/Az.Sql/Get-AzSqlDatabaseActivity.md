---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: df4ad0ea9f0e1990fa3c71915b1882baf1d3a762
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243269"
---
# <span data-ttu-id="de28c-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="de28c-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="de28c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de28c-102">SYNOPSIS</span></span>
<span data-ttu-id="de28c-103">Возвращает состояние операций с базой данных.</span><span class="sxs-lookup"><span data-stu-id="de28c-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="de28c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de28c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de28c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de28c-105">DESCRIPTION</span></span>
<span data-ttu-id="de28c-106">Командлет **Get-AzSqlDatabaseActivity** получает состояние операций с базой данных в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="de28c-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="de28c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de28c-107">EXAMPLES</span></span>

### <span data-ttu-id="de28c-108">Пример 1: получение состояния всех экземпляров базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="de28c-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="de28c-109">Эта команда возвращает состояние операции всех экземпляров базы данных SQL в пуле эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="de28c-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="de28c-110">Пример 2: получение состояния всех операций с базой данных SQL</span><span class="sxs-lookup"><span data-stu-id="de28c-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="de28c-111">Эта команда возвращает состояние всех операций базы данных SQL в базе данных.</span><span class="sxs-lookup"><span data-stu-id="de28c-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="de28c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de28c-112">PARAMETERS</span></span>

### <span data-ttu-id="de28c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="de28c-113">-DatabaseName</span></span>
<span data-ttu-id="de28c-114">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="de28c-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="de28c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de28c-115">-DefaultProfile</span></span>
<span data-ttu-id="de28c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de28c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de28c-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="de28c-117">-ElasticPoolName</span></span>
<span data-ttu-id="de28c-118">Указывает имя пула эластичных баз данных, к которому этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="de28c-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="de28c-119">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="de28c-119">-OperationId</span></span>
<span data-ttu-id="de28c-120">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="de28c-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="de28c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de28c-121">-ResourceGroupName</span></span>
<span data-ttu-id="de28c-122">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="de28c-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="de28c-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="de28c-123">-ServerName</span></span>
<span data-ttu-id="de28c-124">Указывает имя сервера Microsoft SQL Server, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="de28c-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="de28c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de28c-125">-Confirm</span></span>
<span data-ttu-id="de28c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de28c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de28c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de28c-127">-WhatIf</span></span>
<span data-ttu-id="de28c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de28c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de28c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de28c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de28c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de28c-130">CommonParameters</span></span>
<span data-ttu-id="de28c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de28c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de28c-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de28c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de28c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de28c-133">INPUTS</span></span>

### <span data-ttu-id="de28c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="de28c-134">System.String</span></span>

### <span data-ttu-id="de28c-135">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="de28c-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="de28c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de28c-136">OUTPUTS</span></span>

### <span data-ttu-id="de28c-137">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="de28c-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="de28c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="de28c-138">NOTES</span></span>

## <span data-ttu-id="de28c-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de28c-139">RELATED LINKS</span></span>
