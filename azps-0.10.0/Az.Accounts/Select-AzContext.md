---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: c38be0f49e899379d93fc39a2531bcef219c3c29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909365"
---
# <span data-ttu-id="f4018-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="f4018-101">Select-AzContext</span></span>

## <span data-ttu-id="f4018-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4018-102">SYNOPSIS</span></span>
<span data-ttu-id="f4018-103">Выбор подписки и учетной записи для назначения в командлетах PowerShell для Azure</span><span class="sxs-lookup"><span data-stu-id="f4018-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="f4018-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4018-104">SYNTAX</span></span>

### <span data-ttu-id="f4018-105">SelectByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4018-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4018-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="f4018-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="f4018-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4018-107">DESCRIPTION</span></span>
<span data-ttu-id="f4018-108">Выберите подписку для назначения (или учетной записи или клиента) в командлетах Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f4018-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="f4018-109">После этого командлета будущие командлеты будут ориентироваться на выбранный контекст.</span><span class="sxs-lookup"><span data-stu-id="f4018-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="f4018-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4018-110">EXAMPLES</span></span>

### <span data-ttu-id="f4018-111">Пример 1: назначение именованного контекста</span><span class="sxs-lookup"><span data-stu-id="f4018-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="f4018-112">Назначение будущих командлетов PowerShell для Azure для учетной записи, клиента и подписки в контексте "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="f4018-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="f4018-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4018-113">PARAMETERS</span></span>

### <span data-ttu-id="f4018-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4018-114">-DefaultProfile</span></span>
<span data-ttu-id="f4018-115">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f4018-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4018-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4018-116">-InputObject</span></span>
<span data-ttu-id="f4018-117">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="f4018-117">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="f4018-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4018-118">-Name</span></span>
<span data-ttu-id="f4018-119">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="f4018-119">The name of the context</span></span>

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

### <span data-ttu-id="f4018-120">-Scope</span><span class="sxs-lookup"><span data-stu-id="f4018-120">-Scope</span></span>
<span data-ttu-id="f4018-121">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="f4018-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="f4018-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4018-122">-Confirm</span></span>
<span data-ttu-id="f4018-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4018-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4018-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4018-124">-WhatIf</span></span>
<span data-ttu-id="f4018-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4018-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4018-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4018-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4018-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4018-127">CommonParameters</span></span>
<span data-ttu-id="f4018-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4018-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4018-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4018-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4018-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4018-130">INPUTS</span></span>

### <span data-ttu-id="f4018-131">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f4018-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="f4018-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4018-132">OUTPUTS</span></span>

### <span data-ttu-id="f4018-133">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f4018-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="f4018-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4018-134">NOTES</span></span>

## <span data-ttu-id="f4018-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4018-135">RELATED LINKS</span></span>
