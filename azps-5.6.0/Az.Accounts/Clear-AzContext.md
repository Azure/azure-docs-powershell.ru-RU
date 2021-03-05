---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 8db930fe362d25a7b1069af6c3855ef71644e874
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990629"
---
# <span data-ttu-id="103df-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="103df-101">Clear-AzContext</span></span>

## <span data-ttu-id="103df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="103df-102">SYNOPSIS</span></span>
<span data-ttu-id="103df-103">Удалите все учетные данные Azure, учетную запись и данные подписки.</span><span class="sxs-lookup"><span data-stu-id="103df-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="103df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="103df-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="103df-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="103df-105">DESCRIPTION</span></span>
<span data-ttu-id="103df-106">Удалите все учетные данные Azure, учетную запись и сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="103df-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="103df-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="103df-107">EXAMPLES</span></span>

### <span data-ttu-id="103df-108">Пример 1. Очистка глобального контекста</span><span class="sxs-lookup"><span data-stu-id="103df-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="103df-109">Удалите все данные учетной записи, подписки и учетных данных для сеанса Powershell.</span><span class="sxs-lookup"><span data-stu-id="103df-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="103df-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="103df-110">PARAMETERS</span></span>

### <span data-ttu-id="103df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="103df-111">-DefaultProfile</span></span>
<span data-ttu-id="103df-112">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="103df-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="103df-113">-Force</span><span class="sxs-lookup"><span data-stu-id="103df-113">-Force</span></span>
<span data-ttu-id="103df-114">Удаление всех пользователей и групп из глобальной области без запроса</span><span class="sxs-lookup"><span data-stu-id="103df-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="103df-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="103df-115">-PassThru</span></span>
<span data-ttu-id="103df-116">Возвращает значение, указывающее на успех или неудачу.</span><span class="sxs-lookup"><span data-stu-id="103df-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="103df-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="103df-117">-Scope</span></span>
<span data-ttu-id="103df-118">Очистить контекст можно только для текущего сеанса PowerShell или для всех сеансов.</span><span class="sxs-lookup"><span data-stu-id="103df-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="103df-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="103df-119">-Confirm</span></span>
<span data-ttu-id="103df-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="103df-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="103df-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103df-121">-WhatIf</span></span>
<span data-ttu-id="103df-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="103df-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="103df-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="103df-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="103df-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103df-124">CommonParameters</span></span>
<span data-ttu-id="103df-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103df-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103df-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="103df-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103df-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="103df-127">INPUTS</span></span>

### <span data-ttu-id="103df-128">Нет</span><span class="sxs-lookup"><span data-stu-id="103df-128">None</span></span>

## <span data-ttu-id="103df-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="103df-129">OUTPUTS</span></span>

### <span data-ttu-id="103df-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="103df-130">System.Boolean</span></span>

## <span data-ttu-id="103df-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="103df-131">NOTES</span></span>

## <span data-ttu-id="103df-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="103df-132">RELATED LINKS</span></span>
