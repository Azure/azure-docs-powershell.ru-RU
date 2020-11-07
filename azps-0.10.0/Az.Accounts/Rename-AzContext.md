---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 00f9b84c1e3e8a5bb9a506952cce9ab45e55b9e9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909374"
---
# <span data-ttu-id="717b1-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="717b1-101">Rename-AzContext</span></span>

## <span data-ttu-id="717b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="717b1-102">SYNOPSIS</span></span>
<span data-ttu-id="717b1-103">Переименуйте контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="717b1-103">Rename an Azure context.</span></span>  <span data-ttu-id="717b1-104">По умолчанию контексты названы учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="717b1-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="717b1-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="717b1-105">SYNTAX</span></span>

### <span data-ttu-id="717b1-106">RenameByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="717b1-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="717b1-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="717b1-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="717b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="717b1-108">DESCRIPTION</span></span>
<span data-ttu-id="717b1-109">Переименуйте контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="717b1-109">Rename an Azure context.</span></span>  <span data-ttu-id="717b1-110">По умолчанию контексты названы учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="717b1-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="717b1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="717b1-111">EXAMPLES</span></span>

### <span data-ttu-id="717b1-112">Переименование контекста с помощью именованных параметров</span><span class="sxs-lookup"><span data-stu-id="717b1-112">Rename a context using named parameters</span></span>
```
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="717b1-113">Переименуйте контекст для " user1@contoso.org " с подпиской "12345-6789-2345-3567890" на "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="717b1-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="717b1-114">После этой команды вы сможете ориентироваться на контекст с помощью функции "Select-AzContext Work".</span><span class="sxs-lookup"><span data-stu-id="717b1-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="717b1-115">Обратите внимание, что с помощью функции TAB можно прокручивать значения для "SourceName".</span><span class="sxs-lookup"><span data-stu-id="717b1-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="717b1-116">Переименование контекста с помощью позиционных параметров</span><span class="sxs-lookup"><span data-stu-id="717b1-116">Rename a context using positional parameters</span></span>
```
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="717b1-117">Переименуйте контекст с именем "мой контекст" на "трудозатраты".</span><span class="sxs-lookup"><span data-stu-id="717b1-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="717b1-118">После этой команды вы сможете ориентироваться на контекст, используя Select-AzContext трудозатраты.</span><span class="sxs-lookup"><span data-stu-id="717b1-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="717b1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="717b1-119">PARAMETERS</span></span>

### <span data-ttu-id="717b1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="717b1-120">-DefaultProfile</span></span>
<span data-ttu-id="717b1-121">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="717b1-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="717b1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="717b1-122">-Force</span></span>
<span data-ttu-id="717b1-123">Переименование контекста даже в том случае, если целевой контекст уже существует</span><span class="sxs-lookup"><span data-stu-id="717b1-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="717b1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="717b1-124">-InputObject</span></span>
<span data-ttu-id="717b1-125">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="717b1-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="717b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="717b1-126">-PassThru</span></span>
<span data-ttu-id="717b1-127">Возвращает переименованный контекст.</span><span class="sxs-lookup"><span data-stu-id="717b1-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="717b1-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="717b1-128">-Scope</span></span>
<span data-ttu-id="717b1-129">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="717b1-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="717b1-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="717b1-130">-SourceName</span></span>
<span data-ttu-id="717b1-131">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="717b1-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717b1-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="717b1-132">-TargetName</span></span>
<span data-ttu-id="717b1-133">Новое имя контекста.</span><span class="sxs-lookup"><span data-stu-id="717b1-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="717b1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="717b1-134">-Confirm</span></span>
<span data-ttu-id="717b1-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="717b1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="717b1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="717b1-136">-WhatIf</span></span>
<span data-ttu-id="717b1-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="717b1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="717b1-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="717b1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="717b1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="717b1-139">CommonParameters</span></span>
<span data-ttu-id="717b1-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="717b1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="717b1-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="717b1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="717b1-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="717b1-142">INPUTS</span></span>

### <span data-ttu-id="717b1-143">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="717b1-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="717b1-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="717b1-144">OUTPUTS</span></span>

### <span data-ttu-id="717b1-145">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="717b1-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="717b1-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="717b1-146">NOTES</span></span>

## <span data-ttu-id="717b1-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="717b1-147">RELATED LINKS</span></span>
