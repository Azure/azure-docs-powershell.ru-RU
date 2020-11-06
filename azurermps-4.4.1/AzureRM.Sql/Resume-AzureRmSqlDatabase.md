---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570036"
---
# <span data-ttu-id="a63fa-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a63fa-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="a63fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a63fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a63fa-103">Возобновляет базу данных хранилища данных SQL.</span><span class="sxs-lookup"><span data-stu-id="a63fa-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a63fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a63fa-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a63fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a63fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a63fa-106">Командлет **Resume-AzureRmSqlDatabase** возобновляет базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a63fa-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a63fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a63fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a63fa-108">Пример 1: возобновление базы данных хранилища данных SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a63fa-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a63fa-109">Эта команда Возобновляет приостановленную базу данных хранилища данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a63fa-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a63fa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a63fa-110">PARAMETERS</span></span>

### <span data-ttu-id="a63fa-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a63fa-111">-DatabaseName</span></span>
<span data-ttu-id="a63fa-112">Указывает имя базы данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a63fa-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a63fa-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63fa-113">-ResourceGroupName</span></span>
<span data-ttu-id="a63fa-114">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="a63fa-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a63fa-115">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a63fa-115">-ServerName</span></span>
<span data-ttu-id="a63fa-116">Указывает имя сервера, на котором размещается база данных, которая возобновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a63fa-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="a63fa-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a63fa-117">-Confirm</span></span>
<span data-ttu-id="a63fa-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a63fa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a63fa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a63fa-119">-WhatIf</span></span>
<span data-ttu-id="a63fa-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a63fa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a63fa-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a63fa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a63fa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63fa-122">-DefaultProfile</span></span>
<span data-ttu-id="a63fa-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a63fa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a63fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63fa-124">CommonParameters</span></span>
<span data-ttu-id="a63fa-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a63fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63fa-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a63fa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63fa-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a63fa-127">INPUTS</span></span>

### <span data-ttu-id="a63fa-128">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a63fa-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a63fa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a63fa-129">OUTPUTS</span></span>

### <span data-ttu-id="a63fa-130">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a63fa-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a63fa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="a63fa-131">NOTES</span></span>
* <span data-ttu-id="a63fa-132">Командлет **Resume-AzureRmSqlDatabase** работает только в базах данных хранилища данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a63fa-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a63fa-133">Эта операция не поддерживается в основных, стандартных и расширенных выпусках базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a63fa-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a63fa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a63fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="a63fa-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a63fa-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="a63fa-136">New-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a63fa-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="a63fa-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a63fa-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="a63fa-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a63fa-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="a63fa-139">Приостановить — AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a63fa-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="a63fa-140">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="a63fa-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


