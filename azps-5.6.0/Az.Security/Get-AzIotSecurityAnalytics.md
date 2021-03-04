---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: aaa7e89334f2736010e4a762012d5c456a0fac4d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969955"
---
# <span data-ttu-id="5a33f-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="5a33f-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="5a33f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a33f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a33f-103">Получить аналитику безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="5a33f-103">Get IoT security analytics</span></span>

## <span data-ttu-id="5a33f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a33f-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a33f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a33f-105">DESCRIPTION</span></span>
<span data-ttu-id="5a33f-106">Этот Get-AzIotSecurityAnalytics возвращает набор аналитики безопасности определенного решения для защиты iOT-данных.</span><span class="sxs-lookup"><span data-stu-id="5a33f-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="5a33f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a33f-107">EXAMPLES</span></span>

### <span data-ttu-id="5a33f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a33f-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="5a33f-109">Получить глушительное решение IoT Security Analytics для системы безопасности "MySolution" в группе перенастройки "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="5a33f-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="5a33f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a33f-110">PARAMETERS</span></span>

### <span data-ttu-id="5a33f-111">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="5a33f-111">-Default</span></span>
<span data-ttu-id="5a33f-112">В этом случае получите набор аналитики по умолчанию, в противном случае получите список всех наборов аналитики.</span><span class="sxs-lookup"><span data-stu-id="5a33f-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a33f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a33f-113">-DefaultProfile</span></span>
<span data-ttu-id="5a33f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a33f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a33f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a33f-115">-ResourceGroupName</span></span>
<span data-ttu-id="5a33f-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a33f-116">Resource group name.</span></span>

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

### <span data-ttu-id="5a33f-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="5a33f-117">-SolutionName</span></span>
<span data-ttu-id="5a33f-118">Название решения</span><span class="sxs-lookup"><span data-stu-id="5a33f-118">Solution name</span></span>

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

### <span data-ttu-id="5a33f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a33f-119">CommonParameters</span></span>
<span data-ttu-id="5a33f-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a33f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a33f-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a33f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a33f-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a33f-122">INPUTS</span></span>

### <span data-ttu-id="5a33f-123">Нет</span><span class="sxs-lookup"><span data-stu-id="5a33f-123">None</span></span>

## <span data-ttu-id="5a33f-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a33f-124">OUTPUTS</span></span>

### <span data-ttu-id="5a33f-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="5a33f-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="5a33f-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a33f-126">NOTES</span></span>

## <span data-ttu-id="5a33f-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a33f-127">RELATED LINKS</span></span>
