---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564007"
---
# <span data-ttu-id="93fc5-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="93fc5-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="93fc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93fc5-102">SYNOPSIS</span></span>
<span data-ttu-id="93fc5-103">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="93fc5-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93fc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93fc5-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93fc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93fc5-105">DESCRIPTION</span></span>
<span data-ttu-id="93fc5-106">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="93fc5-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="93fc5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93fc5-107">EXAMPLES</span></span>

### <span data-ttu-id="93fc5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93fc5-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="93fc5-109">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="93fc5-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="93fc5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93fc5-110">PARAMETERS</span></span>

### <span data-ttu-id="93fc5-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="93fc5-111">-AlertAdmin</span></span>
<span data-ttu-id="93fc5-112">Оповещения для администраторов.</span><span class="sxs-lookup"><span data-stu-id="93fc5-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fc5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93fc5-113">-DefaultProfile</span></span>
<span data-ttu-id="93fc5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93fc5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93fc5-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="93fc5-115">-Email</span></span>
<span data-ttu-id="93fc5-116">Почтов.</span><span class="sxs-lookup"><span data-stu-id="93fc5-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fc5-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93fc5-117">-Name</span></span>
<span data-ttu-id="93fc5-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="93fc5-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fc5-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="93fc5-119">-NotifyOnAlert</span></span>
<span data-ttu-id="93fc5-120">Уведомления о предупреждениях.</span><span class="sxs-lookup"><span data-stu-id="93fc5-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fc5-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="93fc5-121">-Phone</span></span>
<span data-ttu-id="93fc5-122">Кнопка.</span><span class="sxs-lookup"><span data-stu-id="93fc5-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93fc5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93fc5-123">-Confirm</span></span>
<span data-ttu-id="93fc5-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93fc5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93fc5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93fc5-125">-WhatIf</span></span>
<span data-ttu-id="93fc5-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93fc5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93fc5-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93fc5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93fc5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93fc5-128">CommonParameters</span></span>
<span data-ttu-id="93fc5-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93fc5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93fc5-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93fc5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93fc5-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93fc5-131">INPUTS</span></span>

### <span data-ttu-id="93fc5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="93fc5-132">System.String</span></span>

## <span data-ttu-id="93fc5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93fc5-133">OUTPUTS</span></span>

### <span data-ttu-id="93fc5-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="93fc5-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="93fc5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="93fc5-135">NOTES</span></span>

## <span data-ttu-id="93fc5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93fc5-136">RELATED LINKS</span></span>
