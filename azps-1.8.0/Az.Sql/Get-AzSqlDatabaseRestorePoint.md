---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 52024cfa0adcc93ecb278f0d9bfbad7ea8023530
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729019"
---
# <span data-ttu-id="90b03-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="90b03-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="90b03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90b03-102">SYNOPSIS</span></span>
<span data-ttu-id="90b03-103">Извлекает различные точки восстановления, из которых может быть восстановлено хранилище данных SQL.</span><span class="sxs-lookup"><span data-stu-id="90b03-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="90b03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90b03-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90b03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90b03-105">DESCRIPTION</span></span>
<span data-ttu-id="90b03-106">Командлет **Get-AzSqlDatabaseRestorePoint** извлекает отдельные точки восстановления, из которых может быть восстановлено хранилище данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="90b03-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="90b03-107">Для базы данных SQL Azure окно восстановления непрерывно.</span><span class="sxs-lookup"><span data-stu-id="90b03-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="90b03-108">Это означает, что в качестве точки восстановления можно использовать любой момент времени в течение срока хранения резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="90b03-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="90b03-109">Этот командлет также поддерживается службой SQL Server Stretch Database Service в Azure.</span><span class="sxs-lookup"><span data-stu-id="90b03-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="90b03-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90b03-110">EXAMPLES</span></span>

### <span data-ttu-id="90b03-111">Пример 1: получение всех точек восстановления</span><span class="sxs-lookup"><span data-stu-id="90b03-111">Example 1: Get all restore points</span></span>
```
PS C:\>Get-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : CONTINUOUS
RestorePointCreationDate : 
EarliestRestoreDate      : 8/12/2015 12:00:00 AM
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="90b03-112">Эта команда возвращает все доступные точки восстановления для базы данных SQL Azure с именем Database01.</span><span class="sxs-lookup"><span data-stu-id="90b03-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="90b03-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90b03-113">PARAMETERS</span></span>

### <span data-ttu-id="90b03-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90b03-114">-DatabaseName</span></span>
<span data-ttu-id="90b03-115">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="90b03-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="90b03-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90b03-116">-DefaultProfile</span></span>
<span data-ttu-id="90b03-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="90b03-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90b03-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90b03-118">-ResourceGroupName</span></span>
<span data-ttu-id="90b03-119">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="90b03-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="90b03-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="90b03-120">-ServerName</span></span>
<span data-ttu-id="90b03-121">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="90b03-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="90b03-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90b03-122">-Confirm</span></span>
<span data-ttu-id="90b03-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90b03-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90b03-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90b03-124">-WhatIf</span></span>
<span data-ttu-id="90b03-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90b03-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90b03-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90b03-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90b03-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90b03-127">CommonParameters</span></span>
<span data-ttu-id="90b03-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90b03-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90b03-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90b03-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90b03-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90b03-130">INPUTS</span></span>

### <span data-ttu-id="90b03-131">System. String</span><span class="sxs-lookup"><span data-stu-id="90b03-131">System.String</span></span>

## <span data-ttu-id="90b03-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90b03-132">OUTPUTS</span></span>

### <span data-ttu-id="90b03-133">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="90b03-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="90b03-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="90b03-134">NOTES</span></span>

## <span data-ttu-id="90b03-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90b03-135">RELATED LINKS</span></span>
