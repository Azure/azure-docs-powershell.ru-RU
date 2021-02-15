---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232132"
---
# <span data-ttu-id="2ad58-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="2ad58-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="2ad58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ad58-102">SYNOPSIS</span></span>
<span data-ttu-id="2ad58-103">Сведения об совместном использования подписки в учетной записи обмена данными.</span><span class="sxs-lookup"><span data-stu-id="2ad58-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="2ad58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ad58-104">SYNTAX</span></span>

### <span data-ttu-id="2ad58-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ad58-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ad58-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ad58-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ad58-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ad58-107">DESCRIPTION</span></span>
<span data-ttu-id="2ad58-108">Для получения сведений о подписке в учетной записи обмена данными можно получить сведения о подписке на **Get-AzDataShareSubscription.**</span><span class="sxs-lookup"><span data-stu-id="2ad58-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="2ad58-109">Если предоставлено имя подписки для совместной подписки, с ее можно получить сведения об определенной подписке.</span><span class="sxs-lookup"><span data-stu-id="2ad58-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="2ad58-110">В противном случае с его учетной записью можно поделиться подписками.</span><span class="sxs-lookup"><span data-stu-id="2ad58-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="2ad58-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ad58-111">EXAMPLES</span></span>

### <span data-ttu-id="2ad58-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ad58-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription"

CreatedAt               : 7/9/2019 12:32:53 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 0c14f5b6-0e22-49ab-8043-d6edad51db13
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Test
ShareDescription        : Ads description
ShareTerms              : Ads terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="2ad58-113">Эта команда предоставляет сведения о совместном доступе к подписке AdsShareSubscription в учетной записи обмена данными WikiAds.</span><span class="sxs-lookup"><span data-stu-id="2ad58-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="2ad58-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ad58-114">PARAMETERS</span></span>

### <span data-ttu-id="2ad58-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2ad58-115">-AccountName</span></span>
<span data-ttu-id="2ad58-116">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2ad58-116">Azure data share account name</span></span>

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

### <span data-ttu-id="2ad58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ad58-117">-DefaultProfile</span></span>
<span data-ttu-id="2ad58-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ad58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ad58-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2ad58-119">-Name</span></span>
<span data-ttu-id="2ad58-120">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2ad58-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="2ad58-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ad58-121">-ResourceGroupName</span></span>
<span data-ttu-id="2ad58-122">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="2ad58-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="2ad58-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ad58-123">-ResourceId</span></span>
<span data-ttu-id="2ad58-124">ИД ресурса подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="2ad58-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="2ad58-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ad58-125">CommonParameters</span></span>
<span data-ttu-id="2ad58-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ad58-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ad58-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ad58-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ad58-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ad58-128">INPUTS</span></span>

### <span data-ttu-id="2ad58-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2ad58-129">System.String</span></span>

## <span data-ttu-id="2ad58-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ad58-130">OUTPUTS</span></span>

### <span data-ttu-id="2ad58-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="2ad58-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="2ad58-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ad58-132">NOTES</span></span>

## <span data-ttu-id="2ad58-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ad58-133">RELATED LINKS</span></span>
