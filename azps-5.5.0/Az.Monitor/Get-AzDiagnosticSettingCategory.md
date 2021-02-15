---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: 29c65ef5f5ec3b2b54fb883da706ddc9a38e1d4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214244"
---
# <span data-ttu-id="40a6c-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="40a6c-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="40a6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40a6c-102">SYNOPSIS</span></span>
<span data-ttu-id="40a6c-103">Получить или перечислить поддерживаемую категорию параметров диагностики для ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="40a6c-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="40a6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40a6c-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40a6c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40a6c-105">DESCRIPTION</span></span>
<span data-ttu-id="40a6c-106">Получить или перечислить поддерживаемую категорию диагностических параметров для ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="40a6c-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="40a6c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40a6c-107">EXAMPLES</span></span>

### <span data-ttu-id="40a6c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40a6c-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiagnosticSettingCategory -TargetResourceId /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX
Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/VMProtectionAlerts
Name         : VMProtectionAlerts
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Logs

Id           : /subscriptions/XXXXXXXXXXXX/resourceGroups/XXXXXXXX/providers/Microsoft.Network/virtualNetworks/XXXXXXXX/providers/microsoft.insights/diagnosticSettingsCategories/AllMetrics
Name         : AllMetrics
Type         : microsoft.insights/diagnosticSettingsCategories
CategoryType : Metrics
```

<span data-ttu-id="40a6c-109">Получите поддерживаемые категории параметров диагностики для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="40a6c-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="40a6c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40a6c-110">PARAMETERS</span></span>

### <span data-ttu-id="40a6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40a6c-111">-DefaultProfile</span></span>
<span data-ttu-id="40a6c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40a6c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40a6c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="40a6c-113">-Name</span></span>
<span data-ttu-id="40a6c-114">Имя категории диагностических параметров</span><span class="sxs-lookup"><span data-stu-id="40a6c-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="40a6c-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="40a6c-115">-TargetResourceId</span></span>
<span data-ttu-id="40a6c-116">ИД целевого ресурса</span><span class="sxs-lookup"><span data-stu-id="40a6c-116">Target resource Id</span></span>

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

### <span data-ttu-id="40a6c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40a6c-117">CommonParameters</span></span>
<span data-ttu-id="40a6c-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40a6c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40a6c-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40a6c-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40a6c-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40a6c-120">INPUTS</span></span>

### <span data-ttu-id="40a6c-121">System.String</span><span class="sxs-lookup"><span data-stu-id="40a6c-121">System.String</span></span>

## <span data-ttu-id="40a6c-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40a6c-122">OUTPUTS</span></span>

### <span data-ttu-id="40a6c-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="40a6c-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="40a6c-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40a6c-124">NOTES</span></span>

## <span data-ttu-id="40a6c-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40a6c-125">RELATED LINKS</span></span>
