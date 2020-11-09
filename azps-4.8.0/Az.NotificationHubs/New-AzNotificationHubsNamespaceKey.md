---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: a575ae0151cd28a9bcc3580a77ad3a0c79a2984b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244748"
---
# <span data-ttu-id="40fdd-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="40fdd-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="40fdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40fdd-102">SYNOPSIS</span></span>
<span data-ttu-id="40fdd-103">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="40fdd-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="40fdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40fdd-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40fdd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40fdd-105">DESCRIPTION</span></span>
<span data-ttu-id="40fdd-106">New-AzNotificationHubNamespaceKey командлет повторно создает первичный ключ/вторичный ключ для правила авторизации пространства имен.</span><span class="sxs-lookup"><span data-stu-id="40fdd-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="40fdd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40fdd-107">EXAMPLES</span></span>

### <span data-ttu-id="40fdd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40fdd-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="40fdd-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="40fdd-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="40fdd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40fdd-110">PARAMETERS</span></span>

### <span data-ttu-id="40fdd-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="40fdd-111">-AuthorizationRule</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40fdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40fdd-112">-DefaultProfile</span></span>
<span data-ttu-id="40fdd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="40fdd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40fdd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="40fdd-114">-Force</span></span>
<span data-ttu-id="40fdd-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="40fdd-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="40fdd-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="40fdd-116">-Namespace</span></span>
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

### <span data-ttu-id="40fdd-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="40fdd-117">-PolicyKey</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40fdd-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="40fdd-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="40fdd-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40fdd-119">-Confirm</span></span>
<span data-ttu-id="40fdd-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="40fdd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40fdd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40fdd-121">-WhatIf</span></span>
<span data-ttu-id="40fdd-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="40fdd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40fdd-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="40fdd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40fdd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40fdd-124">CommonParameters</span></span>
<span data-ttu-id="40fdd-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40fdd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40fdd-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40fdd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40fdd-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40fdd-127">INPUTS</span></span>

### <span data-ttu-id="40fdd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="40fdd-128">System.String</span></span>

## <span data-ttu-id="40fdd-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40fdd-129">OUTPUTS</span></span>

### <span data-ttu-id="40fdd-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="40fdd-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="40fdd-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="40fdd-131">NOTES</span></span>

## <span data-ttu-id="40fdd-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40fdd-132">RELATED LINKS</span></span>