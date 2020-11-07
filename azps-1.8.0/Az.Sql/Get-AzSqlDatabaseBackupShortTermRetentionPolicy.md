---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 94efd633a64bd1437206a00b83d86cf09fc56036
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729040"
---
# <span data-ttu-id="c1be1-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c1be1-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="c1be1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1be1-102">SYNOPSIS</span></span>
<span data-ttu-id="c1be1-103">Возвращает политику краткосрочного хранения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c1be1-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="c1be1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1be1-104">SYNTAX</span></span>

### <span data-ttu-id="c1be1-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1be1-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1be1-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1be1-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1be1-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c1be1-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1be1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1be1-108">DESCRIPTION</span></span>
<span data-ttu-id="c1be1-109">Командлет **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** получает краткосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="c1be1-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="c1be1-110">Политика — срок хранения (в днях) для резервного копирования на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="c1be1-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="c1be1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1be1-111">EXAMPLES</span></span>

### <span data-ttu-id="c1be1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c1be1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="c1be1-113">Эта команда получает краткосрочную политику хранения для Database01.</span><span class="sxs-lookup"><span data-stu-id="c1be1-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="c1be1-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c1be1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="c1be1-115">Эта команда получает краткосрочную политику хранения для Database01 через конвейер в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="c1be1-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="c1be1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1be1-116">PARAMETERS</span></span>

### <span data-ttu-id="c1be1-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c1be1-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="c1be1-118">Объект базы данных, для которого требуется получить политику.</span><span class="sxs-lookup"><span data-stu-id="c1be1-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1be1-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c1be1-119">-DatabaseName</span></span>
<span data-ttu-id="c1be1-120">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="c1be1-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1be1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1be1-121">-DefaultProfile</span></span>
<span data-ttu-id="c1be1-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1be1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1be1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1be1-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1be1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c1be1-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1be1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1be1-125">-ResourceId</span></span>
<span data-ttu-id="c1be1-126">Краткосрочный идентификатор ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="c1be1-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1be1-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c1be1-127">-ServerName</span></span>
<span data-ttu-id="c1be1-128">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="c1be1-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1be1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1be1-129">CommonParameters</span></span>
<span data-ttu-id="c1be1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1be1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1be1-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1be1-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1be1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1be1-132">INPUTS</span></span>

### <span data-ttu-id="c1be1-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c1be1-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="c1be1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c1be1-134">System.String</span></span>

## <span data-ttu-id="c1be1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1be1-135">OUTPUTS</span></span>

### <span data-ttu-id="c1be1-136">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c1be1-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="c1be1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1be1-137">NOTES</span></span>

## <span data-ttu-id="c1be1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1be1-138">RELATED LINKS</span></span>
