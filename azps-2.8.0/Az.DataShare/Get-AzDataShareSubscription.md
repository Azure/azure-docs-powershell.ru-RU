---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscription.md
ms.openlocfilehash: 23553e939256b9124369afd79db29a50802dc6cf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721201"
---
# <span data-ttu-id="da098-101">Get-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="da098-101">Get-AzDataShareSubscription</span></span>

## <span data-ttu-id="da098-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da098-102">SYNOPSIS</span></span>
<span data-ttu-id="da098-103">Получение сведений об общем доступе к подписке в учетной записи общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="da098-103">Gets information about share subscription in data share account.</span></span>

## <span data-ttu-id="da098-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da098-104">SYNTAX</span></span>

### <span data-ttu-id="da098-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da098-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da098-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="da098-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscription -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da098-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da098-107">DESCRIPTION</span></span>
<span data-ttu-id="da098-108">Командлет **Get-AzDataShareSubscription** предоставляет сведения о совместном доступе к подписке в учетной записи для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="da098-108">The **Get-AzDataShareSubscription** cmdlet provides information about share subscription in a data share account.</span></span> <span data-ttu-id="da098-109">Если предоставлено имя для доступа к подписке, командлет выдает сведения о конкретной подписке на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="da098-109">If share subscription name is provided, the cmdlet gives information about the particular share subscription.</span></span> <span data-ttu-id="da098-110">В противном случае командлет выводит список подписок на общий доступ в учетной записи для общего доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="da098-110">Otherwise, the cmdlet provides a list of share subscriptions in the data share account.</span></span>

## <span data-ttu-id="da098-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da098-111">EXAMPLES</span></span>

### <span data-ttu-id="da098-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="da098-112">Example 1</span></span>
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

<span data-ttu-id="da098-113">Эта команда предоставляет сведения о том, AdsShareSubscription на общий доступ к подписке в WikiAds учетной записи данных.</span><span class="sxs-lookup"><span data-stu-id="da098-113">This command provides information about share subscription AdsShareSubscription in data share account WikiAds.</span></span>

## <span data-ttu-id="da098-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da098-114">PARAMETERS</span></span>

### <span data-ttu-id="da098-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="da098-115">-AccountName</span></span>
<span data-ttu-id="da098-116">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="da098-116">Azure data share account name</span></span>

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

### <span data-ttu-id="da098-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da098-117">-DefaultProfile</span></span>
<span data-ttu-id="da098-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da098-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da098-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da098-119">-Name</span></span>
<span data-ttu-id="da098-120">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="da098-120">Azure data share subscription name</span></span>

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

### <span data-ttu-id="da098-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da098-121">-ResourceGroupName</span></span>
<span data-ttu-id="da098-122">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="da098-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="da098-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da098-123">-ResourceId</span></span>
<span data-ttu-id="da098-124">Идентификатор ресурса для подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="da098-124">The resource id of the azure data share subscription</span></span>

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

### <span data-ttu-id="da098-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da098-125">CommonParameters</span></span>
<span data-ttu-id="da098-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da098-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da098-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da098-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da098-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da098-128">INPUTS</span></span>

### <span data-ttu-id="da098-129">System. String</span><span class="sxs-lookup"><span data-stu-id="da098-129">System.String</span></span>

## <span data-ttu-id="da098-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da098-130">OUTPUTS</span></span>

### <span data-ttu-id="da098-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="da098-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscription</span></span>

## <span data-ttu-id="da098-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="da098-132">NOTES</span></span>

## <span data-ttu-id="da098-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da098-133">RELATED LINKS</span></span>
