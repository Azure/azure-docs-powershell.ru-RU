---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323752"
---
# <span data-ttu-id="08bd2-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08bd2-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="08bd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="08bd2-103">Удаляет базу данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="08bd2-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="08bd2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08bd2-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08bd2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08bd2-105">DESCRIPTION</span></span>
<span data-ttu-id="08bd2-106">При этом удаляется база данных Azure SQL **AzSqlData.**</span><span class="sxs-lookup"><span data-stu-id="08bd2-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="08bd2-107">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="08bd2-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="08bd2-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08bd2-108">EXAMPLES</span></span>

### <span data-ttu-id="08bd2-109">Пример 1. Удаление базы данных с сервера Azure SQL</span><span class="sxs-lookup"><span data-stu-id="08bd2-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="08bd2-110">Эта команда удаляет базу данных с именем Database01 с сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="08bd2-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="08bd2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08bd2-111">PARAMETERS</span></span>

### <span data-ttu-id="08bd2-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08bd2-112">-DatabaseName</span></span>
<span data-ttu-id="08bd2-113">Указывает имя базы данных, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bd2-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="08bd2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bd2-114">-DefaultProfile</span></span>
<span data-ttu-id="08bd2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="08bd2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="08bd2-116">-Force</span><span class="sxs-lookup"><span data-stu-id="08bd2-116">-Force</span></span>
<span data-ttu-id="08bd2-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="08bd2-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="08bd2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08bd2-118">-ResourceGroupName</span></span>
<span data-ttu-id="08bd2-119">Имя группы ресурсов Azure, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="08bd2-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="08bd2-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08bd2-120">-ServerName</span></span>
<span data-ttu-id="08bd2-121">Имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="08bd2-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="08bd2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08bd2-122">-Confirm</span></span>
<span data-ttu-id="08bd2-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bd2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08bd2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08bd2-124">-WhatIf</span></span>
<span data-ttu-id="08bd2-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08bd2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08bd2-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="08bd2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08bd2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bd2-127">CommonParameters</span></span>
<span data-ttu-id="08bd2-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bd2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bd2-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08bd2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bd2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08bd2-130">INPUTS</span></span>

### <span data-ttu-id="08bd2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="08bd2-131">System.String</span></span>

## <span data-ttu-id="08bd2-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08bd2-132">OUTPUTS</span></span>

### <span data-ttu-id="08bd2-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="08bd2-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="08bd2-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08bd2-134">NOTES</span></span>

## <span data-ttu-id="08bd2-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08bd2-135">RELATED LINKS</span></span>

[<span data-ttu-id="08bd2-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08bd2-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="08bd2-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08bd2-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="08bd2-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08bd2-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="08bd2-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08bd2-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="08bd2-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08bd2-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="08bd2-141">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="08bd2-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


