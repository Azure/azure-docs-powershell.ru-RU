---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065346"
---
# <span data-ttu-id="94525-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94525-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="94525-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94525-102">SYNOPSIS</span></span>
<span data-ttu-id="94525-103">Возобновляет базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="94525-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="94525-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94525-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94525-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94525-105">DESCRIPTION</span></span>
<span data-ttu-id="94525-106">Командлет **Resume-AzSqlDatabase** возобновляет базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="94525-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="94525-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94525-107">EXAMPLES</span></span>

### <span data-ttu-id="94525-108">Пример 1: возобновление базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="94525-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="94525-109">Эта команда Возобновляет приостановленную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="94525-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="94525-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94525-110">PARAMETERS</span></span>

### <span data-ttu-id="94525-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94525-111">-AsJob</span></span>
<span data-ttu-id="94525-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="94525-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94525-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94525-113">-DatabaseName</span></span>
<span data-ttu-id="94525-114">Указывает имя базы данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="94525-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="94525-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94525-115">-DefaultProfile</span></span>
<span data-ttu-id="94525-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94525-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94525-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94525-117">-ResourceGroupName</span></span>
<span data-ttu-id="94525-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="94525-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="94525-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="94525-119">-ServerName</span></span>
<span data-ttu-id="94525-120">Указывает имя сервера, на котором размещается база данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="94525-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="94525-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94525-121">-Confirm</span></span>
<span data-ttu-id="94525-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94525-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94525-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94525-123">-WhatIf</span></span>
<span data-ttu-id="94525-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94525-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94525-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94525-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94525-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94525-126">CommonParameters</span></span>
<span data-ttu-id="94525-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94525-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94525-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94525-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94525-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94525-129">INPUTS</span></span>

### <span data-ttu-id="94525-130">System. String</span><span class="sxs-lookup"><span data-stu-id="94525-130">System.String</span></span>

## <span data-ttu-id="94525-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94525-131">OUTPUTS</span></span>

### <span data-ttu-id="94525-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="94525-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="94525-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="94525-133">NOTES</span></span>
* <span data-ttu-id="94525-134">Командлет **Resume-AzSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="94525-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="94525-135">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="94525-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="94525-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94525-136">RELATED LINKS</span></span>

[<span data-ttu-id="94525-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94525-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="94525-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94525-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="94525-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94525-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="94525-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94525-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="94525-141">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="94525-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="94525-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="94525-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


