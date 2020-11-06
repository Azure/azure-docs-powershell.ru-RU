---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0f43956dfa29dac2d7c6ca1869716400b8adad35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567390"
---
# <span data-ttu-id="38ee2-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="38ee2-101">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="38ee2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="38ee2-103">Возвращает политику хранения для базы данных с долговременным сохранением.</span><span class="sxs-lookup"><span data-stu-id="38ee2-103">Gets a database long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38ee2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38ee2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-Current] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38ee2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38ee2-105">DESCRIPTION</span></span>
<span data-ttu-id="38ee2-106">Командлет **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** получает долгосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="38ee2-106">The **Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="38ee2-107">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="38ee2-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="38ee2-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38ee2-108">EXAMPLES</span></span>

### <span data-ttu-id="38ee2-109">Пример 1: получение текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="38ee2-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -Current


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="38ee2-110">Эта команда получает текущую версию долгосрочной политики хранения для Database01</span><span class="sxs-lookup"><span data-stu-id="38ee2-110">This command gets the current version of the long term retention policy for database01</span></span>

### <span data-ttu-id="38ee2-111">Пример 2: получение устаревшей версии политики хранения долгосрочной оплаты</span><span class="sxs-lookup"><span data-stu-id="38ee2-111">Example 2: Get the legacy version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        :
MonthlyRetention                       :
YearlyRetention                        :
WeekOfYear                             :
State                                  : Enabled
RecoveryServicesBackupPolicyResourceId : /subscriptions/4f2b42fc-4fc3-fd41-8ab8-5a382d8b30df/resourceGroups/resourcegroup01/providers/MicrosoftRecoveryServices/vaults/vault01/backupPolicies/policy01
Location                               : Southeast Asia
```

<span data-ttu-id="38ee2-112">Эта команда получает устаревшую версию политики долгосрочного хранения для Database01</span><span class="sxs-lookup"><span data-stu-id="38ee2-112">This command gets the legacy version of the long term retention policy for database01</span></span>

## <span data-ttu-id="38ee2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38ee2-113">PARAMETERS</span></span>

### <span data-ttu-id="38ee2-114">-Current</span><span class="sxs-lookup"><span data-stu-id="38ee2-114">-Current</span></span>
<span data-ttu-id="38ee2-115">Если этот параметр не указан, команда возвращает данные устаревшей политики хранения.</span><span class="sxs-lookup"><span data-stu-id="38ee2-115">If not provided, the command returns the legacy Long Term Retention policy information.</span></span>
<span data-ttu-id="38ee2-116">В противном случае команда возвращает текущую версию долгосрочной политики хранения.</span><span class="sxs-lookup"><span data-stu-id="38ee2-116">Otherwise, the command returns the current version of the Long Term Retention policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="38ee2-117">-DatabaseName</span></span>
<span data-ttu-id="38ee2-118">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="38ee2-118">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ee2-119">-DefaultProfile</span></span>
<span data-ttu-id="38ee2-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38ee2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ee2-121">-ResourceGroupName</span></span>
<span data-ttu-id="38ee2-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38ee2-122">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="38ee2-123">-ServerName</span></span>
<span data-ttu-id="38ee2-124">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="38ee2-124">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38ee2-125">-Confirm</span></span>
<span data-ttu-id="38ee2-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38ee2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ee2-127">-WhatIf</span></span>
<span data-ttu-id="38ee2-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38ee2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ee2-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38ee2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38ee2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ee2-130">CommonParameters</span></span>
<span data-ttu-id="38ee2-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38ee2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="38ee2-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ee2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ee2-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38ee2-133">INPUTS</span></span>

### <span data-ttu-id="38ee2-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="38ee2-134">None</span></span>
<span data-ttu-id="38ee2-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="38ee2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38ee2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38ee2-136">OUTPUTS</span></span>

### <span data-ttu-id="38ee2-137">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="38ee2-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="38ee2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="38ee2-138">NOTES</span></span>

## <span data-ttu-id="38ee2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38ee2-139">RELATED LINKS</span></span>

[<span data-ttu-id="38ee2-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="38ee2-140">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="38ee2-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="38ee2-141">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="38ee2-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="38ee2-142">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="38ee2-143">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="38ee2-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
