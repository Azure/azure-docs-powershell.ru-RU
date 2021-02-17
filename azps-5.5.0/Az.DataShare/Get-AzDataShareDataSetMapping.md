---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: 99f80aa920a402867b6385a3b4ef7ac118838f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232865"
---
# <span data-ttu-id="ed715-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ed715-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="ed715-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed715-102">SYNOPSIS</span></span>
<span data-ttu-id="ed715-103">Сведения о сопоставлениях наборов данных в подписке на совместное использования</span><span class="sxs-lookup"><span data-stu-id="ed715-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="ed715-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed715-104">SYNTAX</span></span>

### <span data-ttu-id="ed715-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed715-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed715-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed715-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed715-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed715-107">DESCRIPTION</span></span>
<span data-ttu-id="ed715-108">При указании имени cmdlet **Get-AzDataShareDataSetMapping** получает сведения об определенном сопоставлении наборов данных.</span><span class="sxs-lookup"><span data-stu-id="ed715-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="ed715-109">В противном случае он получает сведения обо всех сопоставлениях для наборов данных в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="ed715-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="ed715-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed715-110">EXAMPLES</span></span>

### <span data-ttu-id="ed715-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ed715-111">Example 1</span></span>
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

 <span data-ttu-id="ed715-112">Эта команда отображает сведения обо всех сопоставлениях наборов данных в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="ed715-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="ed715-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed715-113">PARAMETERS</span></span>

### <span data-ttu-id="ed715-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ed715-114">-AccountName</span></span>
<span data-ttu-id="ed715-115">Имя учетной записи для обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="ed715-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="ed715-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed715-116">-DefaultProfile</span></span>
<span data-ttu-id="ed715-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed715-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed715-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ed715-118">-Name</span></span>
<span data-ttu-id="ed715-119">Имя сопоставления набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ed715-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="ed715-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed715-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed715-121">Имя группы ресурсов учетной записи azure data share.</span><span class="sxs-lookup"><span data-stu-id="ed715-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="ed715-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed715-122">-ResourceId</span></span>
<span data-ttu-id="ed715-123">ИД ресурса сопоставления набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="ed715-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="ed715-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="ed715-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="ed715-125">Имя подписки на службу обмена данными Azure.</span><span class="sxs-lookup"><span data-stu-id="ed715-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="ed715-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed715-126">CommonParameters</span></span>
<span data-ttu-id="ed715-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed715-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed715-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed715-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed715-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed715-129">INPUTS</span></span>

### <span data-ttu-id="ed715-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ed715-130">System.String</span></span>

## <span data-ttu-id="ed715-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed715-131">OUTPUTS</span></span>

### <span data-ttu-id="ed715-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="ed715-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="ed715-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed715-133">NOTES</span></span>

## <span data-ttu-id="ed715-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed715-134">RELATED LINKS</span></span>
