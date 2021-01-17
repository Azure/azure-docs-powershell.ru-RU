---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408143"
---
# <span data-ttu-id="dc416-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="dc416-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="dc416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc416-102">SYNOPSIS</span></span>
<span data-ttu-id="dc416-103">Удаляет подписку из группы управления.</span><span class="sxs-lookup"><span data-stu-id="dc416-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="dc416-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc416-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc416-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc416-105">DESCRIPTION</span></span>
<span data-ttu-id="dc416-106">Для удаления подписки из группы управления будет отключена группа **AzManagementGroupSubscription.**</span><span class="sxs-lookup"><span data-stu-id="dc416-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="dc416-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc416-107">EXAMPLES</span></span>

### <span data-ttu-id="dc416-108">Пример 1. Удаление подписки из группы управления</span><span class="sxs-lookup"><span data-stu-id="dc416-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="dc416-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc416-109">PARAMETERS</span></span>

### <span data-ttu-id="dc416-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc416-110">-DefaultProfile</span></span>
<span data-ttu-id="dc416-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc416-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc416-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="dc416-112">-GroupName</span></span>
<span data-ttu-id="dc416-113">ИД группы управления</span><span class="sxs-lookup"><span data-stu-id="dc416-113">Management Group Id</span></span>

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

### <span data-ttu-id="dc416-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc416-114">-PassThru</span></span>
<span data-ttu-id="dc416-115">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="dc416-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="dc416-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc416-116">-SubscriptionId</span></span>
<span data-ttu-id="dc416-117">ИД подписки, связанной с управлением</span><span class="sxs-lookup"><span data-stu-id="dc416-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="dc416-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc416-118">-Confirm</span></span>
<span data-ttu-id="dc416-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc416-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc416-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc416-120">-WhatIf</span></span>
<span data-ttu-id="dc416-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc416-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc416-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc416-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc416-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc416-123">CommonParameters</span></span>
<span data-ttu-id="dc416-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc416-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc416-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc416-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc416-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc416-126">INPUTS</span></span>

### <span data-ttu-id="dc416-127">Нет</span><span class="sxs-lookup"><span data-stu-id="dc416-127">None</span></span>

## <span data-ttu-id="dc416-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc416-128">OUTPUTS</span></span>

### <span data-ttu-id="dc416-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc416-129">System.Boolean</span></span>

## <span data-ttu-id="dc416-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc416-130">NOTES</span></span>

## <span data-ttu-id="dc416-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc416-131">RELATED LINKS</span></span>
