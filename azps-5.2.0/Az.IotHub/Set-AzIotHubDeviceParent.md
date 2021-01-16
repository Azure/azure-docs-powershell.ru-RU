---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeviceparent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeviceParent.md
ms.openlocfilehash: 1ad24866b4e0403693ace7b53b17271786f218d1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407751"
---
# <span data-ttu-id="2cf55-101">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="2cf55-101">Set-AzIotHubDeviceParent</span></span>

## <span data-ttu-id="2cf55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cf55-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf55-103">Установите родительское устройство указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="2cf55-103">Set the parent device of the specified device.</span></span>

## <span data-ttu-id="2cf55-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2cf55-104">SYNTAX</span></span>

### <span data-ttu-id="2cf55-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2cf55-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeviceParent [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ParentDeviceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cf55-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2cf55-106">InputObjectSet</span></span>
```
Set-AzIotHubDeviceParent [-InputObject] <PSIotHub> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cf55-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2cf55-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeviceParent [-ResourceId] <String> [-DeviceId] <String> [-ParentDeviceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cf55-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2cf55-108">DESCRIPTION</span></span>
<span data-ttu-id="2cf55-109">Установите родительское устройство указанного вне границы устройства.</span><span class="sxs-lookup"><span data-stu-id="2cf55-109">Set the parent device of the specified non-edge device.</span></span>

## <span data-ttu-id="2cf55-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2cf55-110">EXAMPLES</span></span>

### <span data-ttu-id="2cf55-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2cf55-111">Example 1</span></span>
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

## <span data-ttu-id="2cf55-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cf55-112">PARAMETERS</span></span>

### <span data-ttu-id="2cf55-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf55-113">-DefaultProfile</span></span>
<span data-ttu-id="2cf55-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf55-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf55-115">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2cf55-115">-DeviceId</span></span>
<span data-ttu-id="2cf55-116">Id of non-edge device.</span><span class="sxs-lookup"><span data-stu-id="2cf55-116">Id of non-edge device.</span></span>

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

### <span data-ttu-id="2cf55-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2cf55-117">-Force</span></span>
<span data-ttu-id="2cf55-118">Переопишет родительское устройство на устройстве, которое не является границым.</span><span class="sxs-lookup"><span data-stu-id="2cf55-118">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="2cf55-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cf55-119">-InputObject</span></span>
<span data-ttu-id="2cf55-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="2cf55-120">IotHub object</span></span>

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

### <span data-ttu-id="2cf55-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2cf55-121">-IotHubName</span></span>
<span data-ttu-id="2cf55-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="2cf55-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2cf55-123">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="2cf55-123">-ParentDeviceId</span></span>
<span data-ttu-id="2cf55-124">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="2cf55-124">Id of edge device.</span></span>

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

### <span data-ttu-id="2cf55-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf55-125">-ResourceGroupName</span></span>
<span data-ttu-id="2cf55-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2cf55-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2cf55-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cf55-127">-ResourceId</span></span>
<span data-ttu-id="2cf55-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="2cf55-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2cf55-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cf55-129">-Confirm</span></span>
<span data-ttu-id="2cf55-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf55-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cf55-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cf55-131">-WhatIf</span></span>
<span data-ttu-id="2cf55-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cf55-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2cf55-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2cf55-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cf55-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf55-134">CommonParameters</span></span>
<span data-ttu-id="2cf55-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf55-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf55-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf55-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf55-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2cf55-137">INPUTS</span></span>

### <span data-ttu-id="2cf55-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2cf55-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2cf55-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2cf55-139">System.String</span></span>

## <span data-ttu-id="2cf55-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2cf55-140">OUTPUTS</span></span>

### <span data-ttu-id="2cf55-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="2cf55-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="2cf55-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2cf55-142">NOTES</span></span>

## <span data-ttu-id="2cf55-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2cf55-143">RELATED LINKS</span></span>
