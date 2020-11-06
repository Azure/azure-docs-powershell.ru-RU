---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: ebed943bfea17bf348c48c6d1378822eb8f9c675
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567501"
---
# <span data-ttu-id="d79c7-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d79c7-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="d79c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d79c7-102">SYNOPSIS</span></span>
<span data-ttu-id="d79c7-103">Возвращает эластичные пулы и значения их свойств в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d79c7-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d79c7-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d79c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79c7-105">DESCRIPTION</span></span>
<span data-ttu-id="d79c7-106">Командлет **Get-AzureRmSqlElasticPool** получает эластичные пулы и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="d79c7-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="d79c7-107">Укажите имя существующего эластичного пула, чтобы просмотреть значения свойств только для этого пула.</span><span class="sxs-lookup"><span data-stu-id="d79c7-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="d79c7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d79c7-108">EXAMPLES</span></span>

### <span data-ttu-id="d79c7-109">Пример 1: получение всех эластичных пулов</span><span class="sxs-lookup"><span data-stu-id="d79c7-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="d79c7-110">Эта команда получает список всех эластичных пулов на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="d79c7-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="d79c7-111">Пример 2: получение определенного эластичного пула</span><span class="sxs-lookup"><span data-stu-id="d79c7-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
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

<span data-ttu-id="d79c7-112">Эта команда получает эластичный пул с именем ElasticPool0127 на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="d79c7-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="d79c7-113">Пример 3: Получение метрик для пула баз данных эластичной БД Azure SQL</span><span class="sxs-lookup"><span data-stu-id="d79c7-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
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

<span data-ttu-id="d79c7-114">Эта команда возвращает метрики для пула баз данных эластичной БД Azure SQL с именем ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="d79c7-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="d79c7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d79c7-115">PARAMETERS</span></span>

### <span data-ttu-id="d79c7-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d79c7-116">-ElasticPoolName</span></span>
<span data-ttu-id="d79c7-117">Указывает имя эластичного пула, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d79c7-117">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d79c7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79c7-118">-ResourceGroupName</span></span>
<span data-ttu-id="d79c7-119">Указывает имя группы ресурсов, содержащей эластичный пул, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d79c7-119">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d79c7-120">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="d79c7-120">-ServerName</span></span>
<span data-ttu-id="d79c7-121">Указывает имя сервера, который содержит пул эластичных БД, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d79c7-121">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d79c7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79c7-122">-DefaultProfile</span></span>
<span data-ttu-id="d79c7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d79c7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79c7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79c7-124">CommonParameters</span></span>
<span data-ttu-id="d79c7-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d79c7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79c7-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79c7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79c7-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d79c7-127">INPUTS</span></span>

## <span data-ttu-id="d79c7-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79c7-128">OUTPUTS</span></span>

### <span data-ttu-id="d79c7-129">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="d79c7-129">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="d79c7-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d79c7-130">NOTES</span></span>

## <span data-ttu-id="d79c7-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d79c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="d79c7-132">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d79c7-132">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="d79c7-133">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d79c7-133">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="d79c7-134">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d79c7-134">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


