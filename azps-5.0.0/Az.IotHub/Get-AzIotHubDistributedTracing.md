---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdistributedtracing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDistributedTracing.md
ms.openlocfilehash: b09671fcb075ff029eaa0a28185d8f88d650caf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94258015"
---
# <span data-ttu-id="ebeca-101">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="ebeca-101">Get-AzIotHubDistributedTracing</span></span>

## <span data-ttu-id="ebeca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ebeca-102">SYNOPSIS</span></span>
<span data-ttu-id="ebeca-103">Получение параметров распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="ebeca-103">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="ebeca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ebeca-104">SYNTAX</span></span>

### <span data-ttu-id="ebeca-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebeca-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebeca-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ebeca-106">InputObjectSet</span></span>
```
Get-AzIotHubDistributedTracing [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebeca-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ebeca-107">ResourceIdSet</span></span>
```
Get-AzIotHubDistributedTracing [-ResourceId] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebeca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebeca-108">DESCRIPTION</span></span>
<span data-ttu-id="ebeca-109">Получение параметров распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="ebeca-109">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="ebeca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ebeca-110">EXAMPLES</span></span>

### <span data-ttu-id="ebeca-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebeca-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDistributedTracing -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId      : mydevice1
Sampling Mode : Enabled
Sampling Rate : 22%
IsSynced      : False
```

<span data-ttu-id="ebeca-112">Получение параметров распределенной трассировки для устройства.</span><span class="sxs-lookup"><span data-stu-id="ebeca-112">Get the distributed tracing settings for a device.</span></span>

## <span data-ttu-id="ebeca-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ebeca-113">PARAMETERS</span></span>

### <span data-ttu-id="ebeca-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebeca-114">-DefaultProfile</span></span>
<span data-ttu-id="ebeca-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebeca-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebeca-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="ebeca-116">-DeviceId</span></span>
<span data-ttu-id="ebeca-117">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="ebeca-117">Target Device Id.</span></span>

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

### <span data-ttu-id="ebeca-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebeca-118">-InputObject</span></span>
<span data-ttu-id="ebeca-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="ebeca-119">IotHub object</span></span>

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

### <span data-ttu-id="ebeca-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="ebeca-120">-IotHubName</span></span>
<span data-ttu-id="ebeca-121">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="ebeca-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="ebeca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebeca-122">-ResourceGroupName</span></span>
<span data-ttu-id="ebeca-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ebeca-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ebeca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ebeca-124">-ResourceId</span></span>
<span data-ttu-id="ebeca-125">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="ebeca-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="ebeca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebeca-126">CommonParameters</span></span>
<span data-ttu-id="ebeca-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ebeca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebeca-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebeca-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebeca-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ebeca-129">INPUTS</span></span>

### <span data-ttu-id="ebeca-130">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="ebeca-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="ebeca-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ebeca-131">System.String</span></span>

## <span data-ttu-id="ebeca-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebeca-132">OUTPUTS</span></span>

### <span data-ttu-id="ebeca-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span><span class="sxs-lookup"><span data-stu-id="ebeca-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTracing</span></span>

## <span data-ttu-id="ebeca-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="ebeca-134">NOTES</span></span>

## <span data-ttu-id="ebeca-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebeca-135">RELATED LINKS</span></span>
