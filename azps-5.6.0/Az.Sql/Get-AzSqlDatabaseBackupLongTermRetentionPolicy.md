---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: b0f3f657caea0da29ecf78baff15fe0afb7008ed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967523"
---
# <span data-ttu-id="01e84-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01e84-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="01e84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01e84-102">SYNOPSIS</span></span>
<span data-ttu-id="01e84-103">Возвращает базу данных с долгосрочной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="01e84-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="01e84-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="01e84-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01e84-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e84-105">DESCRIPTION</span></span>
<span data-ttu-id="01e84-106">Для этой базы данных зарегистрирована долгосрочная политика хранения, зарегистрированная для этого клиента **Get-AzSqlDatabaseBackupLongTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="01e84-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="01e84-107">Политика — это ресурс резервной копии Azure, используемый для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="01e84-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="01e84-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="01e84-108">EXAMPLES</span></span>

### <span data-ttu-id="01e84-109">Пример 1. Получить текущую версию долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="01e84-109">Example 1: Get the current version of the long term retention policy</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01


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

<span data-ttu-id="01e84-110">Эта команда получает текущую версию долгосрочной политики хранения для базы данных01</span><span class="sxs-lookup"><span data-stu-id="01e84-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="01e84-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01e84-111">PARAMETERS</span></span>

### <span data-ttu-id="01e84-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="01e84-112">-DatabaseName</span></span>
<span data-ttu-id="01e84-113">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="01e84-113">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01e84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e84-114">-DefaultProfile</span></span>
<span data-ttu-id="01e84-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01e84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01e84-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e84-116">-ResourceGroupName</span></span>
<span data-ttu-id="01e84-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01e84-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="01e84-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="01e84-118">-ServerName</span></span>
<span data-ttu-id="01e84-119">Имя azure, SQL Server находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="01e84-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="01e84-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e84-120">-Confirm</span></span>
<span data-ttu-id="01e84-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01e84-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e84-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e84-122">-WhatIf</span></span>
<span data-ttu-id="01e84-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01e84-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01e84-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="01e84-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01e84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e84-125">CommonParameters</span></span>
<span data-ttu-id="01e84-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01e84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e84-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="01e84-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e84-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="01e84-128">INPUTS</span></span>

### <span data-ttu-id="01e84-129">System.String</span><span class="sxs-lookup"><span data-stu-id="01e84-129">System.String</span></span>

## <span data-ttu-id="01e84-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="01e84-130">OUTPUTS</span></span>

### <span data-ttu-id="01e84-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="01e84-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="01e84-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="01e84-132">NOTES</span></span>

## <span data-ttu-id="01e84-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01e84-133">RELATED LINKS</span></span>

[<span data-ttu-id="01e84-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="01e84-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="01e84-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="01e84-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="01e84-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="01e84-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="01e84-137">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="01e84-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)