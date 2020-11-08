---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecuritySetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecuritySetting.md
ms.openlocfilehash: 708fb6b3807e874d00c3e555ef84973572edcd1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245877"
---
# <span data-ttu-id="463b3-101">Get-AzSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="463b3-101">Get-AzSecuritySetting</span></span>

## <span data-ttu-id="463b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="463b3-102">SYNOPSIS</span></span>
<span data-ttu-id="463b3-103">Получение параметров безопасности в центре безопасности Azure</span><span class="sxs-lookup"><span data-stu-id="463b3-103">Get security settings in Azure Security Center</span></span>

## <span data-ttu-id="463b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="463b3-104">SYNTAX</span></span>

### <span data-ttu-id="463b3-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="463b3-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecuritySetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="463b3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="463b3-106">SubscriptionLevelResource</span></span>
```
Get-AzSecuritySetting -SettingName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="463b3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="463b3-107">DESCRIPTION</span></span>
<span data-ttu-id="463b3-108">Командлет Get-AzSecuritySetting получить параметры безопасности в центре безопасности Azure.</span><span class="sxs-lookup"><span data-stu-id="463b3-108">The Get-AzSecuritySetting cmdlet get security settings in Azure Security Center.</span></span>

## <span data-ttu-id="463b3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="463b3-109">EXAMPLES</span></span>

### <span data-ttu-id="463b3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="463b3-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecuritySetting -SettingName "MCAS"

Id: "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/settings/MCAS"
Name: "MCAS"
Type: "Microsoft.Security/settings"
Enabled: true
```

<span data-ttu-id="463b3-111">Получает параметр экспорта данных MCAS</span><span class="sxs-lookup"><span data-stu-id="463b3-111">Gets an MCAS data export setting</span></span>   

## <span data-ttu-id="463b3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="463b3-112">PARAMETERS</span></span>

### <span data-ttu-id="463b3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="463b3-113">-DefaultProfile</span></span>
<span data-ttu-id="463b3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="463b3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="463b3-115">-SettingName</span><span class="sxs-lookup"><span data-stu-id="463b3-115">-SettingName</span></span>
<span data-ttu-id="463b3-116">Имя параметра.</span><span class="sxs-lookup"><span data-stu-id="463b3-116">Setting name.</span></span> <span data-ttu-id="463b3-117">(MCAS/WDATP)</span><span class="sxs-lookup"><span data-stu-id="463b3-117">(MCAS/WDATP)</span></span>

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

### <span data-ttu-id="463b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="463b3-118">CommonParameters</span></span>
<span data-ttu-id="463b3-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="463b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="463b3-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="463b3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="463b3-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="463b3-121">INPUTS</span></span>

### <span data-ttu-id="463b3-122">System. String</span><span class="sxs-lookup"><span data-stu-id="463b3-122">System.String</span></span>

## <span data-ttu-id="463b3-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="463b3-123">OUTPUTS</span></span>

### <span data-ttu-id="463b3-124">Microsoft. Azure. Commands. Security. Models. Settings. PSSecuritySetting</span><span class="sxs-lookup"><span data-stu-id="463b3-124">Microsoft.Azure.Commands.Security.Models.Settings.PSSecuritySetting</span></span>
### <span data-ttu-id="463b3-125">Microsoft. Azure. Commands. Security. Models. Settings. PSSecurityDataExportSetting</span><span class="sxs-lookup"><span data-stu-id="463b3-125">Microsoft.Azure.Commands.Security.Models.Settings.PSSecurityDataExportSetting</span></span>

## <span data-ttu-id="463b3-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="463b3-126">NOTES</span></span>

## <span data-ttu-id="463b3-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="463b3-127">RELATED LINKS</span></span>
