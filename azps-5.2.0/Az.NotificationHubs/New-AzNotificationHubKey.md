---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubKey.md
ms.openlocfilehash: 071f5a7b28b6b6b49e965cc118a4a863cbd0142b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404903"
---
# <span data-ttu-id="824aa-101">New-AzNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="824aa-101">New-AzNotificationHubKey</span></span>

## <span data-ttu-id="824aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824aa-102">SYNOPSIS</span></span>
<span data-ttu-id="824aa-103">Повторно сгенерировать ключ правила авторизации для NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="824aa-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

## <span data-ttu-id="824aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="824aa-104">SYNTAX</span></span>

```
New-AzNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824aa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="824aa-105">DESCRIPTION</span></span>
<span data-ttu-id="824aa-106">New-AzNotificationHubKey повторно сгенерирует первичный и дополнительный ключ для правила авторизации NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="824aa-106">New-AzNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="824aa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="824aa-107">EXAMPLES</span></span>

### <span data-ttu-id="824aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="824aa-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="824aa-109">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="824aa-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="824aa-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="824aa-110">PARAMETERS</span></span>

### <span data-ttu-id="824aa-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="824aa-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="824aa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824aa-112">-DefaultProfile</span></span>
<span data-ttu-id="824aa-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="824aa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="824aa-114">-Force</span><span class="sxs-lookup"><span data-stu-id="824aa-114">-Force</span></span>
<span data-ttu-id="824aa-115">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="824aa-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="824aa-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="824aa-116">-Namespace</span></span>
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

### <span data-ttu-id="824aa-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="824aa-117">-NotificationHub</span></span>
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

### <span data-ttu-id="824aa-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="824aa-118">-PolicyKey</span></span>
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

### <span data-ttu-id="824aa-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="824aa-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="824aa-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="824aa-120">-Confirm</span></span>
<span data-ttu-id="824aa-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824aa-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824aa-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824aa-122">-WhatIf</span></span>
<span data-ttu-id="824aa-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824aa-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824aa-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="824aa-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824aa-125">CommonParameters</span></span>
<span data-ttu-id="824aa-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824aa-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="824aa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824aa-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="824aa-128">INPUTS</span></span>

### <span data-ttu-id="824aa-129">System.String</span><span class="sxs-lookup"><span data-stu-id="824aa-129">System.String</span></span>

## <span data-ttu-id="824aa-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="824aa-130">OUTPUTS</span></span>

### <span data-ttu-id="824aa-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="824aa-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="824aa-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="824aa-132">NOTES</span></span>

## <span data-ttu-id="824aa-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="824aa-133">RELATED LINKS</span></span>
