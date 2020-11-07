---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 21106b2c5a8e36f58b6593049fccf28994b0af46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904829"
---
# <span data-ttu-id="36c6d-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="36c6d-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="36c6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="36c6d-103">Настройте параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="36c6d-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="36c6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36c6d-104">SYNTAX</span></span>

### <span data-ttu-id="36c6d-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36c6d-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36c6d-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36c6d-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36c6d-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36c6d-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36c6d-108">Ключив</span><span class="sxs-lookup"><span data-stu-id="36c6d-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36c6d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36c6d-109">DESCRIPTION</span></span>
<span data-ttu-id="36c6d-110">Командлет **Set-AzRecoveryServicesAsrNotificationSetting** настраивает параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="36c6d-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="36c6d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36c6d-111">EXAMPLES</span></span>

### <span data-ttu-id="36c6d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36c6d-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="36c6d-113">Отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="36c6d-113">Disable notification.</span></span>

### <span data-ttu-id="36c6d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="36c6d-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="36c6d-115">Настройка уведомления для настраиваемых адресов электронной почты и владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="36c6d-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="36c6d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36c6d-116">PARAMETERS</span></span>

### <span data-ttu-id="36c6d-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="36c6d-117">-CustomEmailAddress</span></span>
<span data-ttu-id="36c6d-118">Оповещения и уведомления, отправленные в сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="36c6d-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="36c6d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c6d-119">-DefaultProfile</span></span>
<span data-ttu-id="36c6d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36c6d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36c6d-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36c6d-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="36c6d-122">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="36c6d-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="36c6d-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="36c6d-123">-DisableNotification</span></span>
<span data-ttu-id="36c6d-124">Флаг, показывающий отключение всех уведомлений.</span><span class="sxs-lookup"><span data-stu-id="36c6d-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="36c6d-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="36c6d-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="36c6d-126">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="36c6d-126">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="36c6d-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="36c6d-127">-LocaleID</span></span>
<span data-ttu-id="36c6d-128">Язык электронной почты для оповещения/Notification пользователя (Поддерживаемые коды языка и региональных параметров от Microsoft).</span><span class="sxs-lookup"><span data-stu-id="36c6d-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="36c6d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36c6d-129">-Confirm</span></span>
<span data-ttu-id="36c6d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="36c6d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36c6d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c6d-131">-WhatIf</span></span>
<span data-ttu-id="36c6d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="36c6d-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36c6d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="36c6d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36c6d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c6d-134">CommonParameters</span></span>
<span data-ttu-id="36c6d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36c6d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c6d-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c6d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c6d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36c6d-137">INPUTS</span></span>

### <span data-ttu-id="36c6d-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="36c6d-138">None</span></span>

## <span data-ttu-id="36c6d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36c6d-139">OUTPUTS</span></span>

### <span data-ttu-id="36c6d-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="36c6d-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="36c6d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="36c6d-141">NOTES</span></span>

## <span data-ttu-id="36c6d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36c6d-142">RELATED LINKS</span></span>
