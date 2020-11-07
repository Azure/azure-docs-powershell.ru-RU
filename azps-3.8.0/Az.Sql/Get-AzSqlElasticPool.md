---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912937"
---
# <span data-ttu-id="7e68a-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7e68a-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="7e68a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e68a-102">SYNOPSIS</span></span>
<span data-ttu-id="7e68a-103">Возвращает эластичные пулы и значения их свойств в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7e68a-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="7e68a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e68a-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e68a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e68a-105">DESCRIPTION</span></span>
<span data-ttu-id="7e68a-106">Командлет **Get-AzSqlElasticPool** получает эластичные пулы и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="7e68a-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="7e68a-107">Укажите имя существующего эластичного пула, чтобы просмотреть значения свойств только для этого пула.</span><span class="sxs-lookup"><span data-stu-id="7e68a-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="7e68a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e68a-108">EXAMPLES</span></span>

### <span data-ttu-id="7e68a-109">Пример 1: получение всех эластичных пулов</span><span class="sxs-lookup"><span data-stu-id="7e68a-109">Example 1: Get all elastic pools</span></span>
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

<span data-ttu-id="7e68a-110">Эта команда получает список всех эластичных пулов на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="7e68a-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="7e68a-111">Пример 2: получение определенного эластичного пула</span><span class="sxs-lookup"><span data-stu-id="7e68a-111">Example 2: Get a specific elastic pool</span></span>
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

<span data-ttu-id="7e68a-112">Эта команда получает эластичный пул с именем ElasticPool0127 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="7e68a-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="7e68a-113">Пример 3: Получение метрик для пула баз данных эластичной БД Azure SQL</span><span class="sxs-lookup"><span data-stu-id="7e68a-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
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

<span data-ttu-id="7e68a-114">Эта команда возвращает метрики для пула баз данных эластичной БД Azure SQL с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="7e68a-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="7e68a-115">Пример 4: получение всех эластичных пулов с помощью фильтров-ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="7e68a-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
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

<span data-ttu-id="7e68a-116">Эта команда получает список всех эластичных пулов на сервере с именем Server01, которые начинаются с "ElasticPool".</span><span class="sxs-lookup"><span data-stu-id="7e68a-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="7e68a-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e68a-117">PARAMETERS</span></span>

### <span data-ttu-id="7e68a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e68a-118">-DefaultProfile</span></span>
<span data-ttu-id="7e68a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7e68a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e68a-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="7e68a-120">-ElasticPoolName</span></span>
<span data-ttu-id="7e68a-121">Указывает имя эластичного пула, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7e68a-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e68a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e68a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e68a-123">Указывает имя группы ресурсов, содержащей эластичный пул, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7e68a-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7e68a-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="7e68a-124">-ServerName</span></span>
<span data-ttu-id="7e68a-125">Указывает имя сервера, который содержит пул эластичных БД, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7e68a-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7e68a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e68a-126">CommonParameters</span></span>
<span data-ttu-id="7e68a-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e68a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e68a-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e68a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e68a-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e68a-129">INPUTS</span></span>

### <span data-ttu-id="7e68a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e68a-130">System.String</span></span>

## <span data-ttu-id="7e68a-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e68a-131">OUTPUTS</span></span>

### <span data-ttu-id="7e68a-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="7e68a-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="7e68a-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e68a-133">NOTES</span></span>

## <span data-ttu-id="7e68a-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e68a-134">RELATED LINKS</span></span>

[<span data-ttu-id="7e68a-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7e68a-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="7e68a-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7e68a-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="7e68a-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="7e68a-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


