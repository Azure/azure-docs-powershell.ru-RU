---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316303"
---
# <span data-ttu-id="f6ec8-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="f6ec8-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="f6ec8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f6ec8-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ec8-103">Получение аналитической системы безопасности IoT</span><span class="sxs-lookup"><span data-stu-id="f6ec8-103">Get IoT security analytics</span></span>

## <span data-ttu-id="f6ec8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f6ec8-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ec8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ec8-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ec8-106">Командлет Get-AzIotSecurityAnalytics возвращает набор аналитических элементов, связанных с определенным решением безопасности IOT.</span><span class="sxs-lookup"><span data-stu-id="f6ec8-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="f6ec8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f6ec8-107">EXAMPLES</span></span>

### <span data-ttu-id="f6ec8-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f6ec8-108">Example 1</span></span>
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

<span data-ttu-id="f6ec8-109">Получение средства анализа безопасности IoT deafult для системы безопасности "MySolution" в reasource группе "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="f6ec8-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="f6ec8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f6ec8-110">PARAMETERS</span></span>

### <span data-ttu-id="f6ec8-111">-Default</span><span class="sxs-lookup"><span data-stu-id="f6ec8-111">-Default</span></span>
<span data-ttu-id="f6ec8-112">Если задано значение, получить набор аналитических данных по умолчанию, в противном случае получить список всех аналитических наборов.</span><span class="sxs-lookup"><span data-stu-id="f6ec8-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

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

### <span data-ttu-id="f6ec8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ec8-113">-DefaultProfile</span></span>
<span data-ttu-id="f6ec8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ec8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6ec8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ec8-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6ec8-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f6ec8-116">Resource group name.</span></span>

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

### <span data-ttu-id="f6ec8-117">-Имя_решения</span><span class="sxs-lookup"><span data-stu-id="f6ec8-117">-SolutionName</span></span>
<span data-ttu-id="f6ec8-118">Имя решения</span><span class="sxs-lookup"><span data-stu-id="f6ec8-118">Solution name</span></span>

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

### <span data-ttu-id="f6ec8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ec8-119">CommonParameters</span></span>
<span data-ttu-id="f6ec8-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f6ec8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ec8-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6ec8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ec8-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f6ec8-122">INPUTS</span></span>

### <span data-ttu-id="f6ec8-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f6ec8-123">None</span></span>

## <span data-ttu-id="f6ec8-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6ec8-124">OUTPUTS</span></span>

### <span data-ttu-id="f6ec8-125">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="f6ec8-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="f6ec8-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f6ec8-126">NOTES</span></span>

## <span data-ttu-id="f6ec8-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6ec8-127">RELATED LINKS</span></span>
