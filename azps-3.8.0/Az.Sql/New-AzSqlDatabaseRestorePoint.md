---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: d2dc1b6acf1978976ce29adea2e79146828accb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066939"
---
# <span data-ttu-id="64c53-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="64c53-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="64c53-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64c53-102">SYNOPSIS</span></span>
<span data-ttu-id="64c53-103">Создает новую точку восстановления, из которой можно восстановить базу данных SQL.</span><span class="sxs-lookup"><span data-stu-id="64c53-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="64c53-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64c53-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="64c53-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64c53-105">DESCRIPTION</span></span>
<span data-ttu-id="64c53-106">Командлет **New-AzSqlDatabaseRestorePoint** создает новую точку восстановления, из которой может быть восстановлено хранилище данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="64c53-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="64c53-107">Этот командлет в настоящее время поддерживается для хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="64c53-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="64c53-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64c53-108">EXAMPLES</span></span>

### <span data-ttu-id="64c53-109">Пример 1: создание точки восстановления</span><span class="sxs-lookup"><span data-stu-id="64c53-109">Example 1: Create a restore point</span></span>
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

<span data-ttu-id="64c53-110">Эта команда создает точку восстановления для хранилища данных Azure SQL и возвращает сведения о точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="64c53-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="64c53-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64c53-111">PARAMETERS</span></span>

### <span data-ttu-id="64c53-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="64c53-112">-DatabaseName</span></span>
<span data-ttu-id="64c53-113">Указывает имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="64c53-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="64c53-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64c53-114">-DefaultProfile</span></span>
<span data-ttu-id="64c53-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="64c53-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64c53-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64c53-116">-ResourceGroupName</span></span>
<span data-ttu-id="64c53-117">Указывает имя группы ресурсов, которой назначена база данных SQL.</span><span class="sxs-lookup"><span data-stu-id="64c53-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="64c53-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="64c53-118">-RestorePointLabel</span></span>
<span data-ttu-id="64c53-119">Задает метку точки восстановления для упрощения идентификации.</span><span class="sxs-lookup"><span data-stu-id="64c53-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="64c53-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="64c53-120">-ServerName</span></span>
<span data-ttu-id="64c53-121">Указывает имя сервера AzureSQL, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="64c53-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="64c53-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64c53-122">-Confirm</span></span>
<span data-ttu-id="64c53-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64c53-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64c53-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64c53-124">-WhatIf</span></span>
<span data-ttu-id="64c53-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64c53-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64c53-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64c53-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64c53-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64c53-127">CommonParameters</span></span>
<span data-ttu-id="64c53-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64c53-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64c53-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64c53-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64c53-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64c53-130">INPUTS</span></span>

### <span data-ttu-id="64c53-131">System. String</span><span class="sxs-lookup"><span data-stu-id="64c53-131">System.String</span></span>

## <span data-ttu-id="64c53-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64c53-132">OUTPUTS</span></span>

### <span data-ttu-id="64c53-133">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="64c53-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="64c53-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="64c53-134">NOTES</span></span>

## <span data-ttu-id="64c53-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64c53-135">RELATED LINKS</span></span>
