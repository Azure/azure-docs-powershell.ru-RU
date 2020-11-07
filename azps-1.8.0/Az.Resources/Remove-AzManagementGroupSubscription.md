---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: e5a7d0a8e7d000e9d4bdceae41d05990a93c71a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729342"
---
# <span data-ttu-id="2c25d-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="2c25d-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="2c25d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c25d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c25d-103">Удаляет подписку из группы управления.</span><span class="sxs-lookup"><span data-stu-id="2c25d-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="2c25d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c25d-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c25d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c25d-105">DESCRIPTION</span></span>
<span data-ttu-id="2c25d-106">Командлет **Remove-AzManagementGroupSubscription** удаляет подписку из группы управления.</span><span class="sxs-lookup"><span data-stu-id="2c25d-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="2c25d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c25d-107">EXAMPLES</span></span>

### <span data-ttu-id="2c25d-108">Пример 1: Удаление подписки из группы управления</span><span class="sxs-lookup"><span data-stu-id="2c25d-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="2c25d-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c25d-109">PARAMETERS</span></span>

### <span data-ttu-id="2c25d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c25d-110">-DefaultProfile</span></span>
<span data-ttu-id="2c25d-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c25d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c25d-112">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="2c25d-112">-GroupName</span></span>
<span data-ttu-id="2c25d-113">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="2c25d-113">Management Group Id</span></span>

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

### <span data-ttu-id="2c25d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c25d-114">-PassThru</span></span>
<span data-ttu-id="2c25d-115">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="2c25d-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="2c25d-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c25d-116">-SubscriptionId</span></span>
<span data-ttu-id="2c25d-117">Идентификатор подписки, связанной с управлением</span><span class="sxs-lookup"><span data-stu-id="2c25d-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="2c25d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c25d-118">-Confirm</span></span>
<span data-ttu-id="2c25d-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c25d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c25d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c25d-120">-WhatIf</span></span>
<span data-ttu-id="2c25d-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c25d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c25d-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c25d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c25d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c25d-123">CommonParameters</span></span>
<span data-ttu-id="2c25d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c25d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c25d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c25d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c25d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c25d-126">INPUTS</span></span>

### <span data-ttu-id="2c25d-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="2c25d-127">None</span></span>

## <span data-ttu-id="2c25d-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c25d-128">OUTPUTS</span></span>

### <span data-ttu-id="2c25d-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c25d-129">System.Boolean</span></span>

## <span data-ttu-id="2c25d-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c25d-130">NOTES</span></span>

## <span data-ttu-id="2c25d-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c25d-131">RELATED LINKS</span></span>
