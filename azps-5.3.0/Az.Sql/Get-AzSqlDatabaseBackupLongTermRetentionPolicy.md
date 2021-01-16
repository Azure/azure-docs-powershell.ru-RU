---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419407"
---
# <span data-ttu-id="5065c-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5065c-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="5065c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5065c-102">SYNOPSIS</span></span>
<span data-ttu-id="5065c-103">Возвращает базу данных с долгосрочной политикой хранения.</span><span class="sxs-lookup"><span data-stu-id="5065c-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="5065c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5065c-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5065c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5065c-105">DESCRIPTION</span></span>
<span data-ttu-id="5065c-106">Для этой базы данных зарегистрирована долгосрочная политика хранения, зарегистрированная для этого клиента **Get-AzSqlDatabaseBackupLongTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="5065c-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="5065c-107">Политика — это ресурс резервной копии Azure, используемый для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="5065c-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="5065c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5065c-108">EXAMPLES</span></span>

### <span data-ttu-id="5065c-109">Пример 1. Получить текущую версию долгосрочной политики хранения</span><span class="sxs-lookup"><span data-stu-id="5065c-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="5065c-110">Эта команда получает текущую версию долгосрочной политики хранения для базы данных01</span><span class="sxs-lookup"><span data-stu-id="5065c-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="5065c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5065c-111">PARAMETERS</span></span>

### <span data-ttu-id="5065c-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5065c-112">-DatabaseName</span></span>
<span data-ttu-id="5065c-113">Имя базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5065c-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="5065c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5065c-114">-DefaultProfile</span></span>
<span data-ttu-id="5065c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5065c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5065c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5065c-116">-ResourceGroupName</span></span>
<span data-ttu-id="5065c-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5065c-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="5065c-118">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5065c-118">-ServerName</span></span>
<span data-ttu-id="5065c-119">Имя службы Azure SQL Server которая находится в базе данных.</span><span class="sxs-lookup"><span data-stu-id="5065c-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="5065c-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5065c-120">-Confirm</span></span>
<span data-ttu-id="5065c-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5065c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5065c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5065c-122">-WhatIf</span></span>
<span data-ttu-id="5065c-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5065c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5065c-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5065c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5065c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5065c-125">CommonParameters</span></span>
<span data-ttu-id="5065c-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5065c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5065c-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5065c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5065c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5065c-128">INPUTS</span></span>

### <span data-ttu-id="5065c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5065c-129">System.String</span></span>

## <span data-ttu-id="5065c-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5065c-130">OUTPUTS</span></span>

### <span data-ttu-id="5065c-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="5065c-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="5065c-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5065c-132">NOTES</span></span>

## <span data-ttu-id="5065c-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5065c-133">RELATED LINKS</span></span>

[<span data-ttu-id="5065c-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5065c-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="5065c-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="5065c-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="5065c-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="5065c-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="5065c-137">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="5065c-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)