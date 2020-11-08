---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077655"
---
# <span data-ttu-id="5aedf-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="5aedf-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="5aedf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5aedf-102">SYNOPSIS</span></span>
<span data-ttu-id="5aedf-103">Добавляет подписку в группу управления.</span><span class="sxs-lookup"><span data-stu-id="5aedf-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="5aedf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5aedf-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5aedf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aedf-105">DESCRIPTION</span></span>
<span data-ttu-id="5aedf-106">Командлет **New-AzManagementGroupSubscription** Добавляет подписку в группу управления.</span><span class="sxs-lookup"><span data-stu-id="5aedf-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="5aedf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5aedf-107">EXAMPLES</span></span>

### <span data-ttu-id="5aedf-108">Пример 1: Добавление подписки в группу управления</span><span class="sxs-lookup"><span data-stu-id="5aedf-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="5aedf-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5aedf-109">PARAMETERS</span></span>

### <span data-ttu-id="5aedf-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aedf-110">-DefaultProfile</span></span>
<span data-ttu-id="5aedf-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5aedf-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aedf-112">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="5aedf-112">-GroupName</span></span>
<span data-ttu-id="5aedf-113">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="5aedf-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5aedf-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5aedf-114">-PassThru</span></span>
<span data-ttu-id="5aedf-115">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="5aedf-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="5aedf-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5aedf-116">-SubscriptionId</span></span>
<span data-ttu-id="5aedf-117">Идентификатор подписки, связанной с управлением</span><span class="sxs-lookup"><span data-stu-id="5aedf-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="5aedf-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aedf-118">-Confirm</span></span>
<span data-ttu-id="5aedf-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5aedf-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aedf-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aedf-120">-WhatIf</span></span>
<span data-ttu-id="5aedf-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5aedf-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aedf-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5aedf-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aedf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aedf-123">CommonParameters</span></span>
<span data-ttu-id="5aedf-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5aedf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aedf-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5aedf-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aedf-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5aedf-126">INPUTS</span></span>

### <span data-ttu-id="5aedf-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="5aedf-127">None</span></span>

## <span data-ttu-id="5aedf-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5aedf-128">OUTPUTS</span></span>

### <span data-ttu-id="5aedf-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5aedf-129">System.Boolean</span></span>

## <span data-ttu-id="5aedf-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5aedf-130">NOTES</span></span>

## <span data-ttu-id="5aedf-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5aedf-131">RELATED LINKS</span></span>
