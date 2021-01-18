---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516958"
---
# <span data-ttu-id="b8db9-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="b8db9-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="b8db9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8db9-102">SYNOPSIS</span></span>
<span data-ttu-id="b8db9-103">Получает сведения об псевдониме подписки</span><span class="sxs-lookup"><span data-stu-id="b8db9-103">Gets subscription alias details</span></span>

## <span data-ttu-id="b8db9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b8db9-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8db9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8db9-105">DESCRIPTION</span></span>
<span data-ttu-id="b8db9-106">Для получения сведений псевдонима подписки можно получить сведения о **get-AzSubscriptionAlias.**</span><span class="sxs-lookup"><span data-stu-id="b8db9-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="b8db9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b8db9-107">EXAMPLES</span></span>

### <span data-ttu-id="b8db9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8db9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="b8db9-109">Получает сведения об псевдониме подписки</span><span class="sxs-lookup"><span data-stu-id="b8db9-109">Gets subscription alias details</span></span>

## <span data-ttu-id="b8db9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8db9-110">PARAMETERS</span></span>

### <span data-ttu-id="b8db9-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="b8db9-111">-AliasName</span></span>
<span data-ttu-id="b8db9-112">Псевдоним подписки</span><span class="sxs-lookup"><span data-stu-id="b8db9-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8db9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8db9-113">-AsJob</span></span>
<span data-ttu-id="b8db9-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b8db9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b8db9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8db9-115">-DefaultProfile</span></span>
<span data-ttu-id="b8db9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8db9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8db9-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8db9-117">-Confirm</span></span>
<span data-ttu-id="b8db9-118">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b8db9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8db9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8db9-119">-WhatIf</span></span>
<span data-ttu-id="b8db9-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8db9-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8db9-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b8db9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8db9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8db9-122">CommonParameters</span></span>
<span data-ttu-id="b8db9-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8db9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8db9-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8db9-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8db9-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8db9-125">INPUTS</span></span>

### <span data-ttu-id="b8db9-126">Нет</span><span class="sxs-lookup"><span data-stu-id="b8db9-126">None</span></span>

## <span data-ttu-id="b8db9-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8db9-127">OUTPUTS</span></span>

### <span data-ttu-id="b8db9-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b8db9-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="b8db9-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b8db9-129">NOTES</span></span>

## <span data-ttu-id="b8db9-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8db9-130">RELATED LINKS</span></span>
