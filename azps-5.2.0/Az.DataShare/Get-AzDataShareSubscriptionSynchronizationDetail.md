---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronizationDetail.md
ms.openlocfilehash: 49917b7d9719e682060c8a3cf24c30bbb9141874
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391175"
---
# <span data-ttu-id="26c6c-101">Get-AzDataShareSubscriptionSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="26c6c-101">Get-AzDataShareSubscriptionSynchronizationDetail</span></span>

## <span data-ttu-id="26c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="26c6c-103">Сведения о синхронизации подписки для совместной использования.</span><span class="sxs-lookup"><span data-stu-id="26c6c-103">Gets information about synchonization details for share subscription.</span></span>

## <span data-ttu-id="26c6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26c6c-104">SYNTAX</span></span>

### <span data-ttu-id="26c6c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26c6c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="26c6c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26c6c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26c6c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="26c6c-108">Cmdlet **Get-AzDataShareSubscriptionSynchronizationDetail** предоставляет подробные сведения о синхронизации, начатой для подписки на доступ.</span><span class="sxs-lookup"><span data-stu-id="26c6c-108">The **Get-AzDataShareSubscriptionSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share subscription.</span></span>

## <span data-ttu-id="26c6c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26c6c-109">EXAMPLES</span></span>

### <span data-ttu-id="26c6c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26c6c-110">Example 1</span></span>
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

<span data-ttu-id="26c6c-111">Эта команда содержит сведения о синхронизации, инициализированной для share subscription AdsShareSubscription, в учетной записи обмена данными WikiAds.</span><span class="sxs-lookup"><span data-stu-id="26c6c-111">This command provides information about synchronization initiated for share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="26c6c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26c6c-112">PARAMETERS</span></span>

### <span data-ttu-id="26c6c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26c6c-113">-AccountName</span></span>
<span data-ttu-id="26c6c-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="26c6c-114">Azure data share account name</span></span>

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

### <span data-ttu-id="26c6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26c6c-115">-DefaultProfile</span></span>
<span data-ttu-id="26c6c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26c6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26c6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26c6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="26c6c-118">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="26c6c-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="26c6c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26c6c-119">-ResourceId</span></span>
<span data-ttu-id="26c6c-120">Azure Data Share Resource id</span><span class="sxs-lookup"><span data-stu-id="26c6c-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="26c6c-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="26c6c-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="26c6c-122">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="26c6c-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="26c6c-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="26c6c-123">-SynchronizationId</span></span>
<span data-ttu-id="26c6c-124">Synchronization id of share subscription synchronization</span><span class="sxs-lookup"><span data-stu-id="26c6c-124">Synchronization id of share subscription synchronization</span></span>

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

### <span data-ttu-id="26c6c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26c6c-125">CommonParameters</span></span>
<span data-ttu-id="26c6c-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26c6c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26c6c-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26c6c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26c6c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26c6c-128">INPUTS</span></span>

### <span data-ttu-id="26c6c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="26c6c-129">System.String</span></span>

## <span data-ttu-id="26c6c-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26c6c-130">OUTPUTS</span></span>

### <span data-ttu-id="26c6c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="26c6c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="26c6c-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26c6c-132">NOTES</span></span>

## <span data-ttu-id="26c6c-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26c6c-133">RELATED LINKS</span></span>
