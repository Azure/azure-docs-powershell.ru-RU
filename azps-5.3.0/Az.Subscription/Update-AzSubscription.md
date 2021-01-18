---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516957"
---
# <span data-ttu-id="ca4c8-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="ca4c8-101">Update-AzSubscription</span></span>

## <span data-ttu-id="ca4c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca4c8-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4c8-103">Обновление подписки Azure</span><span class="sxs-lookup"><span data-stu-id="ca4c8-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="ca4c8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ca4c8-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca4c8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca4c8-105">DESCRIPTION</span></span>
<span data-ttu-id="ca4c8-106">На **основе cmdlet Update-AzSubscription** обновляется подписка Azure.</span><span class="sxs-lookup"><span data-stu-id="ca4c8-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="ca4c8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ca4c8-107">EXAMPLES</span></span>

### <span data-ttu-id="ca4c8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca4c8-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="ca4c8-109">Обновляет подписку</span><span class="sxs-lookup"><span data-stu-id="ca4c8-109">Updates the subscription</span></span>

## <span data-ttu-id="ca4c8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca4c8-110">PARAMETERS</span></span>

### <span data-ttu-id="ca4c8-111">-Action</span><span class="sxs-lookup"><span data-stu-id="ca4c8-111">-Action</span></span>
<span data-ttu-id="ca4c8-112">Действие по выполнению действия с подпиской</span><span class="sxs-lookup"><span data-stu-id="ca4c8-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="ca4c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca4c8-113">-AsJob</span></span>
<span data-ttu-id="ca4c8-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ca4c8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca4c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4c8-115">-DefaultProfile</span></span>
<span data-ttu-id="ca4c8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca4c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4c8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ca4c8-117">-Name</span></span>
<span data-ttu-id="ca4c8-118">Название подписки</span><span class="sxs-lookup"><span data-stu-id="ca4c8-118">Name of the subscription</span></span>

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

### <span data-ttu-id="ca4c8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca4c8-119">-SubscriptionId</span></span>
<span data-ttu-id="ca4c8-120">Обновление ИД подписки</span><span class="sxs-lookup"><span data-stu-id="ca4c8-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="ca4c8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca4c8-121">-Confirm</span></span>
<span data-ttu-id="ca4c8-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca4c8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca4c8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca4c8-123">-WhatIf</span></span>
<span data-ttu-id="ca4c8-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca4c8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca4c8-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ca4c8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca4c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4c8-126">CommonParameters</span></span>
<span data-ttu-id="ca4c8-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca4c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4c8-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca4c8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4c8-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ca4c8-129">INPUTS</span></span>

### <span data-ttu-id="ca4c8-130">Нет</span><span class="sxs-lookup"><span data-stu-id="ca4c8-130">None</span></span>

## <span data-ttu-id="ca4c8-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca4c8-131">OUTPUTS</span></span>

### <span data-ttu-id="ca4c8-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ca4c8-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ca4c8-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ca4c8-133">NOTES</span></span>

## <span data-ttu-id="ca4c8-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca4c8-134">RELATED LINKS</span></span>
