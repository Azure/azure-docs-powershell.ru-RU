---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: ca17774085e76adad57698c2b0b5689ec1c276e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729619"
---
# <span data-ttu-id="ea763-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ea763-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ea763-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea763-102">SYNOPSIS</span></span>
<span data-ttu-id="ea763-103">Настройте параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="ea763-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ea763-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea763-104">SYNTAX</span></span>

### <span data-ttu-id="ea763-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea763-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea763-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ea763-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea763-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ea763-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea763-108">Ключив</span><span class="sxs-lookup"><span data-stu-id="ea763-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea763-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea763-109">DESCRIPTION</span></span>
<span data-ttu-id="ea763-110">Командлет **Set-AzRecoveryServicesAsrNotificationSetting** настраивает параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="ea763-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ea763-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea763-111">EXAMPLES</span></span>

### <span data-ttu-id="ea763-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea763-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="ea763-113">Отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="ea763-113">Disable notification.</span></span>

### <span data-ttu-id="ea763-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea763-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ea763-115">Настройка уведомления для настраиваемых адресов электронной почты и владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="ea763-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="ea763-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea763-116">PARAMETERS</span></span>

### <span data-ttu-id="ea763-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ea763-117">-CustomEmailAddress</span></span>
<span data-ttu-id="ea763-118">Оповещения и уведомления, отправленные в сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ea763-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea763-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea763-119">-DefaultProfile</span></span>
<span data-ttu-id="ea763-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea763-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea763-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ea763-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="ea763-122">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="ea763-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea763-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="ea763-123">-DisableNotification</span></span>
<span data-ttu-id="ea763-124">Флаг, показывающий отключение всех уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ea763-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea763-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ea763-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="ea763-126">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="ea763-126">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea763-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="ea763-127">-LocaleID</span></span>
<span data-ttu-id="ea763-128">Язык электронной почты для оповещения/notifcation пользователя (Поддерживаемые коды языка и региональных параметров от Microsoft).</span><span class="sxs-lookup"><span data-stu-id="ea763-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea763-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea763-129">-Confirm</span></span>
<span data-ttu-id="ea763-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea763-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea763-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea763-131">-WhatIf</span></span>
<span data-ttu-id="ea763-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea763-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea763-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea763-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea763-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea763-134">CommonParameters</span></span>
<span data-ttu-id="ea763-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea763-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea763-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea763-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea763-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea763-137">INPUTS</span></span>

### <span data-ttu-id="ea763-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="ea763-138">None</span></span>

## <span data-ttu-id="ea763-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea763-139">OUTPUTS</span></span>

### <span data-ttu-id="ea763-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ea763-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="ea763-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea763-141">NOTES</span></span>

## <span data-ttu-id="ea763-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea763-142">RELATED LINKS</span></span>
