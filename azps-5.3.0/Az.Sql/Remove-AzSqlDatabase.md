---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419156"
---
# <span data-ttu-id="b8c63-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c63-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="b8c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8c63-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c63-103">Удаляет базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="b8c63-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="b8c63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b8c63-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c63-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8c63-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c63-106">При этом удаляется база данных Azure SQL **AzSqlData.**</span><span class="sxs-lookup"><span data-stu-id="b8c63-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="b8c63-107">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c63-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="b8c63-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b8c63-108">EXAMPLES</span></span>

### <span data-ttu-id="b8c63-109">Пример 1. Удаление базы данных с сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="b8c63-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="b8c63-110">Эта команда удаляет базу данных с именем Database01 с сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="b8c63-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="b8c63-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8c63-111">PARAMETERS</span></span>

### <span data-ttu-id="b8c63-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b8c63-112">-DatabaseName</span></span>
<span data-ttu-id="b8c63-113">Указывает имя базы данных, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c63-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b8c63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c63-114">-DefaultProfile</span></span>
<span data-ttu-id="b8c63-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b8c63-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8c63-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b8c63-116">-Force</span></span>
<span data-ttu-id="b8c63-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b8c63-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8c63-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c63-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8c63-119">Имя группы ресурсов Azure, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="b8c63-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="b8c63-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b8c63-120">-ServerName</span></span>
<span data-ttu-id="b8c63-121">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="b8c63-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b8c63-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8c63-122">-Confirm</span></span>
<span data-ttu-id="b8c63-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c63-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c63-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c63-124">-WhatIf</span></span>
<span data-ttu-id="b8c63-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c63-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c63-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b8c63-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c63-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c63-127">CommonParameters</span></span>
<span data-ttu-id="b8c63-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c63-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c63-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8c63-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c63-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8c63-130">INPUTS</span></span>

### <span data-ttu-id="b8c63-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b8c63-131">System.String</span></span>

## <span data-ttu-id="b8c63-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8c63-132">OUTPUTS</span></span>

### <span data-ttu-id="b8c63-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b8c63-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="b8c63-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b8c63-134">NOTES</span></span>

## <span data-ttu-id="b8c63-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8c63-135">RELATED LINKS</span></span>

[<span data-ttu-id="b8c63-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c63-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="b8c63-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c63-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="b8c63-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c63-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="b8c63-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c63-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="b8c63-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b8c63-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="b8c63-141">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="b8c63-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


