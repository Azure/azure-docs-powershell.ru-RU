---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248266"
---
# <span data-ttu-id="5ba21-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="5ba21-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="5ba21-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ba21-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba21-103">Контексты Azure — это объекты PowerShell, представляющие активную подписку, для которой выполняются команды, и сведения для проверки подлинности, необходимые для подключения к облаку Azure.</span><span class="sxs-lookup"><span data-stu-id="5ba21-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="5ba21-104">При использовании контекстов Azure для Azure PowerShell не требуется повторная аутентификация учетной записи при каждом переключении подписок.</span><span class="sxs-lookup"><span data-stu-id="5ba21-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="5ba21-105">Дополнительные сведения можно найти в разделе [объекты контекста Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="5ba21-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="5ba21-106">Этот командлет позволяет сохранять и автоматически загружать данные контекста Azure при запуске процесса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ba21-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="5ba21-107">Например, при открытии нового окна.</span><span class="sxs-lookup"><span data-stu-id="5ba21-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="5ba21-108">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ba21-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ba21-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ba21-109">DESCRIPTION</span></span>

<span data-ttu-id="5ba21-110">Позволяет сохранять и автоматически загружать данные контекста Azure при запуске процесса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ba21-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="5ba21-111">Контекст сохраняется по завершении выполнения любого командлета, влияющего на контекст.</span><span class="sxs-lookup"><span data-stu-id="5ba21-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="5ba21-112">Например, любой командлет профиля.</span><span class="sxs-lookup"><span data-stu-id="5ba21-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="5ba21-113">Если вы используете проверку подлинности пользователя, то при запуске любого командлета можно обновить маркеры.</span><span class="sxs-lookup"><span data-stu-id="5ba21-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="5ba21-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ba21-114">EXAMPLES</span></span>

### <span data-ttu-id="5ba21-115">Пример 1: включение учетных данных автосохранения для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="5ba21-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="5ba21-116">Включите Автосохранение учетных данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ba21-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="5ba21-117">Всякий раз, когда открывается окно PowerShell, текущий контекст запоминается без входа.</span><span class="sxs-lookup"><span data-stu-id="5ba21-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="5ba21-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5ba21-118">Example 2</span></span>

<span data-ttu-id="5ba21-119">Вы можете сохранять и автоматически загружать данные об учетных данных Azure, учетной записи и подписках, когда вы открываете окно PowerShell в этом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5ba21-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="5ba21-120">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="5ba21-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="5ba21-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ba21-121">PARAMETERS</span></span>

### <span data-ttu-id="5ba21-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba21-122">-DefaultProfile</span></span>

<span data-ttu-id="5ba21-123">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ba21-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="5ba21-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="5ba21-124">-Scope</span></span>

<span data-ttu-id="5ba21-125">Определяет область действия контекстных изменений.</span><span class="sxs-lookup"><span data-stu-id="5ba21-125">Determines the scope of context changes.</span></span> <span data-ttu-id="5ba21-126">Например, изменения применяются только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ba21-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="5ba21-127">Изменения, внесенные в область, `CurrentUser` влияют на все сеансы PowerShell, запускаемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="5ba21-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="5ba21-128">Если для определенного сеанса требуются разные параметры, используйте область `Process` .</span><span class="sxs-lookup"><span data-stu-id="5ba21-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="5ba21-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ba21-129">-Confirm</span></span>

<span data-ttu-id="5ba21-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ba21-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ba21-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ba21-131">-WhatIf</span></span>

<span data-ttu-id="5ba21-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ba21-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ba21-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ba21-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="5ba21-134">Общие параметры</span><span class="sxs-lookup"><span data-stu-id="5ba21-134">Common Parameters</span></span>

<span data-ttu-id="5ba21-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ba21-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba21-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ba21-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba21-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ba21-137">INPUTS</span></span>

### <span data-ttu-id="5ba21-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="5ba21-138">None</span></span>

## <span data-ttu-id="5ba21-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ba21-139">OUTPUTS</span></span>

### <span data-ttu-id="5ba21-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="5ba21-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="5ba21-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ba21-141">NOTES</span></span>

## <span data-ttu-id="5ba21-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ba21-142">RELATED LINKS</span></span>
