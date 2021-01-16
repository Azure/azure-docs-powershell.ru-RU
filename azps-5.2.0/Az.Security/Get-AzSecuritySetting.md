---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393396"
---
# <span data-ttu-id="b9709-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="b9709-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="b9709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9709-102">SYNOPSIS</span></span>
<span data-ttu-id="b9709-103">Настройка параметров безопасности в Центре безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="b9709-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="b9709-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9709-104">SYNTAX</span></span>

### <span data-ttu-id="b9709-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9709-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9709-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b9709-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9709-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9709-107">DESCRIPTION</span></span>
<span data-ttu-id="b9709-108">Он Get-AzSecuritySetting получить параметры безопасности в Центре безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="b9709-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="b9709-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9709-109">EXAMPLES</span></span>

### <span data-ttu-id="b9709-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9709-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="b9709-111">Параметр экспорта данных MCAS</span><span class="sxs-lookup"><span data-stu-id="b9709-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="b9709-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9709-112">PARAMETERS</span></span>

### <span data-ttu-id="b9709-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9709-113">-DefaultProfile</span></span>
<span data-ttu-id="b9709-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9709-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9709-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="b9709-115">-SettingName</span></span>
<span data-ttu-id="b9709-116">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="b9709-116">Setting name.</span></span> <span data-ttu-id="b9709-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="b9709-117">(MCAS/WDATP)</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9709-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9709-118">CommonParameters</span></span>
<span data-ttu-id="b9709-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9709-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9709-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9709-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9709-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9709-121">INPUTS</span></span>

### <span data-ttu-id="b9709-122">System.String</span><span class="sxs-lookup"><span data-stu-id="b9709-122">System.String</span></span>

## <span data-ttu-id="b9709-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9709-123">OUTPUTS</span></span>

### <span data-ttu-id="b9709-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="b9709-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="b9709-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="b9709-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="b9709-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9709-126">NOTES</span></span>

## <span data-ttu-id="b9709-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9709-127">RELATED LINKS</span></span>
