---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/new-azdatasharesubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/New-AzDataShareSubscription.md
ms.openlocfilehash: e6b911831a84ce708af93ef6cc7b9f9be919758b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420623"
---
# <span data-ttu-id="8ff27-101">New-AzDataShareSubscription</span><span class="sxs-lookup"><span data-stu-id="8ff27-101">New-AzDataShareSubscription</span></span>

## <span data-ttu-id="8ff27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ff27-102">SYNOPSIS</span></span>
<span data-ttu-id="8ff27-103">Создает новую подписку на совместное использования.</span><span class="sxs-lookup"><span data-stu-id="8ff27-103">Creates a new share subscription.</span></span>

## <span data-ttu-id="8ff27-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ff27-104">SYNTAX</span></span>

```
New-AzDataShareSubscription -ResourceGroupName <String> -AccountName <String> -Name <String>
 -InvitationId <String> -SourceShareLocation <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ff27-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ff27-105">DESCRIPTION</span></span>
<span data-ttu-id="8ff27-106">**Новый-AzDataShareSubscription** создает подписку на объединение в указанной учетной записи обмена данными и код приглашения.</span><span class="sxs-lookup"><span data-stu-id="8ff27-106">The **New-AzDataShareSubscription** cmdlet creates a share subscription in specified data share account and invitation id.</span></span>

## <span data-ttu-id="8ff27-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ff27-107">EXAMPLES</span></span>

### <span data-ttu-id="8ff27-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ff27-108">Example 1</span></span>
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

<span data-ttu-id="8ff27-109">Эти команды создают новую подписку на AdsShareSubscription для invitaionId в учетной записи обмена данными WikiAds.</span><span class="sxs-lookup"><span data-stu-id="8ff27-109">This commands creates a new share subscription AdsShareSubscription for invitaionId under data share account WikiAds.</span></span>

## <span data-ttu-id="8ff27-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ff27-110">PARAMETERS</span></span>

### <span data-ttu-id="8ff27-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ff27-111">-AccountName</span></span>
<span data-ttu-id="8ff27-112">Имя учетной записи для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="8ff27-112">Azure data share account name</span></span>

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

### <span data-ttu-id="8ff27-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ff27-113">-DefaultProfile</span></span>
<span data-ttu-id="8ff27-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ff27-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ff27-115">-InvitationId</span><span class="sxs-lookup"><span data-stu-id="8ff27-115">-InvitationId</span></span>
<span data-ttu-id="8ff27-116">Azure data share invitationId</span><span class="sxs-lookup"><span data-stu-id="8ff27-116">Azure data share invitationId</span></span>

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

### <span data-ttu-id="8ff27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8ff27-117">-Name</span></span>
<span data-ttu-id="8ff27-118">Имя подписки на службу обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="8ff27-118">Azure data share subscription name</span></span>

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

### <span data-ttu-id="8ff27-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ff27-119">-ResourceGroupName</span></span>
<span data-ttu-id="8ff27-120">Имя группы ресурсов учетной записи azure data share</span><span class="sxs-lookup"><span data-stu-id="8ff27-120">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="8ff27-121">-SourceShareLocation</span><span class="sxs-lookup"><span data-stu-id="8ff27-121">-SourceShareLocation</span></span>
<span data-ttu-id="8ff27-122">Расположение для обмена данными Azure</span><span class="sxs-lookup"><span data-stu-id="8ff27-122">Azure data share location</span></span>

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

### <span data-ttu-id="8ff27-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ff27-123">-Confirm</span></span>
<span data-ttu-id="8ff27-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ff27-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ff27-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ff27-125">-WhatIf</span></span>
<span data-ttu-id="8ff27-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ff27-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ff27-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ff27-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ff27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ff27-128">CommonParameters</span></span>
<span data-ttu-id="8ff27-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ff27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ff27-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ff27-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ff27-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ff27-131">INPUTS</span></span>

### <span data-ttu-id="8ff27-132">Нет</span><span class="sxs-lookup"><span data-stu-id="8ff27-132">None</span></span>

## <span data-ttu-id="8ff27-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ff27-133">OUTPUTS</span></span>

### <span data-ttu-id="8ff27-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="8ff27-134">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="8ff27-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ff27-135">NOTES</span></span>

## <span data-ttu-id="8ff27-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ff27-136">RELATED LINKS</span></span>
