---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/revoke-azdatasharesubscriptionaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Revoke-AzDataShareSubscriptionAccess.md
ms.openlocfilehash: 6ac4fdbc119c5cd6639e9b688d60e158eea2a62f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074419"
---
# <span data-ttu-id="7c60a-101">Revoke-AzDataShareSubscriptionAccess</span><span class="sxs-lookup"><span data-stu-id="7c60a-101">Revoke-AzDataShareSubscriptionAccess</span></span>

## <span data-ttu-id="7c60a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c60a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c60a-103">Отмена общего доступа к подписке на доступ к исходной папке</span><span class="sxs-lookup"><span data-stu-id="7c60a-103">Revokes share subscription access to source share</span></span>

## <span data-ttu-id="7c60a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c60a-104">SYNTAX</span></span>

### <span data-ttu-id="7c60a-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7c60a-105">ByFieldsParameterSet (Default)</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ResourceGroupName <String> -AccountName <String> [-ShareName <String>]
 -ShareSubscriptionId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7c60a-106">ByProviderShareSubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c60a-106">ByProviderShareSubscriptionIdParameterSet</span></span>
```
Revoke-AzDataShareSubscriptionAccess -ShareSubscriptionId <String> -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c60a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c60a-107">DESCRIPTION</span></span>
<span data-ttu-id="7c60a-108">Командлет **REVOKE-AzDataShareSubscriptionAccess** предоставляет подписку на общий доступ к исходной общей папке</span><span class="sxs-lookup"><span data-stu-id="7c60a-108">The **Revoke-AzDataShareSubscriptionAccess** cmdlet grants a share subscription access to source share</span></span>

## <span data-ttu-id="7c60a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c60a-109">EXAMPLES</span></span>

### <span data-ttu-id="7c60a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c60a-110">Example 1</span></span>
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

<span data-ttu-id="7c60a-111">Отмена доступа к подписке, идентифицированной с помощью идентификатора 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span><span class="sxs-lookup"><span data-stu-id="7c60a-111">Revokes access of share subscription identified by id 8ee6e6fd-b4a1-49a4-bb66-f187f38e0e12</span></span>

## <span data-ttu-id="7c60a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c60a-112">PARAMETERS</span></span>

### <span data-ttu-id="7c60a-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7c60a-113">-AccountName</span></span>
<span data-ttu-id="7c60a-114">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="7c60a-114">Azure data share account name</span></span>

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

### <span data-ttu-id="7c60a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c60a-115">-AsJob</span></span>
<span data-ttu-id="7c60a-116">{{Fill AsJob описание}}</span><span class="sxs-lookup"><span data-stu-id="7c60a-116">{{Fill AsJob Description}}</span></span>

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

### <span data-ttu-id="7c60a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c60a-117">-DefaultProfile</span></span>
<span data-ttu-id="7c60a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c60a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c60a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c60a-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c60a-120">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="7c60a-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="7c60a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c60a-121">-ResourceId</span></span>
<span data-ttu-id="7c60a-122">Идентификатор ресурса общего ресурса данных Azure</span><span class="sxs-lookup"><span data-stu-id="7c60a-122">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="7c60a-123">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="7c60a-123">-ShareName</span></span>
<span data-ttu-id="7c60a-124">Имя общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="7c60a-124">Azure data share name</span></span>

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

### <span data-ttu-id="7c60a-125">-ShareSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c60a-125">-ShareSubscriptionId</span></span>
<span data-ttu-id="7c60a-126">Код подписке на общий доступ к подписке поставщика</span><span class="sxs-lookup"><span data-stu-id="7c60a-126">The share subscription id of the provider share subscription</span></span>

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

### <span data-ttu-id="7c60a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c60a-127">-Confirm</span></span>
<span data-ttu-id="7c60a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c60a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c60a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c60a-129">-WhatIf</span></span>
<span data-ttu-id="7c60a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c60a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c60a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c60a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c60a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c60a-132">CommonParameters</span></span>
<span data-ttu-id="7c60a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c60a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c60a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c60a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c60a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c60a-135">INPUTS</span></span>

### <span data-ttu-id="7c60a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7c60a-136">System.String</span></span>

## <span data-ttu-id="7c60a-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c60a-137">OUTPUTS</span></span>

### <span data-ttu-id="7c60a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span><span class="sxs-lookup"><span data-stu-id="7c60a-138">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareProviderShareSubscription</span></span>

## <span data-ttu-id="7c60a-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c60a-139">NOTES</span></span>

## <span data-ttu-id="7c60a-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c60a-140">RELATED LINKS</span></span>
