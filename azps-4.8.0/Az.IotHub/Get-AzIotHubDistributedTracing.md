---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244515"
---
# <span data-ttu-id="cfbe9-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cfbe9-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="cfbe9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="cfbe9-103">Получение параметров распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="cfbe9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfbe9-104">SYNTAX</span></span>

### <span data-ttu-id="cfbe9-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cfbe9-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfbe9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cfbe9-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfbe9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cfbe9-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfbe9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfbe9-108">DESCRIPTION</span></span>
<span data-ttu-id="cfbe9-109">Получение параметров распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="cfbe9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfbe9-110">EXAMPLES</span></span>

### <span data-ttu-id="cfbe9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfbe9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="cfbe9-112">Получение параметров распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="cfbe9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfbe9-113">PARAMETERS</span></span>

### <span data-ttu-id="cfbe9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfbe9-114">-DefaultProfile</span></span>
<span data-ttu-id="cfbe9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfbe9-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cfbe9-116">-DeviceId</span></span>
<span data-ttu-id="cfbe9-117">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-117">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbe9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfbe9-118">-InputObject</span></span>
<span data-ttu-id="cfbe9-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="cfbe9-119">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfbe9-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="cfbe9-120">-IotHubName</span></span>
<span data-ttu-id="cfbe9-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="cfbe9-121">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbe9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfbe9-122">-ResourceGroupName</span></span>
<span data-ttu-id="cfbe9-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfbe9-123">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfbe9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfbe9-124">-ResourceId</span></span>
<span data-ttu-id="cfbe9-125">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="cfbe9-125">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfbe9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfbe9-126">CommonParameters</span></span>
<span data-ttu-id="cfbe9-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfbe9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfbe9-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfbe9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfbe9-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfbe9-129">INPUTS</span></span>

### <span data-ttu-id="cfbe9-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cfbe9-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cfbe9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cfbe9-131">System.String</span></span>

## <span data-ttu-id="cfbe9-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfbe9-132">OUTPUTS</span></span>

### <span data-ttu-id="cfbe9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="cfbe9-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="cfbe9-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfbe9-134">NOTES</span></span>

## <span data-ttu-id="cfbe9-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfbe9-135">RELATED LINKS</span></span>
