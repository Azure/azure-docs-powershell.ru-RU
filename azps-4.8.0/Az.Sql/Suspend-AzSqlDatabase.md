---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236587"
---
# <span data-ttu-id="fca9c-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fca9c-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="fca9c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fca9c-102">SYNOPSIS</span></span>
<span data-ttu-id="fca9c-103">Приостанавливает базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="fca9c-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="fca9c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fca9c-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fca9c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca9c-105">DESCRIPTION</span></span>
<span data-ttu-id="fca9c-106">Командлет **Suspend-AzSqlDatabase** приостанавливает базу данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fca9c-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="fca9c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fca9c-107">EXAMPLES</span></span>

### <span data-ttu-id="fca9c-108">Пример 1: Приостановка базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fca9c-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fca9c-109">Эта команда приостанавливает активную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fca9c-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="fca9c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fca9c-110">PARAMETERS</span></span>

### <span data-ttu-id="fca9c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fca9c-111">-AsJob</span></span>
<span data-ttu-id="fca9c-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fca9c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fca9c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fca9c-113">-DatabaseName</span></span>
<span data-ttu-id="fca9c-114">Указывает имя базы данных, к которой приостанавливается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fca9c-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="fca9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca9c-115">-DefaultProfile</span></span>
<span data-ttu-id="fca9c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fca9c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fca9c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca9c-117">-ResourceGroupName</span></span>
<span data-ttu-id="fca9c-118">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="fca9c-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="fca9c-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="fca9c-119">-ServerName</span></span>
<span data-ttu-id="fca9c-120">Указывает имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="fca9c-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="fca9c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fca9c-121">-Confirm</span></span>
<span data-ttu-id="fca9c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fca9c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca9c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca9c-123">-WhatIf</span></span>
<span data-ttu-id="fca9c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fca9c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca9c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fca9c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca9c-126">CommonParameters</span></span>
<span data-ttu-id="fca9c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fca9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca9c-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fca9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca9c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fca9c-129">INPUTS</span></span>

### <span data-ttu-id="fca9c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fca9c-130">System.String</span></span>

## <span data-ttu-id="fca9c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fca9c-131">OUTPUTS</span></span>

### <span data-ttu-id="fca9c-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="fca9c-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fca9c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="fca9c-133">NOTES</span></span>
* <span data-ttu-id="fca9c-134">Командлет **Suspend-AzSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fca9c-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="fca9c-135">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="fca9c-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="fca9c-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fca9c-136">RELATED LINKS</span></span>

[<span data-ttu-id="fca9c-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fca9c-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="fca9c-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fca9c-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="fca9c-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fca9c-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="fca9c-140">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fca9c-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="fca9c-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fca9c-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="fca9c-142">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="fca9c-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


