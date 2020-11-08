---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C39ACCAC-2BFF-48D0-95EA-D5B402D74D46
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServer.md
ms.openlocfilehash: 79577b9812f743035d90b2c4fe112dd9f2468fd2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249439"
---
# <span data-ttu-id="2c5c3-101">Get-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2c5c3-101">Get-AzSqlServer</span></span>

## <span data-ttu-id="2c5c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c5c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5c3-103">Возвращает сведения о серверах баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-103">Returns information about SQL Database servers.</span></span>

## <span data-ttu-id="2c5c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c5c3-104">SYNTAX</span></span>

```
Get-AzSqlServer [[-ResourceGroupName] <String>] [[-ServerName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c5c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c5c3-105">DESCRIPTION</span></span>
<span data-ttu-id="2c5c3-106">Командлет **Get-AzSqlServer** возвращает сведения об одном или нескольких серверах баз данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-106">The **Get-AzSqlServer** cmdlet returns information about one or more Azure SQL Database servers.</span></span>
<span data-ttu-id="2c5c3-107">Укажите имя сервера, чтобы просмотреть сведения только для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-107">Specify the name of a server to see information for only that server.</span></span>

## <span data-ttu-id="2c5c3-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c5c3-108">EXAMPLES</span></span>

### <span data-ttu-id="2c5c3-109">Пример 1: получение всех экземпляров сервера SQL Server, назначенных группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="2c5c3-109">Example 1: Get all instances of SQL Server assigned to a resource group</span></span>
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

<span data-ttu-id="2c5c3-110">Эта команда получает сведения обо всех серверах баз данных SQL Azure, назначенных группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-110">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="2c5c3-111">Пример 2: получение сведений о сервере базы данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="2c5c3-111">Example 2: Get information about an Azure SQL Database server</span></span>
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

<span data-ttu-id="2c5c3-112">Эта команда получает сведения о сервере базы данных SQL Azure с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-112">This command gets information about the Azure SQL Database server named Server01.</span></span>

### <span data-ttu-id="2c5c3-113">Пример 3: получение всех экземпляров SQL Server в подписке</span><span class="sxs-lookup"><span data-stu-id="2c5c3-113">Example 3: Get all instances of SQL Server in the subscription</span></span>
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

<span data-ttu-id="2c5c3-114">Эта команда получает сведения обо всех серверах баз данных SQL Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-114">This command gets information about all the Azure SQL Database servers in the current subscription.</span></span>

### <span data-ttu-id="2c5c3-115">Пример 4: получение всех экземпляров SQL Server, назначенных группе ресурсов с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="2c5c3-115">Example 4: Get all instances of SQL Server assigned to a resource group using filtering</span></span>
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

<span data-ttu-id="2c5c3-116">Эта команда получает сведения обо всех серверах баз данных SQL Azure, назначенных группе ресурсов ResourceGroup01, которая начинается с "сервер".</span><span class="sxs-lookup"><span data-stu-id="2c5c3-116">This command gets information about all the Azure SQL Database servers assigned to the resource group ResourceGroup01 that start with "server".</span></span>

## <span data-ttu-id="2c5c3-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c5c3-117">PARAMETERS</span></span>

### <span data-ttu-id="2c5c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5c3-118">-DefaultProfile</span></span>
<span data-ttu-id="2c5c3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c5c3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c5c3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5c3-120">-ResourceGroupName</span></span>
<span data-ttu-id="2c5c3-121">Указывает имя группы ресурсов, которой назначены серверы.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-121">Specifies the name of the resource group to which servers are assigned.</span></span>

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

### <span data-ttu-id="2c5c3-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2c5c3-122">-ServerName</span></span>
<span data-ttu-id="2c5c3-123">Указывает имя сервера, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-123">Specifies the name of the server that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2c5c3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c5c3-124">-Confirm</span></span>
<span data-ttu-id="2c5c3-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5c3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5c3-126">-WhatIf</span></span>
<span data-ttu-id="2c5c3-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c5c3-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5c3-129">CommonParameters</span></span>
<span data-ttu-id="2c5c3-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c5c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5c3-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c5c3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5c3-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c5c3-132">INPUTS</span></span>

### <span data-ttu-id="2c5c3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2c5c3-133">System.String</span></span>

## <span data-ttu-id="2c5c3-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c5c3-134">OUTPUTS</span></span>

### <span data-ttu-id="2c5c3-135">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="2c5c3-135">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="2c5c3-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c5c3-136">NOTES</span></span>

## <span data-ttu-id="2c5c3-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c5c3-137">RELATED LINKS</span></span>

[<span data-ttu-id="2c5c3-138">New-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2c5c3-138">New-AzSqlServer</span></span>](./New-AzSqlServer.md)

[<span data-ttu-id="2c5c3-139">Remove-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2c5c3-139">Remove-AzSqlServer</span></span>](./Remove-AzSqlServer.md)

[<span data-ttu-id="2c5c3-140">Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2c5c3-140">Set-AzSqlServer</span></span>](./Set-AzSqlServer.md)

[<span data-ttu-id="2c5c3-141">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2c5c3-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


