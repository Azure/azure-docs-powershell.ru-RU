---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 7fb55457f62ceb03cc33b70fa6a8699abe0f6f04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566426"
---
# <span data-ttu-id="981e4-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="981e4-101">Get-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="981e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="981e4-102">SYNOPSIS</span></span>
<span data-ttu-id="981e4-103">Получает настроенные параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="981e4-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="981e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="981e4-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="981e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="981e4-105">DESCRIPTION</span></span>
<span data-ttu-id="981e4-106">Командлет **Get-AzureRmRecoveryServicesAsrAlertSetting** получает настроенные параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="981e4-106">The **Get-AzureRmRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="981e4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="981e4-107">EXAMPLES</span></span>

### <span data-ttu-id="981e4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="981e4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="981e4-109">Получение оповещений и уведомлений о настройке Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="981e4-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="981e4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="981e4-110">PARAMETERS</span></span>

### <span data-ttu-id="981e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981e4-111">-DefaultProfile</span></span>
<span data-ttu-id="981e4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="981e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="981e4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981e4-113">CommonParameters</span></span>
<span data-ttu-id="981e4-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="981e4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981e4-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981e4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981e4-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="981e4-116">INPUTS</span></span>

### <span data-ttu-id="981e4-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="981e4-117">None</span></span>

## <span data-ttu-id="981e4-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="981e4-118">OUTPUTS</span></span>

### <span data-ttu-id="981e4-119">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="981e4-119">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="981e4-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="981e4-120">NOTES</span></span>

## <span data-ttu-id="981e4-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="981e4-121">RELATED LINKS</span></span>
