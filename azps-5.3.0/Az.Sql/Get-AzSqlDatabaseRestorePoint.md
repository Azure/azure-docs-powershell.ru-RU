---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 9765afd55ea94bda672d5e1ce43ac3d8d535510d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419311"
---
# <span data-ttu-id="5cd18-101">Get-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5cd18-101">Get-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="5cd18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd18-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd18-103">Извлекает отдельные точки восстановления, из которых SQL можно восстановить хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="5cd18-103">Retrieves the distinct restore points from which a SQL Data Warehouse can be restored.</span></span>

## <span data-ttu-id="5cd18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cd18-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseRestorePoint [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cd18-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cd18-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd18-106">Для восстановления различных точек восстановления, из SQL Azure, извлекается **cmdlet Get-AzSqlDatabaseRestorePoint.**</span><span class="sxs-lookup"><span data-stu-id="5cd18-106">The **Get-AzSqlDatabaseRestorePoint** cmdlet retrieves the distinct restore points that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="5cd18-107">Для базы данных Azure SQL окно восстановления непрерывно.</span><span class="sxs-lookup"><span data-stu-id="5cd18-107">For an Azure SQL Database, the restore window is continuous.</span></span>
<span data-ttu-id="5cd18-108">Это означает, что в качестве точки восстановления можно использовать любую точку времени в периоде хранения резервной копии базы данных.</span><span class="sxs-lookup"><span data-stu-id="5cd18-108">This means that any point in time in the backup retention period of the database can be used as a restore point.</span></span>
<span data-ttu-id="5cd18-109">Этот cmdlet также поддерживается службой SQL Server Stretch Database в Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd18-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5cd18-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cd18-110">EXAMPLES</span></span>

### <span data-ttu-id="5cd18-111">Пример 1. Получить все точки восстановления</span><span class="sxs-lookup"><span data-stu-id="5cd18-111">Example 1: Get all restore points</span></span>
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

<span data-ttu-id="5cd18-112">Эта команда возвращает все доступные точки восстановления для базы данных Azure SQL Database01.</span><span class="sxs-lookup"><span data-stu-id="5cd18-112">This command returns all available restore points for the Azure SQL Database named Database01.</span></span>

## <span data-ttu-id="5cd18-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd18-113">PARAMETERS</span></span>

### <span data-ttu-id="5cd18-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5cd18-114">-DatabaseName</span></span>
<span data-ttu-id="5cd18-115">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5cd18-115">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="5cd18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd18-116">-DefaultProfile</span></span>
<span data-ttu-id="5cd18-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5cd18-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cd18-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd18-118">-ResourceGroupName</span></span>
<span data-ttu-id="5cd18-119">Имя группы ресурсов, которой назначена SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="5cd18-119">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="5cd18-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5cd18-120">-ServerName</span></span>
<span data-ttu-id="5cd18-121">Указывает имя сервера AzureSQL Server, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="5cd18-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="5cd18-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cd18-122">-Confirm</span></span>
<span data-ttu-id="5cd18-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd18-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cd18-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd18-124">-WhatIf</span></span>
<span data-ttu-id="5cd18-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd18-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cd18-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cd18-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cd18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd18-127">CommonParameters</span></span>
<span data-ttu-id="5cd18-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd18-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cd18-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd18-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd18-130">INPUTS</span></span>

### <span data-ttu-id="5cd18-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd18-131">System.String</span></span>

## <span data-ttu-id="5cd18-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd18-132">OUTPUTS</span></span>

### <span data-ttu-id="5cd18-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="5cd18-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="5cd18-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cd18-134">NOTES</span></span>

## <span data-ttu-id="5cd18-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cd18-135">RELATED LINKS</span></span>
