---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230609"
---
# <span data-ttu-id="b6be4-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b6be4-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b6be4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6be4-102">SYNOPSIS</span></span>
<span data-ttu-id="b6be4-103">Сведения о синхронизации выполняется в подписке на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="b6be4-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="b6be4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b6be4-104">SYNTAX</span></span>

### <span data-ttu-id="b6be4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b6be4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6be4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6be4-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6be4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6be4-107">DESCRIPTION</span></span>
<span data-ttu-id="b6be4-108">**Cmdlet Get-AzDataShareSubscriptionSynchronionSynchronization** обеспечивает оповещение обо всех действиях синхронизации, которые выполняется в рамках подписки на объедительный доступ в учетной записи обмена данными для потребителей.</span><span class="sxs-lookup"><span data-stu-id="b6be4-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="b6be4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b6be4-109">EXAMPLES</span></span>

### <span data-ttu-id="b6be4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b6be4-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="b6be4-111">Эта команда содержит сведения обо всех программах синхронизации для share subscription AdsShareSubscription в учетной записи обмена данными WikiAds.</span><span class="sxs-lookup"><span data-stu-id="b6be4-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="b6be4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6be4-112">PARAMETERS</span></span>

### <span data-ttu-id="b6be4-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b6be4-113">-AccountName</span></span>
<span data-ttu-id="b6be4-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="b6be4-114">Azure data share account name</span></span>

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

### <span data-ttu-id="b6be4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6be4-115">-DefaultProfile</span></span>
<span data-ttu-id="b6be4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6be4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6be4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6be4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b6be4-118">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="b6be4-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="b6be4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6be4-119">-ResourceId</span></span>
<span data-ttu-id="b6be4-120">Azure data share resource id</span><span class="sxs-lookup"><span data-stu-id="b6be4-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="b6be4-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="b6be4-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="b6be4-122">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="b6be4-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="b6be4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6be4-123">CommonParameters</span></span>
<span data-ttu-id="b6be4-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6be4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6be4-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6be4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6be4-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b6be4-126">INPUTS</span></span>

### <span data-ttu-id="b6be4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="b6be4-127">System.String</span></span>

## <span data-ttu-id="b6be4-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b6be4-128">OUTPUTS</span></span>

### <span data-ttu-id="b6be4-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="b6be4-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="b6be4-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b6be4-130">NOTES</span></span>

## <span data-ttu-id="b6be4-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6be4-131">RELATED LINKS</span></span>
