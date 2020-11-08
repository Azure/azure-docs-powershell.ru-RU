---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabase.md
ms.openlocfilehash: 4f90d6d0c33874750bf2f32ae7f65bf32457f63c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066044"
---
# <span data-ttu-id="073cc-101">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="073cc-101">Get-AzSqlDatabase</span></span>

## <span data-ttu-id="073cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="073cc-102">SYNOPSIS</span></span>
<span data-ttu-id="073cc-103">Возвращает одну или несколько баз данных.</span><span class="sxs-lookup"><span data-stu-id="073cc-103">Gets one or more databases.</span></span>

## <span data-ttu-id="073cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="073cc-104">SYNTAX</span></span>

```
Get-AzSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="073cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="073cc-105">DESCRIPTION</span></span>
<span data-ttu-id="073cc-106">Командлет **Get-AzSqlDatabase** получает одну или несколько баз данных SQL Azure с сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="073cc-106">The **Get-AzSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>
<span data-ttu-id="073cc-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="073cc-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="073cc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="073cc-108">EXAMPLES</span></span>

### <span data-ttu-id="073cc-109">Пример 1: получение всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="073cc-109">Example 1: Get all databases on a server</span></span>
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

<span data-ttu-id="073cc-110">Эта команда получает все базы данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="073cc-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="073cc-111">Пример 2: получение базы данных по имени на сервере</span><span class="sxs-lookup"><span data-stu-id="073cc-111">Example 2: Get a database by name on a server</span></span>
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

<span data-ttu-id="073cc-112">Эта команда получает базу данных с именем Database02 с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="073cc-112">This command gets a database named Database02 from a server named Server01.</span></span>

### <span data-ttu-id="073cc-113">Пример 3: получение всех баз данных на сервере с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="073cc-113">Example 3: Get all databases on a server using filtering</span></span>
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

<span data-ttu-id="073cc-114">Эта команда получает все базы данных на сервере с именем Server01, которые начинаются с Database.</span><span class="sxs-lookup"><span data-stu-id="073cc-114">This command gets all databases on the server named server01 that start with "database".</span></span>

## <span data-ttu-id="073cc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="073cc-115">PARAMETERS</span></span>

### <span data-ttu-id="073cc-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="073cc-116">-DatabaseName</span></span>
<span data-ttu-id="073cc-117">Указывает имя базы данных, которую требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="073cc-117">Specifies the name of the database to retrieve.</span></span>

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

### <span data-ttu-id="073cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073cc-118">-DefaultProfile</span></span>
<span data-ttu-id="073cc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="073cc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="073cc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073cc-120">-ResourceGroupName</span></span>
<span data-ttu-id="073cc-121">Указывает имя группы ресурсов, которой назначен сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="073cc-121">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="073cc-122">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="073cc-122">-ServerName</span></span>
<span data-ttu-id="073cc-123">Указывает имя сервера, которому назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="073cc-123">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="073cc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="073cc-124">-Confirm</span></span>
<span data-ttu-id="073cc-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="073cc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="073cc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="073cc-126">-WhatIf</span></span>
<span data-ttu-id="073cc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="073cc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="073cc-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="073cc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="073cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073cc-129">CommonParameters</span></span>
<span data-ttu-id="073cc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="073cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073cc-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="073cc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073cc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="073cc-132">INPUTS</span></span>

### <span data-ttu-id="073cc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="073cc-133">System.String</span></span>

## <span data-ttu-id="073cc-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="073cc-134">OUTPUTS</span></span>

### <span data-ttu-id="073cc-135">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="073cc-135">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="073cc-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="073cc-136">NOTES</span></span>

## <span data-ttu-id="073cc-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="073cc-137">RELATED LINKS</span></span>

[<span data-ttu-id="073cc-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="073cc-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="073cc-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="073cc-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="073cc-140">Возобновить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="073cc-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="073cc-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="073cc-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="073cc-142">Приостановить — AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="073cc-142">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)


