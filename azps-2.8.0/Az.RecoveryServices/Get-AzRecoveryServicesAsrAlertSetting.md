---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: e7ce712102ffbb74fd8f19eed544642af5a6ebce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905018"
---
# <span data-ttu-id="08031-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="08031-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="08031-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08031-102">SYNOPSIS</span></span>
<span data-ttu-id="08031-103">Получает настроенные параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="08031-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="08031-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08031-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08031-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08031-105">DESCRIPTION</span></span>
<span data-ttu-id="08031-106">Командлет **Get-AzRecoveryServicesAsrAlertSetting** получает настроенные параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="08031-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="08031-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08031-107">EXAMPLES</span></span>

### <span data-ttu-id="08031-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="08031-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="08031-109">Получение оповещений и уведомлений о настройке Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="08031-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="08031-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08031-110">PARAMETERS</span></span>

### <span data-ttu-id="08031-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08031-111">-DefaultProfile</span></span>
<span data-ttu-id="08031-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08031-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="08031-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08031-113">CommonParameters</span></span>
<span data-ttu-id="08031-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08031-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08031-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08031-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08031-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08031-116">INPUTS</span></span>

### <span data-ttu-id="08031-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="08031-117">None</span></span>

## <span data-ttu-id="08031-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08031-118">OUTPUTS</span></span>

### <span data-ttu-id="08031-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="08031-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="08031-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="08031-120">NOTES</span></span>

## <span data-ttu-id="08031-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08031-121">RELATED LINKS</span></span>
