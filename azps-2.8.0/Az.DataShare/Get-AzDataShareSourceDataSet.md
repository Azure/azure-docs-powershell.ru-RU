---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: e6f4562daf77204a96991ddeef9164f2f6aff17a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721202"
---
# <span data-ttu-id="abf54-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="abf54-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="abf54-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abf54-102">SYNOPSIS</span></span>
<span data-ttu-id="abf54-103">Получение сведений об исходных наборах данных в подписке "общий доступ".</span><span class="sxs-lookup"><span data-stu-id="abf54-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="abf54-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abf54-104">SYNTAX</span></span>

### <span data-ttu-id="abf54-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="abf54-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="abf54-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abf54-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="abf54-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abf54-107">DESCRIPTION</span></span>
<span data-ttu-id="abf54-108">Командлет **Get-AzDataShareSourceDataSet** содержит сведения о наборах исходных данных в подписке "общий доступ".</span><span class="sxs-lookup"><span data-stu-id="abf54-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="abf54-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abf54-109">EXAMPLES</span></span>

### <span data-ttu-id="abf54-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="abf54-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="abf54-111">Возвращает наборы данных, доступные в исходном общем доступе.</span><span class="sxs-lookup"><span data-stu-id="abf54-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="abf54-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abf54-112">PARAMETERS</span></span>

### <span data-ttu-id="abf54-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="abf54-113">-AccountName</span></span>
<span data-ttu-id="abf54-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="abf54-114">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf54-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf54-115">-DefaultProfile</span></span>
<span data-ttu-id="abf54-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abf54-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf54-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf54-117">-ResourceGroupName</span></span>
<span data-ttu-id="abf54-118">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="abf54-118">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf54-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="abf54-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="abf54-120">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="abf54-120">Azure data share subscription name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abf54-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="abf54-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="abf54-122">Идентификатор ресурса подписки на Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="abf54-122">Azure data share subscription resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abf54-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf54-123">CommonParameters</span></span>
<span data-ttu-id="abf54-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abf54-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf54-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf54-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf54-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abf54-126">INPUTS</span></span>

### <span data-ttu-id="abf54-127">System. String</span><span class="sxs-lookup"><span data-stu-id="abf54-127">System.String</span></span>

## <span data-ttu-id="abf54-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abf54-128">OUTPUTS</span></span>

### <span data-ttu-id="abf54-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="abf54-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="abf54-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="abf54-130">NOTES</span></span>

## <span data-ttu-id="abf54-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abf54-131">RELATED LINKS</span></span>
