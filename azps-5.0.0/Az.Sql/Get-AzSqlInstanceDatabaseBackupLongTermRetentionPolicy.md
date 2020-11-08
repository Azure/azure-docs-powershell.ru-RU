---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245833"
---
# <span data-ttu-id="f3211-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f3211-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="f3211-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3211-102">SYNOPSIS</span></span>
<span data-ttu-id="f3211-103">Возвращает политику долгосрочного хранения управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3211-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="f3211-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3211-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3211-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3211-105">DESCRIPTION</span></span>
<span data-ttu-id="f3211-106">Командлет **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** получает долгосрочную политику хранения, зарегистрированную для этой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3211-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="f3211-107">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="f3211-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="f3211-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3211-108">EXAMPLES</span></span>

### <span data-ttu-id="f3211-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3211-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test


ResourceGroupName   : testResourceGroup
ManagedInstanceName : testInstance
DatabaseName        : test
WeeklyRetention     : P2W
MonthlyRetention    : PT0S
YearlyRetention     : PT0S
WeekOfYear          : 0
Location            :
```

<span data-ttu-id="f3211-110">Возвращает текущую версию долгосрочной политики хранения для базы данных.</span><span class="sxs-lookup"><span data-stu-id="f3211-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="f3211-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3211-111">PARAMETERS</span></span>

### <span data-ttu-id="f3211-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3211-112">-DatabaseName</span></span>
<span data-ttu-id="f3211-113">Имя управляемой базы данных Azure, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="f3211-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="f3211-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3211-114">-DefaultProfile</span></span>
<span data-ttu-id="f3211-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3211-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3211-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f3211-116">-InstanceName</span></span>
<span data-ttu-id="f3211-117">Имя экземпляра, управляемого Azure, к которому относится база данных.</span><span class="sxs-lookup"><span data-stu-id="f3211-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="f3211-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3211-118">-ResourceGroupName</span></span>
<span data-ttu-id="f3211-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f3211-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3211-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3211-120">-Confirm</span></span>
<span data-ttu-id="f3211-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3211-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3211-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3211-122">-WhatIf</span></span>
<span data-ttu-id="f3211-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3211-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3211-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3211-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3211-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3211-125">CommonParameters</span></span>
<span data-ttu-id="f3211-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3211-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3211-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3211-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3211-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3211-128">INPUTS</span></span>

### <span data-ttu-id="f3211-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f3211-129">System.String</span></span>

## <span data-ttu-id="f3211-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3211-130">OUTPUTS</span></span>

### <span data-ttu-id="f3211-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f3211-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="f3211-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3211-132">NOTES</span></span>

## <span data-ttu-id="f3211-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3211-133">RELATED LINKS</span></span>

[<span data-ttu-id="f3211-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f3211-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f3211-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="f3211-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="f3211-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f3211-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="f3211-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="f3211-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)