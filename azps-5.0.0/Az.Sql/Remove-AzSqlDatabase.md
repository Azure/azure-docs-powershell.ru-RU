---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246648"
---
# <span data-ttu-id="cb243-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb243-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="cb243-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb243-102">SYNOPSIS</span></span>
<span data-ttu-id="cb243-103">Удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cb243-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="cb243-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb243-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb243-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb243-105">DESCRIPTION</span></span>
<span data-ttu-id="cb243-106">Командлет **Remove-AzSqlDatabase** удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cb243-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="cb243-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="cb243-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cb243-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb243-108">EXAMPLES</span></span>

### <span data-ttu-id="cb243-109">Пример 1: Удаление базы данных из Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cb243-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="cb243-110">Эта команда удаляет базу данных с именем Database01 из сервера SERVER01.</span><span class="sxs-lookup"><span data-stu-id="cb243-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="cb243-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb243-111">PARAMETERS</span></span>

### <span data-ttu-id="cb243-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cb243-112">-DatabaseName</span></span>
<span data-ttu-id="cb243-113">Указывает имя базы данных, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cb243-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb243-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb243-114">-DefaultProfile</span></span>
<span data-ttu-id="cb243-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cb243-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb243-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cb243-116">-Force</span></span>
<span data-ttu-id="cb243-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cb243-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb243-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb243-118">-ResourceGroupName</span></span>
<span data-ttu-id="cb243-119">Указывает имя группы ресурсов Azure, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="cb243-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cb243-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="cb243-120">-ServerName</span></span>
<span data-ttu-id="cb243-121">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="cb243-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="cb243-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb243-122">-Confirm</span></span>
<span data-ttu-id="cb243-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb243-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb243-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb243-124">-WhatIf</span></span>
<span data-ttu-id="cb243-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb243-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb243-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb243-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb243-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb243-127">CommonParameters</span></span>
<span data-ttu-id="cb243-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb243-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb243-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb243-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb243-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb243-130">INPUTS</span></span>

### <span data-ttu-id="cb243-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cb243-131">System.String</span></span>

## <span data-ttu-id="cb243-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb243-132">OUTPUTS</span></span>

### <span data-ttu-id="cb243-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="cb243-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cb243-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb243-134">NOTES</span></span>

## <span data-ttu-id="cb243-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb243-135">RELATED LINKS</span></span>

[<span data-ttu-id="cb243-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb243-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="cb243-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb243-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="cb243-138">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb243-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="cb243-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb243-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="cb243-140">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cb243-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="cb243-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="cb243-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


