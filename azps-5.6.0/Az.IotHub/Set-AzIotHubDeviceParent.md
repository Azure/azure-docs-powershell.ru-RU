---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: af4b605c25ff3c35b0235612d7258be66a772c43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955832"
---
# <span data-ttu-id="1cf89-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="1cf89-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="1cf89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cf89-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf89-103">Установите родительское устройство указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="1cf89-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="1cf89-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cf89-104">SYNTAX</span></span>

### <span data-ttu-id="1cf89-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1cf89-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cf89-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1cf89-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf89-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1cf89-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cf89-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cf89-108">DESCRIPTION</span></span>
<span data-ttu-id="1cf89-109">Установите родительское устройство указанного вне границы устройства.</span><span class="sxs-lookup"><span data-stu-id="1cf89-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="1cf89-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cf89-110">EXAMPLES</span></span>

### <span data-ttu-id="1cf89-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cf89-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeviceParent -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ParentDeviceId "myParentDevice1"

DeviceId                   : myDevice1
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
EdgeEnabled                : False
DeviceScope                : ms-azure-iot-edge://myParentDevice1-637176526047419634
```

## <span data-ttu-id="1cf89-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cf89-112">PARAMETERS</span></span>

### <span data-ttu-id="1cf89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf89-113">-DefaultProfile</span></span>
<span data-ttu-id="1cf89-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cf89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cf89-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="1cf89-115">-DeviceId</span></span>
<span data-ttu-id="1cf89-116">Id of non-edge device.</span><span class="sxs-lookup"><span data-stu-id="1cf89-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="1cf89-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1cf89-117">-Force</span></span>
<span data-ttu-id="1cf89-118">Переопишет родительское устройство на устройстве, которое не является границым.</span><span class="sxs-lookup"><span data-stu-id="1cf89-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="1cf89-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cf89-119">-InputObject</span></span>
<span data-ttu-id="1cf89-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="1cf89-120">IotHub object</span></span>

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

### <span data-ttu-id="1cf89-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="1cf89-121">-IotHubName</span></span>
<span data-ttu-id="1cf89-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="1cf89-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="1cf89-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="1cf89-123">-ParentDeviceId</span></span>
<span data-ttu-id="1cf89-124">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="1cf89-124">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf89-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cf89-125">-ResourceGroupName</span></span>
<span data-ttu-id="1cf89-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1cf89-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1cf89-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cf89-127">-ResourceId</span></span>
<span data-ttu-id="1cf89-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="1cf89-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1cf89-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cf89-129">-Confirm</span></span>
<span data-ttu-id="1cf89-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1cf89-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf89-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf89-131">-WhatIf</span></span>
<span data-ttu-id="1cf89-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cf89-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1cf89-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1cf89-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cf89-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf89-134">CommonParameters</span></span>
<span data-ttu-id="1cf89-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cf89-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf89-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cf89-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf89-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cf89-137">INPUTS</span></span>

### <span data-ttu-id="1cf89-138">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="1cf89-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="1cf89-139">System.String</span><span class="sxs-lookup"><span data-stu-id="1cf89-139">System.String</span></span>

## <span data-ttu-id="1cf89-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cf89-140">OUTPUTS</span></span>

### <span data-ttu-id="1cf89-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="1cf89-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="1cf89-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cf89-142">NOTES</span></span>

## <span data-ttu-id="1cf89-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cf89-143">RELATED LINKS</span></span>
