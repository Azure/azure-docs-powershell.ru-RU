---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 9dcf7b7d7149235d5a2ed211dbccf87415f1c496
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909289"
---
# <span data-ttu-id="e7935-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="e7935-101">Clear-AzContext</span></span>

## <span data-ttu-id="e7935-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7935-102">SYNOPSIS</span></span>
<span data-ttu-id="e7935-103">Удалите все учетные данные Azure, учетную запись и сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="e7935-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="e7935-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7935-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7935-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7935-105">DESCRIPTION</span></span>
<span data-ttu-id="e7935-106">Удалите все учетные данные Azure, учетную запись и сведения о подписке.</span><span class="sxs-lookup"><span data-stu-id="e7935-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="e7935-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7935-107">EXAMPLES</span></span>

### <span data-ttu-id="e7935-108">Очистка глобального контекста</span><span class="sxs-lookup"><span data-stu-id="e7935-108">Clear global context</span></span>
```
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="e7935-109">Удалите все учетные записи, подписки и учетные данные для любого сеанса PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e7935-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="e7935-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7935-110">PARAMETERS</span></span>

### <span data-ttu-id="e7935-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7935-111">-DefaultProfile</span></span>
<span data-ttu-id="e7935-112">Учетные данные, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e7935-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7935-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e7935-113">-Force</span></span>
<span data-ttu-id="e7935-114">Удаление всех пользователей и групп из глобальной области без запроса</span><span class="sxs-lookup"><span data-stu-id="e7935-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="e7935-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7935-115">-PassThru</span></span>
<span data-ttu-id="e7935-116">Возвращение значения, показывающего успешное выполнение или сбой</span><span class="sxs-lookup"><span data-stu-id="e7935-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="e7935-117">-Scope</span><span class="sxs-lookup"><span data-stu-id="e7935-117">-Scope</span></span>
<span data-ttu-id="e7935-118">Очистите контекст только для текущего сеанса PowerShell или для всех сеансов.</span><span class="sxs-lookup"><span data-stu-id="e7935-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="e7935-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e7935-119">-Confirm</span></span>
<span data-ttu-id="e7935-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e7935-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7935-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7935-121">-WhatIf</span></span>
<span data-ttu-id="e7935-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e7935-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7935-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e7935-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7935-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7935-124">CommonParameters</span></span>
<span data-ttu-id="e7935-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7935-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7935-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7935-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7935-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7935-127">INPUTS</span></span>

### <span data-ttu-id="e7935-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="e7935-128">None</span></span>

## <span data-ttu-id="e7935-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7935-129">OUTPUTS</span></span>

### <span data-ttu-id="e7935-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7935-130">System.Boolean</span></span>

## <span data-ttu-id="e7935-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7935-131">NOTES</span></span>

## <span data-ttu-id="e7935-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7935-132">RELATED LINKS</span></span>
