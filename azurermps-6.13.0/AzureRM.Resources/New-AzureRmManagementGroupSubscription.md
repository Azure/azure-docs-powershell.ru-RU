---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmManagementGroupSubscription.md
ms.openlocfilehash: a3c75c653d75a4fde969672a245644ee04412731
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556512"
---
# <span data-ttu-id="367cd-101">New-AzureRmManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="367cd-101">New-AzureRmManagementGroupSubscription</span></span>

## <span data-ttu-id="367cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="367cd-102">SYNOPSIS</span></span>
<span data-ttu-id="367cd-103">Добавляет подписку в группу управления.</span><span class="sxs-lookup"><span data-stu-id="367cd-103">Adds a Subscription to a Management Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="367cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="367cd-104">SYNTAX</span></span>

```
New-AzureRmManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="367cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="367cd-105">DESCRIPTION</span></span>
<span data-ttu-id="367cd-106">Командлет **New-AzureRMManagementGroupSubscription** Добавляет подписку в группу управления.</span><span class="sxs-lookup"><span data-stu-id="367cd-106">The **New-AzureRMManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="367cd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="367cd-107">EXAMPLES</span></span>

### <span data-ttu-id="367cd-108">Пример 1: Добавление подписки в группу управления</span><span class="sxs-lookup"><span data-stu-id="367cd-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzureRMManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="367cd-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="367cd-109">PARAMETERS</span></span>

### <span data-ttu-id="367cd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="367cd-110">-DefaultProfile</span></span>
<span data-ttu-id="367cd-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="367cd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="367cd-112">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="367cd-112">-GroupName</span></span>
<span data-ttu-id="367cd-113">Идентификатор группы управления</span><span class="sxs-lookup"><span data-stu-id="367cd-113">Management Group Id</span></span>

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

### <span data-ttu-id="367cd-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="367cd-114">-PassThru</span></span>
<span data-ttu-id="367cd-115">Возврат `true` к успешному выполнению</span><span class="sxs-lookup"><span data-stu-id="367cd-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="367cd-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="367cd-116">-SubscriptionId</span></span>
<span data-ttu-id="367cd-117">Идентификатор подписки, связанной с управлением</span><span class="sxs-lookup"><span data-stu-id="367cd-117">Subscription Id of the subscription associated witht the management</span></span>

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

### <span data-ttu-id="367cd-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="367cd-118">-Confirm</span></span>
<span data-ttu-id="367cd-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="367cd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="367cd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="367cd-120">-WhatIf</span></span>
<span data-ttu-id="367cd-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="367cd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="367cd-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="367cd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="367cd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="367cd-123">CommonParameters</span></span>
<span data-ttu-id="367cd-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="367cd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="367cd-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="367cd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="367cd-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="367cd-126">INPUTS</span></span>

### <span data-ttu-id="367cd-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="367cd-127">None</span></span>

## <span data-ttu-id="367cd-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="367cd-128">OUTPUTS</span></span>

### <span data-ttu-id="367cd-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="367cd-129">System.Boolean</span></span>

## <span data-ttu-id="367cd-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="367cd-130">NOTES</span></span>

## <span data-ttu-id="367cd-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="367cd-131">RELATED LINKS</span></span>
