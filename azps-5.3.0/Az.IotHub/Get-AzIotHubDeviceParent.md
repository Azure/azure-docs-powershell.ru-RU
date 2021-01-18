---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceParent.md
ms.openlocfilehash: 14e5bbc222bf92f95d77277c6f8d82f578efd0b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518614"
---
# <span data-ttu-id="3e5bd-101">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="3e5bd-101">Get-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="3e5bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e5bd-102">SYNOPSIS</span></span>
<span data-ttu-id="3e5bd-103">Получите родительское устройство указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="3e5bd-103">Get the parent device of the specified device.</span></span>

## <span data-ttu-id="3e5bd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3e5bd-104">SYNTAX</span></span>

### <span data-ttu-id="3e5bd-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e5bd-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e5bd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3e5bd-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e5bd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3e5bd-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e5bd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e5bd-108">DESCRIPTION</span></span>
<span data-ttu-id="3e5bd-109">Получите родительское устройство указанного вне границы устройства.</span><span class="sxs-lookup"><span data-stu-id="3e5bd-109">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="3e5bd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3e5bd-110">EXAMPLES</span></span>

### <span data-ttu-id="3e5bd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e5bd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myParentDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Enabled
StatusReason               : 
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : True
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

<span data-ttu-id="3e5bd-112">Получите родительское устройство указанного вне границы устройства.</span><span class="sxs-lookup"><span data-stu-id="3e5bd-112">Get the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="3e5bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e5bd-113">PARAMETERS</span></span>

### <span data-ttu-id="3e5bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e5bd-114">-DefaultProfile</span></span>
<span data-ttu-id="3e5bd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e5bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e5bd-116">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="3e5bd-116">-DeviceId</span></span>
<span data-ttu-id="3e5bd-117">Id of non-edge device.</span><span class="sxs-lookup"><span data-stu-id="3e5bd-117">Id of non-edge device.</span></span>

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

### <span data-ttu-id="3e5bd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e5bd-118">-InputObject</span></span>
<span data-ttu-id="3e5bd-119">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="3e5bd-119">IotHub object</span></span>

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

### <span data-ttu-id="3e5bd-120">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3e5bd-120">-IotHubName</span></span>
<span data-ttu-id="3e5bd-121">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="3e5bd-121">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3e5bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e5bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="3e5bd-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3e5bd-123">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3e5bd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e5bd-124">-ResourceId</span></span>
<span data-ttu-id="3e5bd-125">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="3e5bd-125">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3e5bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e5bd-126">CommonParameters</span></span>
<span data-ttu-id="3e5bd-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e5bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e5bd-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e5bd-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e5bd-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3e5bd-129">INPUTS</span></span>

### <span data-ttu-id="3e5bd-130">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3e5bd-130">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3e5bd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3e5bd-131">System.String</span></span>

## <span data-ttu-id="3e5bd-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3e5bd-132">OUTPUTS</span></span>

### <span data-ttu-id="3e5bd-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="3e5bd-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="3e5bd-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3e5bd-134">NOTES</span></span>

## <span data-ttu-id="3e5bd-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e5bd-135">RELATED LINKS</span></span>
