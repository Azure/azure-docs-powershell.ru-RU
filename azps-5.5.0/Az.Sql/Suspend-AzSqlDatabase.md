---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229964"
---
# <span data-ttu-id="55b05-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55b05-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="55b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55b05-102">SYNOPSIS</span></span>
<span data-ttu-id="55b05-103">Приостановка SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="55b05-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="55b05-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55b05-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55b05-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55b05-105">DESCRIPTION</span></span>
<span data-ttu-id="55b05-106">Приостановка базы данных Azure SQL **AzSqlDatabase.**</span><span class="sxs-lookup"><span data-stu-id="55b05-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="55b05-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55b05-107">EXAMPLES</span></span>

### <span data-ttu-id="55b05-108">Пример 1. Приостановка базы данных Azure SQL хранилища данных</span><span class="sxs-lookup"><span data-stu-id="55b05-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="55b05-109">Эта команда приостанавливать активную базу данных Azure SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="55b05-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="55b05-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55b05-110">PARAMETERS</span></span>

### <span data-ttu-id="55b05-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55b05-111">-AsJob</span></span>
<span data-ttu-id="55b05-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="55b05-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="55b05-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="55b05-113">-DatabaseName</span></span>
<span data-ttu-id="55b05-114">Указывает имя базы данных, действие которой этот cmdlet приостанавливал.</span><span class="sxs-lookup"><span data-stu-id="55b05-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="55b05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b05-115">-DefaultProfile</span></span>
<span data-ttu-id="55b05-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="55b05-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55b05-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55b05-117">-ResourceGroupName</span></span>
<span data-ttu-id="55b05-118">Имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="55b05-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="55b05-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="55b05-119">-ServerName</span></span>
<span data-ttu-id="55b05-120">Указывает имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="55b05-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="55b05-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55b05-121">-Confirm</span></span>
<span data-ttu-id="55b05-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b05-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55b05-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55b05-123">-WhatIf</span></span>
<span data-ttu-id="55b05-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55b05-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55b05-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="55b05-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55b05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b05-126">CommonParameters</span></span>
<span data-ttu-id="55b05-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55b05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b05-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55b05-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b05-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55b05-129">INPUTS</span></span>

### <span data-ttu-id="55b05-130">System.String</span><span class="sxs-lookup"><span data-stu-id="55b05-130">System.String</span></span>

## <span data-ttu-id="55b05-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55b05-131">OUTPUTS</span></span>

### <span data-ttu-id="55b05-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="55b05-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="55b05-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55b05-133">NOTES</span></span>
* <span data-ttu-id="55b05-134">**Cmdlet Suspend-AzSqlDatabase** работает только в базах данных Azure SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="55b05-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="55b05-135">Эта операция не поддерживается в выпусках Azure SQL Database Basic, Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="55b05-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="55b05-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55b05-136">RELATED LINKS</span></span>

[<span data-ttu-id="55b05-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55b05-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="55b05-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55b05-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="55b05-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55b05-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="55b05-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55b05-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="55b05-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="55b05-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="55b05-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="55b05-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


