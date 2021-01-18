---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 2d1c4b2f272516af31fba17db50d33991dd1db50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508157"
---
# <span data-ttu-id="6d1e9-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="6d1e9-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="6d1e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d1e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1e9-103">Получить или перечислить поддерживаемую категорию параметров диагностики для ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="6d1e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d1e9-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d1e9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-105">DESCRIPTION</span></span>
<span data-ttu-id="6d1e9-106">Получить или перечислить поддерживаемую категорию диагностических параметров для ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="6d1e9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-107">EXAMPLES</span></span>

### <span data-ttu-id="6d1e9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d1e9-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSetting -TargetResourceId -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="6d1e9-109">Получите поддерживаемые категории параметров диагностики для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="6d1e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d1e9-110">PARAMETERS</span></span>

### <span data-ttu-id="6d1e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1e9-111">-DefaultProfile</span></span>
<span data-ttu-id="6d1e9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d1e9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6d1e9-113">-Name</span></span>
<span data-ttu-id="6d1e9-114">Имя категории диагностических параметров</span><span class="sxs-lookup"><span data-stu-id="6d1e9-114">Name of diagnostic setting category</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e9-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6d1e9-115">-TargetResourceId</span></span>
<span data-ttu-id="6d1e9-116">ИД целевого ресурса</span><span class="sxs-lookup"><span data-stu-id="6d1e9-116">Target resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d1e9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1e9-117">CommonParameters</span></span>
<span data-ttu-id="6d1e9-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1e9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1e9-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d1e9-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1e9-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d1e9-120">INPUTS</span></span>

### <span data-ttu-id="6d1e9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6d1e9-121">System.String</span></span>

## <span data-ttu-id="6d1e9-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d1e9-122">OUTPUTS</span></span>

### <span data-ttu-id="6d1e9-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="6d1e9-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="6d1e9-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-124">NOTES</span></span>

## <span data-ttu-id="6d1e9-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d1e9-125">RELATED LINKS</span></span>
