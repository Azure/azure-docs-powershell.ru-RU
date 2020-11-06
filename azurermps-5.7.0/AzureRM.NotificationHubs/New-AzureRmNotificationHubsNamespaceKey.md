---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 1EC19069-B64C-4F0F-99A3-07C16E46C0A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespacekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceKey.md
ms.openlocfilehash: 4756402ab46deb0260db19474a26e2c568055187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568552"
---
# <span data-ttu-id="44ef9-101">New-AzureRmNotificationHubsNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="44ef9-101">New-AzureRmNotificationHubsNamespaceKey</span></span>

## <span data-ttu-id="44ef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="44ef9-103">Повторное создание ключа правила авторизации для пространства имен.</span><span class="sxs-lookup"><span data-stu-id="44ef9-103">Regenerate the Authorization Rule Key for a Namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44ef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44ef9-104">SYNTAX</span></span>

```
New-AzureRmNotificationHubsNamespaceKey [-ResourceGroup] <String> [-Namespace] <String>
 [[-AuthorizationRule] <String>] [-PolicyKey] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44ef9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="44ef9-106">New-AzureRmNotificationHubNamespaceKey командлет повторно создает первичный ключ/вторичный ключ для правила авторизации пространства имен.</span><span class="sxs-lookup"><span data-stu-id="44ef9-106">New-AzureRmNotificationHubNamespaceKey cmdlet regenerates the Primary Key/Secondary Key for the Namespace Authorization Rule.</span></span>

## <span data-ttu-id="44ef9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="44ef9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44ef9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="44ef9-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="44ef9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="44ef9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44ef9-110">PARAMETERS</span></span>

### <span data-ttu-id="44ef9-111">-AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="44ef9-111">-AuthorizationRule</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ef9-112">-DefaultProfile</span></span>
<span data-ttu-id="44ef9-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="44ef9-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-114">-Force</span><span class="sxs-lookup"><span data-stu-id="44ef9-114">-Force</span></span>
<span data-ttu-id="44ef9-115">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="44ef9-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="44ef9-116">-Namespace</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-117">-PolicyKey</span><span class="sxs-lookup"><span data-stu-id="44ef9-117">-PolicyKey</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-118">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="44ef9-118">-ResourceGroup</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44ef9-119">-Confirm</span></span>
<span data-ttu-id="44ef9-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44ef9-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ef9-121">-WhatIf</span></span>
<span data-ttu-id="44ef9-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44ef9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ef9-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44ef9-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ef9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ef9-124">CommonParameters</span></span>
<span data-ttu-id="44ef9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44ef9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ef9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44ef9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ef9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44ef9-127">INPUTS</span></span>

### <span data-ttu-id="44ef9-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="44ef9-128">None</span></span>
<span data-ttu-id="44ef9-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="44ef9-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="44ef9-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44ef9-130">OUTPUTS</span></span>

### <span data-ttu-id="44ef9-131">Microsoft. Azure. Management. NotificationHubs. Models. ResourceListKeys</span><span class="sxs-lookup"><span data-stu-id="44ef9-131">Microsoft.Azure.Management.NotificationHubs.Models.ResourceListKeys</span></span>

## <span data-ttu-id="44ef9-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="44ef9-132">NOTES</span></span>

## <span data-ttu-id="44ef9-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44ef9-133">RELATED LINKS</span></span>

