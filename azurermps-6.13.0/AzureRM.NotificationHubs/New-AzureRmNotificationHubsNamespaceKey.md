---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 070befe362c6730b3592eac18cf8db70cd688716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564184"
---
# <span data-ttu-id="e5045-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="e5045-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="e5045-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5045-102">SYNOPSIS</span></span>
<span data-ttu-id="e5045-103">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e5045-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5045-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5045-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5045-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5045-105">DESCRIPTION</span></span>
<span data-ttu-id="e5045-106">New-AzureRmNotificationHubNamespaceKey командлет повторно создает первичный ключ/вторичный ключ для правила авторизации пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e5045-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="e5045-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5045-107">EXAMPLES</span></span>

### <span data-ttu-id="e5045-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5045-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e5045-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="e5045-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="e5045-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5045-110">PARAMETERS</span></span>

### <span data-ttu-id="e5045-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e5045-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="e5045-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5045-112">-DefaultProfile</span></span>
<span data-ttu-id="e5045-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e5045-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5045-114">-Force</span><span class="sxs-lookup"><span data-stu-id="e5045-114">-Force</span></span>
<span data-ttu-id="e5045-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e5045-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e5045-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5045-116">-Namespace</span></span>
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

### <span data-ttu-id="e5045-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="e5045-117">-PolicyKey</span></span>
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

### <span data-ttu-id="e5045-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5045-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="e5045-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5045-119">-Confirm</span></span>
<span data-ttu-id="e5045-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5045-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5045-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5045-121">-WhatIf</span></span>
<span data-ttu-id="e5045-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5045-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5045-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5045-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5045-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5045-124">CommonParameters</span></span>
<span data-ttu-id="e5045-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5045-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5045-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5045-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5045-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5045-127">INPUTS</span></span>

### <span data-ttu-id="e5045-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e5045-128">System.String</span></span>

## <span data-ttu-id="e5045-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5045-129">OUTPUTS</span></span>

### <span data-ttu-id="e5045-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="e5045-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="e5045-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5045-131">NOTES</span></span>

## <span data-ttu-id="e5045-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5045-132">RELATED LINKS</span></span>
