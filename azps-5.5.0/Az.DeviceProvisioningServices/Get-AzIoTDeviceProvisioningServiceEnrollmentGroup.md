---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220084"
---
# <span data-ttu-id="f0216-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f0216-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="f0216-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0216-102">SYNOPSIS</span></span>
<span data-ttu-id="f0216-103">Получить группу регистрации устройства.</span><span class="sxs-lookup"><span data-stu-id="f0216-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="f0216-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0216-104">SYNTAX</span></span>

### <span data-ttu-id="f0216-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0216-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0216-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0216-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0216-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f0216-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0216-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0216-108">DESCRIPTION</span></span>
<span data-ttu-id="f0216-109">Подробные сведения о группе регистрации или списке всех групп регистрации в службе регистрации для устройств на концентраторе Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="f0216-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f0216-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0216-110">EXAMPLES</span></span>

### <span data-ttu-id="f0216-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0216-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="f0216-112">Получить группу регистрации устройств в службе azure IoT Hub Device Provisioning Service.</span><span class="sxs-lookup"><span data-stu-id="f0216-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="f0216-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f0216-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="f0216-114">Перечислите все группы регистрации устройств в службе регистрации устройств в центре IoT Azure.</span><span class="sxs-lookup"><span data-stu-id="f0216-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f0216-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0216-115">PARAMETERS</span></span>

### <span data-ttu-id="f0216-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0216-116">-DefaultProfile</span></span>
<span data-ttu-id="f0216-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0216-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0216-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f0216-118">-DpsName</span></span>
<span data-ttu-id="f0216-119">Имя службы подготовка устройств ioT</span><span class="sxs-lookup"><span data-stu-id="f0216-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f0216-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f0216-120">-DpsObject</span></span>
<span data-ttu-id="f0216-121">IoT Device Provisioning Service Object</span><span class="sxs-lookup"><span data-stu-id="f0216-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f0216-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f0216-122">-Name</span></span>
<span data-ttu-id="f0216-123">Имя группы регистрации.</span><span class="sxs-lookup"><span data-stu-id="f0216-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="f0216-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0216-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0216-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f0216-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f0216-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0216-126">-ResourceId</span></span>
<span data-ttu-id="f0216-127">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="f0216-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f0216-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0216-128">CommonParameters</span></span>
<span data-ttu-id="f0216-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0216-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0216-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0216-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0216-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0216-131">INPUTS</span></span>

### <span data-ttu-id="f0216-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f0216-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f0216-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f0216-133">System.String</span></span>

## <span data-ttu-id="f0216-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0216-134">OUTPUTS</span></span>

### <span data-ttu-id="f0216-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f0216-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="f0216-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="f0216-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="f0216-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0216-137">NOTES</span></span>

## <span data-ttu-id="f0216-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0216-138">RELATED LINKS</span></span>
