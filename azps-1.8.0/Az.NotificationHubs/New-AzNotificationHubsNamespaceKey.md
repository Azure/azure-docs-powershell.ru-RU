---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/new-aznotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/New-AzNotificationHubsNamespaceKey.md
ms.openlocfilehash: 01ba4388d1cb6166c927096144e628d9fc2d81a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729888"
---
# <span data-ttu-id="6320b-101">New-AzNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="6320b-101">New-AzNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="6320b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6320b-102">SYNOPSIS</span></span>
<span data-ttu-id="6320b-103">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6320b-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

## <span data-ttu-id="6320b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6320b-104">SYNTAX</span></span>

```
New-AzNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6320b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6320b-105">DESCRIPTION</span></span>
<span data-ttu-id="6320b-106">New-AzNotificationHubNamespaceKey командлет повторно создает первичный ключ/вторичный ключ для правила авторизации пространства имен.</span><span class="sxs-lookup"><span data-stu-id="6320b-106">New-AzNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="6320b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6320b-107">EXAMPLES</span></span>

### <span data-ttu-id="6320b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6320b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="6320b-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="6320b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="6320b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6320b-110">PARAMETERS</span></span>

### <span data-ttu-id="6320b-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6320b-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="6320b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6320b-112">-DefaultProfile</span></span>
<span data-ttu-id="6320b-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6320b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6320b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6320b-114">-Force</span></span>
<span data-ttu-id="6320b-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="6320b-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6320b-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6320b-116">-Namespace</span></span>
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

### <span data-ttu-id="6320b-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="6320b-117">-PolicyKey</span></span>
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

### <span data-ttu-id="6320b-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6320b-118">-ResourceGroup</span></span>
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

### <span data-ttu-id="6320b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6320b-119">-Confirm</span></span>
<span data-ttu-id="6320b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6320b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6320b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6320b-121">-WhatIf</span></span>
<span data-ttu-id="6320b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6320b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6320b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6320b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6320b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6320b-124">CommonParameters</span></span>
<span data-ttu-id="6320b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6320b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6320b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6320b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6320b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6320b-127">INPUTS</span></span>

### <span data-ttu-id="6320b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6320b-128">System.String</span></span>

## <span data-ttu-id="6320b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6320b-129">OUTPUTS</span></span>

### <span data-ttu-id="6320b-130">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="6320b-130">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="6320b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6320b-131">NOTES</span></span>

## <span data-ttu-id="6320b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6320b-132">RELATED LINKS</span></span>
