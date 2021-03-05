---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashareprovidersharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareProviderShareSubscription.md
ms.openlocfilehash: b28182a5593454b110b2fe4036b022a8d74c33d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012227"
---
# <span data-ttu-id="55ebc-101">Get-AzDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="55ebc-101">Get-AzDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="55ebc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="55ebc-103">Получает сведения о подписках для потребительского обмена на стороне поставщика.</span><span class="sxs-lookup"><span data-stu-id="55ebc-103">Gets information about consumer share subscriptions on provider side.</span></span>

## <span data-ttu-id="55ebc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="55ebc-104">SYNTAX</span></span>

### <span data-ttu-id="55ebc-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55ebc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareProviderShareSubscription -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-ShareSubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55ebc-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55ebc-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Get-AzDataShareProviderShareSubscription [-ShareSubscriptionId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55ebc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55ebc-107">DESCRIPTION</span></span>
<span data-ttu-id="55ebc-108">Для получения сведений о подписках на потребительские акции на стороне поставщика можно получить сведения о cmdlet **Get-AzDataShareProviderSubscription.**</span><span class="sxs-lookup"><span data-stu-id="55ebc-108">The **Get-AzDataShareProviderSubscription** cmdlet gets information about consumer share subscriptions on provider side.</span></span> <span data-ttu-id="55ebc-109">Если указать для него код, этот cmdlet получит сведения о подписке на share.</span><span class="sxs-lookup"><span data-stu-id="55ebc-109">If you specify the share subscrption id, this cmdlet gets information about the share subscription.</span></span> <span data-ttu-id="55ebc-110">Если не указать код подписки на совместное использования, этот cmdlet получит сведения обо всех связанных с ней подписках на потребительские акции.</span><span class="sxs-lookup"><span data-stu-id="55ebc-110">If you do not specify the share subscription id, this cmdlet gets information about all the consumer share subscriptions in associated with the share.</span></span>

## <span data-ttu-id="55ebc-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="55ebc-111">EXAMPLES</span></span>

### <span data-ttu-id="55ebc-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55ebc-112">Example 1</span></span>
```
PS C:\> Get-AzDataShareProviderShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -ShareSubscriptionId "/subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a"

Company                   : ADS Test
CreatedAt                 : 6/30/2019 12:42:12 AM
CreatedBy                 : adstest@microsoft.com
SharedAt                  : 6/30/2019 12:41:37 AM
SharedBy                  : adsprovider@microsoft.com
ShareSubscriptionObjectId : 505c3500-b2ff-46ab-96bf-50f5ec89d75a
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shares/AdsShare/shareSubscriptions/505c3500-b2ff-46ab-96bf-50f5ec89d75a
Name                      : AdsShareSubscription
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="55ebc-113">Эти команды предоставляют сведения о подписке на потребительский доступ, связанную с share AdsShare в учетной записи вики-центрах обмена данными.</span><span class="sxs-lookup"><span data-stu-id="55ebc-113">This commands provides information about consumer share subscription associated with share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="55ebc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="55ebc-114">PARAMETERS</span></span>

### <span data-ttu-id="55ebc-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="55ebc-115">-AccountName</span></span>
<span data-ttu-id="55ebc-116">Имя учетной записи Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="55ebc-116">Azure DataShare Account name.</span></span>

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

### <span data-ttu-id="55ebc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55ebc-117">-DefaultProfile</span></span>
<span data-ttu-id="55ebc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55ebc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55ebc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55ebc-119">-ResourceGroupName</span></span>
<span data-ttu-id="55ebc-120">Группа ресурсов учетной записи Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="55ebc-120">The resource group of the Azure DataShare Account.</span></span>

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

### <span data-ttu-id="55ebc-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55ebc-121">-ResourceId</span></span>
<span data-ttu-id="55ebc-122">ИД ресурса для ресурса</span><span class="sxs-lookup"><span data-stu-id="55ebc-122">The resource id of the share</span></span>

```yaml
Type: System.String
Parameter Sets: ByProviderShareSubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55ebc-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="55ebc-123">-ShareName</span></span>
<span data-ttu-id="55ebc-124">Имя Azure DataShare.</span><span class="sxs-lookup"><span data-stu-id="55ebc-124">Azure DataShare name.</span></span>

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

### <span data-ttu-id="55ebc-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55ebc-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="55ebc-126">ID подписки на потребительские акции</span><span class="sxs-lookup"><span data-stu-id="55ebc-126">The id of consumer share subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55ebc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55ebc-127">CommonParameters</span></span>
<span data-ttu-id="55ebc-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55ebc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55ebc-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55ebc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55ebc-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="55ebc-130">INPUTS</span></span>

### <span data-ttu-id="55ebc-131">System.String</span><span class="sxs-lookup"><span data-stu-id="55ebc-131">System.String</span></span>

## <span data-ttu-id="55ebc-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="55ebc-132">OUTPUTS</span></span>

### <span data-ttu-id="55ebc-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="55ebc-133">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="55ebc-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="55ebc-134">NOTES</span></span>

## <span data-ttu-id="55ebc-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55ebc-135">RELATED LINKS</span></span>
