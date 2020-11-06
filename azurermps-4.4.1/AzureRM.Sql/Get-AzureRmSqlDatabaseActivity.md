---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseActivity.md
ms.openlocfilehash: b37ae31c1f0dc6360743a863f0305fd5823cbb3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568667"
---
# <span data-ttu-id="541ad-101">Get-AzureRmSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="541ad-101">Get-AzureRmSqlDatabaseActivity</span></span>

## <span data-ttu-id="541ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="541ad-102">SYNOPSIS</span></span>
<span data-ttu-id="541ad-103">Получает состояние перемещения эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="541ad-103">Gets the status of moving elastic databases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="541ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="541ad-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseActivity [-ServerName] <String> -ElasticPoolName <String> -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="541ad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="541ad-105">DESCRIPTION</span></span>
<span data-ttu-id="541ad-106">Командлет **Get-AzureRmSqlDatabaseActivity** возвращает состояние эластичных баз данных, которые перемещаются в пул эластичных баз данных Azure SQL Server или из него.</span><span class="sxs-lookup"><span data-stu-id="541ad-106">The **Get-AzureRmSqlDatabaseActivity** cmdlet gets the status of elastic databases moving into or out of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="541ad-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="541ad-107">EXAMPLES</span></span>

### <span data-ttu-id="541ad-108">Пример 1: получение состояния всех экземпляров базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="541ad-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="541ad-109">Эта команда возвращает состояние операции всех экземпляров базы данных SQL в пуле эластичных БД с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="541ad-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="541ad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="541ad-110">PARAMETERS</span></span>

### <span data-ttu-id="541ad-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="541ad-111">-DatabaseName</span></span>
<span data-ttu-id="541ad-112">Указывает имя базы данных, для которой этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="541ad-112">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="541ad-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="541ad-113">-ElasticPoolName</span></span>
<span data-ttu-id="541ad-114">Указывает имя пула эластичных баз данных, к которому этот командлет получает состояние.</span><span class="sxs-lookup"><span data-stu-id="541ad-114">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="541ad-115">-С идентификатором</span><span class="sxs-lookup"><span data-stu-id="541ad-115">-OperationId</span></span>
<span data-ttu-id="541ad-116">Указывает идентификатор операции, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="541ad-116">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="541ad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="541ad-117">-ResourceGroupName</span></span>
<span data-ttu-id="541ad-118">Указывает имя группы ресурсов, которой назначена база данных.</span><span class="sxs-lookup"><span data-stu-id="541ad-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="541ad-119">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="541ad-119">-ServerName</span></span>
<span data-ttu-id="541ad-120">Указывает имя сервера Microsoft SQL Server, на котором размещается пул эластичных баз данных.</span><span class="sxs-lookup"><span data-stu-id="541ad-120">Specifies the name of the Microsoft SQL Server that hosts the elastic database pool.</span></span>

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

### <span data-ttu-id="541ad-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="541ad-121">-Confirm</span></span>
<span data-ttu-id="541ad-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="541ad-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="541ad-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="541ad-123">-WhatIf</span></span>
<span data-ttu-id="541ad-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="541ad-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="541ad-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="541ad-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="541ad-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="541ad-126">-DefaultProfile</span></span>
<span data-ttu-id="541ad-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="541ad-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="541ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="541ad-128">CommonParameters</span></span>
<span data-ttu-id="541ad-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="541ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="541ad-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="541ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="541ad-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="541ad-131">INPUTS</span></span>

## <span data-ttu-id="541ad-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="541ad-132">OUTPUTS</span></span>

### <span data-ttu-id="541ad-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseActivityModel</span><span class="sxs-lookup"><span data-stu-id="541ad-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="541ad-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="541ad-134">NOTES</span></span>

## <span data-ttu-id="541ad-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="541ad-135">RELATED LINKS</span></span>

