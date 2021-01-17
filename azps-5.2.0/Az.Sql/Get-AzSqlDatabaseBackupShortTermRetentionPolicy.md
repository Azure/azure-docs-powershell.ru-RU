---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d9e872ab11574f07aadfc02a4107c039e41e17e2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415671"
---
# <span data-ttu-id="63972-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="63972-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="63972-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63972-102">SYNOPSIS</span></span>
<span data-ttu-id="63972-103">Получает резервную копию краткого срока хранения.</span><span class="sxs-lookup"><span data-stu-id="63972-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="63972-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63972-104">SYNTAX</span></span>

### <span data-ttu-id="63972-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63972-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63972-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="63972-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63972-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="63972-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="63972-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63972-108">DESCRIPTION</span></span>
<span data-ttu-id="63972-109">Для этой базы данных с недолгой политикой хранения регистрируется политика хранения **Get-AzSqlDatabaseBackupShortTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="63972-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="63972-110">Политика — это период хранения в днях для восстановления резервных копий за данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="63972-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="63972-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63972-111">EXAMPLES</span></span>

### <span data-ttu-id="63972-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63972-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="63972-113">Эта команда получает краткое срок политики хранения для базы данных01.</span><span class="sxs-lookup"><span data-stu-id="63972-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="63972-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63972-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="63972-115">Эта команда получает краткое сроки политики хранения для базы данных01 путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="63972-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="63972-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63972-116">PARAMETERS</span></span>

### <span data-ttu-id="63972-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="63972-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="63972-118">Объект базы данных, для которой нужно получить политику.</span><span class="sxs-lookup"><span data-stu-id="63972-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="63972-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63972-119">-DatabaseName</span></span>
<span data-ttu-id="63972-120">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="63972-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="63972-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63972-121">-DefaultProfile</span></span>
<span data-ttu-id="63972-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63972-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63972-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63972-123">-ResourceGroupName</span></span>
<span data-ttu-id="63972-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63972-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="63972-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63972-125">-ResourceId</span></span>
<span data-ttu-id="63972-126">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="63972-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="63972-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63972-127">-ServerName</span></span>
<span data-ttu-id="63972-128">Имя службы Azure SQL Server которая находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="63972-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="63972-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63972-129">CommonParameters</span></span>
<span data-ttu-id="63972-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63972-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63972-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63972-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63972-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63972-132">INPUTS</span></span>

### <span data-ttu-id="63972-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="63972-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="63972-134">System.String</span><span class="sxs-lookup"><span data-stu-id="63972-134">System.String</span></span>

## <span data-ttu-id="63972-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63972-135">OUTPUTS</span></span>

### <span data-ttu-id="63972-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="63972-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="63972-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63972-137">NOTES</span></span>

## <span data-ttu-id="63972-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63972-138">RELATED LINKS</span></span>
