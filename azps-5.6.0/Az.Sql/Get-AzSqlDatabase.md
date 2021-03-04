---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 24e6d0f96114f6843b5af48fafe6d58cc7b49126
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993247"
---
# <span data-ttu-id="57984-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57984-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="57984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57984-102">SYNOPSIS</span></span>
<span data-ttu-id="57984-103">Получает одну или несколько баз данных.</span><span class="sxs-lookup"><span data-stu-id="57984-103">Gets one or more databases.</span></span>

## <span data-ttu-id="57984-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57984-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57984-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57984-105">DESCRIPTION</span></span>
<span data-ttu-id="57984-106">Для получения одной или SQL базы данных Azure с сервера базы данных Azure SQL-сервера базы данных **Get-AzSqlData.**</span><span class="sxs-lookup"><span data-stu-id="57984-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="57984-107">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="57984-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="57984-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57984-108">EXAMPLES</span></span>

### <span data-ttu-id="57984-109">Пример 1. Все базы данных на сервере</span><span class="sxs-lookup"><span data-stu-id="57984-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : master
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="57984-110">Эта команда получает все базы данных на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="57984-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="57984-111">Пример 2. Как получить базу данных по имени на сервере</span><span class="sxs-lookup"><span data-stu-id="57984-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="57984-112">Эта команда получает базу данных с именем Database02 с сервера Server01.</span><span class="sxs-lookup"><span data-stu-id="57984-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="57984-113">Пример 3. Все базы данных на сервере с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="57984-113">Example 3: Get all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01" -DatabaseName "database*"
ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database01
Location                      : Central US
DatabaseId                    : a2a7f2db-7526-4d86-a7b2-36276ee10dc6
Edition                       : None
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 5368709120
Status                        : Online
CreationDate                  : 7/3/2015 7:32:44 AM
CurrentServiceObjectiveId     : c99ac918-dbea-463f-a475-16ec020fdc12
CurrentServiceObjectiveName   : System1
RequestedServiceObjectiveId   : c99ac918-dbea-463f-a475-16ec020fdc12
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          : 

ResourceGroupName             : resourcegroup01
ServerName                    : server01
DatabaseName                  : database02
Location                      : Central US
DatabaseId                    : a1e6bd1a-735a-4d48-8b98-afead5ef1218
Edition                       : Standard
CollationName                 : SQL_Latin1_General_CP1_CI_AS
CatalogCollation              : 
MaxSizeBytes                  : 268435456000
Status                        : Online
CreationDate                  : 7/3/2015 7:33:37 AM
CurrentServiceObjectiveId     : f1173c43-91bd-4aaa-973c-54e79e15235b
CurrentServiceObjectiveName   : S0
RequestedServiceObjectiveId   : f1173c43-91bd-4aaa-973c-54e79e15235b
RequestedServiceObjectiveName : 
ElasticPoolName               : 
EarliestRestoreDate           : 
Tags                          :
```

<span data-ttu-id="57984-114">Эта команда получает все базы данных на сервере Server01, которые начинаются с "database".</span><span class="sxs-lookup"><span data-stu-id="57984-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="57984-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57984-115">PARAMETERS</span></span>

### <span data-ttu-id="57984-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57984-116">-DatabaseName</span></span>
<span data-ttu-id="57984-117">Имя базы данных, извлекаемой.</span><span class="sxs-lookup"><span data-stu-id="57984-117">Specifies the name of the database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57984-118">-DefaultProfile</span></span>
<span data-ttu-id="57984-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="57984-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57984-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57984-120">-ResourceGroupName</span></span>
<span data-ttu-id="57984-121">Имя группы ресурсов, которой назначен сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="57984-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="57984-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="57984-122">-ServerName</span></span>
<span data-ttu-id="57984-123">Указывает имя сервера, на который назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="57984-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="57984-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57984-124">-Confirm</span></span>
<span data-ttu-id="57984-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57984-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57984-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57984-126">-WhatIf</span></span>
<span data-ttu-id="57984-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57984-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57984-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57984-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57984-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57984-129">CommonParameters</span></span>
<span data-ttu-id="57984-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57984-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57984-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57984-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57984-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57984-132">INPUTS</span></span>

### <span data-ttu-id="57984-133">System.String</span><span class="sxs-lookup"><span data-stu-id="57984-133">System.String</span></span>

## <span data-ttu-id="57984-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57984-134">OUTPUTS</span></span>

### <span data-ttu-id="57984-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="57984-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="57984-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57984-136">NOTES</span></span>

## <span data-ttu-id="57984-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57984-137">RELATED LINKS</span></span>

[<span data-ttu-id="57984-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57984-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="57984-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57984-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="57984-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57984-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="57984-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57984-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="57984-142">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="57984-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


