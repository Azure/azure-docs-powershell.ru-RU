---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248219"
---
# <span data-ttu-id="19fe9-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="19fe9-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="19fe9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19fe9-102">SYNOPSIS</span></span>
<span data-ttu-id="19fe9-103">Настройте параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="19fe9-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="19fe9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19fe9-104">SYNTAX</span></span>

### <span data-ttu-id="19fe9-105">Set (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19fe9-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19fe9-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="19fe9-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19fe9-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="19fe9-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19fe9-108">Ключив</span><span class="sxs-lookup"><span data-stu-id="19fe9-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19fe9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19fe9-109">DESCRIPTION</span></span>
<span data-ttu-id="19fe9-110">Командлет **Set-AzRecoveryServicesAsrNotificationSetting** настраивает параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="19fe9-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="19fe9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19fe9-111">EXAMPLES</span></span>

### <span data-ttu-id="19fe9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19fe9-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="19fe9-113">Отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="19fe9-113">Disable notification.</span></span>

### <span data-ttu-id="19fe9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="19fe9-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="19fe9-115">Настройка уведомления для настраиваемых адресов электронной почты и владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="19fe9-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="19fe9-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="19fe9-116">Example 3</span></span>

<span data-ttu-id="19fe9-117">Настройте параметры уведомлений Azure Site Recovery (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="19fe9-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="19fe9-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="19fe9-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="19fe9-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19fe9-119">PARAMETERS</span></span>

### <span data-ttu-id="19fe9-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="19fe9-120">-CustomEmailAddress</span></span>
<span data-ttu-id="19fe9-121">Оповещения и уведомления, отправленные в сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="19fe9-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="19fe9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19fe9-122">-DefaultProfile</span></span>
<span data-ttu-id="19fe9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19fe9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19fe9-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="19fe9-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="19fe9-125">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="19fe9-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="19fe9-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="19fe9-126">-DisableNotification</span></span>
<span data-ttu-id="19fe9-127">Флаг, показывающий отключение всех уведомлений.</span><span class="sxs-lookup"><span data-stu-id="19fe9-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="19fe9-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="19fe9-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="19fe9-129">Параметр Switch указывает, включено ли уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="19fe9-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="19fe9-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="19fe9-130">-LocaleID</span></span>
<span data-ttu-id="19fe9-131">Язык электронной почты для оповещения/Notification пользователя (Поддерживаемые коды языка и региональных параметров от Microsoft).</span><span class="sxs-lookup"><span data-stu-id="19fe9-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="19fe9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19fe9-132">-Confirm</span></span>
<span data-ttu-id="19fe9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="19fe9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19fe9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19fe9-134">-WhatIf</span></span>
<span data-ttu-id="19fe9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="19fe9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19fe9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="19fe9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19fe9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19fe9-137">CommonParameters</span></span>
<span data-ttu-id="19fe9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19fe9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19fe9-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19fe9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19fe9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19fe9-140">INPUTS</span></span>

### <span data-ttu-id="19fe9-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="19fe9-141">None</span></span>

## <span data-ttu-id="19fe9-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19fe9-142">OUTPUTS</span></span>

### <span data-ttu-id="19fe9-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="19fe9-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="19fe9-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="19fe9-144">NOTES</span></span>

## <span data-ttu-id="19fe9-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19fe9-145">RELATED LINKS</span></span>
