---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505922"
---
# <span data-ttu-id="e25e3-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="e25e3-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="e25e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e25e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e25e3-103">Создает новую точку восстановления, из SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e25e3-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="e25e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e25e3-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e25e3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e25e3-105">DESCRIPTION</span></span>
<span data-ttu-id="e25e3-106">Для создания новой точки восстановления, из SQL Azure можно восстановить хранилище данных **New-AzSqlDataBaseRestorePoint.**</span><span class="sxs-lookup"><span data-stu-id="e25e3-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="e25e3-107">Этот cmdlet в настоящее время поддерживается для хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e25e3-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="e25e3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e25e3-108">EXAMPLES</span></span>

### <span data-ttu-id="e25e3-109">Пример 1. Создание точки восстановления</span><span class="sxs-lookup"><span data-stu-id="e25e3-109">Example 1: Create a restore point</span></span>
```
PS C:\>New-AzSqlDatabaseRestorePoint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RestorePointLabel "RestorePoint01"
ResourceGroupName        : resourcegroup01
ServerName               : server01
DatabaseName             : database01
Location                 : Central US
RestorePointType         : DISCRETE
RestorePointCreationDate : 8/12/2015 12:00:00 AM
EarliestRestoreDate      : 
RestorePointLabel        : RestorePoint01
```

<span data-ttu-id="e25e3-110">Эта команда создает точку восстановления для Azure SQL хранилища данных и возвращает сведения о точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="e25e3-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="e25e3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e25e3-111">PARAMETERS</span></span>

### <span data-ttu-id="e25e3-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e25e3-112">-DatabaseName</span></span>
<span data-ttu-id="e25e3-113">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e25e3-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="e25e3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25e3-114">-DefaultProfile</span></span>
<span data-ttu-id="e25e3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e25e3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e25e3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25e3-116">-ResourceGroupName</span></span>
<span data-ttu-id="e25e3-117">Имя группы ресурсов, которой назначена SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="e25e3-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="e25e3-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="e25e3-118">-RestorePointLabel</span></span>
<span data-ttu-id="e25e3-119">Указывает метку точки восстановления для удобной идентификации.</span><span class="sxs-lookup"><span data-stu-id="e25e3-119">Specifies the label of the restore point for easy identification.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e25e3-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e25e3-120">-ServerName</span></span>
<span data-ttu-id="e25e3-121">Указывает имя сервера AzureSQL Server, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="e25e3-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="e25e3-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e25e3-122">-Confirm</span></span>
<span data-ttu-id="e25e3-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25e3-124">-WhatIf</span></span>
<span data-ttu-id="e25e3-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25e3-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e25e3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25e3-127">CommonParameters</span></span>
<span data-ttu-id="e25e3-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25e3-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e25e3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25e3-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e25e3-130">INPUTS</span></span>

### <span data-ttu-id="e25e3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e25e3-131">System.String</span></span>

## <span data-ttu-id="e25e3-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e25e3-132">OUTPUTS</span></span>

### <span data-ttu-id="e25e3-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="e25e3-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="e25e3-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e25e3-134">NOTES</span></span>

## <span data-ttu-id="e25e3-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e25e3-135">RELATED LINKS</span></span>
