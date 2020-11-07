---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: f0c6de30f0bb38d20f30599a37c1e9a9be378f8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728993"
---
# <span data-ttu-id="a386b-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a386b-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="a386b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a386b-102">SYNOPSIS</span></span>
<span data-ttu-id="a386b-103">Возвращает эластичные пулы и значения их свойств в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a386b-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="a386b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a386b-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a386b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a386b-105">DESCRIPTION</span></span>
<span data-ttu-id="a386b-106">Командлет **Get-AzSqlElasticPool** получает эластичные пулы и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="a386b-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="a386b-107">Укажите имя существующего эластичного пула, чтобы просмотреть значения свойств только для этого пула.</span><span class="sxs-lookup"><span data-stu-id="a386b-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="a386b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a386b-108">EXAMPLES</span></span>

### <span data-ttu-id="a386b-109">Пример 1: получение всех эластичных пулов</span><span class="sxs-lookup"><span data-stu-id="a386b-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="a386b-110">Эта команда получает список всех эластичных пулов на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="a386b-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="a386b-111">Пример 2: получение определенного эластичного пула</span><span class="sxs-lookup"><span data-stu-id="a386b-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="a386b-112">Эта команда получает эластичный пул с именем ElasticPool0127 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="a386b-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="a386b-113">Пример 3: Получение метрик для пула баз данных эластичной БД Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a386b-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="a386b-114">Эта команда возвращает метрики для пула баз данных эластичной БД Azure SQL с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="a386b-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="a386b-115">Пример 4: получение всех эластичных пулов с помощью фильтров-ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="a386b-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="a386b-116">Эта команда получает список всех эластичных пулов на сервере с именем Server01, которые начинаются с "ElasticPool".</span><span class="sxs-lookup"><span data-stu-id="a386b-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="a386b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a386b-117">PARAMETERS</span></span>

### <span data-ttu-id="a386b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a386b-118">-DefaultProfile</span></span>
<span data-ttu-id="a386b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a386b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a386b-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a386b-120">-ElasticPoolName</span></span>
<span data-ttu-id="a386b-121">Указывает имя эластичного пула, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a386b-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="a386b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a386b-122">-ResourceGroupName</span></span>
<span data-ttu-id="a386b-123">Указывает имя группы ресурсов, содержащей эластичный пул, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a386b-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a386b-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="a386b-124">-ServerName</span></span>
<span data-ttu-id="a386b-125">Указывает имя сервера, который содержит пул эластичных БД, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a386b-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a386b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a386b-126">CommonParameters</span></span>
<span data-ttu-id="a386b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a386b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a386b-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a386b-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a386b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a386b-129">INPUTS</span></span>

### <span data-ttu-id="a386b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a386b-130">System.String</span></span>

## <span data-ttu-id="a386b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a386b-131">OUTPUTS</span></span>

### <span data-ttu-id="a386b-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="a386b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a386b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a386b-133">NOTES</span></span>

## <span data-ttu-id="a386b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a386b-134">RELATED LINKS</span></span>

[<span data-ttu-id="a386b-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a386b-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="a386b-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a386b-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="a386b-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a386b-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


