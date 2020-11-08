---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 5fe99e867f4646edc55b2ab304f6549628955a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074288"
---
# <span data-ttu-id="39c7e-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39c7e-101">Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="39c7e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="39c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="39c7e-103">Возвращает политику долгосрочного хранения управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="39c7e-103">Gets a managed database's long term retention policy</span></span>

## <span data-ttu-id="39c7e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="39c7e-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy [-InstanceName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39c7e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c7e-105">DESCRIPTION</span></span>
<span data-ttu-id="39c7e-106">Командлет **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** получает долгосрочную политику хранения, зарегистрированную для этой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="39c7e-106">The **Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy** cmdlet gets the long term retention policy registered to this managed database.</span></span>
<span data-ttu-id="39c7e-107">Политика — это ресурс резервного копирования Azure, который используется для определения политики хранения резервных копий.</span><span class="sxs-lookup"><span data-stu-id="39c7e-107">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="39c7e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="39c7e-108">EXAMPLES</span></span>

### <span data-ttu-id="39c7e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39c7e-109">Example 1</span></span>
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

<span data-ttu-id="39c7e-110">Возвращает текущую версию долгосрочной политики хранения для базы данных.</span><span class="sxs-lookup"><span data-stu-id="39c7e-110">Gets the current version of the long term retention policy for the database</span></span>

## <span data-ttu-id="39c7e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="39c7e-111">PARAMETERS</span></span>

### <span data-ttu-id="39c7e-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39c7e-112">-DatabaseName</span></span>
<span data-ttu-id="39c7e-113">Имя управляемой базы данных Azure, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="39c7e-113">The name of the Azure Managed Database to use.</span></span>

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

### <span data-ttu-id="39c7e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c7e-114">-DefaultProfile</span></span>
<span data-ttu-id="39c7e-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39c7e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c7e-116">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="39c7e-116">-InstanceName</span></span>
<span data-ttu-id="39c7e-117">Имя экземпляра, управляемого Azure, к которому относится база данных.</span><span class="sxs-lookup"><span data-stu-id="39c7e-117">The name of the Azure Managed Instance the database belongs to.</span></span>

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

### <span data-ttu-id="39c7e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39c7e-118">-ResourceGroupName</span></span>
<span data-ttu-id="39c7e-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="39c7e-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="39c7e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39c7e-120">-Confirm</span></span>
<span data-ttu-id="39c7e-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="39c7e-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c7e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39c7e-122">-WhatIf</span></span>
<span data-ttu-id="39c7e-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="39c7e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39c7e-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="39c7e-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39c7e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c7e-125">CommonParameters</span></span>
<span data-ttu-id="39c7e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="39c7e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c7e-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39c7e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c7e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="39c7e-128">INPUTS</span></span>

### <span data-ttu-id="39c7e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="39c7e-129">System.String</span></span>

## <span data-ttu-id="39c7e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="39c7e-130">OUTPUTS</span></span>

### <span data-ttu-id="39c7e-131">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. Model. AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="39c7e-131">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="39c7e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="39c7e-132">NOTES</span></span>

## <span data-ttu-id="39c7e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39c7e-133">RELATED LINKS</span></span>

[<span data-ttu-id="39c7e-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="39c7e-134">Get-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="39c7e-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="39c7e-135">Remove-AzSqlInstanceDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="39c7e-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39c7e-136">Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy</span></span>](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="39c7e-137">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="39c7e-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)