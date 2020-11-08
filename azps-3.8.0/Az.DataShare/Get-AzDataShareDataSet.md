---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedataset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSet.md
ms.openlocfilehash: 73272c2afd0b3d8ef62a522f2e67f04854c2232e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065435"
---
# <span data-ttu-id="a907c-101">Get-AzDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a907c-101">Get-AzDataShareDataSet</span></span>

## <span data-ttu-id="a907c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a907c-102">SYNOPSIS</span></span>
<span data-ttu-id="a907c-103">Получение сведений о наборах данных в службе общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-103">Gets information about Data Sets in Azure data share.</span></span>

## <span data-ttu-id="a907c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a907c-104">SYNTAX</span></span>

### <span data-ttu-id="a907c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a907c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSet -ResourceGroupName <String> -AccountName <String> -ShareName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a907c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a907c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSet -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a907c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a907c-107">DESCRIPTION</span></span>
<span data-ttu-id="a907c-108">Командлет **Get-AzDataShareDataSet** получает сведения о наборах данных, добавленных в общий доступ в учетной записи для общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-108">The **Get-AzDataShareDataSet** cmdlet gets information about data sets added in a share in an Azure data share account.</span></span> <span data-ttu-id="a907c-109">Если указать имя набора данных, этот командлет получает сведения о наборе данных.</span><span class="sxs-lookup"><span data-stu-id="a907c-109">If you specify the name of data set, this cmdlet gets information about the data set.</span></span> <span data-ttu-id="a907c-110">Если имя не задано, этот командлет получает сведения обо всех наборах данных в общем доступе. Думаю</span><span class="sxs-lookup"><span data-stu-id="a907c-110">If you do not specify a name, this cmdlet gets information about all the data sets in a share.I</span></span>

## <span data-ttu-id="a907c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a907c-111">EXAMPLES</span></span>

### <span data-ttu-id="a907c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a907c-112">Example 1</span></span>
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

<span data-ttu-id="a907c-113">Эта команда отображает сведения о настройке AdsDataSet в общем доступе AdsShare в учетной записи общего доступа к данным в Azure WikiAdsAccount и группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a907c-113">This command displays information about data set AdsDataSet in share AdsShare in Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="a907c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a907c-114">PARAMETERS</span></span>

### <span data-ttu-id="a907c-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a907c-115">-AccountName</span></span>
<span data-ttu-id="a907c-116">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-116">Azure data share account name.</span></span>

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

### <span data-ttu-id="a907c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a907c-117">-DefaultProfile</span></span>
<span data-ttu-id="a907c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a907c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a907c-119">-Name</span></span>
<span data-ttu-id="a907c-120">Имя Set данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-120">Azure data set name.</span></span>

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

### <span data-ttu-id="a907c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a907c-121">-ResourceGroupName</span></span>
<span data-ttu-id="a907c-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-122">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="a907c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a907c-123">-ResourceId</span></span>
<span data-ttu-id="a907c-124">Идентификатор ресурса для набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-124">The resource id of the azure data set.</span></span>

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

### <span data-ttu-id="a907c-125">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="a907c-125">-ShareName</span></span>
<span data-ttu-id="a907c-126">Имя общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="a907c-126">Azure data share name.</span></span>

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

### <span data-ttu-id="a907c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a907c-127">CommonParameters</span></span>
<span data-ttu-id="a907c-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a907c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a907c-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a907c-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a907c-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a907c-130">INPUTS</span></span>

### <span data-ttu-id="a907c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a907c-131">System.String</span></span>

## <span data-ttu-id="a907c-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a907c-132">OUTPUTS</span></span>

### <span data-ttu-id="a907c-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span><span class="sxs-lookup"><span data-stu-id="a907c-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSet</span></span>

## <span data-ttu-id="a907c-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a907c-134">NOTES</span></span>

## <span data-ttu-id="a907c-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a907c-135">RELATED LINKS</span></span>
