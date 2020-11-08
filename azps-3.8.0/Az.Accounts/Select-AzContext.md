---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: 6f3ff6868a34eefc9b7cd45cf371b6ef29dbf469
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066468"
---
# <span data-ttu-id="19323-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="19323-101">Select-AzContext</span></span>

## <span data-ttu-id="19323-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19323-102">SYNOPSIS</span></span>
<span data-ttu-id="19323-103">Выбор подписки и учетной записи для назначения в командлетах PowerShell для Azure</span><span class="sxs-lookup"><span data-stu-id="19323-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="19323-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19323-104">SYNTAX</span></span>

### <span data-ttu-id="19323-105">SelectByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19323-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19323-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="19323-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="19323-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19323-107">DESCRIPTION</span></span>
<span data-ttu-id="19323-108">Выберите подписку для назначения (или учетной записи или клиента) в командлетах Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19323-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="19323-109">После этого командлета будущие командлеты будут ориентироваться на выбранный контекст.</span><span class="sxs-lookup"><span data-stu-id="19323-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="19323-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19323-110">EXAMPLES</span></span>

### <span data-ttu-id="19323-111">Пример 1: назначение именованного контекста</span><span class="sxs-lookup"><span data-stu-id="19323-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="19323-112">Назначение будущих командлетов PowerShell для Azure для учетной записи, клиента и подписки в контексте "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="19323-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="19323-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19323-113">PARAMETERS</span></span>

### <span data-ttu-id="19323-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19323-114">-DefaultProfile</span></span>
<span data-ttu-id="19323-115">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19323-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19323-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19323-116">-InputObject</span></span>
<span data-ttu-id="19323-117">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="19323-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19323-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19323-118">-Name</span></span>
<span data-ttu-id="19323-119">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="19323-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19323-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="19323-120">-Scope</span></span>
<span data-ttu-id="19323-121">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="19323-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19323-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19323-122">-Confirm</span></span>
<span data-ttu-id="19323-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19323-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19323-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19323-124">-WhatIf</span></span>
<span data-ttu-id="19323-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19323-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19323-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19323-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19323-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19323-127">CommonParameters</span></span>
<span data-ttu-id="19323-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19323-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19323-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19323-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19323-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19323-130">INPUTS</span></span>

### <span data-ttu-id="19323-131">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="19323-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="19323-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19323-132">OUTPUTS</span></span>

### <span data-ttu-id="19323-133">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="19323-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="19323-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="19323-134">NOTES</span></span>

## <span data-ttu-id="19323-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19323-135">RELATED LINKS</span></span>
