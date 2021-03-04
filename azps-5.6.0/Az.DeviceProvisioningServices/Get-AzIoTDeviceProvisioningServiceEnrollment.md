---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 56aadda2d7f1dccb77795d5226fb79c8a0fc65ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958723"
---
# <span data-ttu-id="d1fac-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="d1fac-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="d1fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1fac-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fac-103">Получить запись о регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="d1fac-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="d1fac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1fac-104">SYNTAX</span></span>

### <span data-ttu-id="d1fac-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d1fac-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1fac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d1fac-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d1fac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d1fac-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1fac-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1fac-108">DESCRIPTION</span></span>
<span data-ttu-id="d1fac-109">Получите сведения о регистрации устройства или списке регистраций устройств в службе регистрации устройства в Центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fac-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d1fac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1fac-110">EXAMPLES</span></span>

### <span data-ttu-id="d1fac-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1fac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="d1fac-112">Получите сведения о регистрации устройства в службе регистрации устройств в центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fac-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="d1fac-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d1fac-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="d1fac-114">Регистрация устройств в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="d1fac-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="d1fac-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1fac-115">PARAMETERS</span></span>

### <span data-ttu-id="d1fac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fac-116">-DefaultProfile</span></span>
<span data-ttu-id="d1fac-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1fac-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="d1fac-118">-DpsName</span></span>
<span data-ttu-id="d1fac-119">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="d1fac-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d1fac-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="d1fac-120">-DpsObject</span></span>
<span data-ttu-id="d1fac-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="d1fac-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d1fac-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="d1fac-122">-RegistrationId</span></span>
<span data-ttu-id="d1fac-123">Индивидуальный регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="d1fac-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="d1fac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1fac-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1fac-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d1fac-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d1fac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1fac-126">-ResourceId</span></span>
<span data-ttu-id="d1fac-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="d1fac-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d1fac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fac-128">CommonParameters</span></span>
<span data-ttu-id="d1fac-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fac-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1fac-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fac-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1fac-131">INPUTS</span></span>

### <span data-ttu-id="d1fac-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d1fac-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d1fac-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d1fac-133">System.String</span></span>

## <span data-ttu-id="d1fac-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1fac-134">OUTPUTS</span></span>

### <span data-ttu-id="d1fac-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="d1fac-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="d1fac-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="d1fac-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="d1fac-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1fac-137">NOTES</span></span>

## <span data-ttu-id="d1fac-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1fac-138">RELATED LINKS</span></span>
