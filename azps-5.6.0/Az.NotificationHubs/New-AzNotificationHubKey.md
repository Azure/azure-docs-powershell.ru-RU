---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 8c6b24dd2d208ea4465138f1e901b030ee5c30e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951267"
---
# <span data-ttu-id="600a4-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="600a4-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="600a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="600a4-102">SYNOPSIS</span></span>
<span data-ttu-id="600a4-103">Повторно сгенерировать ключ правила авторизации для NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="600a4-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="600a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="600a4-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="600a4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="600a4-105">DESCRIPTION</span></span>
<span data-ttu-id="600a4-106">New-AzNotificationHubKey сгенерирует первичный и дополнительный ключ для правила авторизации NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="600a4-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="600a4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="600a4-107">EXAMPLES</span></span>

### <span data-ttu-id="600a4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="600a4-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="600a4-109">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="600a4-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="600a4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="600a4-110">PARAMETERS</span></span>

### <span data-ttu-id="600a4-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="600a4-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600a4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="600a4-112">-DefaultProfile</span></span>
<span data-ttu-id="600a4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="600a4-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="600a4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="600a4-114">-Force</span></span>
<span data-ttu-id="600a4-115">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="600a4-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="600a4-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="600a4-116">-Namespace</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600a4-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="600a4-117">-NotificationHub</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600a4-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="600a4-118">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="600a4-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="600a4-119">-ResourceGroup</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="600a4-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="600a4-120">-Confirm</span></span>
<span data-ttu-id="600a4-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="600a4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="600a4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="600a4-122">-WhatIf</span></span>
<span data-ttu-id="600a4-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="600a4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="600a4-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="600a4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="600a4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="600a4-125">CommonParameters</span></span>
<span data-ttu-id="600a4-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="600a4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="600a4-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="600a4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="600a4-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="600a4-128">INPUTS</span></span>

### <span data-ttu-id="600a4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="600a4-129">System.String</span></span>

## <span data-ttu-id="600a4-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="600a4-130">OUTPUTS</span></span>

### <span data-ttu-id="600a4-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="600a4-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="600a4-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="600a4-132">NOTES</span></span>

## <span data-ttu-id="600a4-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="600a4-133">RELATED LINKS</span></span>
