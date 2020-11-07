---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: b93f9a4ffe0e77d464b1913207d0fd3bf7691699
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728978"
---
# <span data-ttu-id="99704-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="99704-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="99704-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99704-102">SYNOPSIS</span></span>
<span data-ttu-id="99704-103">Возвращает политику краткосрочного хранения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="99704-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="99704-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99704-104">SYNTAX</span></span>

### <span data-ttu-id="99704-105">PolicyByResourceInstanceDatabaseSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99704-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="99704-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="99704-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99704-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="99704-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99704-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99704-108">DESCRIPTION</span></span>
<span data-ttu-id="99704-109">Командлет **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** получает краткосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="99704-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="99704-110">Политика — срок хранения (в днях) для резервного копирования на определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="99704-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="99704-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99704-111">EXAMPLES</span></span>

### <span data-ttu-id="99704-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="99704-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="99704-113">Эта команда получает краткосрочную политику хранения для Database01.</span><span class="sxs-lookup"><span data-stu-id="99704-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="99704-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="99704-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="99704-115">Эта команда получает краткосрочную политику хранения для Database01 через конвейер в объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="99704-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="99704-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="99704-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="99704-117">Эта команда получает краткосрочную политику хранения для всех удаленных баз данных с именем Database01 по конвейеру в удаленном объекте базы данных.</span><span class="sxs-lookup"><span data-stu-id="99704-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="99704-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99704-118">PARAMETERS</span></span>

### <span data-ttu-id="99704-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="99704-119">-DatabaseName</span></span>
<span data-ttu-id="99704-120">Имя базы данных экземпляра Azure SQL, для которой требуется получить резервные копии.</span><span class="sxs-lookup"><span data-stu-id="99704-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99704-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99704-121">-DefaultProfile</span></span>
<span data-ttu-id="99704-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99704-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99704-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="99704-123">-DeletionDate</span></span>
<span data-ttu-id="99704-124">Дата удаления базы данных экземпляра Azure SQL, для которой требуется получить резервные копии с точностью до миллисекунд (например, 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="99704-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99704-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99704-125">-InputObject</span></span>
<span data-ttu-id="99704-126">Объект базы данных Live или DELETE, для которого нужно получить или настроить политику.</span><span class="sxs-lookup"><span data-stu-id="99704-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99704-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="99704-127">-InstanceName</span></span>
<span data-ttu-id="99704-128">Имя управляемого экземпляра Azure SQL, на котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="99704-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99704-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99704-129">-ResourceGroupName</span></span>
<span data-ttu-id="99704-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99704-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99704-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99704-131">-ResourceId</span></span>
<span data-ttu-id="99704-132">Краткосрочный идентификатор ресурса политики хранения.</span><span class="sxs-lookup"><span data-stu-id="99704-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="99704-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99704-133">CommonParameters</span></span>
<span data-ttu-id="99704-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99704-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99704-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99704-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99704-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99704-136">INPUTS</span></span>

### <span data-ttu-id="99704-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="99704-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="99704-138">System. String</span><span class="sxs-lookup"><span data-stu-id="99704-138">System.String</span></span>

## <span data-ttu-id="99704-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99704-139">OUTPUTS</span></span>

### <span data-ttu-id="99704-140">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="99704-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="99704-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="99704-141">NOTES</span></span>

## <span data-ttu-id="99704-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99704-142">RELATED LINKS</span></span>
