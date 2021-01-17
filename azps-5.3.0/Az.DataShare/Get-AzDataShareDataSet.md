---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 7e10c24c62a05650fd618793cb8de088237357ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420780"
---
# <span data-ttu-id="8e699-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8e699-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="8e699-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e699-102">SYNOPSIS</span></span>
<span data-ttu-id="8e699-103">Получает сведения о наборах данных в области обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="8e699-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="8e699-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e699-104">SYNTAX</span></span>

### <span data-ttu-id="8e699-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e699-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e699-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e699-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e699-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e699-107">DESCRIPTION</span></span>
<span data-ttu-id="8e699-108">Чтобы получить сведения о наборах данных, добавленных в обет в учетной записи azure, можно получить с его учетной записью **Get-AzDataShareDataSet.**</span><span class="sxs-lookup"><span data-stu-id="8e699-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="8e699-109">Если указать имя набора данных, этот cmdlet получит сведения о наборе данных.</span><span class="sxs-lookup"><span data-stu-id="8e699-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="8e699-110">Если имя не указано, этот cmdlet получает сведения обо всех наборах данных в области. I</span><span class="sxs-lookup"><span data-stu-id="8e699-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="8e699-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e699-111">EXAMPLES</span></span>

### <span data-ttu-id="8e699-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e699-112">Example 1</span></span>
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

<span data-ttu-id="8e699-113">Эта команда отображает сведения о наборе данных AdsDataSet в share AdsShare в Azure data account Share WikiAdsAccount и группа ресурсов ADS.</span><span class="sxs-lookup"><span data-stu-id="8e699-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="8e699-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e699-114">PARAMETERS</span></span>

### <span data-ttu-id="8e699-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e699-115">-AccountName</span></span>
<span data-ttu-id="8e699-116">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="8e699-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="8e699-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e699-117">-DefaultProfile</span></span>
<span data-ttu-id="8e699-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e699-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e699-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8e699-119">-Name</span></span>
<span data-ttu-id="8e699-120">Имя набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8e699-120">Azure data set name.</span></span>

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

### <span data-ttu-id="8e699-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e699-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e699-122">Имя группы ресурсов учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="8e699-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="8e699-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e699-123">-ResourceId</span></span>
<span data-ttu-id="8e699-124">ИД ресурса для набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="8e699-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="8e699-125">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8e699-125">-ShareName</span></span>
<span data-ttu-id="8e699-126">Имя обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="8e699-126">Azure data share name.</span></span>

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

### <span data-ttu-id="8e699-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e699-127">CommonParameters</span></span>
<span data-ttu-id="8e699-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e699-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e699-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e699-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e699-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e699-130">INPUTS</span></span>

### <span data-ttu-id="8e699-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8e699-131">System.String</span></span>

## <span data-ttu-id="8e699-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e699-132">OUTPUTS</span></span>

### <span data-ttu-id="8e699-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="8e699-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="8e699-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e699-134">NOTES</span></span>

## <span data-ttu-id="8e699-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e699-135">RELATED LINKS</span></span>
