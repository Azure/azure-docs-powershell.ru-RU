---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236378"
---
# <span data-ttu-id="95e31-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="95e31-101">Remove-AzContext</span></span>

## <span data-ttu-id="95e31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95e31-102">SYNOPSIS</span></span>
<span data-ttu-id="95e31-103">Удаление контекста из набора доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="95e31-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="95e31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95e31-104">SYNTAX</span></span>

### <span data-ttu-id="95e31-105">RemoveByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95e31-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95e31-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="95e31-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="95e31-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95e31-107">DESCRIPTION</span></span>
<span data-ttu-id="95e31-108">Удаление контекста Azure из набора контекстов</span><span class="sxs-lookup"><span data-stu-id="95e31-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="95e31-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95e31-109">EXAMPLES</span></span>

### <span data-ttu-id="95e31-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95e31-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="95e31-111">Удалить контекст с именем по умолчанию</span><span class="sxs-lookup"><span data-stu-id="95e31-111">Remove the context named default</span></span>

## <span data-ttu-id="95e31-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95e31-112">PARAMETERS</span></span>

### <span data-ttu-id="95e31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95e31-113">-DefaultProfile</span></span>
<span data-ttu-id="95e31-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95e31-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95e31-115">-Force</span><span class="sxs-lookup"><span data-stu-id="95e31-115">-Force</span></span>
<span data-ttu-id="95e31-116">Удалить контекст, даже если это значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="95e31-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="95e31-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95e31-117">-InputObject</span></span>
<span data-ttu-id="95e31-118">Контекстный объект, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="95e31-118">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95e31-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95e31-119">-Name</span></span>
<span data-ttu-id="95e31-120">Имя контекста.</span><span class="sxs-lookup"><span data-stu-id="95e31-120">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e31-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95e31-121">-PassThru</span></span>
<span data-ttu-id="95e31-122">Вернуть удаленный контекст</span><span class="sxs-lookup"><span data-stu-id="95e31-122">Return the removed context</span></span>

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

### <span data-ttu-id="95e31-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="95e31-123">-Scope</span></span>
<span data-ttu-id="95e31-124">Определяет область изменений контекста, например, применимы ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="95e31-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="95e31-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95e31-125">-Confirm</span></span>
<span data-ttu-id="95e31-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95e31-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95e31-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95e31-127">-WhatIf</span></span>
<span data-ttu-id="95e31-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95e31-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95e31-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95e31-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95e31-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e31-130">CommonParameters</span></span>
<span data-ttu-id="95e31-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95e31-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e31-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95e31-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e31-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95e31-133">INPUTS</span></span>

### <span data-ttu-id="95e31-134">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="95e31-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="95e31-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95e31-135">OUTPUTS</span></span>

### <span data-ttu-id="95e31-136">Microsoft. Azure. Commands. Profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="95e31-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="95e31-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="95e31-137">NOTES</span></span>

## <span data-ttu-id="95e31-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95e31-138">RELATED LINKS</span></span>