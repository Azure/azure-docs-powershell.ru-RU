---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: a3ef84ef6740eb0d505ff2f9f69670ea83242deb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912551"
---
# <span data-ttu-id="c150c-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="c150c-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="c150c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c150c-102">SYNOPSIS</span></span>
<span data-ttu-id="c150c-103">Добавляет подписку в группу управления.</span><span class="sxs-lookup"><span data-stu-id="c150c-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="c150c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c150c-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c150c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c150c-105">DESCRIPTION</span></span>
<span data-ttu-id="c150c-106">Командлет **New-AzManagementGroupSubscription** Добавляет подписку в группу управления.</span><span class="sxs-lookup"><span data-stu-id="c150c-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="c150c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c150c-107">EXAMPLES</span></span>

### <span data-ttu-id="c150c-108">Пример 1: Добавление подписки в группу управления</span><span class="sxs-lookup"><span data-stu-id="c150c-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="c150c-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c150c-109">PARAMETERS</span></span>

### <span data-ttu-id="c150c-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c150c-110">-DefaultProfile</span></span>
<span data-ttu-id="c150c-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c150c-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c150c-112">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="c150c-112">-GroupName</span></span>
<span data-ttu-id="c150c-113">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="c150c-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c150c-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c150c-114">-PassThru</span></span>
<span data-ttu-id="c150c-115">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="c150c-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="c150c-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c150c-116">-SubscriptionId</span></span>
<span data-ttu-id="c150c-117">Идентификатор подписки, связанной с управлением</span><span class="sxs-lookup"><span data-stu-id="c150c-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c150c-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c150c-118">-Confirm</span></span>
<span data-ttu-id="c150c-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c150c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c150c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c150c-120">-WhatIf</span></span>
<span data-ttu-id="c150c-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c150c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c150c-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c150c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c150c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c150c-123">CommonParameters</span></span>
<span data-ttu-id="c150c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c150c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c150c-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c150c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c150c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c150c-126">INPUTS</span></span>

### <span data-ttu-id="c150c-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c150c-127">None</span></span>

## <span data-ttu-id="c150c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c150c-128">OUTPUTS</span></span>

### <span data-ttu-id="c150c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c150c-129">System.Boolean</span></span>

## <span data-ttu-id="c150c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="c150c-130">NOTES</span></span>

## <span data-ttu-id="c150c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c150c-131">RELATED LINKS</span></span>
