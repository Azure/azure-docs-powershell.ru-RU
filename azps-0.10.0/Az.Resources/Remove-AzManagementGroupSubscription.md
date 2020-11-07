---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-Azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: fe3d020bb32e120fe103dd8f90bfbb1d83d9a21d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910857"
---
# <span data-ttu-id="68765-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="68765-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="68765-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="68765-102">SYNOPSIS</span></span>
<span data-ttu-id="68765-103">Удаляет подписку из группы управления.</span><span class="sxs-lookup"><span data-stu-id="68765-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="68765-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="68765-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68765-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68765-105">DESCRIPTION</span></span>
<span data-ttu-id="68765-106">Командлет **Remove-AzManagementGroupSubscription** удаляет подписку из группы управления.</span><span class="sxs-lookup"><span data-stu-id="68765-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="68765-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="68765-107">EXAMPLES</span></span>

### <span data-ttu-id="68765-108">Пример 1: Удаление подписки из группы управления</span><span class="sxs-lookup"><span data-stu-id="68765-108">Example 1 - Remove Subscription from a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="68765-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="68765-109">PARAMETERS</span></span>

### <span data-ttu-id="68765-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68765-110">-DefaultProfile</span></span>
<span data-ttu-id="68765-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68765-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68765-112">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="68765-112">-GroupName</span></span>
<span data-ttu-id="68765-113">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="68765-113">Management Group Id</span></span>

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

### <span data-ttu-id="68765-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68765-114">-PassThru</span></span>
<span data-ttu-id="68765-115">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="68765-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="68765-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68765-116">-SubscriptionId</span></span>
<span data-ttu-id="68765-117">Идентификатор подписки, связанной с управлением</span><span class="sxs-lookup"><span data-stu-id="68765-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="68765-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68765-118">-Confirm</span></span>
<span data-ttu-id="68765-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="68765-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68765-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68765-120">-WhatIf</span></span>
<span data-ttu-id="68765-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="68765-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68765-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="68765-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68765-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68765-123">CommonParameters</span></span>
<span data-ttu-id="68765-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="68765-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68765-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68765-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68765-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="68765-126">INPUTS</span></span>

### <span data-ttu-id="68765-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="68765-127">None</span></span>

## <span data-ttu-id="68765-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="68765-128">OUTPUTS</span></span>

### <span data-ttu-id="68765-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68765-129">System.Boolean</span></span>

## <span data-ttu-id="68765-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="68765-130">NOTES</span></span>

## <span data-ttu-id="68765-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68765-131">RELATED LINKS</span></span>
