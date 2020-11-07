---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharedatasetmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareDataSetMapping.md
ms.openlocfilehash: d19825fea43e8fc029e960a513d1c2ad306a8406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721212"
---
# <span data-ttu-id="9cbcf-101">Get-AzDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="9cbcf-101">Get-AzDataShareDataSetMapping</span></span>

## <span data-ttu-id="9cbcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9cbcf-102">SYNOPSIS</span></span>
<span data-ttu-id="9cbcf-103">Получение сведений о сопоставлениях наборов данных в подписке на общий доступ</span><span class="sxs-lookup"><span data-stu-id="9cbcf-103">Gets information about dataset mappings in share subscription</span></span>

## <span data-ttu-id="9cbcf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9cbcf-104">SYNTAX</span></span>

### <span data-ttu-id="9cbcf-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9cbcf-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareDataSetMapping -ResourceGroupName <String> -AccountName <String> -ShareSubscriptionName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9cbcf-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cbcf-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareDataSetMapping -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9cbcf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cbcf-107">DESCRIPTION</span></span>
<span data-ttu-id="9cbcf-108">Командлет **Get-AzDataShareDataSetMapping** получает сведения о конкретном сопоставлении набора данных, если указано его имя.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-108">The **Get-AzDataShareDataSetMapping** cmdlet gets information about a particular dataset mapping if the name is specified.</span></span> <span data-ttu-id="9cbcf-109">В противном случае он получает сведения обо всех сопоставлениях наборов данных в подписке на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-109">Otherwise, it gets information about all the dataset mappings in a share subscription.</span></span> 

## <span data-ttu-id="9cbcf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9cbcf-110">EXAMPLES</span></span>

### <span data-ttu-id="9cbcf-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9cbcf-111">Example 1</span></span>
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

 <span data-ttu-id="9cbcf-112">Эта команда отображает сведения обо всех сопоставлениях наборов данных в подписке на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-112">This command displays information about all dataset mappings in the share subscription.</span></span>

## <span data-ttu-id="9cbcf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9cbcf-113">PARAMETERS</span></span>

### <span data-ttu-id="9cbcf-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9cbcf-114">-AccountName</span></span>
<span data-ttu-id="9cbcf-115">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-115">Azure data share account name.</span></span>

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

### <span data-ttu-id="9cbcf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cbcf-116">-DefaultProfile</span></span>
<span data-ttu-id="9cbcf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cbcf-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9cbcf-118">-Name</span></span>
<span data-ttu-id="9cbcf-119">Имя сопоставления для Set данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-119">Azure data set mapping name.</span></span>

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

### <span data-ttu-id="9cbcf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cbcf-120">-ResourceGroupName</span></span>
<span data-ttu-id="9cbcf-121">Имя группы ресурсов для учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-121">The resource group name of azure data share account.</span></span>

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

### <span data-ttu-id="9cbcf-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cbcf-122">-ResourceId</span></span>
<span data-ttu-id="9cbcf-123">Идентификатор ресурса для сопоставления набора данных Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-123">The resource id of the azure data set mapping.</span></span>

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

### <span data-ttu-id="9cbcf-124">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9cbcf-124">-ShareSubscriptionName</span></span>
<span data-ttu-id="9cbcf-125">Имя подписки на общий доступ к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-125">Azure data share subscription name.</span></span>

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

### <span data-ttu-id="9cbcf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cbcf-126">CommonParameters</span></span>
<span data-ttu-id="9cbcf-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9cbcf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cbcf-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cbcf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cbcf-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9cbcf-129">INPUTS</span></span>

### <span data-ttu-id="9cbcf-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9cbcf-130">System.String</span></span>

## <span data-ttu-id="9cbcf-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9cbcf-131">OUTPUTS</span></span>

### <span data-ttu-id="9cbcf-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span><span class="sxs-lookup"><span data-stu-id="9cbcf-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareDataSetMapping</span></span>

## <span data-ttu-id="9cbcf-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9cbcf-133">NOTES</span></span>

## <span data-ttu-id="9cbcf-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9cbcf-134">RELATED LINKS</span></span>
