---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518609"
---
# <span data-ttu-id="535b1-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="535b1-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="535b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="535b1-102">SYNOPSIS</span></span>
<span data-ttu-id="535b1-103">Возвращает показатели квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="535b1-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="535b1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="535b1-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="535b1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="535b1-105">DESCRIPTION</span></span>
<span data-ttu-id="535b1-106">Возвращает показатели квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="535b1-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="535b1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="535b1-107">EXAMPLES</span></span>

### <span data-ttu-id="535b1-108">Пример 1. Получить показатели квоты</span><span class="sxs-lookup"><span data-stu-id="535b1-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="535b1-109">Получает сведения о метрической квоте для IotHub с именем myiothub.</span><span class="sxs-lookup"><span data-stu-id="535b1-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="535b1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="535b1-110">PARAMETERS</span></span>

### <span data-ttu-id="535b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535b1-111">-DefaultProfile</span></span>
<span data-ttu-id="535b1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="535b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="535b1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="535b1-113">-Name</span></span>
<span data-ttu-id="535b1-114">Имя концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="535b1-114">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535b1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535b1-115">-ResourceGroupName</span></span>
<span data-ttu-id="535b1-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="535b1-116">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535b1-117">CommonParameters</span></span>
<span data-ttu-id="535b1-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="535b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535b1-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="535b1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535b1-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="535b1-120">INPUTS</span></span>

### <span data-ttu-id="535b1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="535b1-121">System.String</span></span>

## <span data-ttu-id="535b1-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="535b1-122">OUTPUTS</span></span>

### <span data-ttu-id="535b1-123">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="535b1-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="535b1-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="535b1-124">NOTES</span></span>

## <span data-ttu-id="535b1-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="535b1-125">RELATED LINKS</span></span>
