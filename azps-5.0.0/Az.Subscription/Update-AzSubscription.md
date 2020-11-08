---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247971"
---
# <span data-ttu-id="3e4d8-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="3e4d8-101">Update-AzSubscription</span></span>

## <span data-ttu-id="3e4d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e4d8-102">SYNOPSIS</span></span>
<span data-ttu-id="3e4d8-103">Обновляет подписку Azure</span><span class="sxs-lookup"><span data-stu-id="3e4d8-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="3e4d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e4d8-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e4d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4d8-105">DESCRIPTION</span></span>
<span data-ttu-id="3e4d8-106">Командлет **Update-AzSubscription** обновляет подписку на Azure</span><span class="sxs-lookup"><span data-stu-id="3e4d8-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="3e4d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e4d8-107">EXAMPLES</span></span>

### <span data-ttu-id="3e4d8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e4d8-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="3e4d8-109">Обновляет подписку.</span><span class="sxs-lookup"><span data-stu-id="3e4d8-109">Updates the subscription</span></span>

## <span data-ttu-id="3e4d8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e4d8-110">PARAMETERS</span></span>

### <span data-ttu-id="3e4d8-111">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="3e4d8-111">-Action</span></span>
<span data-ttu-id="3e4d8-112">Действие, которое нужно выполнить для подписки</span><span class="sxs-lookup"><span data-stu-id="3e4d8-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="3e4d8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e4d8-113">-AsJob</span></span>
<span data-ttu-id="3e4d8-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3e4d8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3e4d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e4d8-115">-DefaultProfile</span></span>
<span data-ttu-id="3e4d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e4d8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e4d8-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e4d8-117">-Name</span></span>
<span data-ttu-id="3e4d8-118">Имя подписки</span><span class="sxs-lookup"><span data-stu-id="3e4d8-118">Name of the subscription</span></span>

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

### <span data-ttu-id="3e4d8-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e4d8-119">-SubscriptionId</span></span>
<span data-ttu-id="3e4d8-120">Идентификатор подписки для обновления</span><span class="sxs-lookup"><span data-stu-id="3e4d8-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="3e4d8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e4d8-121">-Confirm</span></span>
<span data-ttu-id="3e4d8-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4d8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e4d8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e4d8-123">-WhatIf</span></span>
<span data-ttu-id="3e4d8-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3e4d8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e4d8-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3e4d8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e4d8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e4d8-126">CommonParameters</span></span>
<span data-ttu-id="3e4d8-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e4d8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e4d8-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e4d8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e4d8-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e4d8-129">INPUTS</span></span>

### <span data-ttu-id="3e4d8-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3e4d8-130">None</span></span>

## <span data-ttu-id="3e4d8-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e4d8-131">OUTPUTS</span></span>

### <span data-ttu-id="3e4d8-132">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3e4d8-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="3e4d8-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e4d8-133">NOTES</span></span>

## <span data-ttu-id="3e4d8-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e4d8-134">RELATED LINKS</span></span>
