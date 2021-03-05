---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999057"
---
# <span data-ttu-id="c899e-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="c899e-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="c899e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c899e-102">SYNOPSIS</span></span>
<span data-ttu-id="c899e-103">Контексты Azure — это объекты PowerShell, представляющие активную подписку для запуска команд, а также сведения о проверке подлинности, необходимые для подключения к облаку Azure.</span><span class="sxs-lookup"><span data-stu-id="c899e-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="c899e-104">В контекстах Azure Azure PowerShell не нужно повторно реакторировать учетную запись при смене подписки.</span><span class="sxs-lookup"><span data-stu-id="c899e-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="c899e-105">Дополнительные сведения см. в [контекстных объектах Azure PowerShell.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="c899e-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="c899e-106">Этот cmdlet позволяет сохранить контекстные данные Azure и автоматически загружать их при запуске powerShell.</span><span class="sxs-lookup"><span data-stu-id="c899e-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="c899e-107">Например, при открытии нового окна.</span><span class="sxs-lookup"><span data-stu-id="c899e-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="c899e-108">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c899e-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c899e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c899e-109">DESCRIPTION</span></span>

<span data-ttu-id="c899e-110">Позволяет сохранить контекстные данные Azure и автоматически загружать их при начале процесса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c899e-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="c899e-111">Контекст будет сохранен в конце выполнения любого cmdlet, который влияет на контекст.</span><span class="sxs-lookup"><span data-stu-id="c899e-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="c899e-112">Например, любой из профилей.</span><span class="sxs-lookup"><span data-stu-id="c899e-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="c899e-113">Если вы используете проверку подлинности пользователей, токены могут обновляться во время запуска любого из этих буклетов.</span><span class="sxs-lookup"><span data-stu-id="c899e-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="c899e-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c899e-114">EXAMPLES</span></span>

### <span data-ttu-id="c899e-115">Пример 1. Включить автосбереги учетных данных для текущего пользователя</span><span class="sxs-lookup"><span data-stu-id="c899e-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="c899e-116">Включив автоскрытие учетных данных для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c899e-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="c899e-117">При открытом окне PowerShell текущий контекст запоминается без входа в систему.</span><span class="sxs-lookup"><span data-stu-id="c899e-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="c899e-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c899e-118">Example 2</span></span>

<span data-ttu-id="c899e-119">Разрешить сохранить учетные данные, учетные записи и сведения о подписке Azure и автоматически загружать их, когда вы открываете окно PowerShell в этом сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c899e-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="c899e-120">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c899e-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="c899e-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c899e-121">PARAMETERS</span></span>

### <span data-ttu-id="c899e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c899e-122">-DefaultProfile</span></span>

<span data-ttu-id="c899e-123">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c899e-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="c899e-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="c899e-124">-Scope</span></span>

<span data-ttu-id="c899e-125">Определяет область изменения контекста.</span><span class="sxs-lookup"><span data-stu-id="c899e-125">Determines the scope of context changes.</span></span> <span data-ttu-id="c899e-126">Например, будут ли изменения применяться только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="c899e-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="c899e-127">Изменения, внесенные в область, влияют на все сеансы `CurrentUser` PowerShell, на запущенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="c899e-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="c899e-128">Если у определенного сеанса должны быть другие параметры, используйте область `Process` действия.</span><span class="sxs-lookup"><span data-stu-id="c899e-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="c899e-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c899e-129">-Confirm</span></span>

<span data-ttu-id="c899e-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c899e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c899e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c899e-131">-WhatIf</span></span>

<span data-ttu-id="c899e-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c899e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c899e-133">Не будет выполниться cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c899e-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="c899e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c899e-134">CommonParameters</span></span>
<span data-ttu-id="c899e-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c899e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c899e-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c899e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c899e-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c899e-137">INPUTS</span></span>

### <span data-ttu-id="c899e-138">Нет</span><span class="sxs-lookup"><span data-stu-id="c899e-138">None</span></span>

## <span data-ttu-id="c899e-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c899e-139">OUTPUTS</span></span>

### <span data-ttu-id="c899e-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="c899e-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="c899e-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c899e-141">NOTES</span></span>

## <span data-ttu-id="c899e-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c899e-142">RELATED LINKS</span></span>
