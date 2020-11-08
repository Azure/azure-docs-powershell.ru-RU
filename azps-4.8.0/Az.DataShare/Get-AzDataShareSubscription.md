---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 910afff2a9c5524d452c5a5f4bec48a3f18359a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244569"
---
# <span data-ttu-id="129a0-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="129a0-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="129a0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="129a0-102">SYNOPSIS</span></span>
<span data-ttu-id="129a0-103">Получение сведений об общем доступе к подписке в учетной записи общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="129a0-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="129a0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="129a0-104">SYNTAX</span></span>

### <span data-ttu-id="129a0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="129a0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="129a0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="129a0-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="129a0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="129a0-107">DESCRIPTION</span></span>
<span data-ttu-id="129a0-108">Командлет **Get-AzDataShareSubscription** предоставляет сведения о совместном доступе к подписке в учетной записи для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="129a0-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="129a0-109">Если предоставлено имя для доступа к подписке, командлет выдает сведения о конкретной подписке на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="129a0-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="129a0-110">В противном случае командлет выводит список подписок на общий доступ в учетной записи для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="129a0-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="129a0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="129a0-111">EXAMPLES</span></span>

### <span data-ttu-id="129a0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="129a0-112">Example 1</span></span>
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

<span data-ttu-id="129a0-113">Эта команда предоставляет сведения о том, AdsShareSubscription на общий доступ к подписке в WikiAds учетной записи данных.</span><span class="sxs-lookup"><span data-stu-id="129a0-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="129a0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="129a0-114">PARAMETERS</span></span>

### <span data-ttu-id="129a0-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="129a0-115">-AccountName</span></span>
<span data-ttu-id="129a0-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="129a0-116">Azure data share account name</span></span>

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

### <span data-ttu-id="129a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="129a0-117">-DefaultProfile</span></span>
<span data-ttu-id="129a0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="129a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="129a0-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="129a0-119">-Name</span></span>
<span data-ttu-id="129a0-120">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="129a0-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="129a0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="129a0-121">-ResourceGroupName</span></span>
<span data-ttu-id="129a0-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="129a0-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="129a0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="129a0-123">-ResourceId</span></span>
<span data-ttu-id="129a0-124">Идентификатор ресурса для подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="129a0-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="129a0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="129a0-125">CommonParameters</span></span>
<span data-ttu-id="129a0-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="129a0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="129a0-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="129a0-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="129a0-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="129a0-128">INPUTS</span></span>

### <span data-ttu-id="129a0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="129a0-129">System.String</span></span>

## <span data-ttu-id="129a0-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="129a0-130">OUTPUTS</span></span>

### <span data-ttu-id="129a0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="129a0-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="129a0-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="129a0-132">NOTES</span></span>

## <span data-ttu-id="129a0-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="129a0-133">RELATED LINKS</span></span>
