---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 200e53ef1f23c4b829380a2c8b7ca663443e5f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906005"
---
# <span data-ttu-id="80385-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80385-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="80385-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80385-102">SYNOPSIS</span></span>
<span data-ttu-id="80385-103">Удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="80385-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="80385-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80385-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80385-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80385-105">DESCRIPTION</span></span>
<span data-ttu-id="80385-106">Командлет **Remove-AzSqlDatabase** удаляет базу данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="80385-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="80385-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="80385-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="80385-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80385-108">EXAMPLES</span></span>

### <span data-ttu-id="80385-109">Пример 1: Удаление базы данных из Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="80385-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="80385-110">Эта команда удаляет базу данных с именем Database01 из сервера SERVER01.</span><span class="sxs-lookup"><span data-stu-id="80385-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="80385-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80385-111">PARAMETERS</span></span>

### <span data-ttu-id="80385-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="80385-112">-DatabaseName</span></span>
<span data-ttu-id="80385-113">Указывает имя базы данных, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="80385-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="80385-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80385-114">-DefaultProfile</span></span>
<span data-ttu-id="80385-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="80385-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="80385-116">-Force</span><span class="sxs-lookup"><span data-stu-id="80385-116">-Force</span></span>
<span data-ttu-id="80385-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="80385-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="80385-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80385-118">-ResourceGroupName</span></span>
<span data-ttu-id="80385-119">Указывает имя группы ресурсов Azure, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="80385-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="80385-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="80385-120">-ServerName</span></span>
<span data-ttu-id="80385-121">Указывает имя сервера, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="80385-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="80385-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80385-122">-Confirm</span></span>
<span data-ttu-id="80385-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="80385-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80385-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80385-124">-WhatIf</span></span>
<span data-ttu-id="80385-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="80385-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80385-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="80385-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80385-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80385-127">CommonParameters</span></span>
<span data-ttu-id="80385-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80385-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80385-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80385-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80385-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80385-130">INPUTS</span></span>

### <span data-ttu-id="80385-131">System. String</span><span class="sxs-lookup"><span data-stu-id="80385-131">System.String</span></span>

## <span data-ttu-id="80385-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80385-132">OUTPUTS</span></span>

### <span data-ttu-id="80385-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="80385-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="80385-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="80385-134">NOTES</span></span>

## <span data-ttu-id="80385-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80385-135">RELATED LINKS</span></span>

[<span data-ttu-id="80385-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80385-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="80385-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80385-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="80385-138">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80385-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="80385-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80385-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="80385-140">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="80385-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="80385-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="80385-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


