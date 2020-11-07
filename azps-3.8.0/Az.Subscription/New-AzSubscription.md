---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912396"
---
# <span data-ttu-id="cf58d-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="cf58d-101">New-AzSubscription</span></span>

## <span data-ttu-id="cf58d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf58d-102">SYNOPSIS</span></span>
<span data-ttu-id="cf58d-103">Создание подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="cf58d-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="cf58d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf58d-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf58d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf58d-105">DESCRIPTION</span></span>
<span data-ttu-id="cf58d-106">Командлет **New-AzSubscription** создает подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="cf58d-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="cf58d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf58d-107">EXAMPLES</span></span>

### <span data-ttu-id="cf58d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf58d-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="cf58d-109">Создает подписку Azure в указанной учетной записи с указанным типом предложения.</span><span class="sxs-lookup"><span data-stu-id="cf58d-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="cf58d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf58d-110">PARAMETERS</span></span>

### <span data-ttu-id="cf58d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cf58d-111">-AsJob</span></span>
<span data-ttu-id="cf58d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cf58d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cf58d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf58d-113">-DefaultProfile</span></span>
<span data-ttu-id="cf58d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf58d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf58d-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="cf58d-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="cf58d-116">Имя учетной записи, которую следует использовать при создании подписки.</span><span class="sxs-lookup"><span data-stu-id="cf58d-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="cf58d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf58d-117">-Name</span></span>
<span data-ttu-id="cf58d-118">Имя подписки, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="cf58d-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf58d-119">-OfferType</span><span class="sxs-lookup"><span data-stu-id="cf58d-119">-OfferType</span></span>
<span data-ttu-id="cf58d-120">Тип предложения, которое следует использовать при создании подписки.</span><span class="sxs-lookup"><span data-stu-id="cf58d-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="cf58d-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="cf58d-121">-OwnerApplicationId</span></span>
<span data-ttu-id="cf58d-122">SPN приложения, которым необходимо предоставить доступ владельца к подписке.</span><span class="sxs-lookup"><span data-stu-id="cf58d-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf58d-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="cf58d-123">-OwnerObjectId</span></span>
<span data-ttu-id="cf58d-124">Учетные данные пользователей или групп (ов), которым будет предоставлен доступ владельца к подписке.</span><span class="sxs-lookup"><span data-stu-id="cf58d-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf58d-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="cf58d-125">-OwnerSignInName</span></span>
<span data-ttu-id="cf58d-126">Пользователи, которым необходимо предоставить доступ к подписке на владельца.</span><span class="sxs-lookup"><span data-stu-id="cf58d-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf58d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf58d-127">-Confirm</span></span>
<span data-ttu-id="cf58d-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf58d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf58d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf58d-129">-WhatIf</span></span>
<span data-ttu-id="cf58d-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf58d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf58d-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf58d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf58d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf58d-132">CommonParameters</span></span>
<span data-ttu-id="cf58d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf58d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf58d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf58d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf58d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf58d-135">INPUTS</span></span>

### <span data-ttu-id="cf58d-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="cf58d-136">None</span></span>

## <span data-ttu-id="cf58d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf58d-137">OUTPUTS</span></span>

### <span data-ttu-id="cf58d-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="cf58d-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="cf58d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf58d-139">NOTES</span></span>

## <span data-ttu-id="cf58d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf58d-140">RELATED LINKS</span></span>
