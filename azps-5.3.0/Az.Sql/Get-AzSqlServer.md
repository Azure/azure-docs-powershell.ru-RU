---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506636"
---
# <span data-ttu-id="86e45-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="86e45-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="86e45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86e45-102">SYNOPSIS</span></span>
<span data-ttu-id="86e45-103">Возвращает сведения о серверах SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="86e45-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="86e45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="86e45-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86e45-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86e45-105">DESCRIPTION</span></span>
<span data-ttu-id="86e45-106">Для получения сведений об одном или несколько серверах баз данных Azure в Azure SQL Скайптер возвращается **cmdlet Get-AzSqlServer.**</span><span class="sxs-lookup"><span data-stu-id="86e45-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="86e45-107">Укажите имя сервера, чтобы увидеть сведения только для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="86e45-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="86e45-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="86e45-108">EXAMPLES</span></span>

### <span data-ttu-id="86e45-109">Пример 1. Получить все экземпляры SQL Server ресурсов, которые назначены группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="86e45-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="86e45-110">Эта команда получает сведения обо всех серверах баз данных Azure SQL, которые назначены группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="86e45-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="86e45-111">Пример 2. Сведения о сервере базы данных Azure SQL</span><span class="sxs-lookup"><span data-stu-id="86e45-111">Example 2: Get information about an Azure SQL Database server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="86e45-112">Эта команда получает сведения о сервере базы SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="86e45-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="86e45-113">Пример 3. Все экземпляры SQL Server подписки</span><span class="sxs-lookup"><span data-stu-id="86e45-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzSqlServer
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net

ResourceGroupName        : resourcegroup02
ServerName               : server03
Location                 : East US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server03.database.windows.net
```

<span data-ttu-id="86e45-114">Эта команда получает сведения обо всех серверах баз данных Azure SQL в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="86e45-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="86e45-115">Пример 4. Все экземпляры SQL Server ресурсов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="86e45-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "server*"
ResourceGroupName        : resourcegroup01
ServerName               : server01
Location                 : Central US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net

ResourceGroupName        : resourcegroup01
ServerName               : server02
Location                 : West US
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server02.database.windows.net
```

<span data-ttu-id="86e45-116">Эта команда получает сведения обо всех серверах баз данных Azure SQL, которые назначены группе ресурсов ResourceGroup01, которые начинаются с "сервер".</span><span class="sxs-lookup"><span data-stu-id="86e45-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="86e45-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86e45-117">PARAMETERS</span></span>

### <span data-ttu-id="86e45-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86e45-118">-DefaultProfile</span></span>
<span data-ttu-id="86e45-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86e45-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86e45-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86e45-120">-ResourceGroupName</span></span>
<span data-ttu-id="86e45-121">Имя группы ресурсов, которой назначены серверы.</span><span class="sxs-lookup"><span data-stu-id="86e45-121">Specifies the name of the resource group to which servers are assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e45-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="86e45-122">-ServerName</span></span>
<span data-ttu-id="86e45-123">Указывает имя сервера, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86e45-123">Specifies the name of the server that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86e45-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86e45-124">-Confirm</span></span>
<span data-ttu-id="86e45-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="86e45-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86e45-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86e45-126">-WhatIf</span></span>
<span data-ttu-id="86e45-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86e45-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86e45-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="86e45-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86e45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86e45-129">CommonParameters</span></span>
<span data-ttu-id="86e45-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86e45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86e45-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86e45-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86e45-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="86e45-132">INPUTS</span></span>

### <span data-ttu-id="86e45-133">System.String</span><span class="sxs-lookup"><span data-stu-id="86e45-133">System.String</span></span>

## <span data-ttu-id="86e45-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="86e45-134">OUTPUTS</span></span>

### <span data-ttu-id="86e45-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="86e45-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="86e45-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="86e45-136">NOTES</span></span>

## <span data-ttu-id="86e45-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86e45-137">RELATED LINKS</span></span>

[<span data-ttu-id="86e45-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="86e45-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="86e45-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="86e45-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="86e45-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="86e45-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="86e45-141">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="86e45-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


