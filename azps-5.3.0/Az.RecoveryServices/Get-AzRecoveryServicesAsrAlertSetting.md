---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424764"
---
# <span data-ttu-id="10ed6-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="10ed6-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="10ed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ed6-102">SYNOPSIS</span></span>
<span data-ttu-id="10ed6-103">Настраивает параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="10ed6-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="10ed6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="10ed6-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10ed6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10ed6-105">DESCRIPTION</span></span>
<span data-ttu-id="10ed6-106">Для **параметра Get-AzRecoveryServicesAsrAlertSetting** настраиваются параметры уведомлений восстановления сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="10ed6-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="10ed6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="10ed6-107">EXAMPLES</span></span>

### <span data-ttu-id="10ed6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="10ed6-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="10ed6-109">Настройка оповещений и уведомлений для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="10ed6-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="10ed6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10ed6-110">PARAMETERS</span></span>

### <span data-ttu-id="10ed6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ed6-111">-DefaultProfile</span></span>
<span data-ttu-id="10ed6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10ed6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10ed6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ed6-113">CommonParameters</span></span>
<span data-ttu-id="10ed6-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10ed6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ed6-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="10ed6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ed6-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="10ed6-116">INPUTS</span></span>

### <span data-ttu-id="10ed6-117">Нет</span><span class="sxs-lookup"><span data-stu-id="10ed6-117">None</span></span>

## <span data-ttu-id="10ed6-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="10ed6-118">OUTPUTS</span></span>

### <span data-ttu-id="10ed6-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="10ed6-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="10ed6-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="10ed6-120">NOTES</span></span>

## <span data-ttu-id="10ed6-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10ed6-121">RELATED LINKS</span></span>
