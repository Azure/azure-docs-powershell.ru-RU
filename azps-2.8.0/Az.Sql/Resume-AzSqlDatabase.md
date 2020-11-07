---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: c5f30388e1e3cb804aa0ef8d45e0afe34a1d2cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905933"
---
# <span data-ttu-id="96058-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96058-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="96058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96058-102">SYNOPSIS</span></span>
<span data-ttu-id="96058-103">Возобновляет базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="96058-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="96058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96058-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96058-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96058-105">DESCRIPTION</span></span>
<span data-ttu-id="96058-106">Командлет **Resume-AzSqlDatabase** возобновляет базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="96058-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="96058-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96058-107">EXAMPLES</span></span>

### <span data-ttu-id="96058-108">Пример 1: возобновление базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="96058-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="96058-109">Эта команда Возобновляет приостановленную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="96058-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="96058-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96058-110">PARAMETERS</span></span>

### <span data-ttu-id="96058-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96058-111">-AsJob</span></span>
<span data-ttu-id="96058-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="96058-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96058-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96058-113">-DatabaseName</span></span>
<span data-ttu-id="96058-114">Указывает имя базы данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="96058-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="96058-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96058-115">-DefaultProfile</span></span>
<span data-ttu-id="96058-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96058-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96058-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96058-117">-ResourceGroupName</span></span>
<span data-ttu-id="96058-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="96058-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="96058-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="96058-119">-ServerName</span></span>
<span data-ttu-id="96058-120">Указывает имя сервера, на котором размещается база данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="96058-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="96058-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96058-121">-Confirm</span></span>
<span data-ttu-id="96058-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96058-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96058-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96058-123">-WhatIf</span></span>
<span data-ttu-id="96058-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96058-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96058-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96058-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96058-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96058-126">CommonParameters</span></span>
<span data-ttu-id="96058-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96058-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96058-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96058-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96058-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96058-129">INPUTS</span></span>

### <span data-ttu-id="96058-130">System. String</span><span class="sxs-lookup"><span data-stu-id="96058-130">System.String</span></span>

## <span data-ttu-id="96058-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96058-131">OUTPUTS</span></span>

### <span data-ttu-id="96058-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="96058-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="96058-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="96058-133">NOTES</span></span>
* <span data-ttu-id="96058-134">Командлет **Resume-AzSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="96058-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="96058-135">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="96058-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="96058-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96058-136">RELATED LINKS</span></span>

[<span data-ttu-id="96058-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96058-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="96058-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96058-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="96058-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96058-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="96058-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96058-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="96058-141">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="96058-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="96058-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="96058-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


