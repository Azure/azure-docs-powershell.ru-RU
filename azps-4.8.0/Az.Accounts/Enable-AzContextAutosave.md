---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236396"
---
# <span data-ttu-id="d6fd9-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="d6fd9-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="d6fd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fd9-103">Контексты Azure — это объекты PowerShell, представляющие активную подписку, для которой выполняются команды, и сведения для проверки подлинности, необходимые для подключения к облаку Azure.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="d6fd9-104">При использовании контекстов Azure для Azure PowerShell не требуется повторная аутентификация учетной записи при каждом переключении подписок.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="d6fd9-105">Дополнительные сведения можно найти в разделе [объекты контекста Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="d6fd9-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="d6fd9-106">Этот командлет позволяет сохранять и автоматически загружать данные контекста Azure при запуске процесса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="d6fd9-107">Например, при открытии нового окна.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="d6fd9-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6fd9-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fd9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6fd9-109">DESCRIPTION</span></span>

<span data-ttu-id="d6fd9-110">Позволяет сохранять и автоматически загружать данные контекста Azure при запуске процесса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="d6fd9-111">Контекст сохраняется по завершении выполнения любого командлета, влияющего на контекст.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="d6fd9-112">Например, любой командлет профиля.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="d6fd9-113">Если вы используете проверку подлинности пользователя, то при запуске любого командлета можно обновить маркеры.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="d6fd9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6fd9-114">EXAMPLES</span></span>

### <span data-ttu-id="d6fd9-115">Пример 1: включение учетных данных автосохранения для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="d6fd9-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="d6fd9-116">Включите Автосохранение учетных данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="d6fd9-117">Всякий раз, когда открывается окно PowerShell, текущий контекст запоминается без входа.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="d6fd9-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d6fd9-118">Example 2</span></span>

<span data-ttu-id="d6fd9-119">Вы можете сохранять и автоматически загружать данные об учетных данных Azure, учетной записи и подписках, когда вы открываете окно PowerShell в этом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="d6fd9-120">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="d6fd9-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="d6fd9-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6fd9-121">PARAMETERS</span></span>

### <span data-ttu-id="d6fd9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fd9-122">-DefaultProfile</span></span>

<span data-ttu-id="d6fd9-123">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d6fd9-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="d6fd9-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="d6fd9-124">-Scope</span></span>

<span data-ttu-id="d6fd9-125">Определяет область действия контекстных изменений.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-125">Determines the scope of context changes.</span></span> <span data-ttu-id="d6fd9-126">Например, изменения применяются только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="d6fd9-127">Изменения, внесенные в область, `CurrentUser` влияют на все сеансы PowerShell, запускаемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="d6fd9-128">Если для определенного сеанса требуются разные параметры, используйте область `Process` .</span><span class="sxs-lookup"><span data-stu-id="d6fd9-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fd9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6fd9-129">-Confirm</span></span>

<span data-ttu-id="d6fd9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fd9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fd9-131">-WhatIf</span></span>

<span data-ttu-id="d6fd9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6fd9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="d6fd9-134">Общие параметры</span><span class="sxs-lookup"><span data-stu-id="d6fd9-134">Common Parameters</span></span>

<span data-ttu-id="d6fd9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6fd9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fd9-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6fd9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fd9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6fd9-137">INPUTS</span></span>

### <span data-ttu-id="d6fd9-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6fd9-138">None</span></span>

## <span data-ttu-id="d6fd9-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6fd9-139">OUTPUTS</span></span>

### <span data-ttu-id="d6fd9-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="d6fd9-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="d6fd9-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6fd9-141">NOTES</span></span>

## <span data-ttu-id="d6fd9-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6fd9-142">RELATED LINKS</span></span>
