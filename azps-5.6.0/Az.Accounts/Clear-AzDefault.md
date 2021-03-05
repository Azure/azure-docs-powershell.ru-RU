---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzDefault.md
ms.openlocfilehash: ac017af710531ff3294f858a8f95ad7529cd1c11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990615"
---
# <span data-ttu-id="5c0cc-101">Clear-AzDefault</span><span class="sxs-lookup"><span data-stu-id="5c0cc-101">Clear-AzDefault</span></span>

## <span data-ttu-id="5c0cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c0cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5c0cc-103">Очищает значения по умолчанию, установленные пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-103">Clears the defaults set by the user in the current context.</span></span>

## <span data-ttu-id="5c0cc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c0cc-104">SYNTAX</span></span>

```
Clear-AzDefault [-ResourceGroup] [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c0cc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c0cc-105">DESCRIPTION</span></span>
<span data-ttu-id="5c0cc-106">Этот Clear-AzDefault удаляет значения по умолчанию, установленные пользователем, в зависимости от параметров переключения, заданных пользователем.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-106">The Clear-AzDefault cmdlet removes the defaults set by the user depending on the switch parameters specified by the user.</span></span>

## <span data-ttu-id="5c0cc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c0cc-107">EXAMPLES</span></span>

### <span data-ttu-id="5c0cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c0cc-108">Example 1</span></span>
```powershell
PS C:\> Clear-AzDefault
```

<span data-ttu-id="5c0cc-109">Эта команда удаляет все значения по умолчанию, установленные пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-109">This command removes all the defaults set by the user in the current context.</span></span>

### <span data-ttu-id="5c0cc-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5c0cc-110">Example 2</span></span>
```powershell
PS C:\> Clear-AzDefault -ResourceGroup
```

<span data-ttu-id="5c0cc-111">Эта команда удаляет группу ресурсов по умолчанию, заданной пользователем в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-111">This command removes the default resource group set by the user in the current context.</span></span>

## <span data-ttu-id="5c0cc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c0cc-112">PARAMETERS</span></span>

### <span data-ttu-id="5c0cc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c0cc-113">-DefaultProfile</span></span>
<span data-ttu-id="5c0cc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c0cc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5c0cc-115">-Force</span></span>
<span data-ttu-id="5c0cc-116">Если значение по умолчанию не задано, удалите все значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5c0cc-116">Remove all defaults if no default is specified</span></span>

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

### <span data-ttu-id="5c0cc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c0cc-117">-PassThru</span></span>
<span data-ttu-id="5c0cc-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5c0cc-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5c0cc-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5c0cc-119">-ResourceGroup</span></span>
<span data-ttu-id="5c0cc-120">Очистить группу ресурсов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5c0cc-120">Clear Default Resource Group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c0cc-121">-Scope</span><span class="sxs-lookup"><span data-stu-id="5c0cc-121">-Scope</span></span>
<span data-ttu-id="5c0cc-122">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-122">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="5c0cc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c0cc-123">-Confirm</span></span>
<span data-ttu-id="5c0cc-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c0cc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c0cc-125">-WhatIf</span></span>
<span data-ttu-id="5c0cc-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c0cc-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c0cc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c0cc-128">CommonParameters</span></span>
<span data-ttu-id="5c0cc-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c0cc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c0cc-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5c0cc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c0cc-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c0cc-131">INPUTS</span></span>

### <span data-ttu-id="5c0cc-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5c0cc-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5c0cc-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c0cc-133">OUTPUTS</span></span>

### <span data-ttu-id="5c0cc-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5c0cc-134">System.Boolean</span></span>

## <span data-ttu-id="5c0cc-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c0cc-135">NOTES</span></span>

## <span data-ttu-id="5c0cc-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c0cc-136">RELATED LINKS</span></span>
