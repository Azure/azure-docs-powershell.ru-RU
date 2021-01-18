---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzContext.md
ms.openlocfilehash: d5c31519ba55babb79e3e902a01e46746c5b70f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507017"
---
# <span data-ttu-id="d4bbe-101">Remove-AzContext</span><span class="sxs-lookup"><span data-stu-id="d4bbe-101">Remove-AzContext</span></span>

## <span data-ttu-id="d4bbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="d4bbe-103">Удаление контекста из набора доступных контекстов</span><span class="sxs-lookup"><span data-stu-id="d4bbe-103">Remove a context from the set of available contexts</span></span>

## <span data-ttu-id="d4bbe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4bbe-104">SYNTAX</span></span>

### <span data-ttu-id="d4bbe-105">RemoveByInputObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d4bbe-105">RemoveByInputObject (Default)</span></span>
```
Remove-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4bbe-106">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="d4bbe-106">RemoveByName</span></span>
```
Remove-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="d4bbe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4bbe-107">DESCRIPTION</span></span>
<span data-ttu-id="d4bbe-108">Удаление контекста Azure из набора контекстов</span><span class="sxs-lookup"><span data-stu-id="d4bbe-108">Remove an azure context from the set of contexts</span></span>

## <span data-ttu-id="d4bbe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4bbe-109">EXAMPLES</span></span>

### <span data-ttu-id="d4bbe-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4bbe-110">Example 1</span></span>
```
PS C:\> Remove-AzContext -Name Default
```

<span data-ttu-id="d4bbe-111">Удаление контекста, названного по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d4bbe-111">Remove the context named default</span></span>

## <span data-ttu-id="d4bbe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4bbe-112">PARAMETERS</span></span>

### <span data-ttu-id="d4bbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4bbe-113">-DefaultProfile</span></span>
<span data-ttu-id="d4bbe-114">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4bbe-114">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4bbe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d4bbe-115">-Force</span></span>
<span data-ttu-id="d4bbe-116">Удаление контекста, даже если он является стандартным</span><span class="sxs-lookup"><span data-stu-id="d4bbe-116">Remove context even if it is the default</span></span>

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

### <span data-ttu-id="d4bbe-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4bbe-117">-InputObject</span></span>
<span data-ttu-id="d4bbe-118">Контекстный объект, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="d4bbe-118">A context object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="d4bbe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d4bbe-119">-Name</span></span>
<span data-ttu-id="d4bbe-120">Имя контекста</span><span class="sxs-lookup"><span data-stu-id="d4bbe-120">The name of the context</span></span>

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

### <span data-ttu-id="d4bbe-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4bbe-121">-PassThru</span></span>
<span data-ttu-id="d4bbe-122">Возврат удаленного контекста</span><span class="sxs-lookup"><span data-stu-id="d4bbe-122">Return the removed context</span></span>

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

### <span data-ttu-id="d4bbe-123">-Scope</span><span class="sxs-lookup"><span data-stu-id="d4bbe-123">-Scope</span></span>
<span data-ttu-id="d4bbe-124">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые пользователь начал</span><span class="sxs-lookup"><span data-stu-id="d4bbe-124">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="d4bbe-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4bbe-125">-Confirm</span></span>
<span data-ttu-id="d4bbe-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4bbe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4bbe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4bbe-127">-WhatIf</span></span>
<span data-ttu-id="d4bbe-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4bbe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4bbe-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4bbe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4bbe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4bbe-130">CommonParameters</span></span>
<span data-ttu-id="d4bbe-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4bbe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4bbe-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4bbe-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4bbe-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4bbe-133">INPUTS</span></span>

### <span data-ttu-id="d4bbe-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d4bbe-134">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d4bbe-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4bbe-135">OUTPUTS</span></span>

### <span data-ttu-id="d4bbe-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d4bbe-136">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d4bbe-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4bbe-137">NOTES</span></span>

## <span data-ttu-id="d4bbe-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4bbe-138">RELATED LINKS</span></span>
