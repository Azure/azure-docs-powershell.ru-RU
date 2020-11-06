---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: 64d8dae1b12630c6ef0086ab2648fcd424c0389d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567392"
---
# <span data-ttu-id="03700-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="03700-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="03700-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03700-102">SYNOPSIS</span></span>
<span data-ttu-id="03700-103">Возвращает состояние операций с базой данных.</span><span class="sxs-lookup"><span data-stu-id="03700-103">Gets the status of database operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03700-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03700-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03700-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03700-105">DESCRIPTION</span></span>
<span data-ttu-id="03700-106">Командлет **Get-AzureRmSqlDatabaseActivity** получает состояние операций с базой данных в базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="03700-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="03700-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03700-107">EXAMPLES</span></span>

### <span data-ttu-id="03700-108">Пример 1: получение состояния всех экземпляров базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="03700-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="03700-109">Эта команда возвращает состояние операции всех экземпляров базы данных SQL в пуле эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="03700-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="03700-110">Пример 2: получение состояния всех операций с базой данных SQL</span><span class="sxs-lookup"><span data-stu-id="03700-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="03700-111">Эта команда возвращает состояние всех операций базы данных SQL в базе данных.</span><span class="sxs-lookup"><span data-stu-id="03700-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="03700-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03700-112">PARAMETERS</span></span>

### <span data-ttu-id="03700-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03700-113">-DatabaseName</span></span>
<span data-ttu-id="03700-114">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="03700-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03700-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03700-115">-DefaultProfile</span></span>
<span data-ttu-id="03700-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03700-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03700-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="03700-117">-ElasticPoolName</span></span>
<span data-ttu-id="03700-118">Указывает имя пула эластичных баз данных, к которому этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="03700-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03700-119">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="03700-119">-OperationId</span></span>
<span data-ttu-id="03700-120">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="03700-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03700-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03700-121">-ResourceGroupName</span></span>
<span data-ttu-id="03700-122">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="03700-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="03700-123">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="03700-123">-ServerName</span></span>
<span data-ttu-id="03700-124">Указывает имя сервера Microsoft SQL Server, на котором размещается база данных.</span><span class="sxs-lookup"><span data-stu-id="03700-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="03700-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03700-125">-Confirm</span></span>
<span data-ttu-id="03700-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03700-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03700-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03700-127">-WhatIf</span></span>
<span data-ttu-id="03700-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03700-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03700-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03700-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03700-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03700-130">CommonParameters</span></span>
<span data-ttu-id="03700-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03700-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03700-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03700-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03700-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03700-133">INPUTS</span></span>

### <span data-ttu-id="03700-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="03700-134">None</span></span>
<span data-ttu-id="03700-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="03700-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03700-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03700-136">OUTPUTS</span></span>

### <span data-ttu-id="03700-137">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="03700-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="03700-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="03700-138">NOTES</span></span>

## <span data-ttu-id="03700-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03700-139">RELATED LINKS</span></span>
