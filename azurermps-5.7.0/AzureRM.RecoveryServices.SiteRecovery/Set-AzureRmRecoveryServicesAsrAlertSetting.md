---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 4e51cd90e490442c36b5864e53b4bb7a36e41e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563392"
---
# <span data-ttu-id="ca698-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ca698-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ca698-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca698-102">SYNOPSIS</span></span>
<span data-ttu-id="ca698-103">Настройте параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="ca698-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca698-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca698-104">SYNTAX</span></span>

### <span data-ttu-id="ca698-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ca698-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca698-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca698-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca698-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca698-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca698-108">Ключив</span><span class="sxs-lookup"><span data-stu-id="ca698-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca698-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca698-109">DESCRIPTION</span></span>
<span data-ttu-id="ca698-110">Командлет **Set-AzureRmRecoveryServicesAsrNotificationSetting** настраивает параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="ca698-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ca698-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca698-111">EXAMPLES</span></span>

### <span data-ttu-id="ca698-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ca698-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="ca698-113">Отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="ca698-113">Disable notification.</span></span>

### <span data-ttu-id="ca698-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ca698-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ca698-115">Настройка уведомления для настраиваемых адресов электронной почты и владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="ca698-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="ca698-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca698-116">PARAMETERS</span></span>

### <span data-ttu-id="ca698-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca698-117">-Confirm</span></span>
<span data-ttu-id="ca698-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca698-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca698-119">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca698-119">-CustomEmailAddress</span></span>
<span data-ttu-id="ca698-120">Оповещения и уведомления, отправленные в сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="ca698-120">Alert / Notification sent to emails.</span></span>

```yaml
Type: String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca698-121">-DefaultProfile</span></span>
<span data-ttu-id="ca698-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca698-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca698-123">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca698-123">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="ca698-124">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="ca698-124">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-125">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="ca698-125">-DisableNotification</span></span>
<span data-ttu-id="ca698-126">Флаг, показывающий отключение всех уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ca698-126">Flag to disable all notification.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-127">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca698-127">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="ca698-128">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="ca698-128">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-129">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="ca698-129">-LocaleID</span></span>
<span data-ttu-id="ca698-130">Язык электронной почты для оповещения/notifcation пользователя (Поддерживаемые коды языка и региональных параметров от Microsoft).</span><span class="sxs-lookup"><span data-stu-id="ca698-130">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca698-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca698-131">-WhatIf</span></span>
<span data-ttu-id="ca698-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca698-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca698-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca698-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca698-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca698-134">CommonParameters</span></span>
<span data-ttu-id="ca698-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca698-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca698-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca698-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca698-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca698-137">INPUTS</span></span>

### <span data-ttu-id="ca698-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="ca698-138">None</span></span>

## <span data-ttu-id="ca698-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca698-139">OUTPUTS</span></span>

### <span data-ttu-id="ca698-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="ca698-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ca698-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca698-141">NOTES</span></span>

## <span data-ttu-id="ca698-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca698-142">RELATED LINKS</span></span>
