---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211124"
---
# <span data-ttu-id="2ab93-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="2ab93-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="2ab93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ab93-102">SYNOPSIS</span></span>
<span data-ttu-id="2ab93-103">Получает сведения о наборах данных в области обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab93-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="2ab93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ab93-104">SYNTAX</span></span>

### <span data-ttu-id="2ab93-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ab93-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ab93-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ab93-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ab93-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ab93-107">DESCRIPTION</span></span>
<span data-ttu-id="2ab93-108">Чтобы получить сведения о наборах данных, добавленных в обет в учетной записи azure, можно получить с его учетной записью **Get-AzDataShareDataSet.**</span><span class="sxs-lookup"><span data-stu-id="2ab93-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="2ab93-109">Если указать имя набора данных, этот cmdlet получит сведения о наборе данных.</span><span class="sxs-lookup"><span data-stu-id="2ab93-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="2ab93-110">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в области. I</span><span class="sxs-lookup"><span data-stu-id="2ab93-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="2ab93-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ab93-111">EXAMPLES</span></span>

### <span data-ttu-id="2ab93-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ab93-112">Example 1</span></span>
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

<span data-ttu-id="2ab93-113">Эта команда отображает сведения о наборе данных AdsDataSet в share AdsShare в Azure data account Share WikiAdsAccount и группа ресурсов ADS.</span><span class="sxs-lookup"><span data-stu-id="2ab93-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="2ab93-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ab93-114">PARAMETERS</span></span>

### <span data-ttu-id="2ab93-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ab93-115">-AccountName</span></span>
<span data-ttu-id="2ab93-116">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab93-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="2ab93-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ab93-117">-DefaultProfile</span></span>
<span data-ttu-id="2ab93-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab93-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ab93-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ab93-119">-Name</span></span>
<span data-ttu-id="2ab93-120">Имя набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab93-120">Azure data set name.</span></span>

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

### <span data-ttu-id="2ab93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ab93-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ab93-122">Имя группы ресурсов учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="2ab93-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="2ab93-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ab93-123">-ResourceId</span></span>
<span data-ttu-id="2ab93-124">ИД ресурса для набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab93-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="2ab93-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="2ab93-125">-ShareName</span></span>
<span data-ttu-id="2ab93-126">Имя обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="2ab93-126">Azure data share name.</span></span>

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

### <span data-ttu-id="2ab93-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ab93-127">CommonParameters</span></span>
<span data-ttu-id="2ab93-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ab93-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ab93-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ab93-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ab93-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ab93-130">INPUTS</span></span>

### <span data-ttu-id="2ab93-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2ab93-131">System.String</span></span>

## <span data-ttu-id="2ab93-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ab93-132">OUTPUTS</span></span>

### <span data-ttu-id="2ab93-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="2ab93-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="2ab93-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ab93-134">NOTES</span></span>

## <span data-ttu-id="2ab93-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ab93-135">RELATED LINKS</span></span>
