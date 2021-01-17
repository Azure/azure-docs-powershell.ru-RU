---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesourcedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSourceDataSet.md
ms.openlocfilehash: 5f10289a5890ffa0e2764c475d65a0d5103b705e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420719"
---
# <span data-ttu-id="c7a3f-101">Get-AzDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="c7a3f-101">Get-AzDataShareSourceDataSet</span></span>

## <span data-ttu-id="c7a3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a3f-103">Получает сведения об исходных наборах данных в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="c7a3f-103">Gets information about source data sets in share subscription.</span></span>

## <span data-ttu-id="c7a3f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7a3f-104">SYNTAX</span></span>

### <span data-ttu-id="c7a3f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c7a3f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSourceDataSet -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7a3f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7a3f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSourceDataSet -ShareSubscriptionResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a3f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7a3f-107">DESCRIPTION</span></span>
<span data-ttu-id="c7a3f-108">Для получения сведений об исходных наборах данных в подписке на доступ можно получить сведения о cmdlet **Get-AzDataShareSourceDataSet.**</span><span class="sxs-lookup"><span data-stu-id="c7a3f-108">The **Get-AzDataShareSourceDataSet** cmdlet provides information about the source data sets in the share subscription.</span></span> 

## <span data-ttu-id="c7a3f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7a3f-109">EXAMPLES</span></span>

### <span data-ttu-id="c7a3f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7a3f-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSourceDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription"

DataSetId   : 63116d3f-515a-47a2-9b18-d981b16a9d21
DataSetName : filesystem1
DataSetType : Blob
Id          : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription/consumerSourceDataSets/AdsDataSets
Name        : AdsDataSets
Type        : Microsoft.DataShare/ConsumerSourceDataSet
```

<span data-ttu-id="c7a3f-111">Наборы данных, доступные в источнике</span><span class="sxs-lookup"><span data-stu-id="c7a3f-111">Gets datasets available in the source share</span></span>

## <span data-ttu-id="c7a3f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7a3f-112">PARAMETERS</span></span>

### <span data-ttu-id="c7a3f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c7a3f-113">-AccountName</span></span>
<span data-ttu-id="c7a3f-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="c7a3f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="c7a3f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a3f-115">-DefaultProfile</span></span>
<span data-ttu-id="c7a3f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a3f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a3f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a3f-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7a3f-118">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="c7a3f-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="c7a3f-119">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="c7a3f-119">-ShareSubscriptionName</span></span>
<span data-ttu-id="c7a3f-120">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="c7a3f-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="c7a3f-121">-ShareSubscriptionResourceId</span><span class="sxs-lookup"><span data-stu-id="c7a3f-121">-ShareSubscriptionResourceId</span></span>
<span data-ttu-id="c7a3f-122">Azure data share resource id</span><span class="sxs-lookup"><span data-stu-id="c7a3f-122">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="c7a3f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a3f-123">CommonParameters</span></span>
<span data-ttu-id="c7a3f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a3f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a3f-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7a3f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a3f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a3f-126">INPUTS</span></span>

### <span data-ttu-id="c7a3f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c7a3f-127">System.String</span></span>

## <span data-ttu-id="c7a3f-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a3f-128">OUTPUTS</span></span>

### <span data-ttu-id="c7a3f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span><span class="sxs-lookup"><span data-stu-id="c7a3f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSourceDataSet</span></span>

## <span data-ttu-id="c7a3f-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7a3f-130">NOTES</span></span>

## <span data-ttu-id="c7a3f-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7a3f-131">RELATED LINKS</span></span>
