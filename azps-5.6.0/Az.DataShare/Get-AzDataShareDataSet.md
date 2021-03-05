---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: d0bf60bbfd13474270391afd6f01bc9ec8130b62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991388"
---
# <span data-ttu-id="4316d-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4316d-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="4316d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4316d-102">SYNOPSIS</span></span>
<span data-ttu-id="4316d-103">Получает сведения о наборах данных в области обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="4316d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4316d-104">SYNTAX</span></span>

### <span data-ttu-id="4316d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4316d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4316d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4316d-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4316d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4316d-107">DESCRIPTION</span></span>
<span data-ttu-id="4316d-108">С **его учетной** записью можно получить сведения о наборах данных, добавленных в обет в учетной записи azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="4316d-109">При указании имени набора данных этот cmdlet получает сведения о наборе данных.</span><span class="sxs-lookup"><span data-stu-id="4316d-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="4316d-110">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в области. I</span><span class="sxs-lookup"><span data-stu-id="4316d-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="4316d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4316d-111">EXAMPLES</span></span>

### <span data-ttu-id="4316d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4316d-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareDataSet -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "AdsDataSet"
ContainerName  : AdsContainer
DataSetId      : d2411889-5357-4ca8-8d65-9363e46ef2ed
ResourceGroup  : ADS
SubscriptionId : 1834da9b-787a-44f6-ae81-60707ab8c957
StorageAccount : AdsStorage
Id             : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/shelltest/shares/share4/dataSets/AdsDataSet
Name           : AdsDataSet
Type           : Microsoft.DataShare/DataSets
```

<span data-ttu-id="4316d-113">Эта команда отображает сведения о наборе данных AdsDataSet в share AdsShare в Azure data account Share WikiAdsAccount и группа ресурсов ADS.</span><span class="sxs-lookup"><span data-stu-id="4316d-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="4316d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4316d-114">PARAMETERS</span></span>

### <span data-ttu-id="4316d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4316d-115">-AccountName</span></span>
<span data-ttu-id="4316d-116">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="4316d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4316d-117">-DefaultProfile</span></span>
<span data-ttu-id="4316d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4316d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4316d-119">-Name</span></span>
<span data-ttu-id="4316d-120">Имя набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-120">Azure data set name.</span></span>

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

### <span data-ttu-id="4316d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4316d-121">-ResourceGroupName</span></span>
<span data-ttu-id="4316d-122">Имя группы ресурсов учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="4316d-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="4316d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4316d-123">-ResourceId</span></span>
<span data-ttu-id="4316d-124">ИД ресурса для набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="4316d-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4316d-125">-ShareName</span></span>
<span data-ttu-id="4316d-126">Имя обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="4316d-126">Azure data share name.</span></span>

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

### <span data-ttu-id="4316d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4316d-127">CommonParameters</span></span>
<span data-ttu-id="4316d-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4316d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4316d-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4316d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4316d-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4316d-130">INPUTS</span></span>

### <span data-ttu-id="4316d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="4316d-131">System.String</span></span>

## <span data-ttu-id="4316d-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4316d-132">OUTPUTS</span></span>

### <span data-ttu-id="4316d-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="4316d-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="4316d-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4316d-134">NOTES</span></span>

## <span data-ttu-id="4316d-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4316d-135">RELATED LINKS</span></span>
