---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0C8AC52C-4E70-493C-A299-79CE32EC5EF1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabase.md
ms.openlocfilehash: 9ae96035a4257826ac92dc6dbae75282debf08a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569175"
---
# <span data-ttu-id="f6a9b-101">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f6a9b-101">Get-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f6a9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f6a9b-103">Возвращает одну или несколько баз данных.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-103">Gets one or more databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6a9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6a9b-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabase [[-DatabaseName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6a9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f6a9b-106">Командлет **Get-AzureRmSqlDatabase** получает одну или несколько баз данных SQL Azure с сервера базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-106">The **Get-AzureRmSqlDatabase** cmdlet gets one or more Azure SQL databases from an Azure SQL Database Server.</span></span>

<span data-ttu-id="f6a9b-107">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f6a9b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-108">EXAMPLES</span></span>

### <span data-ttu-id="f6a9b-109">Пример 1: получение всех баз данных на сервере</span><span class="sxs-lookup"><span data-stu-id="f6a9b-109">Example 1: Get all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

<span data-ttu-id="f6a9b-110">Эта команда получает все базы данных на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-110">This command gets all databases on the server named server01.</span></span>

### <span data-ttu-id="f6a9b-111">Пример 2: получение базы данных по имени на сервере</span><span class="sxs-lookup"><span data-stu-id="f6a9b-111">Example 2: Get a database by name on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database02"
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

<span data-ttu-id="f6a9b-112">Эта команда получает базу данных с именем Database02 с сервера с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-112">This command gets a database named Database02 from a server named Server01.</span></span>

## <span data-ttu-id="f6a9b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-113">PARAMETERS</span></span>

### <span data-ttu-id="f6a9b-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f6a9b-114">-DatabaseName</span></span>
<span data-ttu-id="f6a9b-115">Указывает имя базы данных, которую требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-115">Specifies the name of the database to retrieve.</span></span>

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

### <span data-ttu-id="f6a9b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6a9b-116">-ResourceGroupName</span></span>
<span data-ttu-id="f6a9b-117">Указывает имя группы ресурсов, которой назначен сервер базы данных.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-117">Specifies the name of the resource group to which the database server is assigned.</span></span>

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

### <span data-ttu-id="f6a9b-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f6a9b-118">-ServerName</span></span>
<span data-ttu-id="f6a9b-119">Указывает имя сервера, которому назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-119">Specifies the name of the server to which the database is assigned.</span></span>

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

### <span data-ttu-id="f6a9b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6a9b-120">-Confirm</span></span>
<span data-ttu-id="f6a9b-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6a9b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6a9b-122">-WhatIf</span></span>
<span data-ttu-id="f6a9b-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6a9b-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6a9b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6a9b-125">-DefaultProfile</span></span>
<span data-ttu-id="f6a9b-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6a9b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6a9b-127">CommonParameters</span></span>
<span data-ttu-id="f6a9b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6a9b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6a9b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6a9b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6a9b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6a9b-130">INPUTS</span></span>

## <span data-ttu-id="f6a9b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-131">OUTPUTS</span></span>

### <span data-ttu-id="f6a9b-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f6a9b-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f6a9b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6a9b-133">NOTES</span></span>

## <span data-ttu-id="f6a9b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6a9b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f6a9b-135">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f6a9b-135">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f6a9b-136">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f6a9b-136">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f6a9b-137">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f6a9b-137">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="f6a9b-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f6a9b-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f6a9b-139">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f6a9b-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)


