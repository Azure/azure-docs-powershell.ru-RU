---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 2c1d5254d8705d6511d25038e64107a8199496fb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401196"
---
# <span data-ttu-id="9ea34-101">Get-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9ea34-101">Get-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="9ea34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ea34-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea34-103">Настраивает параметры уведомлений о восстановлении сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="9ea34-103">Gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9ea34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9ea34-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrAlertSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ea34-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ea34-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea34-106">Для **параметра Get-AzRecoveryServicesAsrAlertSetting** настраиваются параметры уведомлений восстановления сайта Azure для хранилища.</span><span class="sxs-lookup"><span data-stu-id="9ea34-106">The **Get-AzRecoveryServicesAsrAlertSetting** cmdlet gets the configured Azure Site Recovery notification settings for the vault.</span></span>

## <span data-ttu-id="9ea34-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9ea34-107">EXAMPLES</span></span>

### <span data-ttu-id="9ea34-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ea34-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrAlertSetting

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="9ea34-109">Настройка оповещений и уведомлений для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea34-109">Get Alert / Notification Setting for Azure Site Recovery.</span></span>

## <span data-ttu-id="9ea34-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ea34-110">PARAMETERS</span></span>

### <span data-ttu-id="9ea34-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea34-111">-DefaultProfile</span></span>
<span data-ttu-id="9ea34-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea34-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ea34-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea34-113">CommonParameters</span></span>
<span data-ttu-id="9ea34-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ea34-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea34-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ea34-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea34-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9ea34-116">INPUTS</span></span>

### <span data-ttu-id="9ea34-117">Нет</span><span class="sxs-lookup"><span data-stu-id="9ea34-117">None</span></span>

## <span data-ttu-id="9ea34-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9ea34-118">OUTPUTS</span></span>

### <span data-ttu-id="9ea34-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9ea34-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="9ea34-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9ea34-120">NOTES</span></span>

## <span data-ttu-id="9ea34-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ea34-121">RELATED LINKS</span></span>
