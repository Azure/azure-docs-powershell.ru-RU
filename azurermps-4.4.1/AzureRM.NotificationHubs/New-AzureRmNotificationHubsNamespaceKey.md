---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: ba33dd46a899f03539c39e61368570fb2bce0537
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562352"
---
# <span data-ttu-id="b84e5-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="b84e5-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="b84e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b84e5-102">SYNOPSIS</span></span>
<span data-ttu-id="b84e5-103">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b84e5-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b84e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b84e5-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b84e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b84e5-105">DESCRIPTION</span></span>
<span data-ttu-id="b84e5-106">New-AzureRmNotificationHubNamespaceKey командлет повторно создает первичный ключ/вторичный ключ для правила авторизации пространства имен.</span><span class="sxs-lookup"><span data-stu-id="b84e5-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="b84e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b84e5-107">EXAMPLES</span></span>

### <span data-ttu-id="b84e5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b84e5-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b84e5-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="b84e5-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b84e5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b84e5-110">PARAMETERS</span></span>

### <span data-ttu-id="b84e5-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b84e5-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="b84e5-112">-Force</span><span class="sxs-lookup"><span data-stu-id="b84e5-112">-Force</span></span>
<span data-ttu-id="b84e5-113">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b84e5-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b84e5-114">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b84e5-114">-Namespace</span></span>
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

### <span data-ttu-id="b84e5-115">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="b84e5-115">-PolicyKey</span></span>
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

### <span data-ttu-id="b84e5-116">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b84e5-116">-ResourceGroup</span></span>
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

### <span data-ttu-id="b84e5-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b84e5-117">-Confirm</span></span>
<span data-ttu-id="b84e5-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b84e5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b84e5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b84e5-119">-WhatIf</span></span>
<span data-ttu-id="b84e5-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b84e5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b84e5-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b84e5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b84e5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b84e5-122">-DefaultProfile</span></span>
<span data-ttu-id="b84e5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b84e5-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b84e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b84e5-124">CommonParameters</span></span>
<span data-ttu-id="b84e5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b84e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b84e5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b84e5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b84e5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b84e5-127">INPUTS</span></span>

## <span data-ttu-id="b84e5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b84e5-128">OUTPUTS</span></span>

### <span data-ttu-id="b84e5-129">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="b84e5-129">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="b84e5-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b84e5-130">NOTES</span></span>

## <span data-ttu-id="b84e5-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b84e5-131">RELATED LINKS</span></span>

