---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568281"
---
# <span data-ttu-id="1f1e0-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f1e0-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="1f1e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f1e0-102">SYNOPSIS</span></span>
<span data-ttu-id="1f1e0-103">Приостанавливает базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f1e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f1e0-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f1e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f1e0-105">DESCRIPTION</span></span>
<span data-ttu-id="1f1e0-106">Командлет **Suspend-AzureRmSqlDatabase** приостанавливает базу данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="1f1e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f1e0-107">EXAMPLES</span></span>

### <span data-ttu-id="1f1e0-108">Пример 1: Приостановка базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="1f1e0-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1f1e0-109">Эта команда приостанавливает активную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="1f1e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f1e0-110">PARAMETERS</span></span>

### <span data-ttu-id="1f1e0-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f1e0-111">-DatabaseName</span></span>
<span data-ttu-id="1f1e0-112">Указывает имя базы данных, к которой приостанавливается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="1f1e0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f1e0-113">-ResourceGroupName</span></span>
<span data-ttu-id="1f1e0-114">Указывает имя группы ресурсов, которой назначен сервер.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="1f1e0-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1f1e0-115">-ServerName</span></span>
<span data-ttu-id="1f1e0-116">Указывает имя сервера, на котором размещена база данных.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="1f1e0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f1e0-117">-Confirm</span></span>
<span data-ttu-id="1f1e0-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f1e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f1e0-119">-WhatIf</span></span>
<span data-ttu-id="1f1e0-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f1e0-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f1e0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f1e0-122">-DefaultProfile</span></span>
<span data-ttu-id="1f1e0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f1e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f1e0-124">CommonParameters</span></span>
<span data-ttu-id="1f1e0-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f1e0-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f1e0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f1e0-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f1e0-127">INPUTS</span></span>

### <span data-ttu-id="1f1e0-128">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1f1e0-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1f1e0-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f1e0-129">OUTPUTS</span></span>

### <span data-ttu-id="1f1e0-130">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1f1e0-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1f1e0-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f1e0-131">NOTES</span></span>
* <span data-ttu-id="1f1e0-132">Командлет **Suspend-AzureRmSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="1f1e0-133">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="1f1e0-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="1f1e0-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f1e0-134">RELATED LINKS</span></span>

[<span data-ttu-id="1f1e0-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f1e0-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="1f1e0-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f1e0-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="1f1e0-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f1e0-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="1f1e0-138">Возобновить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f1e0-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="1f1e0-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1f1e0-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="1f1e0-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="1f1e0-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


