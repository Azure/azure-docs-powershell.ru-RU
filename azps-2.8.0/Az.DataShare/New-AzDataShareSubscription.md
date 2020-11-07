---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: 64309b77801646e61e3a144bc4a7405e4e978aa6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721173"
---
# <span data-ttu-id="ddc31-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="ddc31-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="ddc31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddc31-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc31-103">Создание новой подписки на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="ddc31-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="ddc31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddc31-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc31-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddc31-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc31-106">Командлет **New-AzDataShareSubscription** создает подписку на общий доступ в указанной учетной записи данных и идентификаторе приглашения.</span><span class="sxs-lookup"><span data-stu-id="ddc31-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="ddc31-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddc31-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc31-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ddc31-108">Example 1</span></span>
```
PS C:\> New-AzDataShareSubscription -ResourceGroupName "ADS" -AccountName "WikiAds" -Name "AdsShareSubscription" -InvitationId "167e06ff-567f-4bc7-be0c-645a6de710f3"
CreatedAt               : 6/30/2019 12:42:12 AM
CreatedBy               : adstest@microsoft.com
InvitationId            : 167e06ff-567f-4bc7-be0c-645a6de710f3
ProvisioningState       : Succeeded
ShareName               : AdsShare
ShareSender             : adsprovider@microsoft.com
ShareSenderCompanyName  : ADS Company
ShareDescription        : Test description  
ShareTerms              : Test terms of use
ShareSubscriptionStatus : Active
ShareKind               : CopyBased
Id                      : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAds/shareSubscriptions/AdsShareSubscription
Name                    : AdsShareSubscription
Type                    : Microsoft.DataShare/ShareSubscriptions
```

<span data-ttu-id="ddc31-109">Эти команды создают новую подписку на общий доступ AdsShareSubscription для invitaionId в разделе Учетная запись общего доступа к данным WikiAds.</span><span class="sxs-lookup"><span data-stu-id="ddc31-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="ddc31-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddc31-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc31-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="ddc31-111">-AccountName</span></span>
<span data-ttu-id="ddc31-112">Имя учетной записи для общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="ddc31-112">Azure data share account name</span></span>

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

### <span data-ttu-id="ddc31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc31-113">-DefaultProfile</span></span>
<span data-ttu-id="ddc31-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ddc31-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc31-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="ddc31-115">-InvitationId</span></span>
<span data-ttu-id="ddc31-116">InvitationId общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="ddc31-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="ddc31-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddc31-117">-Name</span></span>
<span data-ttu-id="ddc31-118">Имя подписки на общий доступ к данным Azure</span><span class="sxs-lookup"><span data-stu-id="ddc31-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="ddc31-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc31-119">-ResourceGroupName</span></span>
<span data-ttu-id="ddc31-120">Имя группы ресурсов для учетной записи общего доступа к данным Azure</span><span class="sxs-lookup"><span data-stu-id="ddc31-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="ddc31-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddc31-121">-Confirm</span></span>
<span data-ttu-id="ddc31-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ddc31-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc31-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc31-123">-WhatIf</span></span>
<span data-ttu-id="ddc31-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ddc31-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc31-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ddc31-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc31-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc31-126">CommonParameters</span></span>
<span data-ttu-id="ddc31-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddc31-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc31-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc31-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc31-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddc31-129">INPUTS</span></span>

### <span data-ttu-id="ddc31-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="ddc31-130">None</span></span>

## <span data-ttu-id="ddc31-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddc31-131">OUTPUTS</span></span>

### <span data-ttu-id="ddc31-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="ddc31-132">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="ddc31-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddc31-133">NOTES</span></span>

## <span data-ttu-id="ddc31-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddc31-134">RELATED LINKS</span></span>
