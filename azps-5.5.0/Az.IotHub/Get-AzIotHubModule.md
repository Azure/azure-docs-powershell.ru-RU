---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219753"
---
# <span data-ttu-id="aa493-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="aa493-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="aa493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa493-102">SYNOPSIS</span></span>
<span data-ttu-id="aa493-103">Получите сведения о модуле устройства ioT или модулях списка, которые находятся на устройстве ioT в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="aa493-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="aa493-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa493-104">SYNTAX</span></span>

### <span data-ttu-id="aa493-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa493-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa493-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa493-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa493-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa493-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa493-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa493-108">DESCRIPTION</span></span>
<span data-ttu-id="aa493-109">Получите сведения о модуле устройства ioT или модулях списка, которые находятся на устройстве ioT в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="aa493-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="aa493-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa493-110">EXAMPLES</span></span>

### <span data-ttu-id="aa493-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa493-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="aa493-112">Получите сведения о модуле устройства IoT в концентраторе IoT.</span><span class="sxs-lookup"><span data-stu-id="aa493-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="aa493-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aa493-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="aa493-114">Откажите все модули, расположенные на устройстве IoT, в концентраторе IoT.</span><span class="sxs-lookup"><span data-stu-id="aa493-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="aa493-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa493-115">PARAMETERS</span></span>

### <span data-ttu-id="aa493-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa493-116">-DefaultProfile</span></span>
<span data-ttu-id="aa493-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa493-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa493-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="aa493-118">-DeviceId</span></span>
<span data-ttu-id="aa493-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="aa493-119">Target Device Id.</span></span>

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

### <span data-ttu-id="aa493-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa493-120">-InputObject</span></span>
<span data-ttu-id="aa493-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="aa493-121">IotHub object</span></span>

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

### <span data-ttu-id="aa493-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="aa493-122">-IotHubName</span></span>
<span data-ttu-id="aa493-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="aa493-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="aa493-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="aa493-124">-ModuleId</span></span>
<span data-ttu-id="aa493-125">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="aa493-125">Target Module Id.</span></span>

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

### <span data-ttu-id="aa493-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa493-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa493-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="aa493-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aa493-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa493-128">-ResourceId</span></span>
<span data-ttu-id="aa493-129">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="aa493-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="aa493-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa493-130">CommonParameters</span></span>
<span data-ttu-id="aa493-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa493-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa493-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa493-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa493-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa493-133">INPUTS</span></span>

### <span data-ttu-id="aa493-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="aa493-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="aa493-135">System.String</span><span class="sxs-lookup"><span data-stu-id="aa493-135">System.String</span></span>

## <span data-ttu-id="aa493-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa493-136">OUTPUTS</span></span>

### <span data-ttu-id="aa493-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span><span class="sxs-lookup"><span data-stu-id="aa493-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="aa493-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span><span class="sxs-lookup"><span data-stu-id="aa493-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="aa493-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa493-139">NOTES</span></span>

## <span data-ttu-id="aa493-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa493-140">RELATED LINKS</span></span>
