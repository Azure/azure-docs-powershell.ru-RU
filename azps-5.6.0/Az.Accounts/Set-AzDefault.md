---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azdefault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzDefault.md
ms.openlocfilehash: 98e7877ba075aacc1da00291bb557c2e94e276e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010099"
---
# <span data-ttu-id="62328-101">Set-AzDefault</span><span class="sxs-lookup"><span data-stu-id="62328-101">Set-AzDefault</span></span>

## <span data-ttu-id="62328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62328-102">SYNOPSIS</span></span>
<span data-ttu-id="62328-103">Задает значение по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="62328-103">Sets a default in the current context</span></span>

## <span data-ttu-id="62328-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62328-104">SYNTAX</span></span>

```
Set-AzDefault [-ResourceGroupName <String>] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62328-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62328-105">DESCRIPTION</span></span>
<span data-ttu-id="62328-106">Этот Set-AzDefault добавляет или изменяет значения по умолчанию в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="62328-106">The Set-AzDefault cmdlet adds or changes the defaults in the current context.</span></span>

## <span data-ttu-id="62328-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62328-107">EXAMPLES</span></span>

### <span data-ttu-id="62328-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62328-108">Example 1</span></span>
```
PS C:\> Set-AzDefault -ResourceGroupName myResourceGroup

Id         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/myResourceGroup
Name       : myResourceGroup
Properties : Microsoft.Azure.Management.Internal.Resources.Models.ResourceGroupProperties
Location   : eastus
ManagedBy  :
Tags       :
```

<span data-ttu-id="62328-109">Эта команда задает группу ресурсов по умолчанию группе ресурсов, указанной пользователем.</span><span class="sxs-lookup"><span data-stu-id="62328-109">This command sets the default resource group to the resource group specified by the user.</span></span>

## <span data-ttu-id="62328-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62328-110">PARAMETERS</span></span>

### <span data-ttu-id="62328-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62328-111">-DefaultProfile</span></span>
<span data-ttu-id="62328-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62328-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62328-113">-Force</span><span class="sxs-lookup"><span data-stu-id="62328-113">-Force</span></span>
<span data-ttu-id="62328-114">Создание группы ресурсов, если указанное значение по умолчанию не существует</span><span class="sxs-lookup"><span data-stu-id="62328-114">Create a new resource group if specified default does not exist</span></span>

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

### <span data-ttu-id="62328-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62328-115">-ResourceGroupName</span></span>
<span data-ttu-id="62328-116">Имя группы ресурсов, за которая устанавливается по умолчанию</span><span class="sxs-lookup"><span data-stu-id="62328-116">Name of the resource group being set as default</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62328-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="62328-117">-Scope</span></span>
<span data-ttu-id="62328-118">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="62328-118">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="62328-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62328-119">-Confirm</span></span>
<span data-ttu-id="62328-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="62328-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62328-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62328-121">-WhatIf</span></span>
<span data-ttu-id="62328-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62328-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62328-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="62328-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62328-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62328-124">CommonParameters</span></span>
<span data-ttu-id="62328-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62328-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62328-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62328-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62328-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62328-127">INPUTS</span></span>

### <span data-ttu-id="62328-128">System.String</span><span class="sxs-lookup"><span data-stu-id="62328-128">System.String</span></span>

## <span data-ttu-id="62328-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62328-129">OUTPUTS</span></span>

### <span data-ttu-id="62328-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62328-130">Microsoft.Azure.Commands.Profile.Models.PSResourceGroup</span></span>

## <span data-ttu-id="62328-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62328-131">NOTES</span></span>

## <span data-ttu-id="62328-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62328-132">RELATED LINKS</span></span>
