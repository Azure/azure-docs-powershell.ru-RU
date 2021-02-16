---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235476"
---
# <span data-ttu-id="70139-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70139-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="70139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70139-102">SYNOPSIS</span></span>
<span data-ttu-id="70139-103">Возобновление базы SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="70139-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="70139-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="70139-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70139-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70139-105">DESCRIPTION</span></span>
<span data-ttu-id="70139-106">Для **возобновления базы данных Azure SQL AzSqlDatabase.**</span><span class="sxs-lookup"><span data-stu-id="70139-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="70139-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="70139-107">EXAMPLES</span></span>

### <span data-ttu-id="70139-108">Пример 1. Возобновление базы данных azure SQL хранилищ данных</span><span class="sxs-lookup"><span data-stu-id="70139-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="70139-109">Эта команда возобновляет приостановленную базу данных Azure SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="70139-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="70139-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="70139-110">PARAMETERS</span></span>

### <span data-ttu-id="70139-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70139-111">-AsJob</span></span>
<span data-ttu-id="70139-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="70139-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70139-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="70139-113">-DatabaseName</span></span>
<span data-ttu-id="70139-114">Указывает имя базы данных, которую возобновляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70139-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="70139-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70139-115">-DefaultProfile</span></span>
<span data-ttu-id="70139-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="70139-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70139-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70139-117">-ResourceGroupName</span></span>
<span data-ttu-id="70139-118">Имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="70139-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="70139-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="70139-119">-ServerName</span></span>
<span data-ttu-id="70139-120">Указывает имя сервера, на котором размещена база данных, возобновляемая этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70139-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="70139-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70139-121">-Confirm</span></span>
<span data-ttu-id="70139-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70139-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70139-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70139-123">-WhatIf</span></span>
<span data-ttu-id="70139-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70139-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="70139-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="70139-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70139-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70139-126">CommonParameters</span></span>
<span data-ttu-id="70139-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70139-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70139-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="70139-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70139-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="70139-129">INPUTS</span></span>

### <span data-ttu-id="70139-130">System.String</span><span class="sxs-lookup"><span data-stu-id="70139-130">System.String</span></span>

## <span data-ttu-id="70139-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="70139-131">OUTPUTS</span></span>

### <span data-ttu-id="70139-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="70139-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="70139-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="70139-133">NOTES</span></span>
* <span data-ttu-id="70139-134">**Cmdlet Resume-AzSqlDatabase** работает только в базах данных Azure SQL хранилища данных.</span><span class="sxs-lookup"><span data-stu-id="70139-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="70139-135">Эта операция не поддерживается в выпусках Azure SQL Database Basic, Standard и Premium.</span><span class="sxs-lookup"><span data-stu-id="70139-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="70139-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70139-136">RELATED LINKS</span></span>

[<span data-ttu-id="70139-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70139-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="70139-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70139-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="70139-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70139-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="70139-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70139-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="70139-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="70139-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="70139-142">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="70139-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


