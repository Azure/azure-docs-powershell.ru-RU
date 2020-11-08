---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0dd5f38f00e715141a967160cadc8ab075825ac6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235830"
---
# <span data-ttu-id="b7804-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7804-101">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="b7804-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7804-102">SYNOPSIS</span></span>
<span data-ttu-id="b7804-103">Возвращает политику хранения для базы данных с долговременным сохранением.</span><span class="sxs-lookup"><span data-stu-id="b7804-103">Gets a database long term retention policy.</span></span>

## <span data-ttu-id="b7804-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7804-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseBackupLongTermRetentionPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7804-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7804-105">DESCRIPTION</span></span>
<span data-ttu-id="b7804-106">Командлет **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** получает долгосрочную политику хранения, зарегистрированную в этой базе данных.</span><span class="sxs-lookup"><span data-stu-id="b7804-106">The **Get-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="b7804-107">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="b7804-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="b7804-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7804-108">EXAMPLES</span></span>

### <span data-ttu-id="b7804-109">Пример 1: получение текущей версии политики долгосрочного хранения</span><span class="sxs-lookup"><span data-stu-id="b7804-109">Example 1: Get the current version of the long term retention policy</span></span>
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

<span data-ttu-id="b7804-110">Эта команда получает текущую версию долгосрочной политики хранения для Database01</span><span class="sxs-lookup"><span data-stu-id="b7804-110">This command gets the current version of the long term retention policy for database01</span></span>

## <span data-ttu-id="b7804-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7804-111">PARAMETERS</span></span>

### <span data-ttu-id="b7804-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b7804-112">-DatabaseName</span></span>
<span data-ttu-id="b7804-113">Имя базы данных SQL Azure, которую нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="b7804-113">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="b7804-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7804-114">-DefaultProfile</span></span>
<span data-ttu-id="b7804-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7804-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7804-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7804-116">-ResourceGroupName</span></span>
<span data-ttu-id="b7804-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7804-117">The name of the resource group.</span></span>

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

### <span data-ttu-id="b7804-118">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="b7804-118">-ServerName</span></span>
<span data-ttu-id="b7804-119">Имя сервера Azure SQL Server, в котором находится база данных.</span><span class="sxs-lookup"><span data-stu-id="b7804-119">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="b7804-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7804-120">-Confirm</span></span>
<span data-ttu-id="b7804-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7804-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7804-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7804-122">-WhatIf</span></span>
<span data-ttu-id="b7804-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7804-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7804-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7804-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7804-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7804-125">CommonParameters</span></span>
<span data-ttu-id="b7804-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7804-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7804-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7804-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7804-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7804-128">INPUTS</span></span>

### <span data-ttu-id="b7804-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b7804-129">System.String</span></span>

## <span data-ttu-id="b7804-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7804-130">OUTPUTS</span></span>

### <span data-ttu-id="b7804-131">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b7804-131">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="b7804-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7804-132">NOTES</span></span>

## <span data-ttu-id="b7804-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7804-133">RELATED LINKS</span></span>

[<span data-ttu-id="b7804-134">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b7804-134">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b7804-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="b7804-135">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="b7804-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7804-136">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="b7804-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="b7804-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)