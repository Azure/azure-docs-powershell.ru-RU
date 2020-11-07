---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/grant-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Grant-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 5ce4bcc2aa1cf3259072e761a56903c50969a307
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912758"
---
# <span data-ttu-id="a4b1b-101">Grant-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="a4b1b-101">Grant-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="a4b1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b1b-103">Предоставление доступа к общей подписке на доступ к исходному общему доступу</span><span class="sxs-lookup"><span data-stu-id="a4b1b-103">Grants a revoked share subscription access to source share</span></span>

## <span data-ttu-id="a4b1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4b1b-104">SYNTAX</span></span>

### <span data-ttu-id="a4b1b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4b1b-105">ByFieldsParameterSet (Default)</span></span>
```
Grant-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4b1b-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a4b1b-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Grant-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4b1b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b1b-107">DESCRIPTION</span></span>
<span data-ttu-id="a4b1b-108">Командлет **Grant-AzDataShareSubscriptionAccess** предоставляет доступ к подписке для общего доступа к исходной общей папке</span><span class="sxs-lookup"><span data-stu-id="a4b1b-108">The **Grant-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="a4b1b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4b1b-109">EXAMPLES</span></span>

### <span data-ttu-id="a4b1b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4b1b-110">Example 1</span></span>
```
PS C:\> Grant-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Active
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="a4b1b-111">Предоставление доступа к подписке, идентифицированной с помощью идентификатора 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="a4b1b-111">Grants access to share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="a4b1b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4b1b-112">PARAMETERS</span></span>

### <span data-ttu-id="a4b1b-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a4b1b-113">-AccountName</span></span>
<span data-ttu-id="a4b1b-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a4b1b-114">Azure data share account name</span></span>

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

### <span data-ttu-id="a4b1b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b1b-115">-DefaultProfile</span></span>
<span data-ttu-id="a4b1b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4b1b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4b1b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b1b-117">-ResourceGroupName</span></span>
<span data-ttu-id="a4b1b-118">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a4b1b-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="a4b1b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4b1b-119">-ResourceId</span></span>
<span data-ttu-id="a4b1b-120">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="a4b1b-120">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="a4b1b-121">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="a4b1b-121">-ShareName</span></span>
<span data-ttu-id="a4b1b-122">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="a4b1b-122">Azure data share name</span></span>

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

### <span data-ttu-id="a4b1b-123">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a4b1b-123">-ShareSubscriptionId</span></span>
<span data-ttu-id="a4b1b-124">Код подписке на общий доступ к подписке поставщика</span><span class="sxs-lookup"><span data-stu-id="a4b1b-124">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="a4b1b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4b1b-125">-Confirm</span></span>
<span data-ttu-id="a4b1b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a4b1b-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b1b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b1b-127">-WhatIf</span></span>
<span data-ttu-id="a4b1b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a4b1b-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4b1b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a4b1b-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b1b-130">CommonParameters</span></span>
<span data-ttu-id="a4b1b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4b1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b1b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b1b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b1b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4b1b-133">INPUTS</span></span>

### <span data-ttu-id="a4b1b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4b1b-134">System.String</span></span>

## <span data-ttu-id="a4b1b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4b1b-135">OUTPUTS</span></span>

### <span data-ttu-id="a4b1b-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="a4b1b-136">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="a4b1b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4b1b-137">NOTES</span></span>

## <span data-ttu-id="a4b1b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4b1b-138">RELATED LINKS</span></span>
