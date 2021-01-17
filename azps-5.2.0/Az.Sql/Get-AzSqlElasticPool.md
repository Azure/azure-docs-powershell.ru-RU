---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416300"
---
# <span data-ttu-id="a60ff-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a60ff-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="a60ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a60ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a60ff-103">Получает эластичные пулы и значения их свойств в базе данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a60ff-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="a60ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a60ff-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a60ff-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a60ff-105">DESCRIPTION</span></span>
<span data-ttu-id="a60ff-106">**Cmdlet Get-AzSqlElasticPool** получает эластичные пулы и значения их свойств.</span><span class="sxs-lookup"><span data-stu-id="a60ff-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="a60ff-107">Укажите имя существующего эластичного пула, чтобы увидеть значения свойств только этого пула.</span><span class="sxs-lookup"><span data-stu-id="a60ff-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="a60ff-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a60ff-108">EXAMPLES</span></span>

### <span data-ttu-id="a60ff-109">Пример 1. Получите все эластичные пулы</span><span class="sxs-lookup"><span data-stu-id="a60ff-109">Example 1: Get all elastic pools</span></span>
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

<span data-ttu-id="a60ff-110">Эта команда получает все эластичные пулы на сервере Server01.</span><span class="sxs-lookup"><span data-stu-id="a60ff-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="a60ff-111">Пример 2. Получить определенный эластичный пул</span><span class="sxs-lookup"><span data-stu-id="a60ff-111">Example 2: Get a specific elastic pool</span></span>
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

<span data-ttu-id="a60ff-112">Эта команда получает эластичный пул с именем "ГибкостьPool0127" на сервере с именем Server01.</span><span class="sxs-lookup"><span data-stu-id="a60ff-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="a60ff-113">Пример 3. Метрики для пула SQL azure</span><span class="sxs-lookup"><span data-stu-id="a60ff-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
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

<span data-ttu-id="a60ff-114">Эта команда возвращает метрики для пула SQL Azure с именем "ЭластичнаяPool01".</span><span class="sxs-lookup"><span data-stu-id="a60ff-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="a60ff-115">Пример 4. Получить все эластичные пулы с помощью фильтрации -Умя "Эластичныйpool\*"</span><span class="sxs-lookup"><span data-stu-id="a60ff-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
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

<span data-ttu-id="a60ff-116">Эта команда получает все эластичные пулы на сервере Server01, которые начинаются с "Эластичныйpool".</span><span class="sxs-lookup"><span data-stu-id="a60ff-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="a60ff-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a60ff-117">PARAMETERS</span></span>

### <span data-ttu-id="a60ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a60ff-118">-DefaultProfile</span></span>
<span data-ttu-id="a60ff-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a60ff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a60ff-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a60ff-120">-ElasticPoolName</span></span>
<span data-ttu-id="a60ff-121">Определяет имя эластичного пула, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60ff-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a60ff-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a60ff-122">-ResourceGroupName</span></span>
<span data-ttu-id="a60ff-123">Имя группы ресурсов, которая содержит эластичный пул, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60ff-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a60ff-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a60ff-124">-ServerName</span></span>
<span data-ttu-id="a60ff-125">Имя сервера, который содержит эластичный пул, который получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a60ff-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a60ff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a60ff-126">CommonParameters</span></span>
<span data-ttu-id="a60ff-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a60ff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a60ff-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a60ff-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a60ff-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a60ff-129">INPUTS</span></span>

### <span data-ttu-id="a60ff-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a60ff-130">System.String</span></span>

## <span data-ttu-id="a60ff-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a60ff-131">OUTPUTS</span></span>

### <span data-ttu-id="a60ff-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="a60ff-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a60ff-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a60ff-133">NOTES</span></span>

## <span data-ttu-id="a60ff-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a60ff-134">RELATED LINKS</span></span>

[<span data-ttu-id="a60ff-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a60ff-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="a60ff-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a60ff-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="a60ff-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a60ff-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


