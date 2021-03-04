---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 67A9BB67-CF17-4CAA-99D9-002D0D23178B
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaserestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseRestorePoint.md
ms.openlocfilehash: 8fb320c2caa4993b7880ef719a3d9ea0e0e8c811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956584"
---
# <span data-ttu-id="f8f07-101">New-AzSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="f8f07-101">New-AzSqlDatabaseRestorePoint</span></span>

## <span data-ttu-id="f8f07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f07-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f07-103">Создает новую точку восстановления, из SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="f8f07-103">Creates a new restore point from which a SQL Database can be restored.</span></span>

## <span data-ttu-id="f8f07-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8f07-104">SYNTAX</span></span>

```
New-AzSqlDatabaseRestorePoint -RestorePointLabel <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8f07-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8f07-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f07-106">Для создания новой точки восстановления, из SQL Хранилища данных Azure создается новый SQL **AzSqlDatabaseRestorePoint.**</span><span class="sxs-lookup"><span data-stu-id="f8f07-106">The **New-AzSqlDatabaseRestorePoint** cmdlet creates a new restore point that an Azure SQL Data Warehouse can be restored from.</span></span>
<span data-ttu-id="f8f07-107">Этот cmdlet в настоящее время поддерживается для azure SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="f8f07-107">This cmdlet is currently supported for Azure SQL Data Warehouse.</span></span>

## <span data-ttu-id="f8f07-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8f07-108">EXAMPLES</span></span>

### <span data-ttu-id="f8f07-109">Пример 1. Создание точки восстановления</span><span class="sxs-lookup"><span data-stu-id="f8f07-109">Example 1: Create a restore point</span></span>
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

<span data-ttu-id="f8f07-110">Эта команда создает точку восстановления для Azure SQL хранилища данных и возвращает сведения о точке восстановления.</span><span class="sxs-lookup"><span data-stu-id="f8f07-110">This command creates a restore point for Azure SQL Data Warehouse and returns the details of the restore point.</span></span>

## <span data-ttu-id="f8f07-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8f07-111">PARAMETERS</span></span>

### <span data-ttu-id="f8f07-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8f07-112">-DatabaseName</span></span>
<span data-ttu-id="f8f07-113">Имя базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="f8f07-113">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="f8f07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f07-114">-DefaultProfile</span></span>
<span data-ttu-id="f8f07-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f8f07-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8f07-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f07-116">-ResourceGroupName</span></span>
<span data-ttu-id="f8f07-117">Имя группы ресурсов, которой назначена SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="f8f07-117">Specifies the name of the resource group to which the SQL Database is assigned.</span></span>

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

### <span data-ttu-id="f8f07-118">-RestorePointLabel</span><span class="sxs-lookup"><span data-stu-id="f8f07-118">-RestorePointLabel</span></span>
<span data-ttu-id="f8f07-119">Указывает метку точки восстановления для удобной идентификации.</span><span class="sxs-lookup"><span data-stu-id="f8f07-119">Specifies the label of the restore point for easy identification.</span></span>

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

### <span data-ttu-id="f8f07-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8f07-120">-ServerName</span></span>
<span data-ttu-id="f8f07-121">Указывает имя сервера AzureSQL Server, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="f8f07-121">Specifies the name of the AzureSQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="f8f07-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8f07-122">-Confirm</span></span>
<span data-ttu-id="f8f07-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8f07-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8f07-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8f07-124">-WhatIf</span></span>
<span data-ttu-id="f8f07-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8f07-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8f07-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8f07-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8f07-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f07-127">CommonParameters</span></span>
<span data-ttu-id="f8f07-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f07-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f07-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8f07-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f07-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8f07-130">INPUTS</span></span>

### <span data-ttu-id="f8f07-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f8f07-131">System.String</span></span>

## <span data-ttu-id="f8f07-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8f07-132">OUTPUTS</span></span>

### <span data-ttu-id="f8f07-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span><span class="sxs-lookup"><span data-stu-id="f8f07-133">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseRestorePointModel</span></span>

## <span data-ttu-id="f8f07-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8f07-134">NOTES</span></span>

## <span data-ttu-id="f8f07-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8f07-135">RELATED LINKS</span></span>
