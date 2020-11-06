---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: A03F32C3-BB01-46A5-86C5-B7A4DDC42351
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubKey.md
ms.openlocfilehash: d129d34ab9bcbcd67a7c643e4f412bacf262b293
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568858"
---
# <span data-ttu-id="b9132-101">New-AzureRmNotificationHubKey</span><span class="sxs-lookup"><span data-stu-id="b9132-101">New-AzureRmNotificationHubKey</span></span>

## <span data-ttu-id="b9132-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9132-102">SYNOPSIS</span></span>
<span data-ttu-id="b9132-103">Повторное создание ключа правила авторизации для NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="b9132-103">Regenerate the Authorization Rule Key for a NotificationHub .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9132-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9132-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubKey [-ResourceGroup] <String> [-Namespace] <String> [-NotificationHub] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9132-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9132-105">DESCRIPTION</span></span>
<span data-ttu-id="b9132-106">New-AzureRmNotificationHubKey командлет повторно создает первичный ключ/вторичный ключ для правила авторизации NotificationHub.</span><span class="sxs-lookup"><span data-stu-id="b9132-106">New-AzureRmNotificationHubKey cmdlet regenerates the Primary Key/Secondary Key for the NotificationHub Authorization Rule.</span></span>

## <span data-ttu-id="b9132-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9132-107">EXAMPLES</span></span>

### <span data-ttu-id="b9132-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9132-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="b9132-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="b9132-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b9132-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9132-110">PARAMETERS</span></span>

### <span data-ttu-id="b9132-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b9132-111">-AuthorizationRule</span></span>
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

### <span data-ttu-id="b9132-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9132-112">-DefaultProfile</span></span>
<span data-ttu-id="b9132-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b9132-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b9132-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b9132-114">-Force</span></span>
<span data-ttu-id="b9132-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b9132-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b9132-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b9132-116">-Namespace</span></span>
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

### <span data-ttu-id="b9132-117">-NotificationHub</span><span class="sxs-lookup"><span data-stu-id="b9132-117">-NotificationHub</span></span>
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

### <span data-ttu-id="b9132-118">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="b9132-118">-PolicyKey</span></span>
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

### <span data-ttu-id="b9132-119">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b9132-119">-ResourceGroup</span></span>
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

### <span data-ttu-id="b9132-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9132-120">-Confirm</span></span>
<span data-ttu-id="b9132-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9132-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9132-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9132-122">-WhatIf</span></span>
<span data-ttu-id="b9132-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9132-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9132-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9132-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9132-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9132-125">CommonParameters</span></span>
<span data-ttu-id="b9132-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9132-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9132-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9132-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9132-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9132-128">INPUTS</span></span>

### <span data-ttu-id="b9132-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b9132-129">System.String</span></span>

## <span data-ttu-id="b9132-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9132-130">OUTPUTS</span></span>

### <span data-ttu-id="b9132-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="b9132-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="b9132-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9132-132">NOTES</span></span>

## <span data-ttu-id="b9132-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9132-133">RELATED LINKS</span></span>
