---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: dfe0710be411f3739a888cd58d3c0a6ec5353cab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721194"
---
# <span data-ttu-id="9fe39-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9fe39-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="9fe39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fe39-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe39-103">Получение сведений о synchonization для предоставления общего доступа к подписке.</span><span class="sxs-lookup"><span data-stu-id="9fe39-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="9fe39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fe39-104">SYNTAX</span></span>

### <span data-ttu-id="9fe39-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fe39-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9fe39-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fe39-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fe39-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fe39-107">DESCRIPTION</span></span>
<span data-ttu-id="9fe39-108">Командлет **Get-AzDataShareSubscriptionSynchronizationDetail** содержит подробные сведения о синхронизации, инициированной для подписки на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="9fe39-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="9fe39-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fe39-109">EXAMPLES</span></span>

### <span data-ttu-id="9fe39-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9fe39-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareSubscriptionName "AdsShareSubscription" -SynchronizationId "a6ee5c8d-0ce0-485e-b2f2-966b187dc6c7"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="9fe39-111">Эта команда предоставляет сведения о синхронизации, инициированной AdsShareSubscription, для предоставления общего доступа к подписке в разделе "учетная запись данных WikiAds.</span><span class="sxs-lookup"><span data-stu-id="9fe39-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="9fe39-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fe39-112">PARAMETERS</span></span>

### <span data-ttu-id="9fe39-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9fe39-113">-AccountName</span></span>
<span data-ttu-id="9fe39-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="9fe39-114">Azure data share account name</span></span>

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

### <span data-ttu-id="9fe39-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe39-115">-DefaultProfile</span></span>
<span data-ttu-id="9fe39-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fe39-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fe39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe39-117">-ResourceGroupName</span></span>
<span data-ttu-id="9fe39-118">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="9fe39-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="9fe39-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9fe39-119">-ResourceId</span></span>
<span data-ttu-id="9fe39-120">Идентификатор ресурса подписки на Azure Data Share</span><span class="sxs-lookup"><span data-stu-id="9fe39-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="9fe39-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9fe39-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="9fe39-122">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="9fe39-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="9fe39-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="9fe39-123">-SynchronizationId</span></span>
<span data-ttu-id="9fe39-124">Идентификатор синхронизации для общего доступа к синхронизации подписки</span><span class="sxs-lookup"><span data-stu-id="9fe39-124">Synchronization id of share subscription synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fe39-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe39-125">CommonParameters</span></span>
<span data-ttu-id="9fe39-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fe39-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe39-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fe39-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe39-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fe39-128">INPUTS</span></span>

### <span data-ttu-id="9fe39-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9fe39-129">System.String</span></span>

## <span data-ttu-id="9fe39-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fe39-130">OUTPUTS</span></span>

### <span data-ttu-id="9fe39-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="9fe39-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="9fe39-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fe39-132">NOTES</span></span>

## <span data-ttu-id="9fe39-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fe39-133">RELATED LINKS</span></span>
