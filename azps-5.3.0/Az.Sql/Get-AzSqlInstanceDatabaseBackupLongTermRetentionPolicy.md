---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 0ece582a85216637454811621aae8a6262475d5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506671"
---
# <span data-ttu-id="fce11-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fce11-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="fce11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fce11-102">SYNOPSIS</span></span>
<span data-ttu-id="fce11-103">Возвращает политику долгосрочного хранения управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="fce11-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="fce11-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fce11-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fce11-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fce11-105">DESCRIPTION</span></span>
<span data-ttu-id="fce11-106">Для этой управляемой базы данных зарегистрирована долгосрочная политика хранения, зарегистрированная для этой управляемой базы данных, с ее учетом получается с его учетом с учетом **cmdlet Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.**</span><span class="sxs-lookup"><span data-stu-id="fce11-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="fce11-107">Политика — это ресурс резервной копии Azure, используемый для определения политики резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="fce11-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="fce11-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fce11-108">EXAMPLES</span></span>

### <span data-ttu-id="fce11-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fce11-109">Example 1</span></span>
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

<span data-ttu-id="fce11-110">Возвращает текущую версию долгосрочной политики хранения для базы данных.</span><span class="sxs-lookup"><span data-stu-id="fce11-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="fce11-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fce11-111">PARAMETERS</span></span>

### <span data-ttu-id="fce11-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fce11-112">-DatabaseName</span></span>
<span data-ttu-id="fce11-113">Имя управляемой базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="fce11-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="fce11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fce11-114">-DefaultProfile</span></span>
<span data-ttu-id="fce11-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fce11-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fce11-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="fce11-116">-InstanceName</span></span>
<span data-ttu-id="fce11-117">Имя управляемого экземпляра Azure, к которой относится база данных.</span><span class="sxs-lookup"><span data-stu-id="fce11-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="fce11-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fce11-118">-ResourceGroupName</span></span>
<span data-ttu-id="fce11-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fce11-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="fce11-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fce11-120">-Confirm</span></span>
<span data-ttu-id="fce11-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce11-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fce11-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fce11-122">-WhatIf</span></span>
<span data-ttu-id="fce11-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fce11-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fce11-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fce11-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fce11-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fce11-125">CommonParameters</span></span>
<span data-ttu-id="fce11-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fce11-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fce11-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fce11-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fce11-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fce11-128">INPUTS</span></span>

### <span data-ttu-id="fce11-129">System.String</span><span class="sxs-lookup"><span data-stu-id="fce11-129">System.String</span></span>

## <span data-ttu-id="fce11-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fce11-130">OUTPUTS</span></span>

### <span data-ttu-id="fce11-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="fce11-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="fce11-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fce11-132">NOTES</span></span>

## <span data-ttu-id="fce11-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fce11-133">RELATED LINKS</span></span>

[<span data-ttu-id="fce11-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fce11-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fce11-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="fce11-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="fce11-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="fce11-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="fce11-137">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="fce11-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)