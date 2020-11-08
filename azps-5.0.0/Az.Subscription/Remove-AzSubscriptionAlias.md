---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247973"
---
# <span data-ttu-id="691ba-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="691ba-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="691ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="691ba-102">SYNOPSIS</span></span>
<span data-ttu-id="691ba-103">Удаление псевдонима подписки</span><span class="sxs-lookup"><span data-stu-id="691ba-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="691ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="691ba-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="691ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="691ba-105">DESCRIPTION</span></span>
<span data-ttu-id="691ba-106">Командлет **Remove-AzSubscriptionAlias** удаляет псевдоним подписки.</span><span class="sxs-lookup"><span data-stu-id="691ba-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="691ba-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="691ba-107">EXAMPLES</span></span>

### <span data-ttu-id="691ba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="691ba-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="691ba-109">Удаление псевдонима подписки</span><span class="sxs-lookup"><span data-stu-id="691ba-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="691ba-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="691ba-110">PARAMETERS</span></span>

### <span data-ttu-id="691ba-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="691ba-111">-AliasName</span></span>
<span data-ttu-id="691ba-112">Псевдоним для подписки</span><span class="sxs-lookup"><span data-stu-id="691ba-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="691ba-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="691ba-113">-AsJob</span></span>
<span data-ttu-id="691ba-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="691ba-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="691ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="691ba-115">-DefaultProfile</span></span>
<span data-ttu-id="691ba-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="691ba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="691ba-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="691ba-117">-Confirm</span></span>
<span data-ttu-id="691ba-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="691ba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="691ba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="691ba-119">-WhatIf</span></span>
<span data-ttu-id="691ba-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="691ba-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="691ba-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="691ba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="691ba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="691ba-122">CommonParameters</span></span>
<span data-ttu-id="691ba-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="691ba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="691ba-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="691ba-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="691ba-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="691ba-125">INPUTS</span></span>

### <span data-ttu-id="691ba-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="691ba-126">None</span></span>

## <span data-ttu-id="691ba-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="691ba-127">OUTPUTS</span></span>

### <span data-ttu-id="691ba-128">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="691ba-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="691ba-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="691ba-129">NOTES</span></span>

## <span data-ttu-id="691ba-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="691ba-130">RELATED LINKS</span></span>
