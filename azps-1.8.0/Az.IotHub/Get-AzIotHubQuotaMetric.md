---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 6d8ea34de1520326ead270ffa44837388729bc5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900349"
---
# <span data-ttu-id="97a5c-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="97a5c-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="97a5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="97a5c-103">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="97a5c-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="97a5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97a5c-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="97a5c-106">Получает метрики квоты для IotHub.</span><span class="sxs-lookup"><span data-stu-id="97a5c-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="97a5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="97a5c-108">Пример 1. Получение метрик квоты</span><span class="sxs-lookup"><span data-stu-id="97a5c-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="97a5c-109">Получает сведения о метрике квоты для IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="97a5c-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="97a5c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97a5c-110">PARAMETERS</span></span>

### <span data-ttu-id="97a5c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a5c-111">-DefaultProfile</span></span>
<span data-ttu-id="97a5c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97a5c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97a5c-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97a5c-113">-Name</span></span>
<span data-ttu-id="97a5c-114">Имя центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="97a5c-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="97a5c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a5c-115">-ResourceGroupName</span></span>
<span data-ttu-id="97a5c-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="97a5c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="97a5c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a5c-117">CommonParameters</span></span>
<span data-ttu-id="97a5c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97a5c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a5c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a5c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a5c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97a5c-120">INPUTS</span></span>

### <span data-ttu-id="97a5c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="97a5c-121">System.String</span></span>

## <span data-ttu-id="97a5c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a5c-122">OUTPUTS</span></span>

### <span data-ttu-id="97a5c-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="97a5c-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="97a5c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="97a5c-124">NOTES</span></span>

## <span data-ttu-id="97a5c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97a5c-125">RELATED LINKS</span></span>
