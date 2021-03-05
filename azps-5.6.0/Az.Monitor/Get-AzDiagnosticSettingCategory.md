---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsettingcategory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSettingCategory.md
ms.openlocfilehash: df263698a913faf361e5f23bb12d0267be314106
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980056"
---
# <span data-ttu-id="4b3ef-101">Get-AzDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="4b3ef-101">Get-AzDiagnosticSettingCategory</span></span>

## <span data-ttu-id="4b3ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3ef-103">Получить или перечислить поддерживаемую категорию параметров диагностики для ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3ef-103">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="4b3ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b3ef-104">SYNTAX</span></span>

```
Get-AzDiagnosticSettingCategory -TargetResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b3ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b3ef-105">DESCRIPTION</span></span>
<span data-ttu-id="4b3ef-106">Получить или перечислить поддерживаемую категорию параметров диагностики для ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3ef-106">Get or list supported diagnostic setting category for Azure resource.</span></span>

## <span data-ttu-id="4b3ef-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b3ef-107">EXAMPLES</span></span>

### <span data-ttu-id="4b3ef-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b3ef-108">Example 1</span></span>
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

<span data-ttu-id="4b3ef-109">Получите поддерживаемые категории параметров диагностики для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4b3ef-109">Get supported diagnostic setting categories for virtual network.</span></span>

## <span data-ttu-id="4b3ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b3ef-110">PARAMETERS</span></span>

### <span data-ttu-id="4b3ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3ef-111">-DefaultProfile</span></span>
<span data-ttu-id="4b3ef-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b3ef-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4b3ef-113">-Name</span></span>
<span data-ttu-id="4b3ef-114">Имя категории диагностических параметров</span><span class="sxs-lookup"><span data-stu-id="4b3ef-114">Name of diagnostic setting category</span></span>

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

### <span data-ttu-id="4b3ef-115">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4b3ef-115">-TargetResourceId</span></span>
<span data-ttu-id="4b3ef-116">ИД целевого ресурса</span><span class="sxs-lookup"><span data-stu-id="4b3ef-116">Target resource Id</span></span>

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

### <span data-ttu-id="4b3ef-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3ef-117">CommonParameters</span></span>
<span data-ttu-id="4b3ef-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b3ef-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b3ef-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b3ef-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3ef-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b3ef-120">INPUTS</span></span>

### <span data-ttu-id="4b3ef-121">System.String</span><span class="sxs-lookup"><span data-stu-id="4b3ef-121">System.String</span></span>

## <span data-ttu-id="4b3ef-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b3ef-122">OUTPUTS</span></span>

### <span data-ttu-id="4b3ef-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span><span class="sxs-lookup"><span data-stu-id="4b3ef-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSDiagnosticSettingCategory</span></span>

## <span data-ttu-id="4b3ef-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b3ef-124">NOTES</span></span>

## <span data-ttu-id="4b3ef-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b3ef-125">RELATED LINKS</span></span>
