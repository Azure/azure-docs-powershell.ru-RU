---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244551"
---
# <span data-ttu-id="dc878-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="dc878-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="dc878-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc878-102">SYNOPSIS</span></span>
<span data-ttu-id="dc878-103">Получить группу регистрации устройств.</span><span class="sxs-lookup"><span data-stu-id="dc878-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="dc878-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc878-104">SYNTAX</span></span>

### <span data-ttu-id="dc878-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dc878-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc878-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc878-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc878-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="dc878-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc878-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc878-108">DESCRIPTION</span></span>
<span data-ttu-id="dc878-109">Получение сведений о группе регистрации или список всех групп регистрации в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dc878-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="dc878-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc878-110">EXAMPLES</span></span>

### <span data-ttu-id="dc878-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc878-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="dc878-112">Получить группу регистрации устройств в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dc878-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="dc878-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dc878-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="dc878-114">Список всех групп регистрации устройств в службе подготовки устройств центра для Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="dc878-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="dc878-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc878-115">PARAMETERS</span></span>

### <span data-ttu-id="dc878-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc878-116">-DefaultProfile</span></span>
<span data-ttu-id="dc878-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc878-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc878-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="dc878-118">-DpsName</span></span>
<span data-ttu-id="dc878-119">Имя службы подготовки устройств IoT</span><span class="sxs-lookup"><span data-stu-id="dc878-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="dc878-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="dc878-120">-DpsObject</span></span>
<span data-ttu-id="dc878-121">Объект службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="dc878-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc878-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc878-122">-Name</span></span>
<span data-ttu-id="dc878-123">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="dc878-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="dc878-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc878-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc878-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dc878-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="dc878-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc878-126">-ResourceId</span></span>
<span data-ttu-id="dc878-127">Идентификатор ресурса службы подготовки устройства IoT</span><span class="sxs-lookup"><span data-stu-id="dc878-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="dc878-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc878-128">CommonParameters</span></span>
<span data-ttu-id="dc878-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc878-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc878-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc878-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc878-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc878-131">INPUTS</span></span>

### <span data-ttu-id="dc878-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="dc878-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="dc878-133">System. String</span><span class="sxs-lookup"><span data-stu-id="dc878-133">System.String</span></span>

## <span data-ttu-id="dc878-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc878-134">OUTPUTS</span></span>

### <span data-ttu-id="dc878-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="dc878-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="dc878-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="dc878-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="dc878-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc878-137">NOTES</span></span>

## <span data-ttu-id="dc878-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc878-138">RELATED LINKS</span></span>
