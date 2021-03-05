---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 2ff8297ff04f18a903cca3a262d5232ace7c6ef1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965539"
---
# <span data-ttu-id="153c3-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="153c3-101">Rename-AzContext</span></span>

## <span data-ttu-id="153c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="153c3-102">SYNOPSIS</span></span>
<span data-ttu-id="153c3-103">Переименуем контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="153c3-103">Rename an Azure context.</span></span>  <span data-ttu-id="153c3-104">По умолчанию контексты называются учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="153c3-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="153c3-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="153c3-105">SYNTAX</span></span>

### <span data-ttu-id="153c3-106">RenameByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="153c3-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="153c3-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="153c3-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="153c3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="153c3-108">DESCRIPTION</span></span>
<span data-ttu-id="153c3-109">Переименуем контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="153c3-109">Rename an Azure context.</span></span>  <span data-ttu-id="153c3-110">По умолчанию контексты называются учетной записью пользователя и подпиской.</span><span class="sxs-lookup"><span data-stu-id="153c3-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="153c3-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="153c3-111">EXAMPLES</span></span>

### <span data-ttu-id="153c3-112">Пример 1. Переименование контекста с использованием именуемой параметров</span><span class="sxs-lookup"><span data-stu-id="153c3-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="153c3-113">Переименуем контекст для ' с подпиской user1@contoso.org '12345-6789-2345-3567890' в "Работа".</span><span class="sxs-lookup"><span data-stu-id="153c3-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="153c3-114">После этой команды вы сможете выбрать контекст с помощью select-AzContext Work.</span><span class="sxs-lookup"><span data-stu-id="153c3-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="153c3-115">Обратите внимание на то, что вы можете использовать табу желтую вкладку для значения "Имя Источника" с помощью завершения вкладки.</span><span class="sxs-lookup"><span data-stu-id="153c3-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="153c3-116">Пример 2. Переименование контекста с помощью позиционной параметров</span><span class="sxs-lookup"><span data-stu-id="153c3-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="153c3-117">Переименуем контекст с именем "Мой контекст" в "Рабочий".</span><span class="sxs-lookup"><span data-stu-id="153c3-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="153c3-118">После этой команды вы сможете использовать целевой контекст с помощью Select-AzContext трудоемких задач.</span><span class="sxs-lookup"><span data-stu-id="153c3-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="153c3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="153c3-119">PARAMETERS</span></span>

### <span data-ttu-id="153c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="153c3-120">-DefaultProfile</span></span>
<span data-ttu-id="153c3-121">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="153c3-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="153c3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="153c3-122">-Force</span></span>
<span data-ttu-id="153c3-123">Переименование контекста, даже если целевой контекст уже существует</span><span class="sxs-lookup"><span data-stu-id="153c3-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="153c3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="153c3-124">-InputObject</span></span>
<span data-ttu-id="153c3-125">Контекстный объект, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="153c3-125">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="153c3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="153c3-126">-PassThru</span></span>
<span data-ttu-id="153c3-127">Возврат переименованного контекста.</span><span class="sxs-lookup"><span data-stu-id="153c3-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="153c3-128">-Scope</span><span class="sxs-lookup"><span data-stu-id="153c3-128">-Scope</span></span>
<span data-ttu-id="153c3-129">Определяет область изменения контекста( например, применяются ли изменения только к текущему процессу или же к всем сеансам, на запущенным пользователем).</span><span class="sxs-lookup"><span data-stu-id="153c3-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="153c3-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="153c3-130">-SourceName</span></span>
<span data-ttu-id="153c3-131">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="153c3-131">The name of the context</span></span>

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

### <span data-ttu-id="153c3-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="153c3-132">-TargetName</span></span>
<span data-ttu-id="153c3-133">Новое имя контекста</span><span class="sxs-lookup"><span data-stu-id="153c3-133">The new name of the context</span></span>

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

### <span data-ttu-id="153c3-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="153c3-134">-Confirm</span></span>
<span data-ttu-id="153c3-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="153c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="153c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="153c3-136">-WhatIf</span></span>
<span data-ttu-id="153c3-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="153c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="153c3-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="153c3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="153c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="153c3-139">CommonParameters</span></span>
<span data-ttu-id="153c3-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="153c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="153c3-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="153c3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="153c3-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="153c3-142">INPUTS</span></span>

### <span data-ttu-id="153c3-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="153c3-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="153c3-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="153c3-144">OUTPUTS</span></span>

### <span data-ttu-id="153c3-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="153c3-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="153c3-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="153c3-146">NOTES</span></span>

## <span data-ttu-id="153c3-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="153c3-147">RELATED LINKS</span></span>
