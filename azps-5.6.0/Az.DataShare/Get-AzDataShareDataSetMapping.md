---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: a25efdd89e99e52115ade8354d7e96f8ee7972ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991385"
---
# <span data-ttu-id="1b17d-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="1b17d-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="1b17d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b17d-102">SYNOPSIS</span></span>
<span data-ttu-id="1b17d-103">Сведения о сопоставлениях наборов данных в подписке на совместное использования</span><span class="sxs-lookup"><span data-stu-id="1b17d-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="1b17d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b17d-104">SYNTAX</span></span>

### <span data-ttu-id="1b17d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b17d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b17d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b17d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b17d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b17d-107">DESCRIPTION</span></span>
<span data-ttu-id="1b17d-108">При указании имени с его названием можно получить сведения о сопоставлении с набором данных **Get-AzDataShareDataSetMapping.**</span><span class="sxs-lookup"><span data-stu-id="1b17d-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="1b17d-109">В противном случае он получает сведения обо всех сопоставлениях для наборов данных в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="1b17d-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="1b17d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b17d-110">EXAMPLES</span></span>

### <span data-ttu-id="1b17d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b17d-111">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSetMapping -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareSubscriptionName "WikiADS"

ContainerName        : testing
Prefix               : providercontainer
DataSetId            : 372899d4-5e67-4c85-bc60-21168b484424
ResourceGroup        : ADS
SubscriptionId       : 4834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount       : storageaccount
DataSetMappingStatus : Ok
Id                   : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shareSubscriptions/WikiADS/dataSetMappings/dsm
Name                 : dsm
Type                 : Microsoft.DataShare/DataSetMappings
```

 <span data-ttu-id="1b17d-112">Эта команда отображает сведения обо всех сопоставлениях наборов данных в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="1b17d-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="1b17d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b17d-113">PARAMETERS</span></span>

### <span data-ttu-id="1b17d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1b17d-114">-AccountName</span></span>
<span data-ttu-id="1b17d-115">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="1b17d-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="1b17d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b17d-116">-DefaultProfile</span></span>
<span data-ttu-id="1b17d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b17d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b17d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1b17d-118">-Name</span></span>
<span data-ttu-id="1b17d-119">Имя сопоставления набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1b17d-119">Azure data set mapping name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b17d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b17d-120">-ResourceGroupName</span></span>
<span data-ttu-id="1b17d-121">Имя группы ресурсов учетной записи обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="1b17d-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="1b17d-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b17d-122">-ResourceId</span></span>
<span data-ttu-id="1b17d-123">ИД ресурса сопоставления набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="1b17d-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="1b17d-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="1b17d-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="1b17d-125">Имя подписки на службу обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="1b17d-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="1b17d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b17d-126">CommonParameters</span></span>
<span data-ttu-id="1b17d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b17d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b17d-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b17d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b17d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b17d-129">INPUTS</span></span>

### <span data-ttu-id="1b17d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1b17d-130">System.String</span></span>

## <span data-ttu-id="1b17d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b17d-131">OUTPUTS</span></span>

### <span data-ttu-id="1b17d-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="1b17d-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="1b17d-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b17d-133">NOTES</span></span>

## <span data-ttu-id="1b17d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b17d-134">RELATED LINKS</span></span>
