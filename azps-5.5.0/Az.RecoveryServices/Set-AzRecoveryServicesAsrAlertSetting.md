---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225393"
---
# <span data-ttu-id="3c208-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3c208-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="3c208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c208-102">SYNOPSIS</span></span>
<span data-ttu-id="3c208-103">Настройте параметры уведомлений о восстановлении сайта Azure (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="3c208-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="3c208-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c208-104">SYNTAX</span></span>

### <span data-ttu-id="3c208-105">Set (Default)</span><span class="sxs-lookup"><span data-stu-id="3c208-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c208-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3c208-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c208-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3c208-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c208-108">"Отключить"</span><span class="sxs-lookup"><span data-stu-id="3c208-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c208-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c208-109">DESCRIPTION</span></span>
<span data-ttu-id="3c208-110">**Cmdlet Set-AzRecoveryServicesAsrNotificationSetting** настраивает параметры уведомлений восстановления сайта Azure (уведомления по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="3c208-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="3c208-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c208-111">EXAMPLES</span></span>

### <span data-ttu-id="3c208-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c208-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="3c208-113">Отключить уведомление.</span><span class="sxs-lookup"><span data-stu-id="3c208-113">Disable notification.</span></span>

### <span data-ttu-id="3c208-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3c208-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="3c208-115">Настройка уведомлений для пользовательских адресов электронной почты и владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="3c208-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="3c208-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3c208-116">Example 3</span></span>

<span data-ttu-id="3c208-117">Настройте параметры уведомлений о восстановлении сайта Azure (уведомление по электронной почте) для хранилища.</span><span class="sxs-lookup"><span data-stu-id="3c208-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="3c208-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="3c208-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="3c208-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c208-119">PARAMETERS</span></span>

### <span data-ttu-id="3c208-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="3c208-120">-CustomEmailAddress</span></span>
<span data-ttu-id="3c208-121">Оповещение или уведомление, отправленные по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="3c208-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="3c208-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c208-122">-DefaultProfile</span></span>
<span data-ttu-id="3c208-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c208-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c208-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3c208-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="3c208-125">Параметр переключения указывает, что включить уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="3c208-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="3c208-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="3c208-126">-DisableNotification</span></span>
<span data-ttu-id="3c208-127">Пометить, чтобы отключить все уведомления.</span><span class="sxs-lookup"><span data-stu-id="3c208-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="3c208-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="3c208-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="3c208-129">Параметр переключения указывает, что включить уведомление для владельца подписки.</span><span class="sxs-lookup"><span data-stu-id="3c208-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="3c208-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="3c208-130">-LocaleID</span></span>
<span data-ttu-id="3c208-131">Язык сообщений электронной почты с оповещениями и уведомлениями для пользователей (поддерживаемые коды культуры от майкрософт).</span><span class="sxs-lookup"><span data-stu-id="3c208-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="3c208-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c208-132">-Confirm</span></span>
<span data-ttu-id="3c208-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c208-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c208-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c208-134">-WhatIf</span></span>
<span data-ttu-id="3c208-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c208-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c208-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3c208-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c208-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c208-137">CommonParameters</span></span>
<span data-ttu-id="3c208-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c208-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c208-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c208-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c208-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c208-140">INPUTS</span></span>

### <span data-ttu-id="3c208-141">Нет</span><span class="sxs-lookup"><span data-stu-id="3c208-141">None</span></span>

## <span data-ttu-id="3c208-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c208-142">OUTPUTS</span></span>

### <span data-ttu-id="3c208-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="3c208-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="3c208-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c208-144">NOTES</span></span>

## <span data-ttu-id="3c208-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c208-145">RELATED LINKS</span></span>
