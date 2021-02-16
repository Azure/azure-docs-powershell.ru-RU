---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 540426cc8612f4cee7364a7875bb9a142bca07ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100222636"
---
# <span data-ttu-id="8e2be-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="8e2be-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="8e2be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2be-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2be-103">Отзывает доступ к подписке на доступ к источнику</span><span class="sxs-lookup"><span data-stu-id="8e2be-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="8e2be-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e2be-104">SYNTAX</span></span>

### <span data-ttu-id="8e2be-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8e2be-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e2be-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e2be-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e2be-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e2be-107">DESCRIPTION</span></span>
<span data-ttu-id="8e2be-108">**Cmdlet Revoke-AzDataShareSubscriptionAccess** предоставляет доступ к источнику</span><span class="sxs-lookup"><span data-stu-id="8e2be-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="8e2be-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e2be-109">EXAMPLES</span></span>

### <span data-ttu-id="8e2be-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8e2be-110">Example 1</span></span>
```
PS C:\> Revoke-AzDataShareSubscriptionAccess -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -ShareName "AdsShare" -ShareSubscriptionId 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12

Company                   : ADS
CreatedAt                 : 6/15/2019 1:02:28 AM
CreatedBy                 : abc@microsoft.com
SharedAt                  : 6/15/2019 12:08:48 AM
SharedBy                  : abc@microsoft.com
ShareSubscriptionObjectId : 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
ShareSubscriptionStatus   : Revoked
Id                        : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare/shareSubscriptions/8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12
Name                      : AdsShare
Type                      : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="8e2be-111">Отзыв доступа к подписке на совместное использования, означаемой id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="8e2be-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="8e2be-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e2be-112">PARAMETERS</span></span>

### <span data-ttu-id="8e2be-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e2be-113">-AccountName</span></span>
<span data-ttu-id="8e2be-114">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="8e2be-114">Azure data share account name</span></span>

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

### <span data-ttu-id="8e2be-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e2be-115">-AsJob</span></span>
<span data-ttu-id="8e2be-116">{{Fill AsJob Description}}</span><span class="sxs-lookup"><span data-stu-id="8e2be-116">{{Fill AsJob Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e2be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2be-117">-DefaultProfile</span></span>
<span data-ttu-id="8e2be-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e2be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e2be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2be-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e2be-120">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="8e2be-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8e2be-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e2be-121">-ResourceId</span></span>
<span data-ttu-id="8e2be-122">ИД ресурса для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="8e2be-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="8e2be-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="8e2be-123">-ShareName</span></span>
<span data-ttu-id="8e2be-124">Имя обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="8e2be-124">Azure data share name</span></span>

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

### <span data-ttu-id="8e2be-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e2be-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="8e2be-126">The share subscription id of the provider share subscription</span><span class="sxs-lookup"><span data-stu-id="8e2be-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="8e2be-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e2be-127">-Confirm</span></span>
<span data-ttu-id="8e2be-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8e2be-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2be-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2be-129">-WhatIf</span></span>
<span data-ttu-id="8e2be-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e2be-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e2be-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8e2be-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2be-132">CommonParameters</span></span>
<span data-ttu-id="8e2be-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e2be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2be-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e2be-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2be-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2be-135">INPUTS</span></span>

### <span data-ttu-id="8e2be-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8e2be-136">System.String</span></span>

## <span data-ttu-id="8e2be-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e2be-137">OUTPUTS</span></span>

### <span data-ttu-id="8e2be-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8e2be-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="8e2be-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e2be-139">NOTES</span></span>

## <span data-ttu-id="8e2be-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e2be-140">RELATED LINKS</span></span>
