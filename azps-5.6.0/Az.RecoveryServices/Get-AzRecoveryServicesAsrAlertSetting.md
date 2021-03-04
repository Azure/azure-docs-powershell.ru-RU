---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: cadde5ec773452897aa9c6915a5f3e16f00cfef5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007683"
---
# <span data-ttu-id="b3f72-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b3f72-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="b3f72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3f72-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f72-103">Настраивает параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="b3f72-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b3f72-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b3f72-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3f72-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3f72-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f72-106">Для **параметра Get-AzRecoveryServicesAsrAlertSetting** настраиваются параметры уведомлений восстановления сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="b3f72-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="b3f72-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b3f72-107">EXAMPLES</span></span>

### <span data-ttu-id="b3f72-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3f72-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="b3f72-109">Настройка оповещений и уведомлений для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f72-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="b3f72-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3f72-110">PARAMETERS</span></span>

### <span data-ttu-id="b3f72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f72-111">-DefaultProfile</span></span>
<span data-ttu-id="b3f72-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f72-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3f72-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f72-113">CommonParameters</span></span>
<span data-ttu-id="b3f72-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f72-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f72-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3f72-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f72-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b3f72-116">INPUTS</span></span>

### <span data-ttu-id="b3f72-117">Нет</span><span class="sxs-lookup"><span data-stu-id="b3f72-117">None</span></span>

## <span data-ttu-id="b3f72-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3f72-118">OUTPUTS</span></span>

### <span data-ttu-id="b3f72-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="b3f72-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="b3f72-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b3f72-120">NOTES</span></span>

## <span data-ttu-id="b3f72-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3f72-121">RELATED LINKS</span></span>
