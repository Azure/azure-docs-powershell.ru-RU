---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 2acca5ede1d6ef7e4a3767b87053fb356555993d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971651"
---
# <span data-ttu-id="bc5c6-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="bc5c6-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="bc5c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc5c6-102">SYNOPSIS</span></span>
<span data-ttu-id="bc5c6-103">Удаление псевдонима подписки</span><span class="sxs-lookup"><span data-stu-id="bc5c6-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="bc5c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc5c6-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc5c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc5c6-105">DESCRIPTION</span></span>
<span data-ttu-id="bc5c6-106">Для удаления псевдонима подписки будет удаляется cmdlet **Remove-AzSubscriptionAlias.**</span><span class="sxs-lookup"><span data-stu-id="bc5c6-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="bc5c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc5c6-107">EXAMPLES</span></span>

### <span data-ttu-id="bc5c6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bc5c6-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="bc5c6-109">Удаление псевдонима подписки</span><span class="sxs-lookup"><span data-stu-id="bc5c6-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="bc5c6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc5c6-110">PARAMETERS</span></span>

### <span data-ttu-id="bc5c6-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="bc5c6-111">-AliasName</span></span>
<span data-ttu-id="bc5c6-112">Псевдоним подписки</span><span class="sxs-lookup"><span data-stu-id="bc5c6-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc5c6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc5c6-113">-AsJob</span></span>
<span data-ttu-id="bc5c6-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bc5c6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bc5c6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc5c6-115">-DefaultProfile</span></span>
<span data-ttu-id="bc5c6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc5c6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc5c6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc5c6-117">-Confirm</span></span>
<span data-ttu-id="bc5c6-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5c6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc5c6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc5c6-119">-WhatIf</span></span>
<span data-ttu-id="bc5c6-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc5c6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc5c6-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc5c6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc5c6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc5c6-122">CommonParameters</span></span>
<span data-ttu-id="bc5c6-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc5c6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc5c6-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc5c6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc5c6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc5c6-125">INPUTS</span></span>

### <span data-ttu-id="bc5c6-126">Нет</span><span class="sxs-lookup"><span data-stu-id="bc5c6-126">None</span></span>

## <span data-ttu-id="bc5c6-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc5c6-127">OUTPUTS</span></span>

### <span data-ttu-id="bc5c6-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="bc5c6-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="bc5c6-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc5c6-129">NOTES</span></span>

## <span data-ttu-id="bc5c6-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc5c6-130">RELATED LINKS</span></span>
