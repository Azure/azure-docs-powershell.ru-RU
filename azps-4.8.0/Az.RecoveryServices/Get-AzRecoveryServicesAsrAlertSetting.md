---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077703"
---
# <span data-ttu-id="be16b-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="be16b-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="be16b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be16b-102">SYNOPSIS</span></span>
<span data-ttu-id="be16b-103">Получает настроенные параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="be16b-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="be16b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be16b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be16b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be16b-105">DESCRIPTION</span></span>
<span data-ttu-id="be16b-106">Командлет **Get-AzRecoveryServicesAsrAlertSetting** получает настроенные параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="be16b-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="be16b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be16b-107">EXAMPLES</span></span>

### <span data-ttu-id="be16b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be16b-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="be16b-109">Получение оповещений и уведомлений о настройке Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="be16b-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="be16b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be16b-110">PARAMETERS</span></span>

### <span data-ttu-id="be16b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be16b-111">-DefaultProfile</span></span>
<span data-ttu-id="be16b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be16b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be16b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be16b-113">CommonParameters</span></span>
<span data-ttu-id="be16b-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be16b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be16b-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be16b-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be16b-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be16b-116">INPUTS</span></span>

### <span data-ttu-id="be16b-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="be16b-117">None</span></span>

## <span data-ttu-id="be16b-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be16b-118">OUTPUTS</span></span>

### <span data-ttu-id="be16b-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="be16b-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="be16b-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="be16b-120">NOTES</span></span>

## <span data-ttu-id="be16b-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be16b-121">RELATED LINKS</span></span>
