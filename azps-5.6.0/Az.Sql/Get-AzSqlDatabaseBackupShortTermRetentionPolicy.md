---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 4cb97982ed3649502bcf11ce471cef0231ae3058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967507"
---
# <span data-ttu-id="d0c45-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d0c45-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="d0c45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0c45-102">SYNOPSIS</span></span>
<span data-ttu-id="d0c45-103">Получает резервную копию краткого срока хранения.</span><span class="sxs-lookup"><span data-stu-id="d0c45-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="d0c45-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0c45-104">SYNTAX</span></span>

### <span data-ttu-id="d0c45-105">PolicyByResourceServerDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d0c45-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c45-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d0c45-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0c45-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d0c45-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0c45-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0c45-108">DESCRIPTION</span></span>
<span data-ttu-id="d0c45-109">Для этой базы данных с недолгой политикой хранения регистрируется политика хранения **Get-AzSqlDatabaseBackupShortTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="d0c45-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="d0c45-110">Политика — это срок хранения резервных копий, которые будут восстанавливаться за несколько дней.</span><span class="sxs-lookup"><span data-stu-id="d0c45-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="d0c45-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0c45-111">EXAMPLES</span></span>

### <span data-ttu-id="d0c45-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0c45-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="d0c45-113">Эта команда получает краткое срок политики хранения для базы данных01.</span><span class="sxs-lookup"><span data-stu-id="d0c45-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="d0c45-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d0c45-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="d0c45-115">Эта команда получает краткое сроки политики хранения для базы данных01 путем прокажиния в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0c45-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="d0c45-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0c45-116">PARAMETERS</span></span>

### <span data-ttu-id="d0c45-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="d0c45-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="d0c45-118">Объект базы данных, для которой нужно получить политику.</span><span class="sxs-lookup"><span data-stu-id="d0c45-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="d0c45-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0c45-119">-DatabaseName</span></span>
<span data-ttu-id="d0c45-120">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0c45-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="d0c45-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0c45-121">-DefaultProfile</span></span>
<span data-ttu-id="d0c45-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0c45-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0c45-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0c45-123">-ResourceGroupName</span></span>
<span data-ttu-id="d0c45-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0c45-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="d0c45-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0c45-125">-ResourceId</span></span>
<span data-ttu-id="d0c45-126">Краткий ИД ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="d0c45-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="d0c45-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0c45-127">-ServerName</span></span>
<span data-ttu-id="d0c45-128">Имя службы Azure SQL Server которая находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="d0c45-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="d0c45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0c45-129">CommonParameters</span></span>
<span data-ttu-id="d0c45-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0c45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0c45-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0c45-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0c45-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0c45-132">INPUTS</span></span>

### <span data-ttu-id="d0c45-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d0c45-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="d0c45-134">System.String</span><span class="sxs-lookup"><span data-stu-id="d0c45-134">System.String</span></span>

## <span data-ttu-id="d0c45-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0c45-135">OUTPUTS</span></span>

### <span data-ttu-id="d0c45-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d0c45-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="d0c45-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0c45-137">NOTES</span></span>

## <span data-ttu-id="d0c45-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0c45-138">RELATED LINKS</span></span>
