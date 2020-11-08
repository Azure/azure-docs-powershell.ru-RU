---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077552"
---
# <span data-ttu-id="eee13-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eee13-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="eee13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eee13-102">SYNOPSIS</span></span>
<span data-ttu-id="eee13-103">Возобновляет базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="eee13-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="eee13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eee13-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eee13-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee13-105">DESCRIPTION</span></span>
<span data-ttu-id="eee13-106">Командлет **Resume-AzSqlDatabase** возобновляет базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eee13-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="eee13-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eee13-107">EXAMPLES</span></span>

### <span data-ttu-id="eee13-108">Пример 1: возобновление базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="eee13-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="eee13-109">Эта команда Возобновляет приостановленную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eee13-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="eee13-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eee13-110">PARAMETERS</span></span>

### <span data-ttu-id="eee13-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eee13-111">-AsJob</span></span>
<span data-ttu-id="eee13-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="eee13-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eee13-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="eee13-113">-DatabaseName</span></span>
<span data-ttu-id="eee13-114">Указывает имя базы данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eee13-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="eee13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee13-115">-DefaultProfile</span></span>
<span data-ttu-id="eee13-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="eee13-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eee13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee13-117">-ResourceGroupName</span></span>
<span data-ttu-id="eee13-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="eee13-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="eee13-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="eee13-119">-ServerName</span></span>
<span data-ttu-id="eee13-120">Указывает имя сервера, на котором размещается база данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="eee13-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="eee13-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eee13-121">-Confirm</span></span>
<span data-ttu-id="eee13-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eee13-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eee13-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eee13-123">-WhatIf</span></span>
<span data-ttu-id="eee13-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eee13-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eee13-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eee13-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eee13-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee13-126">CommonParameters</span></span>
<span data-ttu-id="eee13-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eee13-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee13-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eee13-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee13-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eee13-129">INPUTS</span></span>

### <span data-ttu-id="eee13-130">System. String</span><span class="sxs-lookup"><span data-stu-id="eee13-130">System.String</span></span>

## <span data-ttu-id="eee13-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eee13-131">OUTPUTS</span></span>

### <span data-ttu-id="eee13-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="eee13-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="eee13-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="eee13-133">NOTES</span></span>
* <span data-ttu-id="eee13-134">Командлет **Resume-AzSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eee13-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="eee13-135">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eee13-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="eee13-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eee13-136">RELATED LINKS</span></span>

[<span data-ttu-id="eee13-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eee13-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="eee13-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eee13-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="eee13-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eee13-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="eee13-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eee13-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="eee13-141">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="eee13-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="eee13-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="eee13-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

